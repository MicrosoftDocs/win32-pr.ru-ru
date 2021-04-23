---
description: В TAPI 3,1 введено понятие терминала с многодорожкностью, терминал, который, по сути, является коллекцией &\# 0034; track&\# 0034; Terminals.
ms.assetid: 8dd6f792-a29e-40fd-9f5b-ee5525028c2e
title: Терминалы с многодорожкностью
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb795169f5e7cbd669e0bceb1d635e33c912c50a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673382"
---
# <a name="multitrack-terminals"></a><span data-ttu-id="3f1c4-103">Терминалы с многодорожкностью</span><span class="sxs-lookup"><span data-stu-id="3f1c4-103">Multitrack Terminals</span></span>

<span data-ttu-id="3f1c4-104">В TAPI 3,1 введено понятие терминала с многодорожкностью, терминал, который, по сути, является коллекцией "Track" терминалов.</span><span class="sxs-lookup"><span data-stu-id="3f1c4-104">TAPI 3.1 introduces the notion of a multitrack terminal, a terminal that, in essence, is a collection of "track" terminals.</span></span> <span data-ttu-id="3f1c4-105">Многодорожкные терминалы упрощают нагрузку программиста в ситуациях, когда в сеансе связи участвуют несколько потоков мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="3f1c4-105">Multitrack terminals ease the programmer's load in situations where multiple media streams are involved in a communications session.</span></span>

<span data-ttu-id="3f1c4-106">[Терминал записи файлов](file-playback-terminal-and-file-recording-terminal.md) является примером многодорожкного терминала.</span><span class="sxs-lookup"><span data-stu-id="3f1c4-106">The [File Recording Terminal](file-playback-terminal-and-file-recording-terminal.md) is an example of a multitrack terminal.</span></span> <span data-ttu-id="3f1c4-107">Он состоит из «дорожек», где каждая «дорожка» — это терминал, соответствующий потоку в записанном файле.</span><span class="sxs-lookup"><span data-stu-id="3f1c4-107">It consists of "tracks," where each "track" is a terminal corresponding to a stream in the recorded file.</span></span>

<span data-ttu-id="3f1c4-108">[Терминал транспортера](track-terminals.md) может быть другим терминалом с несколькими дорожками или терминалом с одной дорожкой.</span><span class="sxs-lookup"><span data-stu-id="3f1c4-108">A [track terminal](track-terminals.md) can be another multitrack terminal or a single-track terminal.</span></span> <span data-ttu-id="3f1c4-109">Терминал с одной дорожкой — это терминал, у которого нет терминалов по дорожкам.</span><span class="sxs-lookup"><span data-stu-id="3f1c4-109">A single-track terminal is a terminal that does not have any track terminals.</span></span> <span data-ttu-id="3f1c4-110">Терминал с одной дорожкой — это терминал в приложении TAPI 3.</span><span class="sxs-lookup"><span data-stu-id="3f1c4-110">A single-track terminal is a terminal in the TAPI 3 sense of the word.</span></span>

<span data-ttu-id="3f1c4-111">Дополнительные сведения о терминалах с несколькими дорожками см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="3f1c4-111">For more information about multitrack terminals, see the following topics:</span></span>

-   [<span data-ttu-id="3f1c4-112">О терминалах с многодорожкностью</span><span class="sxs-lookup"><span data-stu-id="3f1c4-112">About Multitrack Terminals</span></span>](about-multitrack-terminals.md)
-   [<span data-ttu-id="3f1c4-113">Механизм выбора терминала по умолчанию</span><span class="sxs-lookup"><span data-stu-id="3f1c4-113">Default Terminal Selection Mechanism</span></span>](default-terminal-selection-mechanism.md)
-   [<span data-ttu-id="3f1c4-114">Выбор терминала вручную</span><span class="sxs-lookup"><span data-stu-id="3f1c4-114">Manual Terminal Selection</span></span>](manual-terminal-selection.md)
-   [<span data-ttu-id="3f1c4-115">Использование терминалов с многодорожкностью и механизма выбора по умолчанию</span><span class="sxs-lookup"><span data-stu-id="3f1c4-115">Using Multitrack Terminals and the Default Selection Mechanism</span></span>](using-multitrack-terminals-and-the-default-selection-mechanism.md)

 

 



