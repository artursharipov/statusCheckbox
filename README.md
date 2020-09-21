yii2-status-checkbox
=================

Статус ввиде чекбоксов в gridview yii2 
  
Использование
------------------

В контроллер 

```php

public function actions()
{
    return [
        'change-column' => [
            'class' => 'common\components\status\actions\ChangeStatusAction',
            'self' => 'common\modules\page\models\Page'
        ],
    ];
}

```
Добавить поле status в таблицу БД.
В gridview:

```php

'columns' => [
    \common\components\status\StatusColumn::switch('status', [1]),
    //\common\components\status\StatusColumn::switch('visible', [1]),
],

```

status и visible - поля таблицы int
Второй параметр массив id - которые нельзя переключать
