---
title: Имсрдпдевицеколлектион Рескандевицес, метод
description: Обновляет список объектов в коллекции. | Имсрдпдевицеколлектион Рескандевицес, метод
ms.assetid: 2e2a959d-0a1d-4aca-9daf-3c24fb9b3b08
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Рескандевицес
- Службы удаленных рабочих столов метода Рескандевицес, интерфейс Имсрдпдевицеколлектион
- Службы удаленных рабочих столов интерфейса Имсрдпдевицеколлектион, метод Рескандевицес
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection.RescanDevices
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d62011697b21171f8de326689ca35195ad4057e2e6edd01a5159fcf89c32d0f8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959244"
---
# <a name="imsrdpdevicecollectionrescandevices-method"></a>Метод Имсрдпдевицеколлектион:: Рескандевицес

Обновляет список объектов в коллекции.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT RescanDevices(
  [in] VARIANT_BOOL vboolDynRedir
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*вбулдинредир* \[ окне\]
</dt> <dd>

Состояние перенаправления по умолчанию, которое будет применяться к вновь обнаруженным устройствам или дискам.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если метод выполнен успешно, возвращается значение **S \_ OK** . Любое другое значение **HRESULT** указывает на сбой вызова.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                  |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                            |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| IID<br/>                      | IID \_ имсрдпдевицеколлектион определен как 56540617-d281-488c-8738-6a8fdf64a118<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**имсрдпдевицеколлектион**](imsrdpdevicecollection.md)
</dt> </dl>

 

 





