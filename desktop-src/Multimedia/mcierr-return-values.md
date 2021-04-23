---
title: Возвращаемые значения МЦИЕРР
description: Возвращаемые значения МЦИЕРР
ms.assetid: 61f7b128-b4f7-4385-9daf-e2bc9fb36e24
keywords:
- Мультимедиа Windows, возвращаемые значения МЦИЕРР
- мультимедиа, МЦИЕРР возвращаемые значения
- Ссылка на мультимедиа, возвращаемые значения МЦИЕРР
- Справочник по мультимедиа, возвращаемым значениям МЦИЕРР
- Возвращаемые значения МЦИЕРР, сведения
- Функция МЦисендкомманд
- Функция mciSendString
- Мультимедиа Windows, ошибки
- мультимедиа, ошибки
- ссылки мультимедиа, ошибки
- справочные материалы по мультимедиа, ошибки
- Интерфейс управления мультимедиа (MCI), возвращаемые значения МЦИЕРР
- MCI (интерфейс управления мультимедиа), возвращаемые значения МЦИЕРР
- Справочник по МЦИЕРР возвращаемым значениям MCI
- Ссылка MCI, возвращаемые значения МЦИЕРР
- Интерфейс управления мультимедиа (MCI), ошибки
- MCI (интерфейс управления мультимедийными файлами), ошибки
- Справочник по MCI, ошибкам
- Ссылка MCI, ошибки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8912284b98b2aacb60905e3fef4dc32705a5656
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105672271"
---
# <a name="mcierr-return-values"></a><span data-ttu-id="b307a-122">Возвращаемые значения МЦИЕРР</span><span class="sxs-lookup"><span data-stu-id="b307a-122">MCIERR Return Values</span></span>

<span data-ttu-id="b307a-123">Функции [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) и [**mciSendString**](/previous-versions//dd757161(v=vs.85)) возвращают нуль в случае успеха; в противном случае они возвращают значение **DWORD** , которое содержит одно из следующих значений ошибок в нижнем слове.</span><span class="sxs-lookup"><span data-stu-id="b307a-123">The [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) and [**mciSendString**](/previous-versions//dd757161(v=vs.85)) functions return zero if they are successful; otherwise, they return a **DWORD** value that contains one of the following error values in the low word.</span></span>

-   [<span data-ttu-id="b307a-124">Общие ошибки MCI</span><span class="sxs-lookup"><span data-stu-id="b307a-124">General MCI Errors</span></span>](general-mci-errors.md)
-   [<span data-ttu-id="b307a-125">Ошибки mciSendString</span><span class="sxs-lookup"><span data-stu-id="b307a-125">mciSendString Errors</span></span>](mcisendstring-errors.md)
-   [<span data-ttu-id="b307a-126">Ошибки цифрового видео</span><span class="sxs-lookup"><span data-stu-id="b307a-126">Digital-Video Errors</span></span>](digital-video-errors.md)
-   [<span data-ttu-id="b307a-127">Ошибки Sequencer</span><span class="sxs-lookup"><span data-stu-id="b307a-127">Sequencer Errors</span></span>](sequencer-errors.md)
-   [<span data-ttu-id="b307a-128">Волна-ошибки аудио</span><span class="sxs-lookup"><span data-stu-id="b307a-128">Waveform-Audio Errors</span></span>](waveform-audio-errors.md)

<span data-ttu-id="b307a-129">Можно получить описание отдельных возвращаемых значений, передав возвращаемые значения в функцию [**мЦижетеррорстринг**](/previous-versions//dd757158(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="b307a-129">You can obtain a description of individual return values by passing the return values to the [**mciGetErrorString**](/previous-versions//dd757158(v=vs.85)) function.</span></span>

 

 