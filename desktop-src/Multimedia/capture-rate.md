---
title: Частота захвата
description: Частота захвата
ms.assetid: 70cac7ac-0f7e-431e-a099-b075ba5fb039
keywords:
- Сообщение WM_CAP_GET_SEQUENCE_SETUP
- макрос Капкаптурежетсетуп
- Структура КАПТУРЕПАРМС
- Сообщение WM_CAP_SET_SEQUENCE_SETUP
- макрос Капкаптуресетсетуп
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93be9e94f5f9085d25c6ad85a30b115d13349169
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067975"
---
# <a name="capture-rate"></a>Частота захвата

Скорость записи — это число кадров, которые записываются каждую секунду сеанса записи. Текущую скорость записи можно получить с помощью сообщения о [**\_ \_ \_ \_ настройке получения закрепления WM**](wm-cap-get-sequence-setup.md) (или макроса [**капкаптурежетсетуп**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ). Текущая скорость записи хранится в элементе **дврекуестмикросекперфраме** структуры [**каптурепармс**](/windows/win32/api/vfw/ns-vfw-captureparms) . Можно задать скорость записи, указав число микросекунд между последовательными кадрами в качестве значения этого элемента, а затем отправив обновленную структуру **каптурепармс** в окно Capture с помощью сообщения [**\_ установки закрепления WM \_ Set \_ Sequence \_**](wm-cap-set-sequence-setup.md) (или макроса [**капкаптуресетсетуп**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) ). Значение по умолчанию **дврекуестмикросекперфраме** — 66667, которое соответствует 15 кадрам в секунду.

 

 




