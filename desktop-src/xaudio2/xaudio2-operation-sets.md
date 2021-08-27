---
description: В этом обзоре представлено несколько методов XAudio2, которые можно вызывать как часть набора операций.
ms.assetid: 5bfd747d-af65-f619-e549-be8130748261
title: Наборы операций XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68a7f16edfa461d9944691bc4535debc05f820150dadf746caece85cb68c9f97
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089414"
---
# <a name="xaudio2-operation-sets"></a>Наборы операций XAudio2

В этом обзоре представлено несколько методов XAudio2, которые можно вызывать как часть набора операций.

Несколько методов XAudio2 принимают аргумент *Operation* , который позволяет вызывать их как часть отложенной группы. В определенное время можно одновременно применить весь набор изменений, вызвав функцию [**IXAudio2:: CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) с идентификатором набора *операций* для этой группы. Идентификатор является произвольным числом. Таким образом, он позволяет отдельным частям кода клиента применять отдельные атомарные изменения к графу без каких либо конфликтов. Рекомендуется, чтобы клиент увеличивал глобальный счетчик всякий раз, когда ему *нужно создать уникальный новый идентификатор.* Набор изменений, примененных к диаграмме, применяется атомарно, гарантируется точность выборки. Например, голосов начнет синхронизироваться.

Если для параметра *Operation* задано значение XAUDIO2 \_ commit \_ Now, это изменение применяется немедленно. Он вступает в силу на первом проходе обработки звука после вызова метода. При вызове [**CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) с \_ фиксацией XAUDIO2 \_ все незавершенные наборы операций выполняются, независимо от идентификатора их набора операций  .

Некоторые методы вступают в силу немедленно, если они вызываются из обратного вызова XAudio2 с набором *операций* XAudio2 \_ commit \_ Now. Все другие методы, принимающие аргумент *операции* , вступают в силу только при следующем проходе обработки после вызова метода (при вызове с параметром XAUDIO2 \_ commit \_ Now) или после вызова [**CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) с тем же именем *операции*. По этой причине некоторые вызовы методов могут не всегда происходить в том же порядке, в котором они были вызваны.

Все ожидающие операции фиксируются атомарно при вызове [**IXAudio2:: стопенгине**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-stopengine) . Все методы, вызываемые при остановке обработчика, вступают в силу немедленно, независимо от предоставленного значения набора *операций* . При перезапуске подсистемы XAudio2 возвращается в асинхронный режим.

Простые сценарии, в которых наборы операций полезны, включают в себя следующие примеры.

-   Одновременное запуск нескольких голосов.
-   Одновременное отправление буфера в речь, установка параметров голоса и запуск голоса.
-   Внесение крупномасштабных изменений в граф, например подключение всех исходных голосов к новому субмикс Voice.

См. раздел [инструкции. Группирование звуковых методов в качестве набора операций](how-to--group-audio-methods-as-an-operation-set.md) для примера использования набора операций.

## <a name="operation-set-methods"></a>Методы набора операций

В состав набора операций можно вызывать следующие методы.

-   [**IXAudio2SourceVoice:: Екситлуп**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-exitloop)
-   [**IXAudio2Voice:: Сетфилтерпараметерс**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters)
-   [**IXAudio2SourceVoice:: Сетфрекуенциратио**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio)
-   [**IXAudio2Voice::D Исаблиффект**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-disableeffect)
-   [**IXAudio2Voice:: Енаблиффект**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect)
-   [**IXAudio2Voice:: Сетчаннелволумес**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setchannelvolumes)
-   [**IXAudio2Voice:: Сетеффектпараметерс**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters)
-   [**IXAudio2Voice:: Сетаутпутматрикс**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix)
-   [**IXAudio2Voice:: Сетволуме**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume)
-   [**IXAudio2SourceVoice:: Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start)
-   [**IXAudio2SourceVoice:: останавливаться**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-stop)

Как было сказано выше, клиентский код должен в конечном итоге вызвать функцию [**IXAudio2:: CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) для выполнения отложенных изменений.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Наборы операций](operation-sets.md)
</dt> <dt>

[Руководство по программированию для XAudio2](programming-guide.md)
</dt> <dt>

[Руководство: группировка звуковых методов как набора операций](how-to--group-audio-methods-as-an-operation-set.md)
</dt> </dl>

 

 
