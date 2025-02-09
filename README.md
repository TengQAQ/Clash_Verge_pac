# Clash_Verge_pac
Clash Verge通过启动pac模式对国内的网站进行分流

点击齿轮，选择pac模式 编辑 复制下方代码

function FindProxyForURL(url, host) {
  const directList = [
    "*.baidu.com",
    "*.bilibili.com",
    "10.11.12.13",
    "*.423down.com",
    "*.bokecc.com",
    "*.chaipip.com",
    "*.hrtsea.com",
    "*.kaikeba.com",
    "*.laomo.me",
    "*.mpyit.com",
    "*.360.com",
    "*.360kuai.com",
    "*.360safe.com",
    "*.dhrest.com",
    "*.qhres.com",
    "*.qhstatic.com",
    "*.qhupdate.com",
    "*.so.com",
    "*.4399.com",
    "*.4399pk.com",
    "*.5054399.com",
    "*.img4399.com",
    "*.58.com",
    "*.1688.com",
    "*.aliapp.org",
    "*.alibaba.com",
    "*.alibabacloud.com",
    "*.alibabausercontent.com",
    "*.alicdn.com",
    "*.aliexpress.com",
    "*.aliimg.com",
    "*.alikunlun.com",
    "*.alipay.com",
    "*.alipayobjects.com",
    "*.alisoft.com",
    "*.aliyun.com",
    "*.aliyuncdn.com",
    "*.aliyuncs.com",
    "*.amap.com",
    "*.autonavi.com",
    "*.dingtalk.com",
    "*.ele.me",
    "*.hichina.com",
    "*.mmstat.com",
    "*.mxhichina.com",
    "*.soku.com",
    "*.taobao.com",
    "*.taobaocdn.com",
    "*.tbcache.com",
    "*.tbcdn.com",
    "*.tmall.com",
    "*.tmall.hk",
    "*.ucweb.com",
    "*.xiami.com",
    "*.xiami.net",
    "*.ykimg.com",
    "*.youku.com",
    "*.baidu.com",
    "*.baidubcr.com",
    "*.baidupcs.com",
    "*.baidustatic.com",
    "*.bcebos.com",
    "*.bdimg.com",
    "*.bdstatic.com",
    "*.bdurl.net",
    "*.hao123.com",
    "*.hao123img.com",
    "*.jomodns.com",
    "*.biligame.com",
    "*.biligame.net",
    "*.bytedance.com",
    "*.bytedance.net",
    "*.bytedns.net",
    "*.byteimg.com",
    "*.feiliao.com",
    "*.gifshow.com",
    "*.huoshan.com",
    "*.iesdouyin.com",
    "*.douyin.com",
    "*.ixigua.com",
    "*.kspkg.com",
    "*.pstatp.com",
    "*.snssdk.com",
    "*.toutiao.com",
    "*.toutiao13.com",
    "*.toutiaocdn.com",
    "*.toutiaocdn.net",
    "*.toutiaocloud.com",
    "*.toutiaohao.com",
    "*.toutiaohao.net",
    "*.toutiaoimg.com",
    "*.toutiaopage.com",
    "*.wukong.com",
    "*.zijieimg.com",
    "*.zjbyte.com",
    "*.zjcdn.com",
    "*.cctv.com",
    "*.cctvpic.com",
    "*.livechina.com",
    "*.21cn.com",
    "*.didialift.com",
    "*.didiglobal.com",
    "*.udache.com",
    "*.dbankcdn.com",
    "*.hicloud.com",
    "*.huawei.com",
    "*.huaweicloud.com",
    "*.huaweishop.net",
    "*.hwccpc.com",
    "*.vmall.com",
    "*.vmallres.com",
    "*.iflyink.com",
    "*.iflyrec.com",
    "*.iflytek.com",
    "*.360buy.com",
    "*.360buyimg.com",
    "*.jcloudcs.com",
    "*.jd.com",
    "*.jd.hk",
    "*.jdcloud.com",
    "*.jdpay.com",
    "*.paipai.com",
    "*.iciba.com",
    "*.ksosoft.com",
    "*.ksyun.com",
    "*.kuaishou.com",
    "*.yximgs.com",
    "*.meitu.com",
    "*.meitudata.com",
    "*.meitustat.com",
    "*.meipai.com",
    "*.le.com",
    "*.lecloud.com",
    "*.letv.com",
    "*.letvcloud.com",
    "*.letvimg.com",
    "*.letvlive.com",
    "*.letvstore.com",
    "*.hitv.com",
    "*.hunantv.com",
    "*.mgtv.com",
    "*.duokan.com",
    "*.mi.com",
    "*.miui.com",
    "*.xiaomi.com",
    "*.xiaomi.net",
    "*.xiaomicp.com",
    "*.miwifi.com",
    "*.126.com",
    "*.126.net",
    "*.127.net",
    "*.163.com",
    "*.163yun.com",
    "*.lofter.com",
    "*.netease.com",
    "*.ydstatic.com",
    "*.youdao.com",
    "*.pplive.com",
    "*.pptv.com",
    "*.pinduoduo.com",
    "*.yangkeduo.com",
    "*.leju.com",
    "*.miaopai.com",
    "*.sina.com",
    "*.sinaapp.com",
    "*.sinaimg.com",
    "*.weibo.com",
    "*.weibocdn.com",
    "*.xiaoka.tv",
    "*.go2map.com",
    "*.sogo.com",
    "*.sogou.com",
    "*.sogoucdn.com",
    "*.sohu.com",
    "*.sohucs.com",
    "*.sohuno.com",
    "*.sohurdc.com",
    "wwwbattlenet.com.cn",
    "*.amplitude.com",
    "*.firebaseio.com",
    "*.hockeyapp.net",
    "*.smartmailcloud.com",
    "*.csgo.wmsj.cn",
    "*.dl.steam.ksyna.com",
    "*.dota2.wmsj.cn",
    "*.st.dl.bscstorage.net",
    "*.st.dl.eccdnx.com",
    "*.steampowered.com.8686c.com",
    "*.foxmail.com",
    "*.gtimg.com",
    "*.idqqimg.com",
    "*.igamecj.com",
    "*.myapp.com",
    "*.myqcloud.com",
    "*.qq.com",
    "*.qqmail.com",
    "*.qqurl.com",
    "*.ovscdns.com",
    "*.soso.com",
    "*.tencent.com",
    "*.tencentmind.com",
    "*.tenpay.com",
    "*.wechat.com",
    "*.weixin.com",
    "*.weiyun.com",
    "*.appsimg.com",
    "*.appvipshop.com",
    "*.vip.com",
    "*.vipstatic.com",
    "*.ximalaya.com",
    "*.xmcdn.com",
    "*.00cdn.com",
    "*.88cdn.com",
    "*.kanimg.com",
    "*.kankan.com",
    "*.p2cdn.com",
    "*.sandai.net",
    "*.thundercdn.com",
    "*.xunlei.com",
    "*.got001.com",
    "*.jstucdn.com",
    "*.rrys.tv",
    "*.rrys2020.com",
    "*.yyets.com",
    "*.zimuzu.io",
    "*.zimuzu.tv",
    "*.zmz001.com",
    "*.zmz002.com",
    "*.zmz003.com",
    "*.zmz004.com",
    "*.zmz2019.com",
    "*.zmzapi.com",
    "*.zmzapi.net",
    "*.zmzfile.com",
    "wwwannouncewww",
    "wwwtorrentwww",
    "wwwtrackerwww",
    "*.animetorrents.me",
    "*.beitai.pt",
    "*.bittorrent.com",
    "*.broadcasthe.net",
    "*.chdbits.co",
    "*.empornium.me",
    "*.gazellegames.net",
    "*.hd4fans.org",
    "*.hdchina.org",
    "*.hdhome.org",
    "*.hdsky.me",
    "*.hdtime.org",
    "*.hdzone.me",
    "*.icetorrent.org",
    "*.jpopsuki.eu",
    "*.keepfrds.com",
    "*.leaguehd.com",
    "*.madsrevolution.net",
    "*.msg.vg",
    "*.nanyangpt.com",
    "*.ncore.cc",
    "*.open.cd",
    "*.ourbits.club",
    "*.passthepopcorn.me",
    "*.privatehd.to",
    "*.pthome.net",
    "*.redacted.ch",
    "*.springsunday.net",
    "*.tjupt.org",
    "*.totheglory.im",
    "*.trontv.com",
    "*.teamviewer.com",
    "*.baomitu.com",
    "*.bootcss.com",
    "*.jiasule.com",
    "*.jsdelivr.net",
    "*.staticfile.org",
    "*.upaiyun.com",
    "*.staticdn.net",
    "*.wangsu.com",
    "*.cloud.unity3d.com",
    "*.pinyuncloud.com",
    "*.10010.com",
    "*.115.com",
    "*.12306.com",
    "*.17173.com",
    "*.178.com",
    "*.17k.com",
    "*.360doc.com",
    "*.36kr.com",
    "*.3dmgame.com",
    "*.51cto.com",
    "*.51job.com",
    "*.51jobcdn.com",
    "*.56.com",
    "*.8686c.com",
    "*.abchina.com",
    "*.abercrombie.com",
    "*.aixifan.com",
    "*.algocasts.io",
    "*.babytree.com",
    "*.babytreeimg.com",
    "*.baicizhan.com",
    "*.baidupan.com",
    "*.baike.com",
    "*.biqudu.com",
    "*.biquge.com",
    "*.bitauto.com",
    "*.camera360.com",
    "*.cdnmama.com",
    "*.chaoxing.com",
    "*.che168.com",
    "*.chinacache.net",
    "*.chinaso.com",
    "*.chinaz.com",
    "*.chinaz.net",
    "*.chuimg.com",
    "*.cibntv.net",
    "*.clouddn.com",
    "*.cloudxns.net",
    "*.cn163.net",
    "*.cnbeta.com",
    "*.cnbetacdn.com",
    "*.cnblogs.com",
    "*.cnki.net",
    "*.cnmstl.net",
    "*.coolapk.com",
    "*.coolapkmarket.com",
    "*.csdn.net",
    "*.ctrip.com",
    "*.dangdang.com",
    "*.dfcfw.com",
    "*.dianping.com",
    "*.dilidili.wang",
    "*.douban.com",
    "*.doubanio.com",
    "*.dpfile.com",
    "*.duowan.com",
    "*.dxycdn.com",
    "*.dytt8.net",
    "*.easou.com",
    "*.eastday.com",
    "*.eastmoney.com",
    "*.ecitic.com",
    "*.ewqcxz.com",
    "*.fang.com",
    "*.fantasy.tv",
    "*.feng.com",
    "*.fengkongcloud.com",
    "*.fir.im",
    "*.frdic.com",
    "*.ganji.com",
    "*.ganjistatic1.com",
    "*.geetest.com",
    "*.geilicdn.com",
    "*.ghpym.com",
    "*.godic.net",
    "*.gravatar.com",
    "*.guazi.com",
    "*.gwdang.com",
    "*.gzlzfm.com",
    "*.haibian.com",
    "*.haosou.com",
    "*.hollisterco.com",
    "*.hongxiu.com",
    "*.huajiao.com",
    "*.hupu.com",
    "*.huxiucdn.com",
    "*.huya.com",
    "*.ifeng.com",
    "*.ifengimg.com",
    "*.infzm.com",
    "*.it168.com",
    "*.ithome.com",
    "*.ixdzs.com",
    "*.jianguoyun.com",
    "*.jianshu.com",
    "*.jianshu.io",
    "*.jianshuapi.com",
    "*.jiathis.com",
    "*.jmstatic.com",
    "*.jumei.com",
    "*.kaola.com",
    "*.knewone.com",
    "*.koowo.com",
    "*.ksyungslb.com",
    "*.kuaidi100.com",
    "*.kugou.com",
    "*.lancdns.com",
    "*.landiannews.com",
    "*.lanzou.com",
    "*.lemicp.com",
    "*.letitfly.me",
    "*.linkedin.com",
    "*.lizhi.fm",
    "*.lizhi.io",
    "*.lizhifm.com",
    "*.loli.net",
    "*.luoo.net",
    "*.lvmama.com",
    "*.lxdns.com",
    "*.maoyan.com",
    "*.meilishuo.com",
    "*.meituan.com",
    "*.meituan.net",
    "*.meizu.com",
    "*.migucloud.com",
    "*.miguvideo.com",
    "*.mobike.com",
    "*.mogu.com",
    "*.mogucdn.com",
    "*.mogujie.com",
    "*.moji.com",
    "*.moke.com",
    "*.msstatic.com",
    "*.mubu.com",
    "*.myunlu.com",
    "*.nruan.com",
    "*.nuomi.com",
    "*.onedns.net",
    "*.onlinedown.net",
    "*.oracle.com",
    "*.oschina.net",
    "*.ourdvs.com",
    "*.overcast.fm",
    "*.paypal.com",
    "*.polyv.net",
    "*.qbox.me",
    "*.qcloud.com",
    "*.qcloudcdn.com",
    "*.qdaily.com",
    "*.qdmm.com",
    "*.qhimg.com",
    "*.qianqian.com",
    "*.qidian.com",
    "*.qihucdn.com",
    "*.qin.io",
    "*.qiniu.com",
    "*.qiniucdn.com",
    "*.qiniudn.com",
    "*.qiushibaike.com",
    "*.quanmin.tv",
    "*.qunar.com",
    "*.qunarzz.com",
    "*.rarbg.to",
    "*.repaik.com",
    "*.rrmj.tv",
    "*.ruguoapp.com",
    "*.runoob.com",
    "*.sankuai.com",
    "*.segmentfault.com",
    "*.simplecd.me",
    "*.sm.ms",
    "*.smzdm.com",
    "*.snwx.com",
    "*.soufunimg.com",
    "*.sspai.com",
    "*.startssl.com",
    "*.suning.com",
    "*.taihe.com",
    "*.thsjy.com",
    "*.tianqi.com",
    "*.tianqistatic.com",
    "*.tianyancha.com",
    "*.tianyaui.com",
    "*.tietuku.com",
    "*.tiexue.net",
    "*.tmiaoo.com",
    "*.trip.com",
    "*.ttmeiju.com",
    "*.tudou.com",
    "*.tuniu.com",
    "*.tuniucdn.com",
    "*.umengcloud.com",
    "*.upyun.com",
    "*.uxengine.net",
    "*.videocc.net",
    "*.vmware.com",
    "*.wandoujia.com",
    "*.weather.com",
    "*.weico.cc",
    "*.weidian.com",
    "*.weiphone.com",
    "*.weiphone.net",
    "*.womai.com",
    "*.wscdns.com",
    "*.xdrig.com",
    "*.xhscdn.com",
    "*.xiachufang.com",
    "*.xiaohongshu.com",
    "*.xiaojukeji.com",
    "*.xinhuanet.com",
    "*.xip.io",
    "*.xitek.com",
    "*.xiumi.us",
    "*.xslb.net",
    "*.xueqiu.com",
    "*.yach.me",
    "*.yeepay.com",
    "*.yhd.com",
    "*.yihaodianimg.com",
    "*.yinxiang.com",
    "*.yinyuetai.com",
    "*.yixia.com",
    "*.ys168.com",
    "*.yuewen.com",
    "*.yy.com",
    "*.yystatic.com",
    "*.zealer.com",
    "*.zhangzishi.cc",
    "*.zhanqi.tv",
    "*.zhaopin.com",
    "*.zhihu.com",
    "*.zhimg.com",
    "*.zhongsou.com",
    "*.zhuihd.com",
    "www.1337bbs.com",
  ];
  if (directList.includes(host)) {
    return "DIRECT";
  }
  return "PROXY 127.0.0.1:%mixed-port%; SOCKS5 127.0.0.1:%mixed-port%; DIRECT;";
}

