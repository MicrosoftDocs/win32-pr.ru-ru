---
description: Действие Унрегистеркомплус удаляет приложения COM+ из реестра.
ms.assetid: bcedc436-a048-487e-9a84-e766da57a0b3
title: Действие Унрегистеркомплус
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e32d39255229151757f7d6be0ada871f555f77e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999678"
---
# <a name="unregistercomplus-action"></a><span data-ttu-id="d8b90-103">Действие Унрегистеркомплус</span><span class="sxs-lookup"><span data-stu-id="d8b90-103">UnregisterComPlus Action</span></span>

<span data-ttu-id="d8b90-104">Действие Унрегистеркомплус удаляет приложения COM+ из реестра.</span><span class="sxs-lookup"><span data-stu-id="d8b90-104">The UnregisterComPlus action removes COM+ applications from the registry.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="d8b90-105">Ограничения последовательности</span><span class="sxs-lookup"><span data-stu-id="d8b90-105">Sequence Restrictions</span></span>

<span data-ttu-id="d8b90-106">[Действие регистеркомплус](registercomplus-action.md) должно следовать за [действием инсталлфилес](installfiles-action.md) и действием унрегистеркомплус.</span><span class="sxs-lookup"><span data-stu-id="d8b90-106">The [RegisterComPlus action](registercomplus-action.md) must follow the [InstallFiles action](installfiles-action.md) and the UnregisterComPlus action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="d8b90-107">Сообщения Актиондата</span><span class="sxs-lookup"><span data-stu-id="d8b90-107">ActionData Messages</span></span>



| <span data-ttu-id="d8b90-108">Поле</span><span class="sxs-lookup"><span data-stu-id="d8b90-108">Field</span></span> | <span data-ttu-id="d8b90-109">Описание данных действия</span><span class="sxs-lookup"><span data-stu-id="d8b90-109">Description of action data</span></span>                                    |
|-------|---------------------------------------------------------------|
| <span data-ttu-id="d8b90-110">\[1\]</span><span class="sxs-lookup"><span data-stu-id="d8b90-110">\[1\]</span></span> | <span data-ttu-id="d8b90-111">Идентификатор приложения удаляемого приложения COM+.</span><span class="sxs-lookup"><span data-stu-id="d8b90-111">Application identifier of the COM+ application being removed.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="d8b90-112">См. также</span><span class="sxs-lookup"><span data-stu-id="d8b90-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d8b90-113">Действие Регистеркомплус</span><span class="sxs-lookup"><span data-stu-id="d8b90-113">RegisterComPlus action</span></span>](registercomplus-action.md)
</dt> <dt>

[<span data-ttu-id="d8b90-114">Таблица ComPlus</span><span class="sxs-lookup"><span data-stu-id="d8b90-114">Complus table</span></span>](complus-table.md)
</dt> <dt>

[<span data-ttu-id="d8b90-115">Установка приложения COM+ с установщик Windows</span><span class="sxs-lookup"><span data-stu-id="d8b90-115">Installing a COM+ Application with the Windows Installer</span></span>](installing-a-com--application-with-the-windows-installer.md)
</dt> </dl>

 

 



