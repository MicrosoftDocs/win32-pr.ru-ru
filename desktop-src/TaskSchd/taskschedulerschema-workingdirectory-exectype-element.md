---
title: WorkingDirectory (Ексектипе), элемент
description: Указывает каталог, в котором существует исполняемый файл или файлы, используемые исполняемым объектом.
ms.assetid: 09e53748-6d21-42df-bbdd-f0fd9693aab0
keywords:
- планировщик задач элемента WorkingDirectory
topic_type:
- apiref
api_name:
- WorkingDirectory
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5a91908d5cd774f19f32a182934688dc899179d1abba967b7871a646efcfe042
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513744"
---
# <a name="workingdirectory-exectype-element"></a>WorkingDirectory (Ексектипе), элемент

Указывает каталог, в котором существует исполняемый файл или файлы, используемые исполняемым объектом.

``` syntax
<xs:element name="WorkingDirectory"
    type="pathType"
 />
```

Элемент **WorkingDirectory** определяется сложным типом [**ексектипе**](taskschedulerschema-exectype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                      | Унаследован от                                                 | Описание                                                            |
|--------------------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------|
| [**Exec**](taskschedulerschema-exec-actiongroup-element.md) | [**ексектипе**](taskschedulerschema-exectype-complextype.md) | Указывает действие, выполняющее операцию командной строки.<br/> |



## <a name="remarks"></a>Remarks

Для разработки скриптов рабочий каталог указывается свойством [**ексекактион. WorkingDirectory**](execaction-workingdirectory.md) .

Для разработки на C++ рабочий каталог определяется свойством [**иексекактион:: WorkingDirectory**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory) .

## <a name="examples"></a>Примеры

В следующем коде XML определяется действие выполнения.


```XML
<Exec>
    <Command></Command>
    <Arguments></Arguments>
    <WorkingDirectory></WorkingDirectory>
</ServiceResume>
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

 

 





