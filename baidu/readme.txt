�ٶ�ane��һ������flash as3������Ա��flex��flash air �ƶ�Ӧ������Ӱٶ��ƶ�������˹���ane�����
֧��flash air ios��flash air android��֧�ְٶȹ������ȫ������banner���
�ٶȹ��������վ��http://munion.baidu.com/
�汾�ţ�1.0
�����ڣ�adobe air sdk 4.0���ٶ��ƶ��ƹ�sdk android 3.42 ���ٶ��ƶ�Ӧ�ù��ios sdk3.4.7
iphone4/ios7,iphone5/ios7,С��/android 4���Զ�ok

ʹ�ã�
1.�ڰٶȹ��������վ����Ӧ�ã���ȡ���id�ͼƷ�id
2.���baidu1.0.ane��flex air��Ŀ����flash android ��flash ios��Ŀ�С�������ô��flex air��Ŀ�м�ane������������
3.��д�������,��ʽ�ϴ�Ӧ�õ��̵�ʱ��debug�ĳ��ڰٶ���վ��õĹ��id�ͼƷ�ID
if(BaiDu.getInstance().supportDevice){
	BaiDu.getInstance().setKeys("debug","debug");//	BaiDu.getInstance().setKeys("appsid","�Ʒ�id");
	BaiDu.getInstance().showBanner(BaiDu.BANNER,RelationPosition.BOTTOM_CENTER);
}
4.ȷ��xxx-app.xml���Ѿ���ane��id����
 <extensionID>com.baidu.mobads</extensionID>
5.iosֻ��Ҫ����4����android�汾��Ҫ��ios����˲���
     a.��Ӧ��������Ȩ�ޣ�ȷ����xxx-app.xml����������Ȩ�޴���
            <uses-permission android:name="android.permission.INTERNET"/>
	    <uses-permission android:name="android.permission.WRITE_EXTERNAL_STORAGE"/>
	    <uses-permission android:name="android.permission.READ_PHONE_STATE"/>
	    <uses-permission android:name="android.permission.ACCESS_NETWORK_STATE"/>
	    <uses-permission android:name="android.permission.ACCESS_WIFI_STATE"/>
	    <uses-permission android:name="android.permission.ACCESS_COARSE_LOCATION"/>
     b.��������ӹ���Activity���ύ���ٶ����ʱ��Ҫ����meta-data��ֵ�ǰٶ����뵽��ID���ύ���г���ʱ�����ɾ��
        <application>
    	<meta-data android:name="BaiduMobAd_APP_ID" android:value="debug" /> 
	<meta-data android:name="BaiduMobAd_APP_SEC" android:value="debug" />
  	 <activity android:name="com.baidu.mobads.AppActivity" android:configChanges="keyboard|keyboardHidden|orientation"/> 
	</application>
     c.�����apk����extraĿ¼�Ͻ�apk�С�������apktool����Ҳ������winrar�����򿪷�ʽѡ��winrar��Ȼ���extraĿ¼�Ͻ�ȥ���Ϳ�����,�Ͻ�ȥ��apkĿ¼�ṹ���Կ���ͼ
     d.���޸ĺ��apkǩ���������������еķ�ʽ��apkǩ�����������԰ٶ� ��apkǩ����רҵ��������Ҳ��������"APKǩ������.exe"ǩ��(�򵥲��������)
6.apk����ipa�����������Ҫ�ύ���ٶȹ��������ˣ��ύ����ǰ�ǵð�debug������Ӧ�õ�appsid�ͼƷ�id

ane����api:
������ذٶ�ȫ�����
public function cacheInterstitial():void
չʾ��棬չʾǰ����Ҫ�����
public function showInterstitial():void
���ٶ��ƶ�ȫ������Ƿ񻺴����
public function isInterstitialReady():Boolean
���λ�ã�չʾ�ٶ��ƶ�Ӧ��banner���
public function showBanner(adSize:BaiDuSize, position:int):void
���Զ�λչʾ�ٶ�Ӧ�ù��
public function showBannerAbsolute(adSize:BaiDuSize, x:Number, y:Number):void
����banner���
public function hideBanner():void

ane֧�ֹ����صĸ����¼���BaiDuAdEvent�еĳ���
�������
public static const onBannerDismiss:String = "onBannerDismiss";
������ʧ��
public static const onBannerFailedReceive:String = "onBannerFailedReceive";
�������뿪Ӧ��
public static const onBannerLeaveApplication:String = "onBannerLeaveApplication";
չʾ���
public static const onBannerPresent:String = "onBannerPresent";
���յ����
public static const onBannerReceive:String = "onBannerReceive";
ȫ�����ر�
public static const onInterstitialDismiss:String = "onInterstitialDismiss";
ȫ��������ʧ��
public static const onInterstitialFailedReceive:String = "onInterstitialFailedReceive";
�����ȫ���������Ӧ��
public static const onInterstitialLeaveApplication:String = "onInterstitialLeaveApplication";
ȫ����潫չʾ
public static const onInterstitialPresent:String = "onInterstitialPresent";
ȫ�������سɹ�
public static const onInterstitialReceive:String = "onInterstitialReceive";
