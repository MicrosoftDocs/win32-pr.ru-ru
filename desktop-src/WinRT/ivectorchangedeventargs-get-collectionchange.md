---
description: Возвращает тип изменения, произошедшего в векторе.
ms.assetid: 213f4794-b972-44e3-a400-8a24b1583ddd
title: 'Метод Ивекторчанжедевентаргс:: get_CollectionChange (Ивекторчанжедевентаргс. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVectorChangedEventArgs.get_CollectionChange
api_type:
- COM
api_location:
- IVectorChangedEventArgs.h
ms.openlocfilehash: a843574bcaf93ec524173ba76800cc15012c89fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263083"
---
# <a name="ivectorchangedeventargsget_collectionchange-method"></a>Метод Ивекторчанжедевентаргс:: Get \_ коллектиончанже

Возвращает тип изменения, произошедшего в векторе.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_CollectionChange(
  [out, retval] CollectionChange *value
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*значение* \[ out, retval\]
</dt> <dd>

Тип: **коллектиончанже \** _

Значение из перечисления [_ *коллектиончанже* *](/uwp/api/Windows.Foundation.Collections.CollectionChange?view=winrt-19041) , описывающее изменение.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                                 |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                                       |
| Header<br/>                   | <dl> <dt>Ивекторчанжедевентаргс. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ивекторчанжедевентаргс**](ivectorchangedeventargs.md)
</dt> </dl>

 

 
