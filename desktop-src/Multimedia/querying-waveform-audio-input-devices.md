---
title: Запрос Waveform-Audio устройств ввода
description: Запрос Waveform-Audio устройств ввода
ms.assetid: 573b33bc-f445-496e-a0e6-0194d30bb668
keywords:
- звуковая волна, запрос устройств ввода
- аудио-интерфейс, запрос устройств ввода
- запись аудио звукозаписи, запрос устройств ввода
- запросы к звуковым устройствам ввода
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91b915b3f39ad417a3d92396d887e5fb66092119
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103987448"
---
# <a name="querying-waveform-audio-input-devices"></a>Запрос Waveform-Audio устройств ввода

Перед записью звукового аудио-файла необходимо вызвать функцию [**вавеинжетдевкапс**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetdevcaps) , чтобы определить возможности ввода звука с помощью звукового сигнала системы. Эта функция заполняет структуру [**вавеинкапс**](/windows/win32/api/mmeapi/ns-mmeapi-waveincaps) данными о возможностях указанного устройства. Эти сведения включают в себя изготовителя и идентификаторы продуктов, название продукта для устройства и номер версии драйвера устройства. Кроме того, структура **вавеинкапс** предоставляет сведения о стандартных форматах аудио, поддерживаемых устройством.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Запись звука звукозаписи](recording-waveform-audio.md)
</dt> </dl>

 

 