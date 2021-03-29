---
title: Разработка поставщика
description: Для записи событий, определенных в манифесте, используются функции, входящие в API трассировки событий (ETW). Дополнительные сведения о создании поставщика см. в разделе Предоставление событий.
ms.assetid: 23de19c4-5f8d-4faa-acd9-fe6208ca17a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83939429f1dc4d499e7c2d0e0c2bfa7a47522ffe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104134439"
---
# <a name="developing-a-provider"></a><span data-ttu-id="3250d-104">Разработка поставщика</span><span class="sxs-lookup"><span data-stu-id="3250d-104">Developing a Provider</span></span>

<span data-ttu-id="3250d-105">Для записи событий, определенных в манифесте, используются функции, входящие в API [трассировки событий](/windows/desktop/ETW/event-tracing-portal) (ETW).</span><span class="sxs-lookup"><span data-stu-id="3250d-105">To write the events that you define in your manifest, you use the functions included in the [Event Tracing](/windows/desktop/ETW/event-tracing-portal) (ETW) API.</span></span> <span data-ttu-id="3250d-106">Дополнительные сведения о создании поставщика см. в разделе [предоставление событий](/windows/desktop/ETW/providing-events).</span><span class="sxs-lookup"><span data-stu-id="3250d-106">For details on writing a provider, see [Providing Events](/windows/desktop/ETW/providing-events).</span></span>

<span data-ttu-id="3250d-107">После записи поставщика используйте средство WevtUtil.exe для регистрации поставщика и схемы.</span><span class="sxs-lookup"><span data-stu-id="3250d-107">After writing the provider, use the WevtUtil.exe tool to register the provider and schema.</span></span> <span data-ttu-id="3250d-108">Дополнительные сведения об использовании WevtUtil см. в разделе [средства журнала событий Windows](windows-event-log-tools.md).</span><span class="sxs-lookup"><span data-stu-id="3250d-108">For details on using WevtUtil, see [Windows Event Log Tools](windows-event-log-tools.md).</span></span> <span data-ttu-id="3250d-109">Ниже показано, как использовать WevtUtil для регистрации поставщика и удаления регистрации.</span><span class="sxs-lookup"><span data-stu-id="3250d-109">The following shows how to use WevtUtil to register a provider and to remove the registration.</span></span>


```cmd
wevtutil im provider.man

wevtutil um provider.man
```