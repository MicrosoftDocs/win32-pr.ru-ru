---
title: иттснотифисинкв
description: иттснотифисинкв
ms.assetid: 6305dad6-c162-458a-899e-628f6486680e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5820f262779f86deeeca9982d0551b16d3a3406
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/20/2020
ms.locfileid: "104412585"
---
# <a name="ittsnotifysinkw"></a><span data-ttu-id="613b4-103">иттснотифисинкв</span><span class="sxs-lookup"><span data-stu-id="613b4-103">ITTSNotifySinkW</span></span>

<span data-ttu-id="613b4-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="613b4-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="613b4-105">Подсистема должна вызывать [**аудиостоп**](https://www.bing.com/search?q=**AudioStop**), [**аудиостарт**](https://www.bing.com/search?q=**AudioStart**)и [**Visual**](https://www.bing.com/search?q=**Visual**).</span><span class="sxs-lookup"><span data-stu-id="613b4-105">The engine must call out through [**AudioStop**](https://www.bing.com/search?q=**AudioStop**), [**AudioStart**](https://www.bing.com/search?q=**AudioStart**), and [**Visual**](https://www.bing.com/search?q=**Visual**).</span></span> <span data-ttu-id="613b4-106">**Визуальный** обратный вызов должен предоставлять IPA фонемы.</span><span class="sxs-lookup"><span data-stu-id="613b4-106">The **Visual** callback must provide IPA phonemes.</span></span> <span data-ttu-id="613b4-107">(Международный фонетический алфавит \[ IPA \] — это универсальная нотация для описания фонетического содержимого речевого взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="613b4-107">(The International Phonetic Alphabet \[IPA\] is a universal notation for describing the phonetic content of spoken communication.</span></span> <span data-ttu-id="613b4-108">Все произношенные фонемы имеют представления в IPA.</span><span class="sxs-lookup"><span data-stu-id="613b4-108">All speakable phonemes have representations in IPA.</span></span> <span data-ttu-id="613b4-109">Подробные сведения о IPA приведены в спецификации Microsoft Speech API, которая \[ входит в состав пакета SDK для для распознавания речи 4,0 \] [https://www.microsoft.com/speech/](https://msdn.microsoft.com/library/ee705648.aspx) .)</span><span class="sxs-lookup"><span data-stu-id="613b4-109">Details of IPA are in the Microsoft Speech API specification \[part of the Speech SDK 4.0 download\] at [https://www.microsoft.com/speech/](https://msdn.microsoft.com/library/ee705648.aspx).)</span></span>

<span data-ttu-id="613b4-110">Хотя [**визуальное**](https://www.bing.com/search?q=**Visual**) уведомление является довольно широким, Microsoft Agent использует только значение **Ципафонеме** для анимации рот в качестве символа.</span><span class="sxs-lookup"><span data-stu-id="613b4-110">Although the [**Visual**](https://www.bing.com/search?q=**Visual**) notification is fairly rich, Microsoft Agent uses only the **cIPAPhoneme** value to animate the mouth as the character speaks.</span></span> <span data-ttu-id="613b4-111">Любой модуль, совместимый с Microsoft Agent, должен обеспечивать тесно синхронизированный поток **визуальных** уведомлений, отражающих фонетическое содержимое созданного utterance.</span><span class="sxs-lookup"><span data-stu-id="613b4-111">Any Microsoft Agent-compatible engine must provide a closely synchronized stream of **Visual** notifications reflecting the phonetic content of the produced utterance.</span></span> <span data-ttu-id="613b4-112">В этом случае «относительное своевременное уведомление» неадекватно, так как слышать-динамики весьма чувствительны к несоответствиям между положением и акустическим содержимым.</span><span class="sxs-lookup"><span data-stu-id="613b4-112">In this case, "relatively timely notification" is not adequate, because speaker-hearers are fairly sensitive to discrepancies between mouth position and acoustic content.</span></span> <span data-ttu-id="613b4-113">**Визуальные** уведомления должны возвращаться быстро.</span><span class="sxs-lookup"><span data-stu-id="613b4-113">**Visual** notifications need to be returned promptly.</span></span>

 

 




