---
description: Функции ImageHlp в основном используются средствами программирования, служебными программами установки приложений и другими программами, которым требуется доступ к данным, содержащимся в образе PE.
ms.assetid: 831d7bb2-bf01-4422-a940-173f9856a513
title: О ImageHlp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b76da517a396536640df0e9bfcfa05368e4d0b76
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655743"
---
# <a name="about-imagehlp"></a><span data-ttu-id="18d49-103">О ImageHlp</span><span class="sxs-lookup"><span data-stu-id="18d49-103">About ImageHlp</span></span>

<span data-ttu-id="18d49-104">Функции ImageHlp в основном используются средствами программирования, служебными программами установки приложений и другими программами, которым требуется доступ к данным, содержащимся в образе PE.</span><span class="sxs-lookup"><span data-stu-id="18d49-104">The ImageHlp functions are used mostly by programming tools, application setup utilities, and other programs that need access to the data contained in a PE image.</span></span> <span data-ttu-id="18d49-105">Все функции ImageHlp являются отдельными потоками.</span><span class="sxs-lookup"><span data-stu-id="18d49-105">All ImageHlp functions are single threaded.</span></span> <span data-ttu-id="18d49-106">Таким образом, вызовы из более чем одного потока в эту функцию, скорее всего, приведут к непредвиденному поведению или повреждению памяти.</span><span class="sxs-lookup"><span data-stu-id="18d49-106">Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption.</span></span> <span data-ttu-id="18d49-107">Чтобы избежать этого, необходимо синхронизировать все одновременные вызовы из более чем одного потока в эту функцию.</span><span class="sxs-lookup"><span data-stu-id="18d49-107">To avoid this, you must synchronize all concurrent calls from more than one thread to this function.</span></span>

<span data-ttu-id="18d49-108">В следующих разделах описываются образы PE и функции, предоставляемые функциями ImageHlp.</span><span class="sxs-lookup"><span data-stu-id="18d49-108">The following topics describe PE images and the functionality provided by the ImageHlp functions.</span></span>

-   [<span data-ttu-id="18d49-109">Формат PE</span><span class="sxs-lookup"><span data-stu-id="18d49-109">PE Format</span></span>](pe-format.md)
-   [<span data-ttu-id="18d49-110">Функции доступа к изображениям</span><span class="sxs-lookup"><span data-stu-id="18d49-110">Image Access Functions</span></span>](image-access-functions.md)
-   [<span data-ttu-id="18d49-111">Функции целостности изображений</span><span class="sxs-lookup"><span data-stu-id="18d49-111">Image Integrity Functions</span></span>](image-integrity-functions.md)
-   [<span data-ttu-id="18d49-112">Функции изменения изображений</span><span class="sxs-lookup"><span data-stu-id="18d49-112">Image Modification Functions</span></span>](image-modification-functions.md)

 

 



