---
description: Указывает, что Moov будет записано перед полем mdat в созданном файле.
ms.assetid: 97B68B0A-8266-4FCF-8CD9-35890E1AC774
title: Атрибут MF_MPEG4SINK_MOOV_BEFORE_MDAT (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b5d345dc027c457ceb6123ce3854fff4b74f987
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702337"
---
# <a name="mf_mpeg4sink_moov_before_mdat-attribute"></a>MF \_ MPEG4SINK \_ Moov \_ перед \_ атрибутом MDAT

Указывает, что "Moov" будет записан перед полем "mdat" в создаваемом файле.

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="remarks"></a>Комментарии

Поведением приемника мультимедиа MPEG4 по умолчанию является запись "Moov" после поля "mdat". Установка этого атрибута приводит к тому, что созданный файл будет записывать "Moov" перед полем "mdat".

Чтобы приемник MPEG4 мог использовать этот атрибут, переданный поток байтов не должен относиться к низкому или удаленному.

Эта функция включает в себя дополнительное копирование и ремуксинг файлов.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Приложения UWP для классических приложений Windows 8 \|\]<br/>                                  |
| Минимальная версия сервера<br/> | \[Приложения UWP для классических приложений Windows Server 2012 \|\]<br/>                        |
| Header<br/>                   | <dl> <dt>Мфидл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Атрибуты типа мультимедиа](media-type-attributes.md)
</dt> </dl>

 

 




