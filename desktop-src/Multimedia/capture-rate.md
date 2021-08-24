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
ms.openlocfilehash: 855cff56e36d9a246e1f18ae5fc4e3c09a200a2114104424f053a8780881de93
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691664"
---
# <a name="capture-rate"></a>Частота захвата

Скорость записи — это число кадров, которые записываются каждую секунду сеанса записи. Текущую скорость записи можно получить с помощью сообщения о [**\_ \_ \_ \_ настройке получения закрепления WM**](wm-cap-get-sequence-setup.md) (или макроса [**капкаптурежетсетуп**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ). Текущая скорость записи хранится в элементе **дврекуестмикросекперфраме** структуры [**каптурепармс**](/windows/win32/api/vfw/ns-vfw-captureparms) . Можно задать скорость записи, указав число микросекунд между последовательными кадрами в качестве значения этого элемента, а затем отправив обновленную структуру **каптурепармс** в окно Capture с помощью сообщения [**\_ установки закрепления WM \_ Set \_ Sequence \_**](wm-cap-set-sequence-setup.md) (или макроса [**капкаптуресетсетуп**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) ). Значение по умолчанию **дврекуестмикросекперфраме** — 66667, которое соответствует 15 кадрам в секунду.

 

 




