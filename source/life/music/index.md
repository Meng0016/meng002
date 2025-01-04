---
title: 八音盒
date: 2025-01-02 18:54:31
background: url(https://pic.rmb.bdstatic.com/bjh/240407/1308a14fc6acd32301fedb45864aa833685.png)
aplayer: true
comments: false
---

<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/aplayer/dist/APlayer.min.css">
<script src="https://cdn.jsdelivr.net/npm/aplayer/dist/APlayer.min.js"></script>
<script src="https://cdn.jsdelivr.net/npm/meting@2/dist/Meting.min.js"></script>
<meting-js
	server="tencent"
	type="playlist"
	id="9085386461">
</meting-js>

<div
  id="aplayer"
  data-id="9085386461"
  data-server="tencent"
  data-type="playlist"
  data-fixed="false"
  data-listFolded="false"
  data-autoplay="false"
  data-loop="all"
  data-order="list"
></div>
<script>
export default {
  data() {
    return {};
  },
  mounted() {
    const ap = new APlayer({
      container: document.getElementById("aplayer"),
    });
  }
}
</script>
