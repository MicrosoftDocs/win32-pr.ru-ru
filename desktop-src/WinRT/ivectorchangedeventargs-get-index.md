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
ms.openlocfilehash: 5c131567ec7fc2861ce11db9e5d7ec581f6f663a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072752"
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

Тип: **без знака \** _

Отсчитываемая от нуля координата в векторе, где произошло изменение, если применимо.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: _ *HRESULT**

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

 

 




