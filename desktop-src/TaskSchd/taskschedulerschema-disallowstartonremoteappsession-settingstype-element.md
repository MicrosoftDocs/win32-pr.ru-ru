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
ms.openlocfilehash: 11e3d0a367f2385e78cf1ec56231bbf7632fe05b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681851"
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



## <a name="remarks"></a>Комментарии

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
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>              |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[планировщик задач элементы схемы](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





