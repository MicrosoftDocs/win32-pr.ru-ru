---
description: Указывает режим использования кодировщика УВК H. 264.
ms.assetid: 05158F47-CE01-4C99-8FFA-6BBD4F829B59
title: Атрибут MF_MT_H264_USAGE (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ad5239c81e490f5069b8a6f95d4a91c1f150f37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145604"
---
# <a name="mf_mt_h264_usage-attribute"></a>\_ \_ Атрибут использования H264 Single bitrate MF MT \_

Указывает режим использования кодировщика УВК H. 264.

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Применяется к

[**имфмедиатипе**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>Комментарии

Этот атрибут применяется к типам носителей для потоков H. 264, переданных по USB. Значение соответствует полю **бусаже** в элементе управления зонда/commit УВК 1,2 H. 264.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Приложения UWP для классических приложений Windows 8 \|\]<br/>                                  |
| Минимальная версия сервера<br/> | \[Приложения UWP для классических приложений Windows Server 2012 \|\]<br/>                        |
| Header<br/>                   | <dl> <dt>Мфапи. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Атрибуты типа мультимедиа](media-type-attributes.md)
</dt> </dl>

 

 




