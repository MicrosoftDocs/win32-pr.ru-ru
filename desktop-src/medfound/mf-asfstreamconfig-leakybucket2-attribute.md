---
description: Задает пиковое &\# 0034;&\# 0034; параметров (см. примечания) для кодирования файла Windows Media. Эти параметры используются для пиковой скорости. Задайте этот атрибут с помощью интерфейса Имфасфстреамконфиг.
ms.assetid: 422d6d1b-4d29-4156-877b-8dc3bcb7580f
title: Атрибут MF_ASFSTREAMCONFIG_LEAKYBUCKET2 (Вмконтаинер. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94c4cca3252d543d35bef37d70dcb612c24df6ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674013"
---
# <a name="mf_asfstreamconfig_leakybucket2-attribute"></a>\_Атрибут MF асфстреамконфиг \_ LEAKYBUCKET2

Задает пиковые параметры "сегмент утечки" (см. примечания) для кодирования файла Windows Media. Эти параметры используются для пиковой скорости. Задайте этот атрибут с помощью интерфейса [**имфасфстреамконфиг**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) .

## <a name="data-type"></a>Тип данных

массив байтов;

## <a name="remarks"></a>Комментарии

Значение этого атрибута представляет собой массив из трех **DWORD** в следующем порядке:

-   Скорость в битах в секунду.
-   Окно буфера в миллисекундах.
-   Заполнение начальной буферизации в байтах.

Дополнительные сведения о концепции сегмента утечки см. в разделе [модель буферного контейнера с утечкой](the-leaky-bucket-buffer-model.md) данных в документации пакета Windows Media Format SDK.

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Вмконтаинер. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

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

 

 




