---
description: Следуйте общим рекомендациям по применению модулей слияния, описанным в разделе применение модулей слияния.
ms.assetid: 6035b1a9-d452-4020-9fe3-c20ba874a2ed
title: Применение настраиваемого модуля слияния с настройками
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4f1e3da426ba5ca13e149814ab9bb927e83d4e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650729"
---
# <a name="applying-a-configurable-merge-module-with-customizations"></a><span data-ttu-id="54de3-103">Применение настраиваемого модуля слияния с настройками</span><span class="sxs-lookup"><span data-stu-id="54de3-103">Applying a Configurable Merge Module with Customizations</span></span>

<span data-ttu-id="54de3-104">Следуйте общим рекомендациям по применению модулей слияния, описанным в разделе [применение модулей слияния](applying-merge-modules.md).</span><span class="sxs-lookup"><span data-stu-id="54de3-104">Follow the general guidelines for applying merge modules described in [Applying Merge Modules](applying-merge-modules.md).</span></span> <span data-ttu-id="54de3-105">Кроме того, потребители модулей слияния должны выполнить следующие действия, чтобы настроить модуль слияния во время установки.</span><span class="sxs-lookup"><span data-stu-id="54de3-105">In addition, merge module consumers must do the following to configure a merge module at the time of installation:</span></span>

-   <span data-ttu-id="54de3-106">Используйте модуль слияния, который создан с учетом настраиваемых параметров.</span><span class="sxs-lookup"><span data-stu-id="54de3-106">Use a merge module that is authored to have configurable settings.</span></span> <span data-ttu-id="54de3-107">Дополнительные сведения см. [в разделе Создание модуля слияния, который может быть настроен конечным пользователем](creating-a-merge-module-that-can-be-configured-by-the-end-user.md) .</span><span class="sxs-lookup"><span data-stu-id="54de3-107">For more information, see [Creating a Merge Module that Can Be Configured by the End-User](creating-a-merge-module-that-can-be-configured-by-the-end-user.md)</span></span>
-   <span data-ttu-id="54de3-108">Используйте средство слияния и настройки, которое вызывает Mergemod.dll версии 2,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="54de3-108">Use a merge and configuration tool that calls Mergemod.dll version 2.0 or later.</span></span> <span data-ttu-id="54de3-109">Более ранние версии Mergmod.dll не могут настраивать параметры модуля слияния.</span><span class="sxs-lookup"><span data-stu-id="54de3-109">Earlier versions of Mergmod.dll cannot configure merge module settings.</span></span> <span data-ttu-id="54de3-110">Авторы должны создавать модули слияния, предоставляющие значения по умолчанию и совместимые с более ранними версиями Mergmod.dll.</span><span class="sxs-lookup"><span data-stu-id="54de3-110">Authors should create merge modules that provide default values and are compatible with earlier versions of Mergmod.dll.</span></span>
-   <span data-ttu-id="54de3-111">При появлении запроса средства клиента конфигурации укажите сведения о настройке.</span><span class="sxs-lookup"><span data-stu-id="54de3-111">Provide customization information when prompted by the configuration client tool.</span></span> <span data-ttu-id="54de3-112">Авторы должны создавать модули слияния, которые используют значения по умолчанию, когда пользователь отклоняет предоставление информации.</span><span class="sxs-lookup"><span data-stu-id="54de3-112">Authors should create merge modules that use default values when a user declines to provide information.</span></span>

 

 



