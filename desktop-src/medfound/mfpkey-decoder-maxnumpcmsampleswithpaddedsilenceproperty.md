---
description: Указывает максимальное количество дополнительных выборок PCM, которые могут быть возвращены в конце после декодирования файла.
ms.assetid: 82b3676c-7653-421c-aac7-7f20a642779f
title: Свойство MFPKEY_Decoder_MaxNumPCMSamplesWithPaddedSilence (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b1f97b55c2eedd8cc7d6d524379569073fa35d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711785"
---
# <a name="mfpkey_decoder_maxnumpcmsampleswithpaddedsilence-property"></a>\_Свойство макснумпкмсамплесвиспаддедсиленце декодера мфпкэй \_

Указывает максимальное количество дополнительных выборок PCM, которые могут быть возвращены в конце после декодирования файла.

## <a name="constant-for-ipropertybag"></a>Константа для Ипропертибаг

Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Тип данных

VT \_ I4

## <a name="default-value"></a>Значение по умолчанию

2048

## <a name="remarks"></a>Комментарии

Это свойство можно использовать для оценки искусственного тишина, который вставляется между песнями по мере того, как они помещаются в декодер один за другим.

Для декодеров Windows Media Audio 10 Professional и Windows Media Audio 9 без потерь это свойство всегда равно 0.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                             |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Вмкодекдсп. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Свойства Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
