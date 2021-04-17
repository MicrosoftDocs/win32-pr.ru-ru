---
description: Задает окно для Microsoft Media Foundation байтового потока HTTP.
ms.assetid: 52761AC1-4974-4087-B5EE-A797F5BAD86D
title: Свойство MFPKEY_HTTP_ByteStream_Urlmon_Window (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9df398d2c6d7655a68a139545d84cee48f9cf7fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708574"
---
# <a name="mfpkey_http_bytestream_urlmon_window-property"></a>\_Свойство окна мфпкэй HTTP \_ ByteStream \_ Urlmon \_

Задает окно для Microsoft Media Foundation байтового потока HTTP. Это окно используется для представления сведений в пользовательском интерфейсе во время операции привязки.



Тип данных

Тип ПРОПВАРИАНТ (VT)

ПРОПВАРИАНТ, элемент

**IUnknown\***

VT \_ Unknown

**пунквал**



## <a name="remarks"></a>Комментарии

Это свойство используется для настройки потока байтов HTTP Media Foundation. Чтобы задать свойство, передайте указатель [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore) в сопоставитель источника. Дополнительные сведения см. [в разделе Настройка источника мультимедиа](configuring-a-media-source.md).

Значение этого свойства является указателем на интерфейс **ивиндовфорбиндингуи** . Это свойство применяется только в том случае, если свойство [мфпкэй \_ HTTP \_ ByteStream \_ Enable \_ Urlmon](mfpkey-http-bytestream-enable-urlmon.md) имеет значение **Variant \_ true**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Мфидл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Свойства Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
