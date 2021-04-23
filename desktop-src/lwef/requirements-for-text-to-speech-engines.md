---
title: Требования для модулей преобразования текста в речь
description: Требования для модулей преобразования текста в речь
ms.assetid: 21d19949-c9b4-4d9c-9684-6d15162f7a7d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa6d1bc9f4340327c5fbfb71b900e10f60738fdf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486833"
---
# <a name="requirements-for-text-to-speech-engines"></a><span data-ttu-id="888be-103">Требования для модулей преобразования текста в речь</span><span class="sxs-lookup"><span data-stu-id="888be-103">Requirements for Text-To-Speech Engines</span></span>

<span data-ttu-id="888be-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="888be-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="888be-105">Подсистема должна быть полностью совместимой с SAPI 4,0.</span><span class="sxs-lookup"><span data-stu-id="888be-105">The engine must be fully SAPI 4.0-compliant.</span></span> <span data-ttu-id="888be-106">Кроме того, подсистема также должна поддерживать следующие интерфейсы SAPI для помеченных текста и уведомлений закладок.</span><span class="sxs-lookup"><span data-stu-id="888be-106">In addition, the engine must also support the following SAPI interfaces for tagged text and bookmark notifications.</span></span> <span data-ttu-id="888be-107">Эти интерфейсы позволяют Microsoft Agent быстро выводить текст на всплывающую подсказку и пакет LIP — синхронизировать рот символа (или его эквивалент) с произнесенными словами.</span><span class="sxs-lookup"><span data-stu-id="888be-107">These interfaces enable Microsoft Agent to pace the output of text to a character's word balloon and lip-sync the character's mouth (or equivalent) with the spoken words.</span></span>

-   [<span data-ttu-id="888be-108">иттсцентралв</span><span class="sxs-lookup"><span data-stu-id="888be-108">ITTSCentralW</span></span>](ittscentralw.md)
-   [<span data-ttu-id="888be-109">иттснотифисинкв</span><span class="sxs-lookup"><span data-stu-id="888be-109">ITTSNotifySinkW</span></span>](ittsnotifysinkw.md)
-   [<span data-ttu-id="888be-110">иттсбуфнотифисинкв</span><span class="sxs-lookup"><span data-stu-id="888be-110">ITTSBufNotifySinkW</span></span>](ittsbufnotifysinkw.md)
-   [<span data-ttu-id="888be-111">иттсаттрибутесв</span><span class="sxs-lookup"><span data-stu-id="888be-111">ITTSAttributesW</span></span>](ittsattributesw.md)

 

 




