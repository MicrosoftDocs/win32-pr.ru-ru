---
title: RunLevel (Рунлевелтипе), элемент
description: Содержит значение, указывающее уровень контекста безопасности для выполнения задачи.
ms.assetid: dc113ffa-8ac9-4dcd-a106-45295da42f46
keywords:
- планировщик задач элемента RunLevel
topic_type:
- apiref
api_name:
- RunLevel
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9d374f5b9ad388f3ad0a626e1b99ecae96eeef1a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341305"
---
# <a name="runlevel-runleveltype-element"></a>RunLevel (Рунлевелтипе), элемент

Содержит значение, указывающее уровень контекста безопасности для выполнения задачи. Можно указать, чтобы запустить задачу с использованием минимальных привилегий или повышенных привилегий. Значение 0 указывает, что задача запускается с наименьшими привилегиями, а значение 1 указывает на выполнение задачи с повышенными привилегиями.

``` syntax
<xs:element name="RunLevel"
    type="runLevelType"
 />
```

Элемент **runlevel** определяется простым типом [**рунлевелтипе**](taskschedulerschema-runleveltype-simpletype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                                                  | Унаследован от                                                           | Описание                                                                                                                           |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**Субъект (ПринЦипалтипе)**](taskschedulerschema-principal-principaltype-element.md) | [**principalType**](taskschedulerschema-principaltype-complextype.md) | Указывает учетные данные безопасности для участника. Эти учетные данные определяют контекст безопасности, в котором выполняется задача. <br/> |



## <a name="remarks"></a>Комментарии

Сведения о разработке C++ см. в разделе [**свойство runlevel класса IPrincipal**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel).

Сведения о разработке сценариев см. в разделе [**Principal. runlevel**](principal-runlevel.md).

Если задача зарегистрирована с помощью **встроенной \\** учетной записи администратора или учетных записей [LocalSystem](/windows/desktop/Services/localsystem-account) или [LocalService](/windows/desktop/Services/localservice-account) , свойство [**runlevel**](principal-runlevel.md) игнорируется. Значение атрибута также будет игнорироваться, если отключен [контроль учетных записей](/windows/desktop/SecAuthZ/user-account-control) (UAC).

Если задача зарегистрирована с помощью группы **администраторов** для контекста безопасности задачи, необходимо также задать для свойства [**runlevel**](principal-runlevel.md) значение "highestAvailable", чтобы запустить задачу. Дополнительные сведения см. в разделе [контексты безопасности для задач](security-contexts-for-running-tasks.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

