---
description: Действие Регистерекстенсионинфо управляет регистрацией сведений, связанных с расширением, с системой.
ms.assetid: 3c243ca3-9fa7-41ec-968e-7954d7d45432
title: Действие Регистерекстенсионинфо
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0310344b6579ef65faac41238bb607ce98411b52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650782"
---
# <a name="registerextensioninfo-action"></a><span data-ttu-id="008f1-103">Действие Регистерекстенсионинфо</span><span class="sxs-lookup"><span data-stu-id="008f1-103">RegisterExtensionInfo Action</span></span>

<span data-ttu-id="008f1-104">Действие Регистерекстенсионинфо управляет регистрацией сведений, связанных с расширением, с системой.</span><span class="sxs-lookup"><span data-stu-id="008f1-104">The RegisterExtensionInfo action manages the registration of extension related information with the system.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="008f1-105">Ограничения последовательности</span><span class="sxs-lookup"><span data-stu-id="008f1-105">Sequence Restrictions</span></span>

<span data-ttu-id="008f1-106">Действие Регистерекстенсионинфо должно следовать после действия [инсталлфилес](installfiles-action.md) и действия [унрегистерекстенсионинфо](unregisterextensioninfo-action.md) .</span><span class="sxs-lookup"><span data-stu-id="008f1-106">The RegisterExtensionInfo action must come after the [InstallFiles](installfiles-action.md) action and the [UnregisterExtensionInfo](unregisterextensioninfo-action.md) action.</span></span>

<span data-ttu-id="008f1-107">Последовательность действий в следующей группе ограничена.</span><span class="sxs-lookup"><span data-stu-id="008f1-107">The sequencing of the actions in the following group is restricted.</span></span> <span data-ttu-id="008f1-108">Если любое подмножество этих действий выполняется вместе в таблице последовательности, они должны иметь одинаковый относительный порядок последовательности, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="008f1-108">If any subset of these actions occur together in a sequence table, they must have the same relative sequence order as shown:</span></span>

-   [<span data-ttu-id="008f1-109">унрегистерклассинфо</span><span class="sxs-lookup"><span data-stu-id="008f1-109">UnregisterClassInfo</span></span>](unregisterclassinfo-action.md)
-   [<span data-ttu-id="008f1-110">унрегистерекстенсионинфо</span><span class="sxs-lookup"><span data-stu-id="008f1-110">UnregisterExtensionInfo</span></span>](unregisterextensioninfo-action.md)
-   [<span data-ttu-id="008f1-111">унрегистерпрогидинфо</span><span class="sxs-lookup"><span data-stu-id="008f1-111">UnregisterProgIdInfo</span></span>](unregisterprogidinfo-action.md)
-   [<span data-ttu-id="008f1-112">унрегистермимеинфо</span><span class="sxs-lookup"><span data-stu-id="008f1-112">UnregisterMIMEInfo</span></span>](unregistermimeinfo-action.md)
-   [<span data-ttu-id="008f1-113">регистерклассинфо</span><span class="sxs-lookup"><span data-stu-id="008f1-113">RegisterClassInfo</span></span>](registerclassinfo-action.md)
-   <span data-ttu-id="008f1-114">регистерекстенсионинфо</span><span class="sxs-lookup"><span data-stu-id="008f1-114">RegisterExtensionInfo</span></span>
-   [<span data-ttu-id="008f1-115">регистерпрогидинфо</span><span class="sxs-lookup"><span data-stu-id="008f1-115">RegisterProgIdInfo</span></span>](registerprogidinfo-action.md)
-   [<span data-ttu-id="008f1-116">регистермимеинфо</span><span class="sxs-lookup"><span data-stu-id="008f1-116">RegisterMIMEInfo</span></span>](registermimeinfo-action.md)

<span data-ttu-id="008f1-117">Например, Регистерекстенсионинфо должен следовать после [унрегистермимеинфо](unregistermimeinfo-action.md) в таблице Sequence.</span><span class="sxs-lookup"><span data-stu-id="008f1-117">For example, RegisterExtensionInfo must come after [UnregisterMIMEInfo](unregistermimeinfo-action.md) in the sequence table.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="008f1-118">Сообщения Актиондата</span><span class="sxs-lookup"><span data-stu-id="008f1-118">ActionData Messages</span></span>



| <span data-ttu-id="008f1-119">Поле</span><span class="sxs-lookup"><span data-stu-id="008f1-119">Field</span></span> | <span data-ttu-id="008f1-120">Описание данных действия</span><span class="sxs-lookup"><span data-stu-id="008f1-120">Description of action data</span></span> |
|-------|----------------------------|
| <span data-ttu-id="008f1-121">\[1\]</span><span class="sxs-lookup"><span data-stu-id="008f1-121">\[1\]</span></span> | <span data-ttu-id="008f1-122">Зарегистрированное расширение.</span><span class="sxs-lookup"><span data-stu-id="008f1-122">Registered extension.</span></span>      |



 

## <a name="remarks"></a><span data-ttu-id="008f1-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="008f1-123">Remarks</span></span>

<span data-ttu-id="008f1-124">Если система поддерживает установку по запросу для серверов расширений, Регистерекстенсионинфо регистрирует все серверы расширений в [таблице расширений](extension-table.md) , связанной с набором компонентов для установки или объявления.</span><span class="sxs-lookup"><span data-stu-id="008f1-124">If the system supports installation-on-demand for extension servers, RegisterExtensionInfo registers all extension servers in the [Extension table](extension-table.md) associated with features set for installation or advertisement.</span></span> <span data-ttu-id="008f1-125">В противном случае это действие регистрирует только серверы расширений, связанные с компонентами, для которых установлено значение установка.</span><span class="sxs-lookup"><span data-stu-id="008f1-125">Otherwise this action only registers extension servers associated with features set to installation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="008f1-126">См. также</span><span class="sxs-lookup"><span data-stu-id="008f1-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="008f1-127">**Шелладвтсуппорт, свойство**</span><span class="sxs-lookup"><span data-stu-id="008f1-127">**ShellAdvtSupport property**</span></span>](shelladvtsupport.md)
</dt> </dl>

 

 



