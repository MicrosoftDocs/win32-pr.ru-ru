---
description: Перечисление ресурсов обеспечивает закрытие и точное представление действий инструментирования, выполняемых при выполнении приложения.
ms.assetid: 4a421006-32ff-4555-a3c8-69fffdb46845
title: Сведения о перечислении ресурсов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 601e65550dacbd07d493f35a6c35fece98657b6e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655617"
---
# <a name="about-resource-enumeration"></a><span data-ttu-id="4e58f-103">Сведения о перечислении ресурсов</span><span class="sxs-lookup"><span data-stu-id="4e58f-103">About Resource Enumeration</span></span>

<span data-ttu-id="4e58f-104">Перечисление ресурсов обеспечивает закрытие и точное представление действий инструментирования, выполняемых при выполнении приложения.</span><span class="sxs-lookup"><span data-stu-id="4e58f-104">Resource enumeration provides a close and precise view of instrumentation activity that takes place when an application is running.</span></span> <span data-ttu-id="4e58f-105">Сведения инструментирования могут быть абстрактными и классифицированы как набор элементов, зависящих от процесса, в рамках процесса отладки.</span><span class="sxs-lookup"><span data-stu-id="4e58f-105">The instrumentation information can be abstracted and categorized as a set of process-specific items as part of the debugging process.</span></span>

<span data-ttu-id="4e58f-106">Средствам, таким как отладчики, часто требуется доступ к информации инструментирования, но они могут оказаться недоступными.</span><span class="sxs-lookup"><span data-stu-id="4e58f-106">Tools, such as debuggers, often require access to instrumentation information but may find it is unavailable.</span></span> <span data-ttu-id="4e58f-107">Чтобы решить эту проблему, функция [**верифиеренумератересаурце**](/windows/desktop/api/Avrfsdk/nf-avrfsdk-verifierenumerateresource) извлекает из приложений данные этого типа, чтобы предоставить более подробные сведения о контексте для отлаживаемой проблемы.</span><span class="sxs-lookup"><span data-stu-id="4e58f-107">To solve this problem, the [**VerifierEnumerateResource**](/windows/desktop/api/Avrfsdk/nf-avrfsdk-verifierenumerateresource) function extracts this type of information from applications to provide better context information for the problem being debugged.</span></span>

 

 



