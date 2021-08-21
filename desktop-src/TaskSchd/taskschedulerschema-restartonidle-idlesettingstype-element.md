---
title: Рестартонидле (Идлесеттингстипе), элемент
description: Указывает, перезапускается ли задача, когда компьютер циклически перегружается в состояние простоя.
ms.assetid: 7a7a388c-8dc9-4106-82c1-3435d9f89866
keywords:
- планировщик задач элемента Рестартонидле
topic_type:
- apiref
api_name:
- RestartOnIdle
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 16a636ebc052bb04a150390659909f0b73cae78871acaacfb4ba529ea2d8e917
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119575144"
---
# <a name="restartonidle-idlesettingstype-element"></a>Рестартонидле (Идлесеттингстипе), элемент

Указывает, перезапускается ли задача, когда компьютер циклически перегружается в состояние простоя.

``` syntax
<xs:element name="RestartOnIdle"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

Элемент **рестартонидле** определяется сложным типом [**идлесеттингстипе**](taskschedulerschema-idlesettingstype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                                       | Унаследован от                                                                 | Описание                                                                                       |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**идлесеттингс**](taskschedulerschema-idlesettings-settingstype-element.md) | [**идлесеттингстипе**](taskschedulerschema-idlesettingstype-complextype.md) | Указывает, как планировщик задач выполняет задачи, когда компьютер находится в состоянии простоя.<br/> |



## <a name="remarks"></a>Remarks

Этот элемент используется только в том случае, если для элемента [**терминатеонидлинд**](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) задано значение true.

Для разработки скриптов эти параметры задач указываются с помощью свойства [**идлесеттингс. рестартонидле**](idlesettings-restartonidle.md) .

Для разработки на C++ эти параметры задачи указываются с помощью свойства [**иидлесеттингс:: рестартонидле**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_restartonidle) .

## <a name="examples"></a>Примеры

Следующий XML-код определяет параметр простоя, который указывает, что задачу не следует перезапускать при цикле условия простоя.


```XML
<IdleSettings>
     <TerminateOnIdleEnd>true</TerminateOnIdleEnd>
     <RestartOnIdle>true</RestartOnIdle>
</IdleSettings>
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[планировщик задач элементы схемы](task-scheduler-schema-elements.md)
</dt> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> </dl>

 

 





