---
title: Дисалловстартифонбаттериес (Сеттингстипе), элемент
description: Указывает, что задача не будет запущена, если компьютер работает от батарей.
ms.assetid: 48c0fd32-4441-4628-8090-c736f2945b4d
keywords:
- планировщик задач элемента Дисалловстартифонбаттериес
topic_type:
- apiref
api_name:
- DisallowStartIfOnBatteries
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: efd78b3e868c41431521b4c584a4044b9086362cf55d86466eb38ed75fcee148
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100044"
---
# <a name="disallowstartifonbatteries-settingstype-element"></a>Дисалловстартифонбаттериес (Сеттингстипе), элемент

Указывает, что задача не будет запущена, если компьютер работает от батарей.

``` syntax
<xs:element name="DisallowStartIfOnBatteries"
    type="boolean"
 />
```

Элемент **дисалловстартифонбаттериес** определяется сложным типом [**сеттингстипе**](taskschedulerschema-settingstype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                           | Унаследован от                                                         | Описание                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Параметры**](taskschedulerschema-settings-tasktype-element.md) | [**сеттингстипе**](taskschedulerschema-settingstype-complextype.md) | Содержит параметры, которые планировщик задач использует для выполнения задачи.<br/> |



## <a name="remarks"></a>Remarks

Значение по умолчанию для этого элемента — true.

Для разработки сценариев эти сведения доступны через свойство [**тасксеттингс. дисалловстартифонбаттериес**](tasksettings-disallowstartifonbatteries.md) .

Для разработки на C++ эта информация доступна через свойство [**итасксеттингс::D исалловстартифонбаттериес**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_disallowstartifonbatteries) .

## <a name="examples"></a>Примеры

Следующий XML-код определяет элемент Settings, который не разрешает выполнение задачи, если компьютер работает под управлением батарей.


```XML
<Settings>
    <DisallowStartIfOnBatteries>true</DisallowStartIfOnBatteries>
</Settings>
        
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[планировщик задач элементы схемы](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





