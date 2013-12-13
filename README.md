Metro Framework
===
Libraries for nofw micro framework.

Sample Configuration
=====
```php
associate_iCanHandle('analyze',  'metrofw/analyzer.php');
associate_iCanHandle('analyze',  'metrofw/router.php');
associate_iCanHandle('resources', 'metrofw/utils.php');
associate_iCanHandle('output', 'metrofw/output.php');
associate_iCanHandle('exception', 'metrofw/template.php::onException');

associate_iAmA('request',  'metrofw/request.php');
associate_iAmA('response', 'metrofw/response.php');
associate_iAmA('router',   'metrofw/router.php');

associate_set('template_basedir', 'templates/');
associate_set('template_baseuri', 'templates/');
associate_set('template_name', 'webapp01');

associate_set('route_rules', 
	array_merge(array('/:appName'=>array( 'modName'=>'main', 'actName'=>'main' )),
	associate_get('route_rules')));

associate_set('route_rules', 
	array_merge(array('/:appName/:modName'=>array( 'actName'=>'main' )),
	associate_get('route_rules')));

associate_set('route_rules', 
	array_merge(array('/:appName/:modName/:actName'=>array(  )),
	associate_get('route_rules')));

associate_set('route_rules', 
	array_merge(array('/:appName/:modName/:actName/:arg'=>array(  )),
	associate_get('route_rules')));
```
