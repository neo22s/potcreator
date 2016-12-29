# potcreator
Fork from http://hpyer.cn/codes/potcreator 
@author	Hpyer <coolhpy@163.com>

Sample

<?php

include('POTCreator.php');

$obj = new POTCreator;

$obj->set_root(dirname(__FILE__) . '/example');
$obj->set_exts('php|tpl');
$obj->set_regular('/_[_|e]\([\"|\']([^\"|\']+)[\"|\']\)/i');
$obj->set_base_path('..');
$obj->set_read_subdir(true);

$potfile = 'example/language/example.pot';
$obj->write_pot($potfile);

header('Content-type:text/html; Charset=GBK');
echo "<p>POT ÎÄ¼þÎ»ÓÚ - The POT file located in:<br>\n{$potfile}</p>\n";
echo "<p>È»ºóÄã¾Í¿ÉÒÔÊ¹ÓÃ Poedit ½øÐÐ·­ÒëÀ² - Then you can translate it by Poedit.</p>\n";

?>
