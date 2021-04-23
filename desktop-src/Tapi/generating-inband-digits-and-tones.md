---
description: После того как вызов находится в состоянии Connected, данные могут передаваться по нему.
ms.assetid: a2afa7e9-c625-48ec-920b-0ae8c3e1b395
title: Создание нестандартных цифр и тонов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8325087882f90ae175edfd27a9f75aab492969af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673230"
---
# <a name="generating-inband-digits-and-tones"></a><span data-ttu-id="3ef96-103">Создание нестандартных цифр и тонов</span><span class="sxs-lookup"><span data-stu-id="3ef96-103">Generating Inband Digits and Tones</span></span>

<span data-ttu-id="3ef96-104">После того как вызов находится в состоянии *Connected* , данные могут передаваться по нему.</span><span class="sxs-lookup"><span data-stu-id="3ef96-104">After a call is in the *connected* state, information can be transmitted over it.</span></span> <span data-ttu-id="3ef96-105">Предоставляются две функции, обеспечивающие сквозной контроль сигналов между приложением и удаленным офисом, например отвечающим компьютером.</span><span class="sxs-lookup"><span data-stu-id="3ef96-105">Two functions are provided that allow end-to-end inband signaling between the application and remote station equipment such as an answering machine.</span></span> <span data-ttu-id="3ef96-106">Одна функция — [**линеженератедигитс**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits), которая создает нечередующиеся цифры в вызове и сигнализирует им о канале голоса.</span><span class="sxs-lookup"><span data-stu-id="3ef96-106">One function is [**lineGenerateDigits**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits), which generates inband digits on a call, signaling them over the voice channel.</span></span> <span data-ttu-id="3ef96-107">Цифры могут быть сигнальными как с помощью дисковых или импульсных последовательностей, так и в виде тонов DTMF.</span><span class="sxs-lookup"><span data-stu-id="3ef96-107">Digits can be signaled as either rotary/pulse sequences or as DTMF tones.</span></span> <span data-ttu-id="3ef96-108">Другая функция — [**линеженератетоне**](/windows/desktop/api/Tapi/nf-tapi-linegeneratetone), которая позволяет приложению создавать один из множества многочастотных тонов с нелинейным чередованием (по потоку мультимедиа).</span><span class="sxs-lookup"><span data-stu-id="3ef96-108">The other function is [**lineGenerateTone**](/windows/desktop/api/Tapi/nf-tapi-linegeneratetone), which enables the application to generate one of a variety of multifrequency tones inband (over the media stream).</span></span> <span data-ttu-id="3ef96-109">Это создает звуки телефонии, такие как звонка, beep и Busy, а также произвольные Многочастотные многотактовые тона.</span><span class="sxs-lookup"><span data-stu-id="3ef96-109">This generates telephony tones, such as ringback, beep, and busy, as well as arbitrary multifrequency, multicadenced tones.</span></span>

<span data-ttu-id="3ef96-110">На вызов в любой момент времени может выполняться только одна цифра или тоновая генерация.</span><span class="sxs-lookup"><span data-stu-id="3ef96-110">Only one digit or tone generation can be in progress on a call at any one time.</span></span> <span data-ttu-id="3ef96-111">При завершении создания цифры или тона в приложение, которое запросило создание, отправляется сообщение о [**\_ формировании строки**](line-generate.md) .</span><span class="sxs-lookup"><span data-stu-id="3ef96-111">When digit or tone generation completes, a [**LINE\_GENERATE**](line-generate.md) message is sent to the application that requested the generation.</span></span> <span data-ttu-id="3ef96-112">В случае, когда формируется несколько цифр, только одно сообщение отправляется обратно после создания всех цифр.</span><span class="sxs-lookup"><span data-stu-id="3ef96-112">In the case where multiple digits are generated, only a single message is sent back after all digits have been generated.</span></span> <span data-ttu-id="3ef96-113">Вызов [**линеженератедигитс**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits) или [**линеженератетоне**](/windows/desktop/api/Tapi/nf-tapi-linegeneratetone) во время создания цифры или тона приведет к прерыванию выполняющегося в данный момент поколения и отправит \_ сообщение о формировании строки приложению, поколение которого было прервано с указанием отмены.</span><span class="sxs-lookup"><span data-stu-id="3ef96-113">Calling [**lineGenerateDigits**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits) or [**lineGenerateTone**](/windows/desktop/api/Tapi/nf-tapi-linegeneratetone) while digit or tone generation is in progress will abort the generation currently in progress and send the LINE\_GENERATE message to the application whose generation was aborted with a cancel indication.</span></span>

 

 



