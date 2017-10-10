# Yii1 API controller
_Template for API controller in Yii 1_

## Usage

* Add the *ApiController.php* file to your controllers folder
* Change the `APPLICATION_ID`, and add your models in each action in the switch-case statement (_remove the MyModel example before that_)
* Open the *protected/config/main.php* file and add this to your configuration:
```
'urlManager' => array(
            'urlFormat' => 'path',
            'showScriptName' => false,
            'caseSensitive' => true,
            'rules' => array(
                //API rules
                array('api/list', 'pattern'=>'api/<model>', 'verb'=>'GET'),
                array('api/view', 'pattern'=>'api/<model>/<id:\d+>', 'verb'=>'GET'),
                array('api/update', 'pattern'=>'api/<model>/<id:\d+>', 'verb'=>'PUT'),
                array('api/delete', 'pattern'=>'api/<model>/<id:\d+>', 'verb'=>'DELETE'),
                array('api/create', 'pattern'=>'api/<model>', 'verb'=>'POST'),
            ),
        ), 
 ```      
