---
description: Указывает, каким образом звуковой декодер должен преобразовать многоканальный звук в стерео вывод. Этот процесс также называется свертыванием.
ms.assetid: 6dfe2b97-1ebc-4954-b478-85b3bbba89e3
title: Атрибут MF_MT_AUDIO_FOLDDOWN_MATRIX (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10bb8aa00835ab31f6c05eaa9a1d0e5d9d126b41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683120"
---
# <a name="mf_mt_audio_folddown_matrix-attribute"></a>\_ \_ \_ \_ Атрибут матрицы фолддовн MF Audio

Указывает, каким образом звуковой декодер должен преобразовать многоканальный звук в стерео вывод. Этот процесс также называется *свертыванием*.

## <a name="data-type"></a>Тип данных

массив байтов;

## <a name="remarks"></a>Комментарии

Этот атрибут применяется к типам звуковых носителей.

Значение этого атрибута является структурой [**\_ матрицы мффолддовн**](/windows/desktop/api/mfapi/ns-mfapi-mffolddown_matrix) .

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

 

 




