---
title: Открытие Waveform-Audio устройств ввода
description: Открытие Waveform-Audio устройств ввода
ms.assetid: 46cdbce6-2433-433a-abd2-39e4146aa2e9
keywords:
- звуковая волна, открытие устройств ввода
- аудио-интерфейс, открытие устройств ввода
- запись звука звукозаписи, открытие устройств ввода
- Открытие звуковых устройств аудио ввода
- Функция Вавеинопен
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c92b7f49b9d170ceb8ebce287025ce0e0c1c5530
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105672263"
---
# <a name="opening-waveform-audio-input-devices"></a><span data-ttu-id="b5cc7-108">Открытие Waveform-Audio устройств ввода</span><span class="sxs-lookup"><span data-stu-id="b5cc7-108">Opening Waveform-Audio Input Devices</span></span>

<span data-ttu-id="b5cc7-109">Используйте функцию [**вавеинопен**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) , чтобы открыть входное устройство аудио звукозаписи.</span><span class="sxs-lookup"><span data-stu-id="b5cc7-109">Use the [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) function to open a waveform-audio input device for recording.</span></span> <span data-ttu-id="b5cc7-110">Эта функция открывает устройство, связанное с указанным идентификатором устройства, и возвращает маркер открытого устройства путем записи маркера указанного расположения в памяти.</span><span class="sxs-lookup"><span data-stu-id="b5cc7-110">This function opens the device associated with the specified device identifier and returns a handle of the open device by writing the handle of a specified memory location.</span></span>

<span data-ttu-id="b5cc7-111">Некоторые мультимедийные компьютеры имеют несколько входных устройств с аудио-волнами.</span><span class="sxs-lookup"><span data-stu-id="b5cc7-111">Some multimedia computers have multiple waveform-audio input devices.</span></span> <span data-ttu-id="b5cc7-112">Если вы не хотите открывать конкретное устройство ввода аудио-звука в системе, при \_ открытии устройства следует использовать константу СОПОСТАВИТЕЛЯ Wave для идентификатора устройства.</span><span class="sxs-lookup"><span data-stu-id="b5cc7-112">Unless you know you want to open a specific waveform-audio input device in a system, you should use the WAVE\_MAPPER constant for the device identifier when you open a device.</span></span> <span data-ttu-id="b5cc7-113">Функция [**вавеинопен**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) выберет устройство в системе, чтобы обеспечить возможность записи в указанном формате данных.</span><span class="sxs-lookup"><span data-stu-id="b5cc7-113">The [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) function will choose the device in the system best able to record in the specified data format.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b5cc7-114">См. также</span><span class="sxs-lookup"><span data-stu-id="b5cc7-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5cc7-115">Запись звука звукозаписи</span><span class="sxs-lookup"><span data-stu-id="b5cc7-115">Recording Waveform Audio</span></span>](recording-waveform-audio.md)
</dt> </dl>

 

 