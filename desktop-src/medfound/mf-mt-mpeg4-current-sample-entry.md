---
description: Задает текущую запись в поле Образец описания для типа носителя MPEG-4.
ms.assetid: c8c36abf-6905-4874-a6d2-90dd0725421b
title: Атрибут MF_MT_MPEG4_CURRENT_SAMPLE_ENTRY (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 660f74c1f9335556b514607cc2100f7ef59a00fba84f6cfe90412b91e1ff500a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117877038"
---
# <a name="mf_mt_mpeg4_current_sample_entry-attribute"></a>\_ \_ \_ Текущий \_ пример \_ атрибута записи MF MT MPEG4

Задает текущую запись в поле Образец описания для типа носителя MPEG-4.

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Применяется к

[**имфмедиатипе**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>Remarks

В файле MP4 или 3GP в поле Описание примера описывается кодировка, используемая для потока в файле. В поле Описание образца может содержаться несколько записей. Этот атрибут указывает, какую запись использовать. Значение — это Отсчитываемый от нуля индекс в списке.

В настоящее время единственным поддерживаемым значением является 0. Атрибут был определен для будущего расширения.

Источник файла MPEG-4 всегда задает значение 0. Приемники файлов MP4 и 3GP игнорируют значение этого атрибута, если оно имеется.

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[приложения UWP для классических приложений Windows 7 \|\]<br/>                                  |
| Минимальная версия сервера<br/> | Windows \[Приложения UWP для настольных приложений Server 2008 R2 \|\]<br/>                     |
| Заголовок<br/>                   | <dl> <dt>Мфапи. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Атрибуты типа мультимедиа](media-type-attributes.md)
</dt> <dt>

[\_ \_ \_ Описание образца MPEG4 \_ MF](mf-mt-mpeg4-sample-description.md)
</dt> </dl>

 

 




