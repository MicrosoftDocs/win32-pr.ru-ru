---
title: Структура ORPC_INIT_ARGS
description: '\_ \_ Структура args ОРПК init содержит сведения, используемые для инициализации удаленной отладки с помощью интерфейса иорпкдебугнотифи.'
ms.assetid: be7646c7-3394-45ae-ae8f-9cee68bbc789
keywords:
- ORPC_INIT_ARGS структуры COM
- COM LPORPC_INIT_ARGS указателя структуры
topic_type:
- apiref
api_name:
- ORPC_INIT_ARGS
api_location:
- N/A
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e7dca0209f745d5034bde2da852829b99d7dcb8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135490"
---
# <a name="orpc_init_args-structure"></a>ОРПК \_ init \_ args, структура

Структура **\_ \_ args ОРПК init** содержит сведения, используемые для инициализации удаленной отладки с помощью интерфейса [**иорпкдебугнотифи**](iorpcdebugnotify.md) .

## <a name="syntax"></a>Синтаксис


```C++
typedef struct ORPC_INIT_ARGS {
  IOrpcDebugNotify *lpIntfOrpcDebug;
  void             *pvPSN;
  DWORD            *dwReserved1;
  DWORD            *dwReserved2;
} ORPC_INIT_ARGS, *LPORPC_INIT_ARGS;
```



## <a name="members"></a>Члены

<dl> <dt>

**лпинтфорпкдебуг**
</dt> <dd>

Указатель на интерфейс [**иорпкдебугнотифи**](iorpcdebugnotify.md) для использования в внутрипроцессного отладчиках. Если отладчик не находится в процессе или является системой Macintosh, это поле должно иметь **значение NULL**.

</dd> <dt>

**пвпсн**
</dt> <dd>

Указатель на серийный номер процесса отлаживаемого процесса в системе Macintosh. Если отлаживаемый объект не является системой Macintosh, это поле должно иметь **значение NULL**.

</dd> <dt>

**dwReserved1**
</dt> <dd>

Зарезервировано. Должно быть равно 0.

</dd> <dt>

**dwReserved2**
</dt> <dd>

Зарезервировано. Должно быть равно 0.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                     |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                           |
| Заголовок<br/>                   | <dl> <dt>Н/Д</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ОРПК \_ dbg \_ ALL**](orpc-dbg-all.md)
</dt> <dt>

[**\_БУФЕР ОРПК dbg \_**](orpc-dbg-buffer.md)
</dt> <dt>

[**дллдебугобжектрпчук**](dlldebugobjectrpchook.md)
</dt> <dt>

[**иорпкдебугнотифи**](iorpcdebugnotify.md)
</dt> </dl>

 

 





