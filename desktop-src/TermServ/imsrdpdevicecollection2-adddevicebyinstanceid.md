---
title: IMsRdpDeviceCollection2 Адддевицебинстанцеид, метод
description: Добавляет устройство, не имеющее список, в коллекцию устройств.
ms.assetid: 7ef200c5-b99e-40c9-80e1-0758ddfa0902
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Адддевицебинстанцеид
- Службы удаленных рабочих столов метода Адддевицебинстанцеид, интерфейс IMsRdpDeviceCollection2
- Службы удаленных рабочих столов интерфейса IMsRdpDeviceCollection2, метод Адддевицебинстанцеид
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection2.AddDeviceByInstanceId
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97f817a5beb4d8762787c4bf2f8a3995d3918e8e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071140"
---
# <a name="imsrdpdevicecollection2adddevicebyinstanceid-method"></a>Метод IMsRdpDeviceCollection2:: Адддевицебинстанцеид

Добавляет устройство, не имеющее список, в коллекцию устройств.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT AddDeviceByInstanceId(
  [in] RedirectDeviceType Type,
  [in] BSTR               InstanceId
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Тип* \[ окне\]
</dt> <dd>

Тип: **[ **редиректдевицетипе**](redirectdevicetype.md)**

Значение перечисления [**редиректдевицетипе**](redirectdevicetype.md) , указывающее тип добавляемого устройства.

</dd> <dt>

*InstanceId* \[ окне\]
</dt> <dd>

Тип: **BSTR**

Идентификатор экземпляра добавляемого устройства.

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

 

 





