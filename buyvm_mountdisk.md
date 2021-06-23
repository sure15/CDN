购买及挂载流程
1、在Buyvm官网购买一台Las Vegas机房的KVM VPS，如果仅用于存储，买最低配的512M内存就行了；同时按需购买Block Storage空间。

2、进入 Storage Volumes 后台，将 Block Storage 附加到（Attached To） 对应的VPS

3、查看数据块编号(开通邮件里也有)

`ls /dev/disk/by-id/`

4、假设看到的结果是scsi-0BUYVM_SLAB_VOLUME-1331，那么1331就是数据块的id，或者后台也能直接看到。

5、格式化

`mkfs.ext4 -F /dev/disk/by-id/scsi-0BUYVM_SLAB_VOLUME-1331`

6、创建文件夹

`mkdir /storage`

7、挂载

`mount -o discard,defaults /dev/disk/by-id/scsi-0BUYVM_SLAB_VOLUME-1331 /storage`

8、设置开机/重启自动挂载

`echo '/dev/disk/by-id/scsi-0BUYVM_SLAB_VOLUME-1331 /storage ext4 defaults,nofail,discard 0 0' | sudo tee -a /etc/fstab`

其他
1、Buyvm家所有的KVM VPS均免费提供Directadmin面板，有需要的可以联系客服。

2、如果没有中途退款的需求，强烈推荐使用支付宝付款，支付宝付款有神秘加成，默认加元汇率，使用Paypal等付款是美元

TAG 不限流量 大盘鸡
声明：本文由菠萝发布，如需转载请注明出处。
