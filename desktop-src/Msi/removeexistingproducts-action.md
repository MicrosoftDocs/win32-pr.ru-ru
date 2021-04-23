---
description: Действие RemoveExistingProducts проходит по кодам продуктов, перечисленным в столбце Актионпроперти таблицы Upgrade, и удаляет продукты последовательно путем вызова параллельных установок.
ms.assetid: 3e96283b-1085-4ace-b004-2fd94310eeb2
title: Действие RemoveExistingProducts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dea3b792b02352277e8f29fa422b093fe876b560
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663376"
---
# <a name="removeexistingproducts-action"></a><span data-ttu-id="1056c-103">Действие RemoveExistingProducts</span><span class="sxs-lookup"><span data-stu-id="1056c-103">RemoveExistingProducts Action</span></span>

<span data-ttu-id="1056c-104">Действие RemoveExistingProducts проходит по кодам продуктов, перечисленным в столбце Актионпроперти [таблицы Upgrade](upgrade-table.md) , и удаляет продукты последовательно путем вызова параллельных установок.</span><span class="sxs-lookup"><span data-stu-id="1056c-104">The RemoveExistingProducts action goes through the product codes listed in the ActionProperty column of the [Upgrade table](upgrade-table.md) and removes the products in sequence by invoking concurrent installations.</span></span> <span data-ttu-id="1056c-105">Для каждой параллельной установки установщик задает для свойства [**ProductCode**](productcode.md) код продукта и задает для свойства [**Remove**](remove.md) значение в поле удалить таблицы Upgrade.</span><span class="sxs-lookup"><span data-stu-id="1056c-105">For each concurrent installation the installer sets the [**ProductCode**](productcode.md) property to the product code and sets the [**REMOVE**](remove.md) property to the value in the Remove field of the Upgrade table.</span></span> <span data-ttu-id="1056c-106">Если поле удалить пустое, его значение по умолчанию равно ALL, и установщик удалит весь продукт.</span><span class="sxs-lookup"><span data-stu-id="1056c-106">If the Remove field is blank, its value defaults to ALL and the installer removes the entire product.</span></span>

<span data-ttu-id="1056c-107">Установщик выполняет только действие RemoveExistingProducts при первой установке продукта.</span><span class="sxs-lookup"><span data-stu-id="1056c-107">The installer only runs the RemoveExistingProducts action the first time it installs a product.</span></span> <span data-ttu-id="1056c-108">Он не выполняет действие во время установки или удаления [обслуживания](maintenance-installation.md) .</span><span class="sxs-lookup"><span data-stu-id="1056c-108">It does not run the action during a [maintenance installation](maintenance-installation.md) or uninstallation.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="1056c-109">Ограничения последовательности</span><span class="sxs-lookup"><span data-stu-id="1056c-109">Sequence Restrictions</span></span>

<span data-ttu-id="1056c-110">Действие RemoveExistingProducts должно быть запланировано в последовательности действий в одном из следующих расположений.</span><span class="sxs-lookup"><span data-stu-id="1056c-110">The RemoveExistingProducts action must be scheduled in the action sequence in one of the following locations.</span></span>

