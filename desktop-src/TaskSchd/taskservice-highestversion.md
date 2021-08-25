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
ms.openlocfilehash: e27618490fcf404936532d272402bebc03d94eb72ba8156e897f344b708d90ec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959494"
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



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                          |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                    |
| Библиотека типов<br/>             | <dl> <dt>Тасксчд. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

