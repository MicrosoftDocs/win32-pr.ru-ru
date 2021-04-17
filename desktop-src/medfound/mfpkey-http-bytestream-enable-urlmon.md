---
description: Разрешает потоку байтов HTTP Microsoft Media Foundation использовать моникеры URL-адресов (также называемые Urlmon).
ms.assetid: 8B7D2FF7-D8A8-49E9-8CED-D37853B97A8F
title: Свойство MFPKEY_HTTP_ByteStream_Enable_Urlmon (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1858f34a5f719caba1a48f049b95f2031b400240
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675015"
---
# <a name="mfpkey_http_bytestream_enable_urlmon-property"></a>МФПКЭЙ \_ HTTP \_ ByteStream \_ Enable \_ Urlmon, свойство

Разрешает потоку байтов HTTP Microsoft Media Foundation использовать моникеры URL-адресов (также называемые *Urlmon*).



Тип данных

Тип ПРОПВАРИАНТ (VT)

ПРОПВАРИАНТ, элемент

**VARIANT \_ bool**

Логическое значение VT \_

**булвал**



## <a name="remarks"></a>Комментарии

Это свойство используется для настройки потока байтов HTTP Media Foundation. Чтобы задать свойство, передайте указатель [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore) в сопоставитель источника. Дополнительные сведения см. [в разделе Настройка источника мультимедиа](configuring-a-media-source.md).

Если значение является **вариантным \_ true**, то поток байтов HTTP использует Urlmon для транспорта HTTP. В противном случае, если значение является **вариантным \_ false**, байтовый поток использует WinHTTP.

Значение по умолчанию — **вариант \_ true** для приложений Магазина Windows и **вариант \_ false** для классического приложения Windows.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Мфидл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Свойства Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
