---
title: WMT_STATUS уведомления о событии в DirectShow
description: '\_Уведомление о событии состояния ВМТ в DirectShow'
ms.assetid: 6b777c7e-2777-445b-88de-a9a28be6da9c
keywords:
- Windows Пакет SDK для формата мультимедиа, WMT_STATUS уведомлений о событиях в DirectShow
- Windows Пакет SDK для формата мультимедиа, уведомления о событиях
- Windows Пакет SDK для формата мультимедиа, DirectShow
- Расширенный формат систем (ASF), WMT_STATUS уведомления о событиях в DirectShow
- ASF (Расширенный системный формат), WMT_STATUS уведомлений о событиях в DirectShow
- Расширенный формат систем (ASF), уведомления о событиях
- ASF (Расширенный системный формат), уведомления о событиях
- Расширенный формат систем (ASF), DirectShow
- ASF (Расширенный системный формат), DirectShow
- DirectShow, уведомления о событиях
- DirectShow, WMT_STATUS уведомления о событиях
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb4bbe430f16872baf94a0d47417381bc8bcd23d5c9fbbdb69ff2496cd873908
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089634"
---
# <a name="wmt_status-event-notification-in-directshow"></a>\_Уведомление о событии состояния ВМТ в DirectShow

Обработчики ASF и модуля записи ASF пересылают [**события \_ состояния ВМТ**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) в приложения. Модуль записи перенаправляет все такие события, а модуль чтения перенаправляет только те из них, которые относятся к приобретению лицензии DRM. Чтобы получать эти уведомления о событиях в приложении, добавьте обращение к **\_ \_ событию EC ВМТ** в функции обработки событий. Параметр *lParam1* , связанный с событием, содержит **код \_ состояния ВМТ** (который может быть **ВМТ \_ Error**), а lParam2 содержит [**\_ \_ \_ данные о событии AM ВМТ**](/previous-versions/windows/desktop/api/evcode/ns-evcode-am_wmt_event_data) , включающие **HRESULT**.

 

 