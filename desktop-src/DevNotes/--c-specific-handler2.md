---
description: Вызывается компилятором для реализации расширений структурированной обработки исключений.
ms.assetid: 6EAE0B4E-35E1-48EB-A8A9-0C1DC5387B03
title: Функция __C_specific_handler (WDM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __C_specific_handler
- __C_specific_handler
api_type:
- DllExport
api_location:
- ntoskrnl.exe
- NTDll.dll
- wpdupfltr.sys
ms.openlocfilehash: fc89105a6a68c920fccb123dd95a08ed4ddee696
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657135"
---
# <a name="__c_specific_handler-function"></a>\_\_\_Конкретная \_ функция обработчика C

Вызывается компилятором для реализации расширений структурированной обработки исключений.

Относительный адрес обработчика, относящегося к конкретному языку, содержится в \_ сведениях очистки, если заданы флаги УНВ \_ \_ ехандлер или УНВ \_ Flag \_ ухандлер. Обработчик конкретного языка вызывается как часть поиска обработчика исключений или в процессе очистки. Дополнительные сведения см. в разделе [обработчик конкретного языка](/cpp/build/language-specific-handler).

## <a name="syntax"></a>Синтаксис


```C++
_CRTIMP  __C_specific_handler(
  _In_    struct _EXCEPTION_RECORD   *ExceptionRecord,
  _In_    void                       *EstablisherFrame,
  _Inout_ struct _CONTEXT            *ContextRecord,
  _Inout_ struct _DISPATCHER_CONTEXT *DispatcherContext
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Ексцептионрекорд* \[ окне\]
</dt> <dd>

Предоставляет указатель на запись исключения, имеющую стандартное определение Win64.

</dd> <dt>

*Естаблишерфраме* \[ окне\]
</dt> <dd>

Адрес основания фиксированного выделения стека для этой функции.

</dd> <dt>

*Контекстрекорд* \[ в, out\]
</dt> <dd>

Указывает на контекст исключения на момент возникновения исключения (в случае обработчика исключений) или текущего контекста очистки (в случае обработчика завершения).

</dd> <dt>

*Диспатчерконтекст* \[ в, out\]
</dt> <dd>

Указывает на контекст Dispatcher для этой функции.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>WDM. h</dt> </dl>        |
| Библиотека<br/> | <dl> <dt>NtosKrnl. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Ntoskrnl.exe</dt> </dl> |



 

