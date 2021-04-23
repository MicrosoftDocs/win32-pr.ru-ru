---
description: ICE26 проверяет таблицы последовательности в базе данных установщик Windows.
ms.assetid: 7ea47452-3147-4d39-961d-a10eca8328c9
title: ICE26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d7b110d0b15b37441170980d0fd3e96e2eb00d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910911"
---
# <a name="ice26"></a><span data-ttu-id="c3edd-103">ICE26</span><span class="sxs-lookup"><span data-stu-id="c3edd-103">ICE26</span></span>

<span data-ttu-id="c3edd-104">ICE26 проверяет, что каждая из следующих [*таблиц последовательности*](s-gly.md) содержит действия, необходимые для таблицы, и не содержит никаких действий, запрещенных в таблице.</span><span class="sxs-lookup"><span data-stu-id="c3edd-104">ICE26 validates that each of the following [*sequence tables*](s-gly.md) contain the actions that are required by the table and does not contain any actions disallowed in the table:</span></span>

-   [<span data-ttu-id="c3edd-105">Таблица Админуисекуенце</span><span class="sxs-lookup"><span data-stu-id="c3edd-105">AdminUISequence table</span></span>](adminuisequence-table.md)
-   [<span data-ttu-id="c3edd-106">Таблица Админексекутесекуенце</span><span class="sxs-lookup"><span data-stu-id="c3edd-106">AdminExecuteSequence table</span></span>](adminexecutesequence-table.md)
-   [<span data-ttu-id="c3edd-107">Таблица Инсталлуисекуенце</span><span class="sxs-lookup"><span data-stu-id="c3edd-107">InstallUISequence table</span></span>](installuisequence-table.md)
-   [<span data-ttu-id="c3edd-108">Таблица Инсталлексекутесекуенце</span><span class="sxs-lookup"><span data-stu-id="c3edd-108">InstallExecuteSequence table</span></span>](installexecutesequence-table.md)

## <a name="result"></a><span data-ttu-id="c3edd-109">Результат</span><span class="sxs-lookup"><span data-stu-id="c3edd-109">Result</span></span>

<span data-ttu-id="c3edd-110">ICE26 отправляет сообщение об ошибке, если у пакета установки есть таблица последовательности, в которой отсутствует необходимое действие или содержится действие, запрещенное для таблицы.</span><span class="sxs-lookup"><span data-stu-id="c3edd-110">ICE26 posts an error message if the installation package has a sequence table that lacks a required action or that contains an action that is disallowed for the table.</span></span>

## <a name="example"></a><span data-ttu-id="c3edd-111">Пример</span><span class="sxs-lookup"><span data-stu-id="c3edd-111">Example</span></span>



| <span data-ttu-id="c3edd-112">ICE26, ошибка</span><span class="sxs-lookup"><span data-stu-id="c3edd-112">ICE26 error</span></span>                                                                   | <span data-ttu-id="c3edd-113">Описание</span><span class="sxs-lookup"><span data-stu-id="c3edd-113">Description</span></span>                                                                                                                                                                    |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3edd-114">Действие: "Action1 превышают" требуется в таблице последовательностей Инсталлексекутесекуенце.</span><span class="sxs-lookup"><span data-stu-id="c3edd-114">Action: 'Action1' is required in the InstallExecuteSequence Sequence table.</span></span>   | <span data-ttu-id="c3edd-115">В указанной таблице последовательностей отсутствует требуемое действие.</span><span class="sxs-lookup"><span data-stu-id="c3edd-115">A required action is missing from the indicated sequence table.</span></span> <span data-ttu-id="c3edd-116">См. template.msi или предлагаемые таблицы последовательностей в разделе [Использование таблицы последовательностей](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="c3edd-116">See the template.msi or the suggested sequence tables in [Using a Sequence Table](using-a-sequence-table.md).</span></span> |
| <span data-ttu-id="c3edd-117">Действие: "Action2" запрещено в таблице последовательностей Инсталлексекутесекуенце.</span><span class="sxs-lookup"><span data-stu-id="c3edd-117">Action: 'Action2' is prohibited in the InstallExecuteSequence Sequence table.</span></span> | <span data-ttu-id="c3edd-118">Это действие не может находиться в указанной таблице последовательностей.</span><span class="sxs-lookup"><span data-stu-id="c3edd-118">This action cannot be in the indicated sequence table.</span></span> <span data-ttu-id="c3edd-119">Удалите это действие из таблицы последовательности.</span><span class="sxs-lookup"><span data-stu-id="c3edd-119">Remove this action from the sequence table.</span></span>                                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="c3edd-120">См. также</span><span class="sxs-lookup"><span data-stu-id="c3edd-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c3edd-121">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="c3edd-121">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



