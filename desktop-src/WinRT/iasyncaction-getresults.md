---
description: Возвращает результат асинхронного действия.
ms.assetid: E5AF357D-B1EE-4581-AEBC-6F1C89D7DBB0
title: 'IAsyncAction:: Results, метод'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAsyncAction.GetResults
api_type:
- COM
api_location:
- Windows.Foundation.idl
ms.openlocfilehash: 62196c7f8ded67bed0ecdb3ea33420de54301bbd379615126ada158ea9e725ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118561056"
---
# <a name="iasyncactiongetresults-method"></a>IAsyncAction:: Results, метод

Возвращает результат асинхронного действия.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetResults();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Этот метод всегда возвращает значение **S \_ ОК**.

## <a name="remarks"></a>Remarks

Вызов метода **IAsyncAction** не имеет силы, если текущая реализация имеет динамический тип [](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                              |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                                    |
| Header<br/>                   | <dl> <dt>Windows. Foundation. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IAsyncAction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction)
</dt> </dl>

 

 
