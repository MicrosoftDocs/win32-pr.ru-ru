---
description: Содержит пример поля описания для файла MP4 или 3GP.
ms.assetid: ea157988-bd15-465c-bd6a-6d33cc1a0323
title: Атрибут MF_MT_MPEG4_SAMPLE_DESCRIPTION (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4620ae0b50a2c6f2dae7663aab0c49f13bc5a162
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912163"
---
# <a name="mf_mt_mpeg4_sample_description-attribute"></a>\_ \_ \_ Атрибут описания примера "MF MT MPEG4" \_

Содержит пример поля описания для файла MP4 или 3GP.

## <a name="data-type"></a>Тип данных

**ДВУХБАЙТОВЫХ\[\]**

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес::-BLOB**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).

## <a name="applies-to"></a>Применяется к

[**имфмедиатипе**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>Комментарии

В поле Описание примера описывается кодировка, используемая для потока в файле.

Источник файлов MPEG-4 задает этот атрибут для типа носителя для каждого потока. Значением атрибута является необработанные данные в поле Описание образца. Если источник файла MPEG-4 может выполнить синтаксический анализ образца описания, он также добавляет сведения о формате в тип мультимедиа. В противном случае приложение или декодер должны проанализировать пример описания в \_ \_ \_ \_ атрибуте описания образца Description MF.

При задании этого атрибута в приемнике MPEG-4 с помощью метода [**имфмедиатипехандлер:: сеткуррентмедиатипе**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) данные для атрибута с описанием в формате MF, \_ записанные в виде \_ \_ описания образца, \_ не должны изменяться после отправки одного или нескольких выборок в приемник в соответствующем потоке [**имфстреамсинк::P роцесссампле**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-processsample) .

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Приложения UWP для классических приложений Windows 7 \|\]<br/>                                  |
| Минимальная версия сервера<br/> | \[Приложения UWP для классических приложений Windows Server 2008 R2 \|\]<br/>                     |
| Header<br/>                   | <dl> <dt>Мфапи. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Атрибуты типа мультимедиа](media-type-attributes.md)
</dt> </dl>

 

 




