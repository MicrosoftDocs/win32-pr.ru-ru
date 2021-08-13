---
description: Возвращает позицию в векторе, где произошло изменение.
ms.assetid: 00756d77-aae0-45f0-8bd4-cf68af9bdc7c
title: 'Метод Ивекторчанжедевентаргс:: get_Index (Ивекторчанжедевентаргс. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVectorChangedEventArgs.get_Index
api_type:
- COM
api_location:
- IVectorChangedEventArgs.h
ms.openlocfilehash: 72df7f0d46e1e3073262c43064daf58b1fefbf43af913bb7f1b912ed22e67a7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118560650"
---
# <a name="ivectorchangedeventargsget_index-method"></a>Метод индекса Ивекторчанжедевентаргс:: Get \_

Возвращает позицию в векторе, где произошло изменение.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_Index(
  [out, retval] unsigned *value
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*значение* \[ out, retval\]
</dt> <dd>

Тип: **без знака \***

Отсчитываемая от нуля координата в векторе, где произошло изменение, если применимо.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                                 |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                                       |
| Header<br/>                   | <dl> <dt>Ивекторчанжедевентаргс. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ивекторчанжедевентаргс**](ivectorchangedeventargs.md)
</dt> </dl>

 

 




