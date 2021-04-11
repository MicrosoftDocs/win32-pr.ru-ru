---
title: Формат аудио
description: Формат аудио
ms.assetid: a65dbd3f-1539-4f02-8573-c527c4e3c58d
keywords:
- Сообщение WM_CAP_GET_AUDIOFORMAT
- макрос Капжетаудиоформат
- макрос Капжетаудиоформатсизе
- Сообщение WM_CAP_SET_AUDIOFORMAT
- макрос Капсетаудиоформат
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e362abd393097ae8763b44b3ee3474685ffd5c2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103890497"
---
# <a name="audio-format"></a>Формат аудио

Вы можете получить текущий формат записи для звуковых данных или размер структуры звуковых форматов, отправив сообщение с [**\_ закреплениями WM \_ \_ аудиоформат Get**](wm-cap-get-audioformat.md) (или макросы [**капжетаудиоформат**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformat) и [**капжетаудиоформатсизе**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformatsize) ) в окно записи. Формат записи звука по умолчанию — моно, 8-разрядный, 11 кГц PCM (импульсный код). При получении формата с помощью WM \_ Cap \_ Get \_ аудиоформат всегда используйте структуру [**вавеформатекс**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) .

Вы можете задать формат записи для звуковых данных, отправив [**сообщение \_ \_ \_ аудиоформат с закреплениями WM**](wm-cap-set-audioformat.md) (или макрос [**капсетаудиоформат**](/windows/desktop/api/Vfw/nf-vfw-capsetaudioformat) ) в окно записи. При задании звукового формата можно передать указатель на структуру [**вавеформат**](/windows/win32/api/mmreg/ns-mmreg-waveformat), **вавеформатекс** или [**пкмвавеформат**](/windows/win32/api/mmreg/ns-mmreg-pcmwaveformat) в зависимости от указанного формата аудио.

 

 