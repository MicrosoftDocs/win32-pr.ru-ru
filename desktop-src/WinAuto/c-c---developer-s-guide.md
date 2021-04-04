---
title: Рекомендации для разработчиков C/C++
description: В этом разделе содержатся сведения о том, как Microsoft Active Accessibility работает с точки зрения разработчика приложений C или C++. В нем рассматриваются проблемы, характерные для разработчиков клиентов и серверов.
ms.assetid: 2210cfbc-e27a-4a91-85a3-acbee7524758
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0c24e27603420c6332985e95fb1b23d1a4c4b2d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793626"
---
# <a name="cc-developers-guide"></a><span data-ttu-id="3a6be-104">Рекомендации для разработчиков C/C++</span><span class="sxs-lookup"><span data-stu-id="3a6be-104">C/C++ Developer's Guide</span></span>

<span data-ttu-id="3a6be-105">В этом разделе содержатся сведения о том, как Microsoft Active Accessibility работает с точки зрения разработчика приложений C или C++.</span><span class="sxs-lookup"><span data-stu-id="3a6be-105">This section provides information about how Microsoft Active Accessibility works from the perspective of a C or C++ application developer.</span></span> <span data-ttu-id="3a6be-106">В нем рассматриваются проблемы, характерные для разработчиков клиентов и серверов.</span><span class="sxs-lookup"><span data-stu-id="3a6be-106">It covers issues specific to client and server developers.</span></span>

<span data-ttu-id="3a6be-107">Обратите внимание, что *клиент* является вспомогательной программой или другим приложением, которое использует Microsoft Active Accessibility для получения сведений об элементах пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="3a6be-107">Note that a *client* is an accessibility aid or other application that uses Microsoft Active Accessibility to obtain information about user interface elements.</span></span> <span data-ttu-id="3a6be-108">*Сервер* — это приложение, которое использует Microsoft Active Accessibility для предоставления сведений об элементах пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="3a6be-108">A *server* is an application that uses Microsoft Active Accessibility to provide information about user interface elements.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="3a6be-109">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="3a6be-109">In this section</span></span>

- [<span data-ttu-id="3a6be-110">Active Accessibility служб пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="3a6be-110">Active Accessibility User Interface Services</span></span>](active-accessibility-user-interface-services-dev-guide.md)

> [!Note]  
> <span data-ttu-id="3a6be-111">Active Accessibility текстовые службы являются устаревшими.</span><span class="sxs-lookup"><span data-stu-id="3a6be-111">Active Accessibility Text Services is deprecated.</span></span> <span data-ttu-id="3a6be-112">Дополнительные сведения о расширенном вводе текста и технологиях естественного языка см. в [статье Microsoft Windows Text Services Framework](../tsf/text-services-framework.md) .</span><span class="sxs-lookup"><span data-stu-id="3a6be-112">Please see [Microsoft Windows Text Services Framework](../tsf/text-services-framework.md) for more information on advanced text input and natural language technologies.</span></span>