JOIN Tables in controller

```php
$user = $this->User->find('all', array(
    'fields' => array(
        'User.name',
        'Dashlet.id',
        'Dashlet.name',
    ),
    'joins' => array(
        array(
            'table' => 'user_dashlets',
            'alias' => 'UserDashlet',
            'type' => 'left',
            'conditions' => array(
                'UserDashlet.user_id = "User"."id"'
            ),
        ),
        array(
            'table' => 'dashlets',
            'alias' => 'Dashlet',
            'type' => 'left',
            'conditions' => array(
                'UserDashlet.dashlet_id = "Dashlet"."id"'
            ),
            'fields' => array(
                'id',
                'name'
            )
        )
    ),
    'conditions' => array(
        'User.id' => 1
    )));
```
