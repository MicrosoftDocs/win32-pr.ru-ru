---
description: Значения реестра должны быть заданы для команд, чтобы обрабатывать ситуации, когда пользователь может выбрать один элемент, несколько элементов или выбрать из элемента. Команда требует наличия отдельных значений реестра для каждой из трех ситуаций, поддерживаемых командой.
ms.assetid: B6D4C879-3E52-4010-9B2E-3BCD81BB6C93
title: Как применить модель выбора глагола
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 724cd1c15b18657e27f9cfc53e9362685c6e2e7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985448"
---
# <a name="how-to-employ-the-verb-selection-model"></a><span data-ttu-id="c9c66-104">Как применить модель выбора глагола</span><span class="sxs-lookup"><span data-stu-id="c9c66-104">How to Employ the Verb Selection Model</span></span>

<span data-ttu-id="c9c66-105">Значения реестра должны быть заданы для команд, чтобы обрабатывать ситуации, когда пользователь может выбрать один элемент, несколько элементов или выбрать из элемента.</span><span class="sxs-lookup"><span data-stu-id="c9c66-105">Registry values must be set for verbs to handle situations where a user can select a single item, multiple items, or a selection from an item.</span></span> <span data-ttu-id="c9c66-106">Команда требует наличия отдельных значений реестра для каждой из трех ситуаций, поддерживаемых командой.</span><span class="sxs-lookup"><span data-stu-id="c9c66-106">A verb requires separate registry values for each of these three situations that the verb supports.</span></span>

## <a name="instructions"></a><span data-ttu-id="c9c66-107">Инструкции</span><span class="sxs-lookup"><span data-stu-id="c9c66-107">Instructions</span></span>


<span data-ttu-id="c9c66-108">Укажите значение Мултиселектмодел для всех команд.</span><span class="sxs-lookup"><span data-stu-id="c9c66-108">Specify the MultiSelectModel value for all verbs.</span></span> <span data-ttu-id="c9c66-109">Если значение Мултиселектмодел не указано, оно выводится из выбранного типа реализации глагола.</span><span class="sxs-lookup"><span data-stu-id="c9c66-109">If the MultiSelectModel value is not specified, it is inferred from the type of verb implementation you have chosen.</span></span> <span data-ttu-id="c9c66-110">Для **методов,** основанных на com (например, Дроптаржет и **ExecuteCommand),** предполагается, а для других методов —.</span><span class="sxs-lookup"><span data-stu-id="c9c66-110">For COM-based methods (such as DropTarget and ExecuteCommand) **Player** is assumed, and for the other methods **Document** is assumed.</span></span>

<span data-ttu-id="c9c66-111">Ниже приведены возможные значения для модели выбора команд.</span><span class="sxs-lookup"><span data-stu-id="c9c66-111">The possible values for the verb selection model are as follows:</span></span>

1.  <span data-ttu-id="c9c66-112">Укажите **одну** для команд, поддерживающих только один выбор.</span><span class="sxs-lookup"><span data-stu-id="c9c66-112">Specify **Single** for verbs that support only a single selection.</span></span>
2.  <span data-ttu-id="c9c66-113">Укажите **проигрыватель** для команд, которые поддерживают любое количество элементов.</span><span class="sxs-lookup"><span data-stu-id="c9c66-113">Specify **Player** for verbs that support any number of items.</span></span>
3.  <span data-ttu-id="c9c66-114">Укажите **документ** для команд, которые создают окно верхнего уровня для каждого элемента.</span><span class="sxs-lookup"><span data-stu-id="c9c66-114">Specify **Document** for verbs that create a top-level window for each item.</span></span> <span data-ttu-id="c9c66-115">Это ограничивает количество активированных элементов и помогает избежать переполнения системных ресурсов, если пользователь открывает слишком много окон.</span><span class="sxs-lookup"><span data-stu-id="c9c66-115">Doing so limits the number of items that are activated and helps avoid running out of system resources if the user opens too many windows.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9c66-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="c9c66-116">Remarks</span></span>

<span data-ttu-id="c9c66-117">Если выбранное число элементов не соответствует модели выбора глагола или превышает ограничения по умолчанию, описанные в следующей таблице, команда не отображается.</span><span class="sxs-lookup"><span data-stu-id="c9c66-117">When the number of items selected does not match the verb selection model or is greater than the default limits outlined in the following table, the verb fails to appear.</span></span>



| <span data-ttu-id="c9c66-118">Тип реализации глагола</span><span class="sxs-lookup"><span data-stu-id="c9c66-118">Type of verb implementation</span></span> | <span data-ttu-id="c9c66-119">Документ</span><span class="sxs-lookup"><span data-stu-id="c9c66-119">Document</span></span> | <span data-ttu-id="c9c66-120">Проигрыватель</span><span class="sxs-lookup"><span data-stu-id="c9c66-120">Player</span></span>    |
|-----------------------------|----------|-----------|
| <span data-ttu-id="c9c66-121">Прежняя версия</span><span class="sxs-lookup"><span data-stu-id="c9c66-121">Legacy</span></span>                      | <span data-ttu-id="c9c66-122">15 элементов</span><span class="sxs-lookup"><span data-stu-id="c9c66-122">15 items</span></span> | <span data-ttu-id="c9c66-123">100 элементов</span><span class="sxs-lookup"><span data-stu-id="c9c66-123">100 items</span></span> |
| <span data-ttu-id="c9c66-124">COM</span><span class="sxs-lookup"><span data-stu-id="c9c66-124">COM</span></span>                         | <span data-ttu-id="c9c66-125">15 элементов</span><span class="sxs-lookup"><span data-stu-id="c9c66-125">15 items</span></span> | <span data-ttu-id="c9c66-126">Без ограничений</span><span class="sxs-lookup"><span data-stu-id="c9c66-126">No limit</span></span>  |



 

<span data-ttu-id="c9c66-127">Ниже приведены примеры записей реестра, в которых используется значение Мултиселектмодел.</span><span class="sxs-lookup"><span data-stu-id="c9c66-127">The following are example registry entries that use the MultiSelectModel value.</span></span>

```
HKEY_CLASSES_ROOT
   Folder
      shell
         open
             = MultiSelectModel = Document
```

```
HKEY_CLASSES_ROOT
   ProgID
      shell
         verb
             = MultiSelectModel = Single | Document | Player
```

 

 



