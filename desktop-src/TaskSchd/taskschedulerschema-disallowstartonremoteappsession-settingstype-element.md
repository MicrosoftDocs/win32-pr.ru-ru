---
title: Дисалловстартонремотеаппсессион (Сеттингстипе), элемент
description: Указывает, что задача не будет запущена, если она запускается в удаленном сеансе, интегрированном локально.
ms.assetid: 8323d8d9-fb6a-4876-9967-cc2344c77de3
keywords:
- планировщик задач элемента Дисалловстартонремотеаппсессион
topic_type:
- apiref
api_name:
- DisallowStartOnRemoteAppSession
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d2f7834ecd57fa10aaaabfa21945f1e908834d535d50f94b4dd21e6ca45c0a62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120010804"
---
# <a name="disallowstartonremoteappsession-settingstype-element"></a>Дисалловстартонремотеаппсессион (Сеттингстипе), элемент

Указывает, что задача не будет запущена, если она запускается в удаленном сеансе, интегрированном локально.

``` syntax
<xs:element name="DisallowStartOnRemoteAppSession"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

Элемент **дисалловстартонремотеаппсессион** определяется сложным типом [**сеттингстипе**](taskschedulerschema-settingstype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                           | Унаследован от                                                         | Описание                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Параметры**](taskschedulerschema-settings-tasktype-element.md) | [**сеттингстипе**](taskschedulerschema-settingstype-complextype.md) | Содержит параметры, которые планировщик задач использует для выполнения задачи.<br/> |



## <a name="remarks"></a>Remarks

Значение по умолчанию для этого элемента — false.

Для разработки на C++ эта информация доступна через свойство [**ITaskSettings2::D исалловстартонремотеаппсессион**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings2-get_disallowstartonremoteappsession) .

## <a name="examples"></a>Примеры

Следующий XML-код определяет элемент Settings, который не разрешает запуск задачи, если задача запускается в сеансе на границе.


```XML
<Settings>
    <DisallowStartOnRemoteAppSession>true</DisallowStartOnRemoteAppSession>
</Settings>
        
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>              |
| Минимальная версия сервера<br/> | Windows \[Только для настольных приложений сервера 2008 R2\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[планировщик задач элементы схемы](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





