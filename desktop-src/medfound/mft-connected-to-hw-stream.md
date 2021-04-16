---
description: Указывает, подключено ли аппаратное преобразование Media Foundation к другому MFT на основе оборудования.
ms.assetid: 9166c43f-d2ae-4dc7-84e9-02146b67efe2
title: Атрибут MFT_CONNECTED_TO_HW_STREAM (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d5a3e8e4da74b3d581dd5ae4a53a03dc2b0fd67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105656555"
---
# <a name="mft_connected_to_hw_stream-attribute"></a>MFT \_ подключено \_ к \_ \_ атрибуту потока HW

Указывает, подключено ли аппаратное преобразование Media Foundation к другому MFT на основе оборудования.

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Комментарии

Приложения обычно не используют этот атрибут.

Этот атрибут используется с МФТС на основе оборудования. При подключении двух МФТС оборудования в топологии загрузчик топологии присваивает этому атрибуту **значение true** для следующих объектов:

-   Выходной поток вышестоящей MFT
-   Входной поток нисходящих файлов MFT

Чтобы получить хранилище атрибутов для выходного потока, загрузчик топологии вызывает [**имфтрансформ:: жетаутпутстреаматтрибутес**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes) в вышестоящей MFT. Чтобы получить хранилище атрибутов для входного потока, загрузчик топологии вызывает [**имфтрансформ:: жетинпутстреаматтрибутес**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes) в ПОДЧИНЕННОЙ таблице MFT.

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Приложения UWP для классических приложений Windows 7 \|\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Приложения UWP для классических приложений Windows Server 2008 R2 \|\]<br/>                           |
| Header<br/>                   | <dl> <dt>Мфтрансформ. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Оборудование МФТС](hardware-mfts.md)
</dt> <dt>

[Атрибуты преобразования](transform-attributes.md)
</dt> </dl>

 

 




