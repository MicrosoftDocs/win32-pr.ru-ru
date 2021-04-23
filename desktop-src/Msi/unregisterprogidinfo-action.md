---
description: Действие Унрегистерпрогидинфо управляет отменой регистрации данных OLE ProgId в системе.
ms.assetid: c9837845-4ffc-4496-8330-11b46d27ec7a
title: Действие Унрегистерпрогидинфо
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff880c1d339fc3db3db50bd34d3afb828f65ec07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913655"
---
# <a name="unregisterprogidinfo-action"></a><span data-ttu-id="fbd89-103">Действие Унрегистерпрогидинфо</span><span class="sxs-lookup"><span data-stu-id="fbd89-103">UnregisterProgIdInfo Action</span></span>

<span data-ttu-id="fbd89-104">Действие Унрегистерпрогидинфо управляет отменой регистрации данных OLE ProgId в системе.</span><span class="sxs-lookup"><span data-stu-id="fbd89-104">The UnregisterProgIdInfo action manages the unregistration of OLE ProgId information with the system.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="fbd89-105">Ограничения последовательности</span><span class="sxs-lookup"><span data-stu-id="fbd89-105">Sequence Restrictions</span></span>

<span data-ttu-id="fbd89-106">Действие Унрегистерпрогидинфо должно следовать после действия [инсталлинитиализе](installinitialize-action.md) , [Унрегистерклассинфо](unregisterclassinfo-action.md) действия, [унрегистерекстенсионинфо](unregisterextensioninfo-action.md) действия и перед действием [RegisterProgIdInfo](registerprogidinfo-action.md) .</span><span class="sxs-lookup"><span data-stu-id="fbd89-106">The UnregisterProgIdInfo action must come after the [InstallInitialize](installinitialize-action.md) action, [UnregisterClassInfo](unregisterclassinfo-action.md) action, [UnregisterExtensioninfo](unregisterextensioninfo-action.md) action, and before the [RegisterProgIdInfo](registerprogidinfo-action.md) action.</span></span>

<span data-ttu-id="fbd89-107">[Ремоверегистривалуес](removeregistryvalues-action.md) должен предшествовать унрегистерпрогидинфо в последовательности.</span><span class="sxs-lookup"><span data-stu-id="fbd89-107">[RemoveRegistryValues](removeregistryvalues-action.md) must come before UnregisterProgIdInfo in the sequence.</span></span>

<span data-ttu-id="fbd89-108">Последовательность действий в следующей группе ограничена.</span><span class="sxs-lookup"><span data-stu-id="fbd89-108">The sequencing of the actions in the following group is restricted.</span></span> <span data-ttu-id="fbd89-109">Если любое подмножество этих действий выполняется вместе в таблице последовательности, они должны иметь одинаковый относительный порядок последовательности, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="fbd89-109">If any subset of these actions occur together in a sequence table, they must have the same relative sequence order as shown:</span></span>

-   [<span data-ttu-id="fbd89-110">унрегистерклассинфо</span><span class="sxs-lookup"><span data-stu-id="fbd89-110">UnregisterClassInfo</span></span>](unregisterclassinfo-action.md)
-   [<span data-ttu-id="fbd89-111">унрегистерекстенсионинфо</span><span class="sxs-lookup"><span data-stu-id="fbd89-111">UnregisterExtensioninfo</span></span>](unregisterextensioninfo-action.md)
-   <span data-ttu-id="fbd89-112">унрегистерпрогидинфо</span><span class="sxs-lookup"><span data-stu-id="fbd89-112">UnregisterProgIdInfo</span></span>
-   [<span data-ttu-id="fbd89-113">унрегистермимеинфо</span><span class="sxs-lookup"><span data-stu-id="fbd89-113">UnregisterMIMEInfo</span></span>](unregistermimeinfo-action.md)
-   [<span data-ttu-id="fbd89-114">регистерклассинфо</span><span class="sxs-lookup"><span data-stu-id="fbd89-114">RegisterClassInfo</span></span>](registerclassinfo-action.md)
-   [<span data-ttu-id="fbd89-115">регистерекстенсионинфо</span><span class="sxs-lookup"><span data-stu-id="fbd89-115">RegisterExtensionInfo</span></span>](registerextensioninfo-action.md)
-   [<span data-ttu-id="fbd89-116">регистерпрогидинфо</span><span class="sxs-lookup"><span data-stu-id="fbd89-116">RegisterProgIdInfo</span></span>](registerprogidinfo-action.md)
-   [<span data-ttu-id="fbd89-117">регистермимеинфо</span><span class="sxs-lookup"><span data-stu-id="fbd89-117">RegisterMIMEInfo</span></span>](registermimeinfo-action.md)

<span data-ttu-id="fbd89-118">Например, Унрегистерпрогидинфо должен предшествовать [унрегистермимеинфо](unregistermimeinfo-action.md) в таблице Sequence.</span><span class="sxs-lookup"><span data-stu-id="fbd89-118">For example, UnregisterProgIdInfo must come before [UnregisterMIMEInfo](unregistermimeinfo-action.md) in the sequence table.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="fbd89-119">Сообщения Актиондата</span><span class="sxs-lookup"><span data-stu-id="fbd89-119">ActionData Messages</span></span>



| <span data-ttu-id="fbd89-120">Поле</span><span class="sxs-lookup"><span data-stu-id="fbd89-120">Field</span></span> | <span data-ttu-id="fbd89-121">Описание данных действия</span><span class="sxs-lookup"><span data-stu-id="fbd89-121">Description of action data</span></span>                |
|-------|-------------------------------------------|
| <span data-ttu-id="fbd89-122">\[1\]</span><span class="sxs-lookup"><span data-stu-id="fbd89-122">\[1\]</span></span> | <span data-ttu-id="fbd89-123">Идентификатор программы зарегистрированной программы.</span><span class="sxs-lookup"><span data-stu-id="fbd89-123">Program identifier of registered program.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="fbd89-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fbd89-124">Remarks</span></span>

<span data-ttu-id="fbd89-125">Действие Унрегистерпрогидинфо удаляет сведения о ProgId из реестра ([Таблица ProgID](progid-table.md)) для функций, которые подключены к сведениям о расширении ([таблице расширения](extension-table.md)) или сведениям о классе ([таблице классов](class-table.md)) и выбираются для удаления.</span><span class="sxs-lookup"><span data-stu-id="fbd89-125">The UnregisterProgIdInfo action removes ProgId information from the registry ([ProgId Table](progid-table.md)) for features that are connected to the extension information ([Extension table](extension-table.md)) or the Class information ([Class table](class-table.md)) and are currently selected to be uninstalled.</span></span>

 

 



