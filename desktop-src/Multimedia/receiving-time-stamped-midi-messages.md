---
title: Получение Time-Stamped сообщений MIDI
description: Получение Time-Stamped сообщений MIDI
ms.assetid: a91c85fe-f9c4-4cf6-b0bb-49aa8ed45644
keywords:
- Цифровой интерфейс MIDI, сообщения с отметкой времени
- MIDI (цифровой интерфейс музыкального инструмента), сообщения с штампом времени
- запись аудио MIDI, сообщений с штампом времени
- сообщения MIDI с отметкой времени
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7ead268c6d022f67a3607bb8a43a3d773bd7325
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337113"
---
# <a name="receiving-time-stamped-midi-messages"></a><span data-ttu-id="146b4-107">Получение Time-Stamped сообщений MIDI</span><span class="sxs-lookup"><span data-stu-id="146b4-107">Receiving Time-Stamped MIDI Messages</span></span>

<span data-ttu-id="146b4-108">Из-за задержки между тем, когда драйвер устройства получает сообщение MIDI и время, когда приложение получает сообщение, драйвер MIDI input Devices Time отмечает сообщение MIDI на время получения сообщения.</span><span class="sxs-lookup"><span data-stu-id="146b4-108">Because of the delay between when the device driver receives a MIDI message and the time the application receives the message, MIDI input device drivers time stamp the MIDI message with the time that the message was received.</span></span> <span data-ttu-id="146b4-109">Метки времени MIDI, которые определяются как время получения первого байта сообщения, указываются в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="146b4-109">MIDI time stamps, which are defined as the time the first byte of the message was received, are specified in milliseconds.</span></span> <span data-ttu-id="146b4-110">Функция [**мидиинстарт**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) сбрасывает отметки времени для устройства в ноль.</span><span class="sxs-lookup"><span data-stu-id="146b4-110">The [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) function resets the time stamps for a device to zero.</span></span>

<span data-ttu-id="146b4-111">Как упоминалось ранее, для получения меток времени с помощью ввода MIDI необходимо использовать функцию обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="146b4-111">As stated previously, to receive time stamps with MIDI input, you must use a callback function.</span></span> <span data-ttu-id="146b4-112">Параметр *dwParam2* функции обратного вызова задает отметку времени для данных, связанных с [**\_ данными MIM**](mim-data.md) и сообщениями [**MIM \_ лонгдата**](mim-longdata.md) .</span><span class="sxs-lookup"><span data-stu-id="146b4-112">The *dwParam2* parameter of the callback function specifies the time stamp for data associated with the [**MIM\_DATA**](mim-data.md) and [**MIM\_LONGDATA**](mim-longdata.md) messages.</span></span>

## <a name="related-topics"></a><span data-ttu-id="146b4-113">См. также</span><span class="sxs-lookup"><span data-stu-id="146b4-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="146b4-114">Запись звука MIDI</span><span class="sxs-lookup"><span data-stu-id="146b4-114">Recording MIDI Audio</span></span>](recording-midi-audio.md)
</dt> </dl>

 

 