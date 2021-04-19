---
description: Извлекает версию API защиты от потери данных для конечной точки на текущем устройстве.
title: Функция Длпжетенфорцементапиверсион (ендпоинтдлп. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpGetEnforcementApiVersion
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: d2b38b6bdcfd761b8ae3c90ee5d3b430767ad29c
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495948"
---
# <a name="dlpgetenforcementapiversion-function"></a>Функция Длпжетенфорцементапиверсион

Извлекает версию API защиты от потери данных для конечной точки на текущем устройстве.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT WINAPI DlpGetEnforcementApiVersion(_Out_ DWORD* MajorVersion, _Out_ DWORD* MinorVersion);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Majorversion* \[ окне\]
</dt> <dd>

Значение **типа DWORD** , указывающее основной номер версии.

</dd> </dl>

<dl> <dt>

*Majorversion* \[ окне\]
</dt> <dd>

Значение **типа DWORD** , указывающее дополнительный номер версии.

</dd> </dl>


## <a name="return-value"></a>Возвращаемое значение

Возвращает значение HRESULT, включая (но не ограничиваясь) следующие значения.

| HRESULT | Описание: |
|---------|-------------|
| S_OK | Функция успешно завершена |




## <a name="remarks"></a>Remarks


## <a name="requirements"></a>Требования



| Требование          |    Значение                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10, версия 1809 (10,0; Сборка 17763)           |
| DLL<br/>                      | EndpointDlp.dll |