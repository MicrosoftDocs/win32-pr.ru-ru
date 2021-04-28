---
description: Защита DEP/NX
ms.assetid: 92F628E4-6106-42F7-B868-A3101C7A3F0A
title: Защита DEP/NX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3565460cbfd2e6b13c3c5ba6b1f0693a3d5b25ba
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088572"
---
# <a name="depnx-protection"></a><span data-ttu-id="cf741-103">Защита DEP/NX</span><span class="sxs-lookup"><span data-stu-id="cf741-103">DEP/NX Protection</span></span>

<span data-ttu-id="cf741-104">Начиная с Windows Internet Explorer 7 в Windows Vista, элемент панели управления Интернет включает параметр **включить защиту памяти** для устранения сетевых атак.</span><span class="sxs-lookup"><span data-stu-id="cf741-104">Starting with Windows Internet Explorer 7 on Windows Vista, the Internet control panel item includes an **Enable memory protection** option to help mitigate online attacks.</span></span> <span data-ttu-id="cf741-105">Этот параметр также называется *предотвращением выполнения данных* (DEP) или *без выполнения* (NX).</span><span class="sxs-lookup"><span data-stu-id="cf741-105">This option is also referred to as *Data Execution Prevention* (DEP) or *No-Execute* (NX).</span></span> <span data-ttu-id="cf741-106">Если этот параметр включен, он работает с процессором, чтобы предотвратить атаки переполнения буфера, блокируя выполнение кода из памяти, помеченной как не исполняемый.</span><span class="sxs-lookup"><span data-stu-id="cf741-106">When this option is enabled, it works with the processor to help prevent buffer overflow attacks by blocking code execution from memory that is marked as non-executable.</span></span>

<span data-ttu-id="cf741-107">В Windows Internet Explorer 8 в операционной системе Windows Vista с пакетом обновления 1 (SP1) или более поздней версии этот параметр включен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="cf741-107">In Windows Internet Explorer 8 on the Windows Vista with Service Pack 1 (SP1) operating system or a later version, this option is enabled by default.</span></span> <span data-ttu-id="cf741-108">DEP/NX не защищает от всех уязвимостей на основе памяти.</span><span class="sxs-lookup"><span data-stu-id="cf741-108">DEP/NX does not protect against all memory-based vulnerabilities.</span></span> <span data-ttu-id="cf741-109">Но если он сочетается с другими технологиями, например с помощью технологии ASLR для разметки адресного пространства, он помогает предотвратить распространенные уязвимости переполнения буфера в Windows Internet Explorer и загружаемые надстройки.</span><span class="sxs-lookup"><span data-stu-id="cf741-109">But when it is combined with other technologies like Address Space Layout Randomization (ASLR), it helps prevent common buffer overflow vulnerabilities in Windows Internet Explorer and the add-ons that it loads.</span></span> <span data-ttu-id="cf741-110">Для обеспечения этой защиты не требуется никакого дополнительного взаимодействия с пользователем, и новые запросы вводиться не будут.</span><span class="sxs-lookup"><span data-stu-id="cf741-110">No additional user interaction is required to provide this protection, and no new prompts are introduced.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cf741-111">Связанные разделы</span><span class="sxs-lookup"><span data-stu-id="cf741-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cf741-112">Устранение проблем совместимости в веб-приложениях с помощью представления совместимости</span><span class="sxs-lookup"><span data-stu-id="cf741-112">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 



