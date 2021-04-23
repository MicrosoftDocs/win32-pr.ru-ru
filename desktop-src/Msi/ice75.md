---
description: ICE75 проверяет, что все пользовательские действия типа 17 (DLL), тип настраиваемого действия 18 (EXE), тип настраиваемого действия 21 (JScript) и настраиваемое действие типа 22 (VBScript) являются упорядоченными после действия Костфинализе.
ms.assetid: 831de042-bea6-42da-90a0-3847bb447414
title: ICE75
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23d708552b3ed2d397e29d37abdf0ceed01093fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347355"
---
# <a name="ice75"></a><span data-ttu-id="1909f-103">ICE75</span><span class="sxs-lookup"><span data-stu-id="1909f-103">ICE75</span></span>

<span data-ttu-id="1909f-104">ICE75 проверяет, что все [пользовательские действия типа 17](custom-action-type-17.md) (DLL), [тип настраиваемого действия 18](custom-action-type-18.md) (exe), [тип настраиваемого действия 21](custom-action-type-21.md) (JScript) и настраиваемое [действие типа 22](custom-action-type-22.md) (VBScript) являются упорядоченными после [действия костфинализе](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="1909f-104">ICE75 verifies that all [Custom Action Type 17](custom-action-type-17.md) (DLL), [Custom Action Type 18](custom-action-type-18.md) (EXE), [Custom Action type 21](custom-action-type-21.md) (JScript), and [Custom Action Type 22](custom-action-type-22.md) (VBScript) custom actions are sequenced after the [CostFinalize action](costfinalize-action.md).</span></span> <span data-ttu-id="1909f-105">Эти типы настраиваемых действий используют в качестве источника установленный файл.</span><span class="sxs-lookup"><span data-stu-id="1909f-105">These types of custom action use an installed file as their source.</span></span> <span data-ttu-id="1909f-106">ICE75 проверяет [таблицу инсталлуисекуенце](installuisequence-table.md), таблицу [инсталлексекутесекуенце](installexecutesequence-table.md), таблицу [админуисекуенце](adminuisequence-table.md)и [таблицу админексекутесекуенце](adminexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="1909f-106">ICE75 checks the [InstallUISequence Table](installuisequence-table.md), [InstallExecuteSequence Table](installexecutesequence-table.md), [AdminUISequence Table](adminuisequence-table.md), and [AdminExecuteSequence Table](adminexecutesequence-table.md).</span></span> <span data-ttu-id="1909f-107">Обратите внимание, что в этих таблицах последовательностей требуется действие Костфинализе.</span><span class="sxs-lookup"><span data-stu-id="1909f-107">Note that the CostFinalize action is required in these sequence tables.</span></span>

## <a name="result"></a><span data-ttu-id="1909f-108">Результат</span><span class="sxs-lookup"><span data-stu-id="1909f-108">Result</span></span>

<span data-ttu-id="1909f-109">ICE75 отправляет сообщение об ошибке, если обнаруживает пользовательское действие, используя установленный файл в качестве исходного файла, который не является последовательным после действия Костфинализе.</span><span class="sxs-lookup"><span data-stu-id="1909f-109">ICE75 posts an error if it finds a custom action using an installed file as a source file that is not sequenced after the CostFinalize action.</span></span>

## <a name="example"></a><span data-ttu-id="1909f-110">Пример</span><span class="sxs-lookup"><span data-stu-id="1909f-110">Example</span></span>

<span data-ttu-id="1909f-111">ICE75 сообщает о следующих ошибках в приведенном примере:</span><span class="sxs-lookup"><span data-stu-id="1909f-111">ICE75 reports the following errors for the example shown:</span></span>

``` syntax
CostFinalize is missing from 'AdminUISequence'. CA_FileExe is a custom
 action whose source is an installed file. It must be sequenced after 
the CostFinalize action.
 
CA_FileDLL is a custom action whose source is an installed file.  It 
must be sequenced after the CostFinalize action in the 
AdminExecuteSequence table
```

<span data-ttu-id="1909f-112">[Таблица CustomAction](customaction-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="1909f-112">[CustomAction Table](customaction-table.md) (partial)</span></span>



| <span data-ttu-id="1909f-113">Действие</span><span class="sxs-lookup"><span data-stu-id="1909f-113">Action</span></span>      | <span data-ttu-id="1909f-114">Тип</span><span class="sxs-lookup"><span data-stu-id="1909f-114">Type</span></span> | <span data-ttu-id="1909f-115">Источник</span><span class="sxs-lookup"><span data-stu-id="1909f-115">Source</span></span>  |
|-------------|------|---------|
| <span data-ttu-id="1909f-116">\_ФИЛИКСЕ CA</span><span class="sxs-lookup"><span data-stu-id="1909f-116">CA\_FileExe</span></span> | <span data-ttu-id="1909f-117">18</span><span class="sxs-lookup"><span data-stu-id="1909f-117">18</span></span>   | <span data-ttu-id="1909f-118">филиксе</span><span class="sxs-lookup"><span data-stu-id="1909f-118">FileExe</span></span> |
| <span data-ttu-id="1909f-119">\_ФИЛЕДЛЛ CA</span><span class="sxs-lookup"><span data-stu-id="1909f-119">CA\_FileDLL</span></span> | <span data-ttu-id="1909f-120">17</span><span class="sxs-lookup"><span data-stu-id="1909f-120">17</span></span>   | <span data-ttu-id="1909f-121">филедлл</span><span class="sxs-lookup"><span data-stu-id="1909f-121">FileDLL</span></span> |



 

<span data-ttu-id="1909f-122">[Таблица админуисекуенце](adminuisequence-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="1909f-122">[AdminUISequence Table](adminuisequence-table.md) (partial)</span></span>



| <span data-ttu-id="1909f-123">Действие</span><span class="sxs-lookup"><span data-stu-id="1909f-123">Action</span></span>      | <span data-ttu-id="1909f-124">Последовательность</span><span class="sxs-lookup"><span data-stu-id="1909f-124">Sequence</span></span> |
|-------------|----------|
| <span data-ttu-id="1909f-125">\_ФИЛИКСЕ CA</span><span class="sxs-lookup"><span data-stu-id="1909f-125">CA\_FileExe</span></span> | <span data-ttu-id="1909f-126">1100</span><span class="sxs-lookup"><span data-stu-id="1909f-126">1100</span></span>     |



 

<span data-ttu-id="1909f-127">[Таблица админексекутесекуенце](adminexecutesequence-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="1909f-127">[AdminExecuteSequence Table](adminexecutesequence-table.md) (partial)</span></span>



| <span data-ttu-id="1909f-128">Действие</span><span class="sxs-lookup"><span data-stu-id="1909f-128">Action</span></span>       | <span data-ttu-id="1909f-129">Последовательность</span><span class="sxs-lookup"><span data-stu-id="1909f-129">Sequence</span></span> |
|--------------|----------|
| <span data-ttu-id="1909f-130">\_ФИЛЕДЛЛ CA</span><span class="sxs-lookup"><span data-stu-id="1909f-130">CA\_FileDLL</span></span>  | <span data-ttu-id="1909f-131">800</span><span class="sxs-lookup"><span data-stu-id="1909f-131">800</span></span>      |
| <span data-ttu-id="1909f-132">костфинализе</span><span class="sxs-lookup"><span data-stu-id="1909f-132">CostFinalize</span></span> | <span data-ttu-id="1909f-133">1000</span><span class="sxs-lookup"><span data-stu-id="1909f-133">1000</span></span>     |



 

<span data-ttu-id="1909f-134">Чтобы устранить ошибки, поочередно Создавайте настраиваемые действия после действия Костфинализе.</span><span class="sxs-lookup"><span data-stu-id="1909f-134">To fix the errors, sequence the custom actions after the CostFinalize action.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1909f-135">См. также</span><span class="sxs-lookup"><span data-stu-id="1909f-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1909f-136">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="1909f-136">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



