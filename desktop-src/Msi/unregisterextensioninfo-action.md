---
description: Действие Унрегистерекстенсионинфо управляет удалением сведений, относящихся к расширению, из системного реестра.
ms.assetid: 62bb9d17-c221-4bd2-bd7f-9930e28bb946
title: Действие Унрегистерекстенсионинфо
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85d069a686c5f0e517a0cc9556634895216dd8cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105651187"
---
# <a name="unregisterextensioninfo-action"></a><span data-ttu-id="9fb83-103">Действие Унрегистерекстенсионинфо</span><span class="sxs-lookup"><span data-stu-id="9fb83-103">UnregisterExtensionInfo Action</span></span>

<span data-ttu-id="9fb83-104">Действие Унрегистерекстенсионинфо управляет удалением сведений, относящихся к расширению, из системного реестра.</span><span class="sxs-lookup"><span data-stu-id="9fb83-104">The UnregisterExtensionInfo action manages the removal of extension-related information from the system registry.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="9fb83-105">Ограничения последовательности</span><span class="sxs-lookup"><span data-stu-id="9fb83-105">Sequence Restrictions</span></span>

<span data-ttu-id="9fb83-106">Действие Унрегистерекстенсионинфо должно следовать после действия [инсталлинитиализе](installinitialize-action.md) и перед действием [регистерекстенсионинфо](registerextensioninfo-action.md) .</span><span class="sxs-lookup"><span data-stu-id="9fb83-106">The UnregisterExtensionInfo action must come after the [InstallInitialize](installinitialize-action.md) action and before the [RegisterExtensionInfo](registerextensioninfo-action.md) action.</span></span>

<span data-ttu-id="9fb83-107">[Ремоверегистривалуес](removeregistryvalues-action.md) должен предшествовать унрегистерекстенсионинфо в последовательности.</span><span class="sxs-lookup"><span data-stu-id="9fb83-107">[RemoveRegistryValues](removeregistryvalues-action.md) must come before UnregisterExtensionInfo in the sequence.</span></span>

<span data-ttu-id="9fb83-108">Последовательность действий в следующей группе ограничена.</span><span class="sxs-lookup"><span data-stu-id="9fb83-108">The sequencing of the actions in the following group is restricted.</span></span> <span data-ttu-id="9fb83-109">Если любое подмножество этих действий выполняется вместе в таблице последовательности, они должны иметь одинаковый относительный порядок последовательности, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="9fb83-109">If any subset of these actions occur together in a sequence table, they must have the same relative sequence order as shown:</span></span>

-   [<span data-ttu-id="9fb83-110">унрегистерклассинфо</span><span class="sxs-lookup"><span data-stu-id="9fb83-110">UnregisterClassInfo</span></span>](unregisterclassinfo-action.md)
-   <span data-ttu-id="9fb83-111">унрегистерекстенсионинфо</span><span class="sxs-lookup"><span data-stu-id="9fb83-111">UnregisterExtensionInfo</span></span>
-   [<span data-ttu-id="9fb83-112">унрегистерпрогидинфо</span><span class="sxs-lookup"><span data-stu-id="9fb83-112">UnregisterProgIdInfo</span></span>](unregisterprogidinfo-action.md)
-   [<span data-ttu-id="9fb83-113">унрегистермимеинфо</span><span class="sxs-lookup"><span data-stu-id="9fb83-113">UnregisterMIMEInfo</span></span>](unregistermimeinfo-action.md)
-   [<span data-ttu-id="9fb83-114">регистерклассинфо</span><span class="sxs-lookup"><span data-stu-id="9fb83-114">RegisterClassInfo</span></span>](registerclassinfo-action.md)
-   [<span data-ttu-id="9fb83-115">регистерекстенсионинфо</span><span class="sxs-lookup"><span data-stu-id="9fb83-115">RegisterExtensionInfo</span></span>](registerextensioninfo-action.md)
-   [<span data-ttu-id="9fb83-116">регистерпрогидинфо</span><span class="sxs-lookup"><span data-stu-id="9fb83-116">RegisterProgIdInfo</span></span>](registerprogidinfo-action.md)
-   [<span data-ttu-id="9fb83-117">регистермимеинфо</span><span class="sxs-lookup"><span data-stu-id="9fb83-117">RegisterMIMEInfo</span></span>](registermimeinfo-action.md)

<span data-ttu-id="9fb83-118">Например, Унрегистерекстенсионинфо должен предшествовать [унрегистерпрогидинфо](unregisterprogidinfo-action.md) в таблице Sequence.</span><span class="sxs-lookup"><span data-stu-id="9fb83-118">For example, UnregisterExtensionInfo must come before [UnregisterProgIdInfo](unregisterprogidinfo-action.md) in the sequence table.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="9fb83-119">Сообщения Актиондата</span><span class="sxs-lookup"><span data-stu-id="9fb83-119">ActionData Messages</span></span>



| <span data-ttu-id="9fb83-120">Поле</span><span class="sxs-lookup"><span data-stu-id="9fb83-120">Field</span></span> | <span data-ttu-id="9fb83-121">Описание данных действия</span><span class="sxs-lookup"><span data-stu-id="9fb83-121">Description of action data</span></span> |
|-------|----------------------------|
| <span data-ttu-id="9fb83-122">\[1\]</span><span class="sxs-lookup"><span data-stu-id="9fb83-122">\[1\]</span></span> | <span data-ttu-id="9fb83-123">Удалено расширение.</span><span class="sxs-lookup"><span data-stu-id="9fb83-123">Removed extension.</span></span>         |



 

## <a name="remarks"></a><span data-ttu-id="9fb83-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9fb83-124">Remarks</span></span>

<span data-ttu-id="9fb83-125">Если система не поддерживает установку серверов расширений по запросу, Унрегистерекстенсионинфо удаляет все серверы расширений в [таблице расширений](extension-table.md) , связанной с удаленным компонентом, или компонент, установленный как объявленный из реестра.</span><span class="sxs-lookup"><span data-stu-id="9fb83-125">If the system does not support the install-on-demand of extension servers, UnregisterExtensionInfo removes all extension servers in the [Extension table](extension-table.md) associated with either an uninstalled feature or a feature installed as advertised from the registry.</span></span> <span data-ttu-id="9fb83-126">В противном случае это действие удаляет серверы расширений, связанные с компонентом, который выбран для удаления из реестра.</span><span class="sxs-lookup"><span data-stu-id="9fb83-126">Otherwise, this action removes the extension servers associated with a feature that is selected to be removed from the registry.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9fb83-127">См. также</span><span class="sxs-lookup"><span data-stu-id="9fb83-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9fb83-128">**Шелладвтсуппорт, свойство**</span><span class="sxs-lookup"><span data-stu-id="9fb83-128">**ShellAdvtSupport Property**</span></span>](shelladvtsupport.md)
</dt> </dl>

 

 



