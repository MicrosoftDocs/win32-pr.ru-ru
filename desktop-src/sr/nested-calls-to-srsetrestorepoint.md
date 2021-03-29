---
title: Вложенные вызовы Срсетресторепоинт
description: В этом разделе описывается поддержка вложенных вызовов Срсетресторепоинт с помощью \_ типов событий Begin Nested \_ System \_ Change и End \_ Nested \_ System \_ Change.
ms.assetid: ee2dea47-f95d-4293-ac33-eff622b84db6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5654dc7bb6e42ae55cbad18fc2418df3bdd942d2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104258518"
---
# <a name="nested-calls-to-srsetrestorepoint"></a><span data-ttu-id="a9675-103">Вложенные вызовы Срсетресторепоинт</span><span class="sxs-lookup"><span data-stu-id="a9675-103">Nested Calls to SRSetRestorePoint</span></span>

<span data-ttu-id="a9675-104">В этом разделе описывается поддержка вложенных вызовов [**срсетресторепоинт**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) с помощью \_ типов событий Begin Nested \_ System \_ Change и End \_ Nested \_ System \_ Change.</span><span class="sxs-lookup"><span data-stu-id="a9675-104">This topic describes support for nested calls to [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) through the BEGIN\_NESTED\_SYSTEM\_CHANGE and END\_NESTED\_SYSTEM\_CHANGE event types.</span></span>

<span data-ttu-id="a9675-105">Приложения могут безопасно вызывать [**срсетресторепоинт**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) при использовании этих типов событий.</span><span class="sxs-lookup"><span data-stu-id="a9675-105">Applications can safely call [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) when using these event types.</span></span> <span data-ttu-id="a9675-106">Первый вызов функции создает точку восстановления.</span><span class="sxs-lookup"><span data-stu-id="a9675-106">The first call to the function creates a restore point.</span></span> <span data-ttu-id="a9675-107">Последующие вложенные вызовы функции не создают точки восстановления.</span><span class="sxs-lookup"><span data-stu-id="a9675-107">Subsequent nested calls to the function do not create restore points.</span></span> <span data-ttu-id="a9675-108">Например, предположим, что приложение выполняет следующие вызовы **срсетресторепоинт**:</span><span class="sxs-lookup"><span data-stu-id="a9675-108">For example, suppose an application makes the following calls to **SRSetRestorePoint**:</span></span><dl> <span data-ttu-id="a9675-109">Для точки восстановления A с Двевенттипе = начало \_ вложенного \_ \_ изменения системы</span><span class="sxs-lookup"><span data-stu-id="a9675-109">For restore point A with dwEventType = BEGIN\_NESTED\_SYSTEM\_CHANGE</span></span>  
<span data-ttu-id="a9675-110">Для точки восстановления B с Двевенттипе = начало \_ вложенного \_ \_ изменения системы</span><span class="sxs-lookup"><span data-stu-id="a9675-110">For restore point B with dwEventType = BEGIN\_NESTED\_SYSTEM\_CHANGE</span></span>  
<span data-ttu-id="a9675-111">Для точки восстановления B с Двевенттипе = конец \_ вложенного \_ \_ изменения системы</span><span class="sxs-lookup"><span data-stu-id="a9675-111">For restore point B with dwEventType = END\_NESTED\_SYSTEM\_CHANGE</span></span>  
<span data-ttu-id="a9675-112">Для точки восстановления A с Двевенттипе = конец \_ вложенного \_ \_ изменения системы</span><span class="sxs-lookup"><span data-stu-id="a9675-112">For restore point A with dwEventType = END\_NESTED\_SYSTEM\_CHANGE</span></span>  
</dl>

<span data-ttu-id="a9675-113">Второй вызов не создает новую точку восстановления, так как вызов является вложенным.</span><span class="sxs-lookup"><span data-stu-id="a9675-113">The second call does not create a new restore point because the call is nested.</span></span>

 

 




