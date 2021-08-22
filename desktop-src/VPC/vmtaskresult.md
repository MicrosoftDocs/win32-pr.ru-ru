---
title: Перечисление Вмтаскресулт (Впккоминтерфацес. h)
description: Указывает результат задачи.
ms.assetid: 34aa193a-466d-492e-8648-467c286a8c11
keywords:
- Перечисление Вмтаскресулт Virtual PC
topic_type:
- apiref
api_name:
- VMTaskResult
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0884d89776ac840586f221f21f8335f1d93c18886fd36bbe790164ebd1ba4cd8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998444"
---
# <a name="vmtaskresult-enumeration"></a>Перечисление Вмтаскресулт

\[Windows Virtual PC больше не доступен для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Указывает результат задачи.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum  { 
  vmTaskResult_Success                      = 0,
  vmTaskResult_Cancelled                    = 1,
  vmTaskResult_UnexpectedError              = 2,
  vmTaskResult_OutOfMemoryError             = 3,
  vmTaskResult_DiskRelatedError             = 4,
  vmTaskResult_IncompatibleSavedStateError  = 5,
  vmTaskResult_TimeOutError                 = 6,
  vmTaskResult_IllegalValueError            = 7,
  vmTaskResult_ThreadCrashError             = 8,
  vmTaskResult_ShutdownAbort                = 9
} VMTaskResult;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="vmTaskResult_Success"></span><span id="vmtaskresult_success"></span><span id="VMTASKRESULT_SUCCESS"></span>**Вмтаскресулт \_ успешно**
</dt> <dd>

Задача выполнена успешно.

</dd> <dt>

<span id="vmTaskResult_Cancelled"></span><span id="vmtaskresult_cancelled"></span><span id="VMTASKRESULT_CANCELLED"></span>**Вмтаскресулт \_ отменена**
</dt> <dd>

Задача отменена.

</dd> <dt>

<span id="vmTaskResult_UnexpectedError"></span><span id="vmtaskresult_unexpectederror"></span><span id="VMTASKRESULT_UNEXPECTEDERROR"></span>**Вмтаскресулт \_ унекспектедеррор**
</dt> <dd>

Непредвиденная ошибка в задаче.

</dd> <dt>

<span id="vmTaskResult_OutOfMemoryError"></span><span id="vmtaskresult_outofmemoryerror"></span><span id="VMTASKRESULT_OUTOFMEMORYERROR"></span>**Вмтаскресулт \_ OutOfMemoryError**
</dt> <dd>

Недостаточно памяти для завершения задачи.

</dd> <dt>

<span id="vmTaskResult_DiskRelatedError"></span><span id="vmtaskresult_diskrelatederror"></span><span id="VMTASKRESULT_DISKRELATEDERROR"></span>**Вмтаскресулт \_ дискрелатедеррор**
</dt> <dd>

При записи на диск в задаче произошла ошибка (убедитесь, что на диске достаточно места).

</dd> <dt>

<span id="vmTaskResult_IncompatibleSavedStateError"></span><span id="vmtaskresult_incompatiblesavedstateerror"></span><span id="VMTASKRESULT_INCOMPATIBLESAVEDSTATEERROR"></span>**Вмтаскресулт \_ инкомпатиблесаведстатиррор**
</dt> <dd>

Не удалось восстановить виртуальную машину, так как сохраненное состояние несовместимо.

</dd> <dt>

<span id="vmTaskResult_TimeOutError"></span><span id="vmtaskresult_timeouterror"></span><span id="VMTASKRESULT_TIMEOUTERROR"></span>**Вмтаскресулт \_ тимеаутеррор**
</dt> <dd>

Время ожидания задачи истекло.

</dd> <dt>

<span id="vmTaskResult_IllegalValueError"></span><span id="vmtaskresult_illegalvalueerror"></span><span id="VMTASKRESULT_ILLEGALVALUEERROR"></span>**Вмтаскресулт \_ иллегалвалуиррор**
</dt> <dd>

При обработке задачи было считано недопустимое значение предпочтения.

</dd> <dt>

<span id="vmTaskResult_ThreadCrashError"></span><span id="vmtaskresult_threadcrasherror"></span><span id="VMTASKRESULT_THREADCRASHERROR"></span>**Вмтаскресулт \_ среадкрашеррор**
</dt> <dd>

Поток, связанный с задачей, завершился сбоем.

</dd> <dt>

<span id="vmTaskResult_ShutdownAbort"></span><span id="vmtaskresult_shutdownabort"></span><span id="VMTASKRESULT_SHUTDOWNABORT"></span>**Вмтаскресулт \_ шутдовнаборт**
</dt> <dd>

Запрошенное завершение работы прервано.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                     |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                          |
| Продукт<br/>                  | Windows Virtual PC<br/>                                                                 |
| Заголовок<br/>                   | <dl> <dt>Впккоминтерфацес. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Ивмтаск:: result**](ivmtask-result.md)
</dt> </dl>

 

