---
description: ICE13 проверяет, появляются ли диалоговые окна в таблицах последовательностей в таблицах Админуисекуенце или Инсталлуисекуенце. Диалоговые окна не должны присутствовать в таблицах Инсталлексекутесекуенце, Админексекутесекуенце или Адвтексекутесекуенце.
ms.assetid: 51542a8f-2fb6-4021-b52d-6f7a2b0294d6
title: ICE13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fff440217ccffe41d5e4036f4ea0d03d1eabb0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998800"
---
# <a name="ice13"></a><span data-ttu-id="773ee-104">ICE13</span><span class="sxs-lookup"><span data-stu-id="773ee-104">ICE13</span></span>

<span data-ttu-id="773ee-105">ICE13 проверяет, появляются ли диалоговые окна в таблицах последовательностей в таблицах [админуисекуенце](adminuisequence-table.md)или [инсталлуисекуенце](installuisequence-table.md) .</span><span class="sxs-lookup"><span data-stu-id="773ee-105">ICE13 validates that dialogs in sequence tables appear in the [AdminUISequence](adminuisequence-table.md), or [InstallUISequence](installuisequence-table.md) tables.</span></span> <span data-ttu-id="773ee-106">Диалоговые окна не должны присутствовать в таблицах [инсталлексекутесекуенце](installexecutesequence-table.md), [админексекутесекуенце](adminexecutesequence-table.md)или [адвтексекутесекуенце](advtexecutesequence-table.md) .</span><span class="sxs-lookup"><span data-stu-id="773ee-106">Dialogs must not be listed in the [InstallExecuteSequence](installexecutesequence-table.md), [AdminExecuteSequence](adminexecutesequence-table.md), or [AdvtExecuteSequence](advtexecutesequence-table.md) tables.</span></span>

## <a name="result"></a><span data-ttu-id="773ee-107">Результат</span><span class="sxs-lookup"><span data-stu-id="773ee-107">Result</span></span>

<span data-ttu-id="773ee-108">ICE13 отправляет сообщение об ошибке, если диалоговое окно появляется в таблице выполнения последовательности.</span><span class="sxs-lookup"><span data-stu-id="773ee-108">ICE13 posts an error message if a dialog appears in an execute sequence table.</span></span>

## <a name="example"></a><span data-ttu-id="773ee-109">Пример</span><span class="sxs-lookup"><span data-stu-id="773ee-109">Example</span></span>

<span data-ttu-id="773ee-110">В следующем примере ICE13 отправляет сообщение об ошибке с информацией о том, что "Велкомедиалог" не может быть указан в таблице "Инсталлексекутесекуенце".</span><span class="sxs-lookup"><span data-stu-id="773ee-110">For the following example, ICE13 posts an error message stating that the 'WelcomeDialog' cannot be listed in the 'InstallExecuteSequence' table.</span></span>

<span data-ttu-id="773ee-111">[Таблица инсталлексекутесекуенце](installexecutesequence-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="773ee-111">[InstallExecuteSequence Table](installexecutesequence-table.md) (partial)</span></span>



| <span data-ttu-id="773ee-112">Действие</span><span class="sxs-lookup"><span data-stu-id="773ee-112">Action</span></span>          |
|-----------------|
| <span data-ttu-id="773ee-113">Функции InstallFinalize</span><span class="sxs-lookup"><span data-stu-id="773ee-113">InstallFinalize</span></span> |
| <span data-ttu-id="773ee-114">костфинализе</span><span class="sxs-lookup"><span data-stu-id="773ee-114">CostFinalize</span></span>    |
| <span data-ttu-id="773ee-115">велкомедиалог</span><span class="sxs-lookup"><span data-stu-id="773ee-115">WelcomeDialog</span></span>   |



 

<span data-ttu-id="773ee-116">[Таблица инсталлуисекуенце](installuisequence-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="773ee-116">[InstallUISequence Table](installuisequence-table.md) (partial)</span></span>



| <span data-ttu-id="773ee-117">Действие</span><span class="sxs-lookup"><span data-stu-id="773ee-117">Action</span></span>         |
|----------------|
| <span data-ttu-id="773ee-118">костфинализе</span><span class="sxs-lookup"><span data-stu-id="773ee-118">CostFinalize</span></span>   |
| <span data-ttu-id="773ee-119">костинитиализе</span><span class="sxs-lookup"><span data-stu-id="773ee-119">CostInitialize</span></span> |
| <span data-ttu-id="773ee-120">бровседиалог</span><span class="sxs-lookup"><span data-stu-id="773ee-120">BrowseDialog</span></span>   |



 

<span data-ttu-id="773ee-121">[Таблица диалоговых окон](dialog-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="773ee-121">[Dialog Table](dialog-table.md) (partial)</span></span>



| <span data-ttu-id="773ee-122">Диалог</span><span class="sxs-lookup"><span data-stu-id="773ee-122">Dialog</span></span>        |
|---------------|
| <span data-ttu-id="773ee-123">бровседиалог</span><span class="sxs-lookup"><span data-stu-id="773ee-123">BrowseDialog</span></span>  |
| <span data-ttu-id="773ee-124">велкомедиалог</span><span class="sxs-lookup"><span data-stu-id="773ee-124">WelcomeDialog</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="773ee-125">См. также</span><span class="sxs-lookup"><span data-stu-id="773ee-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="773ee-126">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="773ee-126">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



