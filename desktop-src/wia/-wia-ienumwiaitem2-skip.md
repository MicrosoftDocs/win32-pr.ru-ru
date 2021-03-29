---
description: Пропускает указанное число элементов во время перечисления доступных объектов IWiaItem2.
ms.assetid: 7a5e9e1c-1e6e-4de0-9499-bf89e35c19aa
title: 'Метод IEnumWiaItem2:: Skip (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumWiaItem2.Skip
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 7618aad923136a9a32d8b7fb935050fefe07bff1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991279"
---
# <a name="ienumwiaitem2skip-method"></a>Метод IEnumWiaItem2:: Skip

Пропускает указанное число элементов во время перечисления доступных объектов [**IWiaItem2**](-wia-iwiaitem2.md) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Skip(
  [in] ULONG cElt
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*cElt* \[ окне\]
</dt> <dd>

Тип: **ulong**

Указывает число пропускаемых элементов.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                               |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 




