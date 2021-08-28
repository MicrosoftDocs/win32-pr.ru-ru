---
description: Задает режим работы с голосовым кодеком.
ms.assetid: 8425cdab-e43c-41ca-9c20-09ab6a5f06f4
title: Свойство MFPKEY_WMAVOICE_ENC_MusicSpeechClassMode (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 303a86adbf9c443149ff78a47d19922284e38d2c0aeb56dcc13a74ca20cd54a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113124"
---
# <a name="mfpkey_wmavoice_enc_musicspeechclassmode-property"></a>МФПКЭЙ \_ вмавоице \_ ENC, \_ свойство мусикспичклассмоде

Задает режим работы с голосовым кодеком.

## <a name="constant-for-ipropertybag"></a>Константа для Ипропертибаг

g \_ всзвмакмусикспичклассмоде

## <a name="data-type"></a>Тип данных

VT \_ I4

## <a name="default-value"></a>Значение по умолчанию

1

## <a name="remarks"></a>Remarks

Значение 1 информирует кодек о том, что содержимое является только голосовым, значение 2 имеет кодек для автоматического определения режима, а любое другое значение информирует кодек о необходимости использования музыкального режима.

Если в автоматическом режиме не выполняется правильная кодировка смешанного голоса и музыки, можно указать кодировку для отдельных разделов файла с помощью свойства [мфпкэй \_ вмавоице \_ ENC \_ ЕДЛ](mfpkey-wmavoice-enc-edlproperty.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                                             |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                    |
| Заголовок<br/>                   | <dl> <dt>Вмкодекдсп. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Свойства Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




