---
description: Действие Унрегистерклассинфо управляет удалением сведений о классе COM из системного реестра. В нем используется таблица AppId.
ms.assetid: 579a69ee-92cd-4d4c-a007-998ec042f9fc
title: Действие Унрегистерклассинфо
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57ee701925e07e4f74439efb45da00d430d90304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105651189"
---
# <a name="unregisterclassinfo-action"></a><span data-ttu-id="4e926-104">Действие Унрегистерклассинфо</span><span class="sxs-lookup"><span data-stu-id="4e926-104">UnregisterClassInfo Action</span></span>

<span data-ttu-id="4e926-105">Действие Унрегистерклассинфо управляет удалением сведений о классе COM из системного реестра.</span><span class="sxs-lookup"><span data-stu-id="4e926-105">The UnregisterClassInfo action manages the removal of COM class information from the system registry.</span></span> <span data-ttu-id="4e926-106">В нем используется [Таблица AppID](appid-table.md).</span><span class="sxs-lookup"><span data-stu-id="4e926-106">It uses the [AppId table](appid-table.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="4e926-107">Ограничения последовательности</span><span class="sxs-lookup"><span data-stu-id="4e926-107">Sequence Restrictions</span></span>

<span data-ttu-id="4e926-108">Действие Унрегистерклассинфо должно следовать после действия [инсталлинитиализе](installinitialize-action.md) и перед действием [регистерклассинфо](registerclassinfo-action.md) .</span><span class="sxs-lookup"><span data-stu-id="4e926-108">The UnregisterClassInfo action must come after the [InstallInitialize](installinitialize-action.md) action and before the [RegisterClassInfo](registerclassinfo-action.md) action.</span></span>

<span data-ttu-id="4e926-109">[Ремоверегистривалуес](removeregistryvalues-action.md) должен предшествовать унрегистерклассинфо в последовательности.</span><span class="sxs-lookup"><span data-stu-id="4e926-109">[RemoveRegistryValues](removeregistryvalues-action.md) must come before UnregisterClassInfo in the sequence.</span></span>

<span data-ttu-id="4e926-110">Последовательность действий в следующей группе ограничена.</span><span class="sxs-lookup"><span data-stu-id="4e926-110">The sequencing of the actions in the following group is restricted.</span></span> <span data-ttu-id="4e926-111">Если любое подмножество этих действий выполняется вместе в таблице последовательности, они должны находиться в той же относительной последовательности, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="4e926-111">If any subset of these actions occur together in a sequence table, they must occur in the same relative sequence as shown in the following table:</span></span>

-   <span data-ttu-id="4e926-112">унрегистерклассинфо</span><span class="sxs-lookup"><span data-stu-id="4e926-112">UnregisterClassInfo</span></span>
-   [<span data-ttu-id="4e926-113">унрегистерекстенсионинфо</span><span class="sxs-lookup"><span data-stu-id="4e926-113">UnregisterExtensionInfo</span></span>](unregisterextensioninfo-action.md)
-   [<span data-ttu-id="4e926-114">унрегистерпрогидинфо</span><span class="sxs-lookup"><span data-stu-id="4e926-114">UnregisterProgIdInfo</span></span>](unregisterprogidinfo-action.md)
-   [<span data-ttu-id="4e926-115">унрегистермимеинфо</span><span class="sxs-lookup"><span data-stu-id="4e926-115">UnregisterMIMEInfo</span></span>](unregistermimeinfo-action.md)
-   [<span data-ttu-id="4e926-116">регистерклассинфо</span><span class="sxs-lookup"><span data-stu-id="4e926-116">RegisterClassInfo</span></span>](registerclassinfo-action.md)
-   [<span data-ttu-id="4e926-117">регистерекстенсионинфо</span><span class="sxs-lookup"><span data-stu-id="4e926-117">RegisterExtensionInfo</span></span>](registerextensioninfo-action.md)
-   [<span data-ttu-id="4e926-118">регистерпрогидинфо</span><span class="sxs-lookup"><span data-stu-id="4e926-118">RegisterProgIdInfo</span></span>](registerprogidinfo-action.md)
-   [<span data-ttu-id="4e926-119">регистермимеинфо</span><span class="sxs-lookup"><span data-stu-id="4e926-119">RegisterMIMEInfo</span></span>](registermimeinfo-action.md)

<span data-ttu-id="4e926-120">Например, [регистерекстенсионинфо](registerextensioninfo-action.md) должен предшествовать унрегистерклассинфо в таблице Sequence.</span><span class="sxs-lookup"><span data-stu-id="4e926-120">For example, [RegisterExtensionInfo](registerextensioninfo-action.md) must come before UnregisterClassInfo in the sequence table.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="4e926-121">Сообщения Актиондата</span><span class="sxs-lookup"><span data-stu-id="4e926-121">ActionData Messages</span></span>



| <span data-ttu-id="4e926-122">Поле</span><span class="sxs-lookup"><span data-stu-id="4e926-122">Field</span></span> | <span data-ttu-id="4e926-123">Описание данных действия</span><span class="sxs-lookup"><span data-stu-id="4e926-123">Description of action data</span></span>      |
|-------|---------------------------------|
| <span data-ttu-id="4e926-124">\[1\]</span><span class="sxs-lookup"><span data-stu-id="4e926-124">\[1\]</span></span> | <span data-ttu-id="4e926-125">Идентификатор GUID незарегистрированного класса COM.</span><span class="sxs-lookup"><span data-stu-id="4e926-125">GUID of unregistered COM class.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="4e926-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4e926-126">Remarks</span></span>

<span data-ttu-id="4e926-127">Установщик устанавливает свойство [**олеадвтсуппорт**](oleadvtsupport.md) в значение true, если система текущего пользователя была обновлена для работы с Install-On-Demand by com.</span><span class="sxs-lookup"><span data-stu-id="4e926-127">The installer sets the [**OLEAdvtSupport**](oleadvtsupport.md) property to true when the current user's system has been upgraded to work with install-on-demand through COM.</span></span> <span data-ttu-id="4e926-128">Если система не поддерживает установку по запросу через COM, Унрегистерклассинфо удаляет все COM-классы, перечисленные в [таблице классов](class-table.md) , связанной с удаленными компонентами или компонентами, установленными из системного реестра.</span><span class="sxs-lookup"><span data-stu-id="4e926-128">If the system does not support install-on-demand through COM, UnregisterClassInfo removes all COM classes listed in the [Class table](class-table.md) associated with either uninstalled features or features installed as advertised from the system registry.</span></span> <span data-ttu-id="4e926-129">В противном случае это действие удаляет только классы COM, связанные с компонентами, выбранными для удаления из системного реестра.</span><span class="sxs-lookup"><span data-stu-id="4e926-129">Otherwise, this action removes only the COM classes associated with features selected to be uninstalled from the system registry.</span></span>

 

 



