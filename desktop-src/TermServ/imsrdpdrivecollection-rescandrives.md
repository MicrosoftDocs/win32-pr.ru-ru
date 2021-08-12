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
ms.openlocfilehash: 2490e3879420701537cd36999ba33fde9ebfaf1e2f93d75550807e552fadacd0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118606191"
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

 

 





