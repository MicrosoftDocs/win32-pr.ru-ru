---
description: Задает корневой идентификатор безопасности для Microsoft Media Foundation байтового потока HTTP.
ms.assetid: DD2B9487-53B0-4753-8C47-4D6BFE113109
title: Свойство MFPKEY_HTTP_ByteStream_Urlmon_Security_Id (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cf23e0c3d4aa5ab25590cfdb207fd50f04ecaec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699112"
---
# <a name="mfpkey_http_bytestream_urlmon_security_id-property"></a>\_ \_ \_ \_ Свойство идентификатора безопасности мфпкэй HTTP ByteStream Urlmon \_

Задает корневой идентификатор безопасности для Microsoft Media Foundation байтового потока HTTP.



Тип данных

Тип ПРОПВАРИАНТ (VT)

ПРОПВАРИАНТ, элемент

**кауб**

VT \_ вектор \| VT \_ UI1

**кауб**



## <a name="remarks"></a>Комментарии

Это свойство используется для настройки потока байтов HTTP Media Foundation. Чтобы задать свойство, передайте указатель [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore) в сопоставитель источника. Дополнительные сведения см. [в разделе Настройка источника мультимедиа](configuring-a-media-source.md).

Это свойство применяется только в том случае, если свойство [мфпкэй \_ HTTP \_ ByteStream \_ Enable \_ Urlmon](mfpkey-http-bytestream-enable-urlmon.md) имеет значение **Variant \_ true**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Мфидл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Свойства Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
