# printSDK
易联云开放接口PHP sdk
##接口示例：
include("print.class.php");
$print = new Yprint();
//<table><tr><td>菜名</td><td>分数</td><td>总价</td></tr></tr></table>
/*$content = "@@2               食有材
@@2订单编号：B16122211455970
@@2下单时间：2016/12/22 11:45:59
@@2实际金额：321.00
@@2配送方式：送货上门
@@2收货名称：王先生
@@2收货电话：13688180214
@@2店铺名称：测试
@@2收货地址：四川省 眉山市 东坡区
@@2测试地址
@@2备注信息：
@@2
@@2商品名       单价       数量
@@2卷肠,,,10kg/件
@@2             216.00       1
@@2手抓饼,手抓饼,10个/袋,1x100个
@@2             105.00       1";*/
//$content .='菜名          分数         价格';
$content ='周黑鸭        1份          10.00';
$apikey = "xxxxxxxxx";
$msign = 'xxxxxxxx';
###打印
echo $print->action_print(626,'xxxxxxxxx',$content,$apikey,$msign);
###添加打印机
echo $print->action_addprint(xxx,'xxx','ceshizhanghao','k2s测试','18111111111',$apikey,$msign);
###删除打印机
echo $print->action_removeprinter(xxx,'xxx ',$apikey,$msign);
###添加应用菜单
$printmenu = [urlencode('美团开店'),urlencode('http://www.10ss.net/uel?id=1')];
$printmenu = urlencode(json_encode($printmenu,JSON_UNESCAPED_UNICODE));
echo $print->action_addprintmenu(xxx,'xxx',$apikey,$msign,$printmenu);
