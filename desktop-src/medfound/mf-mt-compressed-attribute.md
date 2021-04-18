---
description: Указывает тип носителя для сжатия данных мультимедиа.
ms.assetid: b44fb757-4390-4392-b1cb-37772b4ae3fb
title: Атрибут MF_MT_COMPRESSED (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d049795f09845b5d32daf29ef033ab2e4b23007f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544343"
---
# <a name="mf_mt_compressed-attribute"></a>\_ \_ Сжатый атрибут (MF MT)

Указывает тип носителя для сжатия данных мультимедиа.

## <a name="data-type"></a>Тип данных

**UINT32**

Рассматривать как логическое значение.

## <a name="remarks"></a>Комментарии

Если этот атрибут имеет **значение true**, то тип мультимедиа имеет сжатый формат. В противном случае либо тип носителя не сжат, либо тип сжатия неизвестен.

Этот атрибут не обязательно должен иметь значение **true** для всех сжатых форматов, поэтому приложения обычно не полагаются на этот атрибут. Самый надежный способ определить, сжимается ли формат, — поддерживать список известных форматов. Если приложение не распознает формат, как указано в атрибуте [**\_ \_ подтипа MF MT**](mf-mt-subtype-attribute.md) , он не должен принимать никаких сведений о сжатии формата.

Чтобы определить, использует ли формат временное сжатие (это означает, что некоторые примеры вычисляются как разность из предыдущих выборок), проверьте [**\_ \_ \_ \_ независимый атрибут MF MT ALL Samples**](mf-mt-all-samples-independent-attribute.md) .

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

[**Имфаттрибутес:: UINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**Имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**имфмедиатипе**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Атрибуты типа мультимедиа](media-type-attributes.md)
</dt> </dl>

 

 




