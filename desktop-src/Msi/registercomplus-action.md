---
description: Действие Регистеркомплус регистрирует приложения COM+.
ms.assetid: e42bb993-7079-4d5b-bb2e-c958e99e705e
title: Действие Регистеркомплус
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb824d67e776a99f8cd05c56f73f171f436c71d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156463"
---
# <a name="registercomplus-action"></a><span data-ttu-id="bcfba-103">Действие Регистеркомплус</span><span class="sxs-lookup"><span data-stu-id="bcfba-103">RegisterComPlus Action</span></span>

<span data-ttu-id="bcfba-104">Действие Регистеркомплус регистрирует приложения COM+.</span><span class="sxs-lookup"><span data-stu-id="bcfba-104">The RegisterComPlus action registers COM+ applications.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="bcfba-105">Ограничения последовательности</span><span class="sxs-lookup"><span data-stu-id="bcfba-105">Sequence Restrictions</span></span>

<span data-ttu-id="bcfba-106">Действие Регистеркомплус должно следовать за [действием инсталлфилес](installfiles-action.md) и [действием унрегистеркомплус](unregistercomplus-action.md).</span><span class="sxs-lookup"><span data-stu-id="bcfba-106">The RegisterComPlus action must follow the [InstallFiles action](installfiles-action.md) and the [UnregisterComPlus action](unregistercomplus-action.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="bcfba-107">Сообщения Актиондата</span><span class="sxs-lookup"><span data-stu-id="bcfba-107">ActionData Messages</span></span>



| <span data-ttu-id="bcfba-108">Поле</span><span class="sxs-lookup"><span data-stu-id="bcfba-108">Field</span></span> | <span data-ttu-id="bcfba-109">Описание данных действия</span><span class="sxs-lookup"><span data-stu-id="bcfba-109">Description of action data</span></span>              |
|-------|-----------------------------------------|
| <span data-ttu-id="bcfba-110">\[1\]</span><span class="sxs-lookup"><span data-stu-id="bcfba-110">\[1\]</span></span> | <span data-ttu-id="bcfba-111">Идентификатор приложения COM+.</span><span class="sxs-lookup"><span data-stu-id="bcfba-111">Application ID of the COM+ application.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="bcfba-112">См. также</span><span class="sxs-lookup"><span data-stu-id="bcfba-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bcfba-113">Таблица ComPlus</span><span class="sxs-lookup"><span data-stu-id="bcfba-113">Complus table</span></span>](complus-table.md)
</dt> <dt>

[<span data-ttu-id="bcfba-114">Действие Унрегистеркомплус</span><span class="sxs-lookup"><span data-stu-id="bcfba-114">UnregisterComPlus action</span></span>](unregistercomplus-action.md)
</dt> <dt>

[<span data-ttu-id="bcfba-115">Установка приложения COM+ с установщик Windows</span><span class="sxs-lookup"><span data-stu-id="bcfba-115">Installing a COM+ Application with the Windows Installer</span></span>](installing-a-com--application-with-the-windows-installer.md)
</dt> </dl>

 

 



