---
title: Руннингтаск. Енгинепид, свойство
description: Для сценариев возвращает идентификатор процесса для подсистемы (процесса), выполняющей задачу.
ms.assetid: cb8a0f2f-ebe3-4f52-8fbd-b0cebb539728
keywords:
- планировщик задач свойства Енгинепид
- Планировщик задач свойства Енгинепид, объект Руннингтаск
- Планировщик задач объекта Руннингтаск, свойство Енгинепид
topic_type:
- apiref
api_name:
- RunningTask.EnginePID
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eed259ccc92e954ae1acde076f0cc09167d15071ea71a33039e7298479875b5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117759077"
---
# <a name="runningtaskenginepid-property"></a>Руннингтаск. Енгинепид, свойство

Для сценариев возвращает идентификатор процесса для подсистемы (процесса), выполняющей задачу.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```VB
RunningTask.EnginePID As Integer
```



## <a name="property-value"></a>Значение свойства

Идентификатор процесса для подсистемы, в которой выполняется задача.

## <a name="remarks"></a>Remarks

Идентификатор процесса, возвращаемый этим свойством, не может быть добавлен непосредственно в строку. Возвращаемое значение должно быть преобразовано в целочисленное значение первым путем вызова функции [CInt](/previous-versions//fctcwhw9(v=vs.85)) возвращаемого значения.


```VB
ProcessId = cint(RunningTask.EnginePID)
wscript.echo "Process Id of Engine is " & "ProcessId
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                          |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                    |
| Библиотека типов<br/>             | <dl> <dt>Тасксчд. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

