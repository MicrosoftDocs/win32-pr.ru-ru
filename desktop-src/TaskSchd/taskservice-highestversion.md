---
title: TaskService. Хигхестверсион, свойство
description: Для сценариев указывает самую новую версию планировщик задач, поддерживаемую компьютером.
ms.assetid: b4e55e46-6f33-4224-811b-06bf218dd1ac
keywords:
- планировщик задач свойства Хигхестверсион
- Планировщик задач свойства Хигхестверсион, объект TaskService
- Планировщик задач объекта TaskService, свойство Хигхестверсион
topic_type:
- apiref
api_name:
- TaskService.HighestVersion
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b4e381326ab901fcaf8657975ce3f8401facd44
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803952"
---
# <a name="taskservicehighestversion-property"></a>TaskService. Хигхестверсион, свойство

Для сценариев указывает самую новую версию планировщик задач, поддерживаемую компьютером.

## <a name="syntax"></a>Синтаксис


```VB
TaskService.HighestVersion As Integer
```



## <a name="property-value"></a>Значение свойства

Самая высокая версия планировщик задач, поддерживаемая компьютером. Самая высокая версия — это значение, разделенное на MajorVersion/MinorVersion на 16-разрядной границе. Служба планировщик задач возвращает значение 1 для основной версии и 2 для дополнительной версии. Используйте функцию [CLng](/previous-versions//ck4c5842(v=vs.85)) для получения целочисленного значения свойства.

## <a name="examples"></a>Примеры

В следующем коде показано, как использовать функцию [CLng](/previous-versions//ck4c5842(v=vs.85)) для получения значения свойства **хигхестверсион** .


```VB
wscript.echo service.HighestVersion
Test = clng( service.HighestVersion )
If Test <> 65538  Then
    wscript.echo "Fail"

Else
    wscript.echo "Pass"
End If
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                          |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                    |
| Библиотека типов<br/>             | <dl> <dt>Тасксчд. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

