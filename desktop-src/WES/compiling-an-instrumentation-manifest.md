---
title: Компиляция манифеста инструментирования
description: После записи манифеста используйте компилятор сообщений для проверки манифеста и создания файлов ресурсов и заголовков, включаемых в поставщик.
ms.assetid: ecb72942-08fc-470d-b4d6-f5f1a70de3fa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b9db6c02705a203c6836bf3a2c56f5049a00038
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104253166"
---
# <a name="compiling-an-instrumentation-manifest"></a><span data-ttu-id="7f3ce-103">Компиляция манифеста инструментирования</span><span class="sxs-lookup"><span data-stu-id="7f3ce-103">Compiling an Instrumentation Manifest</span></span>

<span data-ttu-id="7f3ce-104">После [записи манифеста](writing-an-instrumentation-manifest.md)используйте компилятор сообщений для проверки манифеста и создания файлов ресурсов и заголовков, включаемых в поставщик.</span><span class="sxs-lookup"><span data-stu-id="7f3ce-104">After [writing your manifest](writing-an-instrumentation-manifest.md), use the message compiler to validate the manifest and generate the resource and header files that you include in your provider.</span></span> <span data-ttu-id="7f3ce-105">Дополнительные сведения об использовании компилятора см. в разделе [**компилятор сообщений**](message-compiler--mc-exe-.md).</span><span class="sxs-lookup"><span data-stu-id="7f3ce-105">For details on using the compiler, see [**Message Compiler**](message-compiler--mc-exe-.md).</span></span> <span data-ttu-id="7f3ce-106">Включите в проект файлы заголовков и ресурсов, которые компилятор создает в проекте, содержащем оставшуюся часть исходного кода поставщика.</span><span class="sxs-lookup"><span data-stu-id="7f3ce-106">Include the header and resource files that the compiler generates in the project that contains the rest of your provider's source code.</span></span> <span data-ttu-id="7f3ce-107">Сведения о том, как записать события, определенные в манифесте, см. в разделе [Разработка поставщика](developing-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="7f3ce-107">For information on how to write the events that are defined in your manifest, see [Developing a Provider](developing-a-provider.md).</span></span>

 

 




