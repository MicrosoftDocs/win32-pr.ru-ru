---
title: Буферы видео
description: Буферы видео
ms.assetid: 0dfe01ec-f997-4e5e-a73d-e6b712d0e19e
keywords:
- Сообщение WM_CAP_GET_SEQUENCE_SETUP
- макрос Капкаптурежетсетуп
- Сообщение WM_CAP_SET_SEQUENCE_SETUP
- макрос Капкаптуресетсетуп
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46a6493d22a495a56084e89d2b067c1cf9a874752b44b81f636b5a184b895199
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687694"
---
# <a name="video-buffers"></a>Буферы видео

Буферы, используемые для записи видео, находятся в куче памяти. Количество буферов, используемых в операции записи, может зависеть от значения элемента **внумвидеорекуестед** структуры [**каптурепармс**](/windows/win32/api/vfw/ns-vfw-captureparms) и доступной системной памяти.

Текущее значение запрошенных буферов видео можно получить с помощью сообщения о [**\_ \_ \_ \_ настройке получения закрепления WM**](wm-cap-get-sequence-setup.md) (или макроса [**капкаптурежетсетуп**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ). Текущее запрошенное число буферов видео хранится в элементе **внумвидеорекуестед** структуры **каптурепармс** . Вы можете запросить размещение и количество буферов, обновив этот элемент, а затем отправив обновленную структуру **каптурепармс** в окно Capture с помощью сообщения [**\_ установки закрепления WM \_ Set \_ Sequence \_**](wm-cap-set-sequence-setup.md) (или макроса [**капкаптуресетсетуп**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) ).

 

 




