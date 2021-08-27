---
description: задает пиковое &\# 0034;&\# 0034; параметров (см. примечания) для кодирования файла Windows мультимедиа. Эти параметры используются для пиковой скорости. Задайте этот атрибут с помощью интерфейса Имфасфстреамконфиг.
ms.assetid: 422d6d1b-4d29-4156-877b-8dc3bcb7580f
title: Атрибут MF_ASFSTREAMCONFIG_LEAKYBUCKET2 (Вмконтаинер. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a540cab766cbd6a6a7246139d0e19e12c89e5ed837d40cdc3e10d9589f72ebe5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060844"
---
# <a name="mf_asfstreamconfig_leakybucket2-attribute"></a>\_Атрибут MF асфстреамконфиг \_ LEAKYBUCKET2

задает пиковые параметры "сегмент утечки" (см. примечания) для кодирования Windowsного файла мультимедиа. Эти параметры используются для пиковой скорости. Задайте этот атрибут с помощью интерфейса [**имфасфстреамконфиг**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) .

## <a name="data-type"></a>Тип данных

массив байтов;

## <a name="remarks"></a>Remarks

Значение этого атрибута представляет собой массив из трех **DWORD** в следующем порядке:

-   Скорость в битах в секунду.
-   Окно буфера в миллисекундах.
-   Заполнение начальной буферизации в байтах.

дополнительные сведения о концепции сегмента утечки см. в разделе [модель буферного контейнера с утечкой](the-leaky-bucket-buffer-model.md) данных в документации по Windows Media Format SDK.

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                           |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                     |
| Заголовок<br/>                   | <dl> <dt>Вмконтаинер. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Атрибуты ASF](asf-attributes.md)
</dt> <dt>

[**Имфаттрибутес:: BLOB**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**Имфаттрибутес:: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**MF \_ асфстреамконфиг \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md)
</dt> </dl>

 

 