-   <span data-ttu-id="1056c-111">Между [действием инсталлвалидате](installvalidate-action.md) и [действием инсталлинитиализе](installinitialize-action.md).</span><span class="sxs-lookup"><span data-stu-id="1056c-111">Between the [InstallValidate action](installvalidate-action.md) and the [InstallInitialize action](installinitialize-action.md).</span></span> <span data-ttu-id="1056c-112">В этом случае установщик удаляет старые приложения полностью перед установкой новых приложений.</span><span class="sxs-lookup"><span data-stu-id="1056c-112">In this case, the installer removes the old applications entirely before installing the new applications.</span></span> <span data-ttu-id="1056c-113">Это неэффективное размещение действия, поскольку необходимо повторно скопировать все повторно используемые файлы.</span><span class="sxs-lookup"><span data-stu-id="1056c-113">This is an inefficient placement for the action because all reused files have to be recopied.</span></span>
-   <span data-ttu-id="1056c-114">После [действия инсталлинитиализе](installinitialize-action.md) и перед всеми действиями, создающими скрипт выполнения.</span><span class="sxs-lookup"><span data-stu-id="1056c-114">After the [InstallInitialize action](installinitialize-action.md) and before any actions that generate execution script.</span></span>
-   <span data-ttu-id="1056c-115">Между [действием инсталлексекуте](installexecute-action.md), [действием инсталлексекутеагаин](installexecuteagain-action.md)и [действием функции InstallFinalize](installfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="1056c-115">Between the [InstallExecute action](installexecute-action.md), or the [InstallExecuteAgain action](installexecuteagain-action.md), and the [InstallFinalize action](installfinalize-action.md).</span></span> <span data-ttu-id="1056c-116">Как правило, последние три действия запланированы прямо друг за другом: Инсталлексекуте, RemoveExistingProducts и функции InstallFinalize.</span><span class="sxs-lookup"><span data-stu-id="1056c-116">Generally the last three actions are scheduled right after one another: InstallExecute, RemoveExistingProducts, and InstallFinalize.</span></span> <span data-ttu-id="1056c-117">В этом случае сначала устанавливаются обновленные файлы, а затем старые файлы удаляются.</span><span class="sxs-lookup"><span data-stu-id="1056c-117">In this case the updated files are installed first and then the old files are removed.</span></span> <span data-ttu-id="1056c-118">Однако если при удалении старого приложения произойдет сбой, то программа установки произведет откат и удаление старого приложения, и установку нового приложения.</span><span class="sxs-lookup"><span data-stu-id="1056c-118">However, if the removal of the old application fails, then the installer rolls back both the removal of the old application and the install of the new application.</span></span>
-   <span data-ttu-id="1056c-119">После [действия функции InstallFinalize](installfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="1056c-119">After the [InstallFinalize action](installfinalize-action.md).</span></span> <span data-ttu-id="1056c-120">Это наиболее эффективный способ размещения действия.</span><span class="sxs-lookup"><span data-stu-id="1056c-120">This is the most efficient placement for the action.</span></span> <span data-ttu-id="1056c-121">В этом случае установщик обновляет файлы перед удалением старых приложений.</span><span class="sxs-lookup"><span data-stu-id="1056c-121">In this case, the installer updates files before removing the old applications.</span></span> <span data-ttu-id="1056c-122">Во время установки устанавливаются только обновляемые файлы.</span><span class="sxs-lookup"><span data-stu-id="1056c-122">Only the files being updated get installed during the installation.</span></span> <span data-ttu-id="1056c-123">В случае сбоя удаления старого приложения Установщик выполняет откат только удаления старого приложения.</span><span class="sxs-lookup"><span data-stu-id="1056c-123">If the removal of the old application fails, then the installer only rolls back the uninstallation of the old application.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="1056c-124">Сообщения Актиондата</span><span class="sxs-lookup"><span data-stu-id="1056c-124">ActionData Messages</span></span>



| <span data-ttu-id="1056c-125">Поле</span><span class="sxs-lookup"><span data-stu-id="1056c-125">Field</span></span> | <span data-ttu-id="1056c-126">Описание данных действия</span><span class="sxs-lookup"><span data-stu-id="1056c-126">Description of action data</span></span> |
|-------|----------------------------|
| <span data-ttu-id="1056c-127">\[1\]</span><span class="sxs-lookup"><span data-stu-id="1056c-127">\[1\]</span></span> | <span data-ttu-id="1056c-128">Удален продукт.</span><span class="sxs-lookup"><span data-stu-id="1056c-128">Removed product.</span></span>           |



 

## <a name="remarks"></a><span data-ttu-id="1056c-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1056c-129">Remarks</span></span>

<span data-ttu-id="1056c-130">Установщик Windows задает свойство [**упградингпродукткоде**](upgradingproductcode.md) при выполнении этого действия.</span><span class="sxs-lookup"><span data-stu-id="1056c-130">Windows Installer sets the [**UPGRADINGPRODUCTCODE**](upgradingproductcode.md) Property when it runs this action.</span></span>

 

 



