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
ms.openlocfilehash: 8fd22a2b65746202a831d475fcde38b31259619dbc645a5cbca3b91d03ff6e0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118371926"
---
# <a name="querying-waveform-audio-input-devices"></a>Запрос Waveform-Audio устройств ввода

Перед записью звукового аудио-файла необходимо вызвать функцию [**вавеинжетдевкапс**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetdevcaps) , чтобы определить возможности ввода звука с помощью звукового сигнала системы. Эта функция заполняет структуру [**вавеинкапс**](/windows/win32/api/mmeapi/ns-mmeapi-waveincaps) данными о возможностях указанного устройства. Эти сведения включают в себя изготовителя и идентификаторы продуктов, название продукта для устройства и номер версии драйвера устройства. Кроме того, структура **вавеинкапс** предоставляет сведения о стандартных форматах аудио, поддерживаемых устройством.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Запись звука звукозаписи](recording-waveform-audio.md)
</dt> </dl>

 

 