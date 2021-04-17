---
description: Задает флаги привязки моникера для Microsoft Media Foundation байтового потока HTTP.
ms.assetid: 9426D235-65E1-40BA-94E9-CF0C49263E6F
title: Свойство MFPKEY_HTTP_ByteStream_Urlmon_Bind_Flags (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32863929b92f16a809468055db81361f8116196e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694653"
---
# <a name="mfpkey_http_bytestream_urlmon_bind_flags-property"></a>\_ \_ \_ \_ Свойство флагов привязки мфпкэй HTTP ByteStream Urlmon \_

Задает флаги привязки моникера для Microsoft Media Foundation байтового потока HTTP.



Тип данных

Тип ПРОПВАРИАНТ (VT)

ПРОПВАРИАНТ, элемент

**ULONG**

VT \_ UI4

**улвал**



## <a name="remarks"></a>Комментарии

Это свойство используется для настройки потока байтов HTTP Media Foundation. Чтобы задать свойство, передайте указатель [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore) в сопоставитель источника. Дополнительные сведения см. [в разделе Настройка источника мультимедиа](configuring-a-media-source.md).

Значение этого свойства является **побитовым** для флагов перечисления **биндф** . Это свойство применяется только в том случае, если свойство [мфпкэй \_ HTTP \_ ByteStream \_ Enable \_ Urlmon](mfpkey-http-bytestream-enable-urlmon.md) имеет значение **Variant \_ true**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Мфидл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Свойства Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
