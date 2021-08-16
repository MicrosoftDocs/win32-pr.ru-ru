---
description: Указывает, каким образом звуковой декодер должен преобразовать многоканальный звук в стерео вывод. Этот процесс также называется свертыванием.
ms.assetid: 6dfe2b97-1ebc-4954-b478-85b3bbba89e3
title: Атрибут MF_MT_AUDIO_FOLDDOWN_MATRIX (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46763f3a32999136993cd3237da9c6cbcdd1d1addb5f6d9041555ac747a6d655
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119714664"
---
# <a name="mf_mt_audio_folddown_matrix-attribute"></a>\_ \_ \_ \_ Атрибут матрицы фолддовн MF Audio

Указывает, каким образом звуковой декодер должен преобразовать многоканальный звук в стерео вывод. Этот процесс также называется *свертыванием*.

## <a name="data-type"></a>Тип данных

массив байтов;

## <a name="remarks"></a>Remarks

Этот атрибут применяется к типам звуковых носителей.

Значение этого атрибута является структурой [**\_ матрицы мффолддовн**](/windows/desktop/api/mfapi/ns-mfapi-mffolddown_matrix) .

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Приложения UWP для классических приложений Vista \|\]<br/>                              |
| Минимальная версия сервера<br/> | Windows \[Приложения UWP для классических приложений сервера 2008 \|\]<br/>                        |
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

 

 




