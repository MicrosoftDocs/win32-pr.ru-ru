---
description: '\_ \_ Структура Cap в настройках потока TAPI \_ содержит сведения о конфигурации видео или звукового потока.'
ms.assetid: 83b39751-b00f-4762-830b-13cafbcb1cfd
title: Структура TAPI_STREAM_CONFIG_CAPS (Ипмсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cbbb3b3ec72cc99810311cc510e36c2adc8242e2b3d98b321fd8bc8c6a9ab4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002652"
---
# <a name="tapi_stream_config_caps-structure"></a>\_ \_ Структура Caps конфигурации потока TAPI \_

\[эта структура недоступна для использования в Windows Vista, Windows Server 2008 и последующих версиях операционной системы. API клиента RTC предоставляет аналогичные функциональные возможности.\]

Структура **\_ Cap в \_ настройках \_ потока TAPI** содержит сведения о конфигурации видео или звукового потока.

## <a name="syntax"></a>Синтаксис


```C++
} TAPI_STREAM_CONFIG_CAPS, *PTAPI_STREAM_CONFIG_CAPS;
```



## <a name="members"></a>Члены

<dl> <dt>

**капстипе**
</dt> <dd>

Определяет, содержит ли член объединения данные видео или аудио.

</dd> <dt>

**видеокап**
</dt> <dd>

Структура [**\_ \_ \_ \_ Caps конфигурации потока видео TAPI**](tapi-video-stream-config-caps.md) , содержащая возможности потокового видео.

</dd> <dt>

**аудиокап**
</dt> <dd>

Структура [**\_ \_ \_ \_ Caps конфигурации аудио-потока TAPI**](tapi-audio-stream-config-caps.md) , содержащая возможности аудиопотока.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------|------------------------------------------------------------------------------------|
| Версия TAPI<br/> | Требуется TAPI 3,1<br/>                                                       |
| Заголовок<br/>       | <dl> <dt>Ипмсп. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Итформатконтрол:: Жетстреамкапс**](itformatcontrol-getstreamcaps.md)
</dt> <dt>

[**стреамконфигкапстипе**](streamconfigcapstype.md)
</dt> <dt>

[**\_ \_ \_ политики настройки потока видео \_ TAPI**](tapi-video-stream-config-caps.md)
</dt> <dt>

[**\_ \_ \_ ограничения конфигурации аудио потока \_ TAPI**](tapi-audio-stream-config-caps.md)
</dt> </dl>

 

 




