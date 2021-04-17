---
description: Задает режим работы с голосовым кодеком.
ms.assetid: 8425cdab-e43c-41ca-9c20-09ab6a5f06f4
title: Свойство MFPKEY_WMAVOICE_ENC_MusicSpeechClassMode (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9776c76f2a8863afe73626f5a2940de2c0ccb7cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692592"
---
# <a name="mfpkey_wmavoice_enc_musicspeechclassmode-property"></a>МФПКЭЙ \_ вмавоице \_ ENC, \_ свойство мусикспичклассмоде

Задает режим работы с голосовым кодеком.

## <a name="constant-for-ipropertybag"></a>Константа для Ипропертибаг

g \_ всзвмакмусикспичклассмоде

## <a name="data-type"></a>Тип данных

VT \_ I4

## <a name="default-value"></a>Значение по умолчанию

1

## <a name="remarks"></a>Комментарии

Значение 1 информирует кодек о том, что содержимое является только голосовым, значение 2 имеет кодек для автоматического определения режима, а любое другое значение информирует кодек о необходимости использования музыкального режима.

Если в автоматическом режиме не выполняется правильная кодировка смешанного голоса и музыки, можно указать кодировку для отдельных разделов файла с помощью свойства [мфпкэй \_ вмавоице \_ ENC \_ ЕДЛ](mfpkey-wmavoice-enc-edlproperty.md) .

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

 

 




