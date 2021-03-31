---
description: Содержит тип мультимедиа, упакованный в другой тип мультимедиа.
ms.assetid: 3bd94523-0206-44d8-83a2-e569e4ab7815
title: Атрибут MF_MT_WRAPPED_TYPE (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ad09c69f7b99c2c376a207270cadb034e735546
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423526"
---
# <a name="mf_mt_wrapped_type-attribute"></a>\_ \_ Атрибут типа, упакованного в формате MF \_

Содержит тип мультимедиа, упакованный в другой тип мультимедиа.

## <a name="data-type"></a>Тип данных

массив байтов;

## <a name="remarks"></a>Комментарии

Этот атрибут используется в функции [**мфврапмедиатипе**](/windows/desktop/api/mfapi/nf-mfapi-mfwrapmediatype) , которая создает оболочку для типа мультимедиа внутри другого типа мультимедиа.

Функция [**мфврапмедиатипе**](/windows/desktop/api/mfapi/nf-mfapi-mfwrapmediatype) выполняет следующие действия:

1.  Преобразует исходный тип мультимедиа в двоичный массив.
2.  Задает атрибут **\_ типа MF MT, \_ упакованный \_** для нового типа носителя. Значением атрибута является двоичный массив.

Обычно приложения не используют этот атрибут напрямую. Для распаковки исходного типа мультимедиа вызовите [**мфунврапмедиатипе**](/windows/desktop/api/mfapi/nf-mfapi-mfunwrapmediatype).

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Приложения UWP для классических приложений Windows Vista \|\]<br/>                              |
| Минимальная версия сервера<br/> | \[Приложения UWP для классических приложений Windows Server 2008 \|\]<br/>                        |
| Header<br/>                   | <dl> <dt>Мфапи. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**Имфаттрибутес:: BLOB**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**Имфаттрибутес:: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**имфмедиатипе**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Атрибуты типа мультимедиа](media-type-attributes.md)
</dt> </dl>

 

 




