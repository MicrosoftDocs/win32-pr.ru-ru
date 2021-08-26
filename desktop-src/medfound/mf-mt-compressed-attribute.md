---
description: Указывает тип носителя для сжатия данных мультимедиа.
ms.assetid: b44fb757-4390-4392-b1cb-37772b4ae3fb
title: Атрибут MF_MT_COMPRESSED (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afea99ffb0c9f7f9f53fb6edd0b4b87b2ecd4ff4f451e5fd0e56d47a70aee994
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060694"
---
# <a name="mf_mt_compressed-attribute"></a>\_ \_ Сжатый атрибут (MF MT)

Указывает тип носителя для сжатия данных мультимедиа.

## <a name="data-type"></a>Тип данных

**UINT32**

Рассматривать как логическое значение.

## <a name="remarks"></a>Remarks

Если этот атрибут имеет **значение true**, то тип мультимедиа имеет сжатый формат. В противном случае либо тип носителя не сжат, либо тип сжатия неизвестен.

Этот атрибут не обязательно должен иметь значение **true** для всех сжатых форматов, поэтому приложения обычно не полагаются на этот атрибут. Самый надежный способ определить, сжимается ли формат, — поддерживать список известных форматов. Если приложение не распознает формат, как указано в атрибуте [**\_ \_ подтипа MF MT**](mf-mt-subtype-attribute.md) , он не должен принимать никаких сведений о сжатии формата.

Чтобы определить, использует ли формат временное сжатие (это означает, что некоторые примеры вычисляются как разность из предыдущих выборок), проверьте [**\_ \_ \_ \_ независимый атрибут MF MT ALL Samples**](mf-mt-all-samples-independent-attribute.md) .

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Приложения UWP для классических приложений Vista \|\]<br/>                              |
| Минимальная версия сервера<br/> | Windows \[Приложения UWP для классических приложений сервера 2008 \|\]<br/>                        |
| Заголовок<br/>                   | <dl> <dt>Мфапи. h</dt> </dl> |



## <a name="see-also"></a>См. также

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

 

 




