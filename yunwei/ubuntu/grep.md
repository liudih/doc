```shell
cat filename | grep '"*"'
cat seller-photon.2020-10-19.log | grep 'API>>INFO>replenishment>>>>>>request'
cat photon-web.2020-10-20.log | grep -m1 -C50 'OrderAttributeMapper.queryByIdsAnd'
cat /opt/photon-web/log/photon-web.2020-11-06.log | grep  'transferContainerOrThings2_time'

#grep -C 3 love filename  显示filename文件中，love行上下3行内容（含love行）
grep -A 3 love filename  显示filename文件中，love行下3行内容（含love行）
grep -B 3 love filename  显示filename文件中，love行上3行内容（含love行）
#上下10行
grep -n -i -m1 -C10 UK-FXT  orbit-wms.2020-12-08.log
grep -n -i -m1 -B50 UK-FXT  orbit-wms.2020-12-08.log

grep -n -i -m1 -C10 "API>>ERROR>>>>>>>FbaPlanApi.changeLabel"  seller-photon.2021-02-25.log
cat seller-photon.2021-02-25.log | grep -m1 -C50 "API>>INFO>>>replenishment>>>>organization:"

```