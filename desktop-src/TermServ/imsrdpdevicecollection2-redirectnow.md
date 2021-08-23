---
title: IMsRdpDeviceCollection2 Редиректнов, метод
description: Принудительное перенаправление или удаление устройств, которые были выбраны или отменены из коллекции.
ms.assetid: 9cd5849d-a589-43f3-b904-6b2e15ca033d
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Редиректнов
- Службы удаленных рабочих столов метода Редиректнов, интерфейс IMsRdpDeviceCollection2
- Службы удаленных рабочих столов интерфейса IMsRdpDeviceCollection2, метод Редиректнов
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection2.RedirectNow
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60c92eff142305e95a71c69cdce9789b0d2316e3d5e60b703a7c1aa8e835688f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058922"
---
# <a name="imsrdpdevicecollection2redirectnow-method"></a>Метод IMsRdpDeviceCollection2:: Редиректнов

Принудительное перенаправление или удаление устройств, которые были выбраны или отменены из коллекции.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT RedirectNow(
  [in] RedirectDeviceType Type
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Тип* \[ окне\]
</dt> <dd>

Тип: **[ **редиректдевицетипе**](redirectdevicetype.md)**

Значение перечисления [**редиректдевицетипе**](redirectdevicetype.md) , указывающее тип устройства для перенаправления.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                   |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                         |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**редиректдевицетипе**](redirectdevicetype.md)
</dt> <dt>

[**IMsRdpDeviceCollection2**](imsrdpdevicecollection2.md)
</dt> </dl>

 

 





