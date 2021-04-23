---
description: ICE28 обычно используется для проверки того, что действие Форцеребут размещается до или после, и никогда в рамках определенной группы действий в таблицах последовательности действий. Чтобы определить действия, составляющие эту группу, см. раздел действие Форцеребут.
ms.assetid: 746d907a-33e1-479a-bcb0-93e7fd5dd975
title: ICE28
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc65878bdc3db4f9b79ba95b4a170b694a4728ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808747"
---
# <a name="ice28"></a><span data-ttu-id="931ff-104">ICE28</span><span class="sxs-lookup"><span data-stu-id="931ff-104">ICE28</span></span>

<span data-ttu-id="931ff-105">ICE28 обычно используется для проверки того, что действие Форцеребут размещается до или после, и никогда в рамках определенной группы действий в таблицах последовательности действий.</span><span class="sxs-lookup"><span data-stu-id="931ff-105">ICE28 is commonly used to validate that the ForceReboot action is placed before or after, and never within, a specific group of actions in the action sequence tables.</span></span> <span data-ttu-id="931ff-106">Чтобы определить действия, составляющие эту группу, см. раздел [действие форцеребут](forcereboot-action.md) .</span><span class="sxs-lookup"><span data-stu-id="931ff-106">See the [ForceReboot action](forcereboot-action.md) topic to determine the actions that comprise this group.</span></span>

<span data-ttu-id="931ff-107">ICE28 проверяет действия в следующих таблицах последовательностей:</span><span class="sxs-lookup"><span data-stu-id="931ff-107">ICE28 validates actions in the following sequence tables:</span></span>

[<span data-ttu-id="931ff-108">Таблица Админуисекуенце</span><span class="sxs-lookup"><span data-stu-id="931ff-108">AdminUISequence table</span></span>](adminuisequence-table.md)

[<span data-ttu-id="931ff-109">Таблица Админексекутесекуенце</span><span class="sxs-lookup"><span data-stu-id="931ff-109">AdminExecuteSequence table</span></span>](adminexecutesequence-table.md)

[<span data-ttu-id="931ff-110">Таблица Инсталлуисекуенце</span><span class="sxs-lookup"><span data-stu-id="931ff-110">InstallUISequence table</span></span>](installuisequence-table.md)

[<span data-ttu-id="931ff-111">Таблица Инсталлексекутесекуенце</span><span class="sxs-lookup"><span data-stu-id="931ff-111">InstallExecuteSequence table</span></span>](installexecutesequence-table.md)

## <a name="result"></a><span data-ttu-id="931ff-112">Результат</span><span class="sxs-lookup"><span data-stu-id="931ff-112">Result</span></span>

<span data-ttu-id="931ff-113">ICE28 отправляет сообщение об ошибке, если Форцеребут помещается в последовательность в указанной группе действий.</span><span class="sxs-lookup"><span data-stu-id="931ff-113">ICE28 posts an error message if ForceReboot is sequenced within the specified action group.</span></span>

## <a name="example"></a><span data-ttu-id="931ff-114">Пример</span><span class="sxs-lookup"><span data-stu-id="931ff-114">Example</span></span>

<span data-ttu-id="931ff-115">В приведенном примере ICE28 отправляет следующее сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="931ff-115">For the example shown, ICE28 posts the following error message:</span></span>

``` syntax
Action: 'ForceReboot' of table InstallExecuteSequence is not permitted in the range 5 to 15 because it cannot separate a set of actions contained in this range.
```

[<span data-ttu-id="931ff-116">Таблица Инсталлексекутесекуенце</span><span class="sxs-lookup"><span data-stu-id="931ff-116">InstallExecuteSequence Table</span></span>](installexecutesequence-table.md)



| <span data-ttu-id="931ff-117">Действие</span><span class="sxs-lookup"><span data-stu-id="931ff-117">Action</span></span>             | <span data-ttu-id="931ff-118">Последовательность</span><span class="sxs-lookup"><span data-stu-id="931ff-118">Sequence</span></span> |
|--------------------|----------|
| <span data-ttu-id="931ff-119">форцеребут</span><span class="sxs-lookup"><span data-stu-id="931ff-119">ForceReboot</span></span>        | <span data-ttu-id="931ff-120">10</span><span class="sxs-lookup"><span data-stu-id="931ff-120">10</span></span>       |
| <span data-ttu-id="931ff-121">регистермимеинфо</span><span class="sxs-lookup"><span data-stu-id="931ff-121">RegisterMIMEInfo</span></span>   |   <span data-ttu-id="931ff-122">5</span><span class="sxs-lookup"><span data-stu-id="931ff-122">5</span></span>      |
| <span data-ttu-id="931ff-123">регистерпрогидинфо</span><span class="sxs-lookup"><span data-stu-id="931ff-123">RegisterProgIdInfo</span></span> | <span data-ttu-id="931ff-124">15</span><span class="sxs-lookup"><span data-stu-id="931ff-124">15</span></span>       |



 

<span data-ttu-id="931ff-125">Порядковый номер 10, присвоенный Форцеребут разрывам, приводит к возникновению ошибки, так как он находится между порядковыми номерами Регистермимеинфо и Регистерпрогидинфо.</span><span class="sxs-lookup"><span data-stu-id="931ff-125">The sequence number of 10 given to ForceReboot breaks generates the error, because it comes between the sequence numbers of RegisterMIMEInfo and RegisterProgIdInfo.</span></span>

## <a name="related-topics"></a><span data-ttu-id="931ff-126">См. также</span><span class="sxs-lookup"><span data-stu-id="931ff-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="931ff-127">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="931ff-127">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



