---
description: Указывает категорию Media Foundation преобразования (MFT).
ms.assetid: cebd64ea-b20f-4ccc-805f-0deab3096bc3
title: Атрибут MF_TRANSFORM_CATEGORY_Attribute (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd3c64fd5e19bba10646957e7c247294b6d82a97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263356"
---
# <a name="mf_transform_category_attribute-attribute"></a>\_ \_ Атрибут атрибута категории для преобразования MF \_

Указывает категорию Media Foundation преобразования (MFT).

## <a name="data-type"></a>Тип данных

**GUID**

Список возможных значений см. в разделе [**MFT \_ Category**](mft-category.md).

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите [**имфаттрибутес::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)InAttribute.

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: сетгуид**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).

## <a name="remarks"></a>Комментарии

Этот атрибут задается для указателей [**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) , возвращаемых функцией [**мфтенумекс**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .

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

[Атрибуты преобразования](transform-attributes.md)
</dt> </dl>

 

 




