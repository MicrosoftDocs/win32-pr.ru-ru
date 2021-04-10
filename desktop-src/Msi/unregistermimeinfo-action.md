---
description: Действие Унрегистермимеинфо отменяет регистрацию в системе сведений о реестре, связанных с MIME. Действие отменяет регистрацию сведений MIME для серверов из таблицы MIME, для которой в данный момент выбрана соответствующая функция для удаления.
ms.assetid: 9a5c12da-e78f-4c99-9b82-d41624593c61
title: Действие Унрегистермимеинфо
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02c1ca7c0cd12d9ec6236a0c0298ba793713f5ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272937"
---
# <a name="unregistermimeinfo-action"></a><span data-ttu-id="f7f36-104">Действие Унрегистермимеинфо</span><span class="sxs-lookup"><span data-stu-id="f7f36-104">UnregisterMIMEInfo Action</span></span>

<span data-ttu-id="f7f36-105">Действие Унрегистермимеинфо отменяет регистрацию в системе сведений о реестре, связанных с MIME.</span><span class="sxs-lookup"><span data-stu-id="f7f36-105">The UnregisterMIMEInfo action unregisters MIME-related registry information from the system.</span></span> <span data-ttu-id="f7f36-106">Действие отменяет регистрацию сведений MIME для серверов из [таблицы MIME](mime-table.md) , для которой в данный момент выбрана соответствующая функция для удаления.</span><span class="sxs-lookup"><span data-stu-id="f7f36-106">The action unregisters MIME information for servers from the [MIME table](mime-table.md) for which the corresponding feature is currently selected to be uninstalled.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="f7f36-107">Ограничения последовательности</span><span class="sxs-lookup"><span data-stu-id="f7f36-107">Sequence Restrictions</span></span>

<span data-ttu-id="f7f36-108">Действие Унрегистермимеинфо должно следовать после действия [инсталлинитиализе](installinitialize-action.md) , [Унрегистерклассинфо](unregisterclassinfo-action.md) действия, [унрегистерекстенсионинфо](unregisterextensioninfo-action.md) действия и перед действием [RegisterMIMEInfo](registermimeinfo-action.md) .</span><span class="sxs-lookup"><span data-stu-id="f7f36-108">The UnregisterMIMEInfo action must come after the [InstallInitialize](installinitialize-action.md) action, [UnregisterClassInfo](unregisterclassinfo-action.md) action, [UnregisterExtensionInfo](unregisterextensioninfo-action.md) action, and before the [RegisterMIMEInfo](registermimeinfo-action.md) action.</span></span>

<span data-ttu-id="f7f36-109">[Ремоверегистривалуес](removeregistryvalues-action.md) должен предшествовать унрегистермимеинфо в последовательности.</span><span class="sxs-lookup"><span data-stu-id="f7f36-109">[RemoveRegistryValues](removeregistryvalues-action.md) must come before UnregisterMIMEInfo in the sequence.</span></span>

<span data-ttu-id="f7f36-110">Последовательность действий в следующей группе ограничена.</span><span class="sxs-lookup"><span data-stu-id="f7f36-110">The sequencing of the actions in the following group is restricted.</span></span> <span data-ttu-id="f7f36-111">Если любое подмножество этих действий выполняется вместе в таблице последовательности, они должны иметь одинаковый относительный порядок последовательности, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="f7f36-111">If any subset of these actions occur together in a sequence table, they must have the same relative sequence order as shown:</span></span>

-   [<span data-ttu-id="f7f36-112">унрегистерклассинфо</span><span class="sxs-lookup"><span data-stu-id="f7f36-112">UnregisterClassInfo</span></span>](unregisterclassinfo-action.md)
-   [<span data-ttu-id="f7f36-113">унрегистерекстенсионинфо</span><span class="sxs-lookup"><span data-stu-id="f7f36-113">UnregisterExtensionInfo</span></span>](unregisterextensioninfo-action.md)
-   [<span data-ttu-id="f7f36-114">унрегистерпрогидинфо</span><span class="sxs-lookup"><span data-stu-id="f7f36-114">UnregisterProgIdInfo</span></span>](unregisterprogidinfo-action.md)
-   <span data-ttu-id="f7f36-115">унрегистермимеинфо</span><span class="sxs-lookup"><span data-stu-id="f7f36-115">UnregisterMIMEInfo</span></span>
-   [<span data-ttu-id="f7f36-116">регистерклассинфо</span><span class="sxs-lookup"><span data-stu-id="f7f36-116">RegisterClassInfo</span></span>](registerclassinfo-action.md)
-   [<span data-ttu-id="f7f36-117">регистерекстенсионинфо</span><span class="sxs-lookup"><span data-stu-id="f7f36-117">RegisterExtensionInfo</span></span>](registerextensioninfo-action.md)
-   [<span data-ttu-id="f7f36-118">регистерпрогидинфо</span><span class="sxs-lookup"><span data-stu-id="f7f36-118">RegisterProgIdInfo</span></span>](registerprogidinfo-action.md)
-   [<span data-ttu-id="f7f36-119">регистермимеинфо</span><span class="sxs-lookup"><span data-stu-id="f7f36-119">RegisterMIMEInfo</span></span>](registermimeinfo-action.md)

<span data-ttu-id="f7f36-120">Например, Унрегистермимеинфо должен предшествовать [регистерекстенсионинфо](registerextensioninfo-action.md) в таблице Sequence.</span><span class="sxs-lookup"><span data-stu-id="f7f36-120">For example, UnregisterMIMEInfo must come before [RegisterExtensionInfo](registerextensioninfo-action.md) in the sequence table.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="f7f36-121">Сообщения Актиондата</span><span class="sxs-lookup"><span data-stu-id="f7f36-121">ActionData Messages</span></span>



| <span data-ttu-id="f7f36-122">Поле</span><span class="sxs-lookup"><span data-stu-id="f7f36-122">Field</span></span> | <span data-ttu-id="f7f36-123">Описание данных действия</span><span class="sxs-lookup"><span data-stu-id="f7f36-123">Description of action data</span></span>                    |
|-------|-----------------------------------------------|
| <span data-ttu-id="f7f36-124">\[1\]</span><span class="sxs-lookup"><span data-stu-id="f7f36-124">\[1\]</span></span> | <span data-ttu-id="f7f36-125">Идентификатор незарегистрированного типа содержимого MIME.</span><span class="sxs-lookup"><span data-stu-id="f7f36-125">Identifier of unregistered MIME content type.</span></span> |
| <span data-ttu-id="f7f36-126">\[2\]</span><span class="sxs-lookup"><span data-stu-id="f7f36-126">\[2\]</span></span> | <span data-ttu-id="f7f36-127">Расширение, связанное с типом содержимого MIME.</span><span class="sxs-lookup"><span data-stu-id="f7f36-127">Extension associated with MIME content type.</span></span>  |



 

 

 



