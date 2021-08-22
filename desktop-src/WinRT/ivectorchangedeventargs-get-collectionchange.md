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
ms.openlocfilehash: 2476f9563b4e2a0cabf9babbcfc265ee4f3549416c2fdfda0dbb0f204b7ca9bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119504814"
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

Тип: **коллектиончанже \***

Значение из перечисления [**коллектиончанже**](/uwp/api/Windows.Foundation.Collections.CollectionChange?view=winrt-19041) , описывающее изменение.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                                 |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                                       |
| Заголовок<br/>                   | <dl> <dt>Ивекторчанжедевентаргс. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**ивекторчанжедевентаргс**](ivectorchangedeventargs.md)
</dt> </dl>

 

 
