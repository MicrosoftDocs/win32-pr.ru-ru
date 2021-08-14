---
title: Включенный (Сеттингстипе) элемент
description: Указывает, что задача включена. Задачу можно выполнить, только если этот параметр имеет значение true.
ms.assetid: d28f0d54-1205-4b70-a178-72d809da9ce1
keywords:
- Включенный элемент планировщик задач
topic_type:
- apiref
api_name:
- Enabled
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ff198520e354147ff092b2374bb5a766e1ce1c6db6a4b8fc6302b92670bddcda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118131873"
---
# <a name="enabled-settingstype-element"></a>Включенный (Сеттингстипе) элемент

Указывает, что задача включена. Задачу можно выполнить, только если этот параметр имеет значение true.

``` syntax
<xs:element name="Enabled"
    type="boolean"
    default="true"
    minOccurs="1"
 />
```

Элемент **Enabled** определяется сложным типом [**сеттингстипе**](taskschedulerschema-settingstype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                           | Унаследован от                                                         | Описание                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Параметры**](taskschedulerschema-settings-tasktype-element.md) | [**сеттингстипе**](taskschedulerschema-settingstype-complextype.md) | Содержит параметры, которые планировщик задач использует для выполнения задачи.<br/> |



## <a name="remarks"></a>Remarks

Сведения о разработке на языке C++ см. в разделе [**Enabled Property объекта итасксеттингс**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_enabled).

Сведения о разработке сценариев см. в разделе [**тасксеттингс. Enabled**](tasksettings-enabled.md).

## <a name="examples"></a>Примеры

Полный пример XML-кода для включенной задачи см. в разделе [пример триггера времени (XML)](time-trigger-example--xml-.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



 

 





