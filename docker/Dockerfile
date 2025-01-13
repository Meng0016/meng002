# 第一阶段：构建 Hexo 静态文件
FROM node:22.12.0 AS builder

# 设置工作目录
WORKDIR /usr/src/app

# 复制 package.json 和 package-lock.json
COPY package*.json ./

# 安装 Hexo 及其插件
RUN npm install

# 复制 Hexo 项目文件
COPY . .

# 生成静态文件
RUN npx hexo generate

# 第二阶段：使用 Nginx 提供静态文件
FROM nginx:alpine

# 复制 Nginx 配置文件
COPY nginx.conf /etc/nginx/nginx.conf

# 复制构建的静态文件到 Nginx 的默认目录
COPY --from=builder /usr/src/app/public /usr/share/nginx/html

# 暴露 Nginx 端口
EXPOSE 80

# 启动 Nginx
CMD ["nginx", "-g", "daemon off;"]



