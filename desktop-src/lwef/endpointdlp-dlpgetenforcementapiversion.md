---
description: Извлекает версию API защиты от потери данных для конечной точки на текущем устройстве.
title: Функция DlpGetEnforcementApiVersion (endpointdlp.h)
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
ms.openlocfilehash: d126b720f1b6a0912598671c75240fb7f2a351098fc1fb00a748d873d1481905
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119725804"
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