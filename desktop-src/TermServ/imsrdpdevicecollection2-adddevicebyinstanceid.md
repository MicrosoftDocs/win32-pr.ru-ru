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
ms.openlocfilehash: df11fa2a58aca505661da1f7643f8d1d6ff2f502e6c10bf835aa67a6e2d0615d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119870824"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                   |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                         |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**редиректдевицетипе**](redirectdevicetype.md)
</dt> <dt>

[**IMsRdpDeviceCollection2**](imsrdpdevicecollection2.md)
</dt> </dl>

 

 





