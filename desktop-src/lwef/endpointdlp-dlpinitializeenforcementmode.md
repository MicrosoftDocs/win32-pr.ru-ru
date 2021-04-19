---
description: Уведомляет систему о требуемых режимах применения для набора операций защиты от потери данных в конечной точке.
title: Функция Длпинитиализинфорцементмоде (ендпоинтдлп. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpInitializeEnforcementMode
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: cff3e1609f15f2cbbe6f6d9f76c6433ba3f4e5d7
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495918"
---
# <a name="dlpinitializeenforcementmode-function"></a>Функция Длпинитиализинфорцементмоде

Уведомляет систему о требуемых режимах применения для набора операций защиты от потери данных в конечной точке.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT WINAPI DlpInitializeEnforcementMode(_In_ DWORD Count, _In_reads_(Count) PDLP_APP_OP_ENLIGHTENED_LEVEL OperationEnforcement);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Количество* \[ окне\]
</dt> <dd>

Значение **типа DWORD** , указывающее количество операций, включаемых в массив *оператионенфорцемент* .

</dd> </dl>

<dl> <dt>

*Оператионенфорцемент* \[ окне\]
</dt> <dd>

Массив структур [DLP_APP_OP_ENLIGHTENED_LEVEL](endpointdlp-dlp_app_op_enlightened_level.md) , которые указывают уровень применения для операции защиты от потери данных конечной точки.

</dd> </dl>


## <a name="return-value"></a>Возвращаемое значение

Возвращает значение HRESULT, включая (но не ограничиваясь) следующие значения.

| HRESULT | Описание: |
|---------|-------------|
| S_OK | Функция успешно завершена |
| E_INVALIDARG | Один или несколько параметров функции являются недопустимыми. |
| E_OUTOFMEMORY | Не удалось выделить память для операции. |



## <a name="remarks"></a>Remarks


## <a name="requirements"></a>Требования



| Требование          |    Значение                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10, версия 1809 (10,0; Сборка 17763)           |
| DLL<br/>                      | EndpointDlp.dll |