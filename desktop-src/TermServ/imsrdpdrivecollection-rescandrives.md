---
title: Имсрдпдривеколлектион Рескандривес, метод
description: Обновляет список объектов в коллекции. | Имсрдпдривеколлектион Рескандривес, метод
ms.assetid: 5997b76c-d130-4375-b6ff-5ea871f059cc
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Рескандривес
- Службы удаленных рабочих столов метода Рескандривес, интерфейс Имсрдпдривеколлектион
- Службы удаленных рабочих столов интерфейса Имсрдпдривеколлектион, метод Рескандривес
topic_type:
- apiref
api_name:
- IMsRdpDriveCollection.RescanDrives
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7488187e44caeaedb7c73b01ff8a3711e20dcdd1
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105684840"
---
# <a name="imsrdpdrivecollectionrescandrives-method"></a>Метод Имсрдпдривеколлектион:: Рескандривес

Обновляет список объектов в коллекции.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT RescanDrives(
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                 |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                           |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| IID<br/>                      | IID \_ имсрдпдривеколлектион определен как 7ff17599-da2c-4677-ad35-f60c04fe1585<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**имсрдпдривеколлектион**](imsrdpdrivecollection.md)
</dt> </dl>

 

 





