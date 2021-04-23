---
description: Логическое значение свойства, которое было задано, равно true.
ms.assetid: aee818aa-912d-4e59-b061-61cd35993593
title: Использование свойств в условных инструкциях
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73596c465c4bcc0864caf8512e97c92d68f05fc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673301"
---
# <a name="using-properties-in-conditional-statements"></a><span data-ttu-id="65bdc-103">Использование свойств в условных инструкциях</span><span class="sxs-lookup"><span data-stu-id="65bdc-103">Using Properties in Conditional Statements</span></span>

<span data-ttu-id="65bdc-104">Логическое значение свойства, которое было задано, равно true.</span><span class="sxs-lookup"><span data-stu-id="65bdc-104">The logical value of a property that has been set is True.</span></span> <span data-ttu-id="65bdc-105">Чтобы определить, задано ли свойство без фактического получения его значения, проверьте логическое выражение "MyProperty" или "not MyProperty".</span><span class="sxs-lookup"><span data-stu-id="65bdc-105">To determine whether a property is set without actually getting its value, test the logical expression "MyProperty" or "Not MyProperty".</span></span> <span data-ttu-id="65bdc-106">Если задано свойство MyProperty, первое значение вычисляется как true, а второе — как false.</span><span class="sxs-lookup"><span data-stu-id="65bdc-106">When the property MyProperty is set, the former evaluates as True and the latter as False.</span></span>

<span data-ttu-id="65bdc-107">Одно или несколько свойств можно сочетать с операторами для формирования логических выражений, используемых в условных инструкциях.</span><span class="sxs-lookup"><span data-stu-id="65bdc-107">One or more properties can be combined with operators to form logical expressions used in a conditional statements.</span></span> <span data-ttu-id="65bdc-108">Дополнительные сведения об операторах, которые можно использовать в условных инструкциях, см. в разделе [Синтаксис условных](conditional-statement-syntax.md)инструкций.</span><span class="sxs-lookup"><span data-stu-id="65bdc-108">For more information about the operators that can be used in conditional statements, see [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

<span data-ttu-id="65bdc-109">Условный оператор, использующий свойства, может быть введен в столбец Условие [таблицы условие](condition-table.md) для изменения состояния выбора любой записи в [таблице Feature](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="65bdc-109">A conditional statement using properties can be entered into the Condition column of the [Condition table](condition-table.md) to modify the selection state of any entry in the [Feature table](feature-table.md).</span></span>

<span data-ttu-id="65bdc-110">Условные операторы с одним или несколькими свойствами обычно используются в столбце Условие таблиц базы данных.</span><span class="sxs-lookup"><span data-stu-id="65bdc-110">Conditional statements with one or more properties are commonly used in the Condition column of database tables.</span></span>

<span data-ttu-id="65bdc-111">В следующих таблицах есть столбец для условных выражений:</span><span class="sxs-lookup"><span data-stu-id="65bdc-111">The following tables each have a column for conditional expressions:</span></span>

-   [<span data-ttu-id="65bdc-112">Таблица условий</span><span class="sxs-lookup"><span data-stu-id="65bdc-112">Condition table</span></span>](condition-table.md)
-   [<span data-ttu-id="65bdc-113">Таблица таблице ControlEvent событие</span><span class="sxs-lookup"><span data-stu-id="65bdc-113">ControlEvent table</span></span>](controlevent-table.md)
-   [<span data-ttu-id="65bdc-114">Таблица Лаунчкондитион</span><span class="sxs-lookup"><span data-stu-id="65bdc-114">LaunchCondition table</span></span>](launchcondition-table.md)
-   [<span data-ttu-id="65bdc-115">Таблица Инсталлуисекуенце</span><span class="sxs-lookup"><span data-stu-id="65bdc-115">InstallUISequence table</span></span>](installuisequence-table.md)
-   [<span data-ttu-id="65bdc-116">Таблица Инсталлексекутесекуенце</span><span class="sxs-lookup"><span data-stu-id="65bdc-116">InstallExecuteSequence table</span></span>](installexecutesequence-table.md)
-   [<span data-ttu-id="65bdc-117">Таблица Таблица controlcondition</span><span class="sxs-lookup"><span data-stu-id="65bdc-117">ControlCondition table</span></span>](controlcondition-table.md)
-   [<span data-ttu-id="65bdc-118">Таблица Админексекутесекуенце</span><span class="sxs-lookup"><span data-stu-id="65bdc-118">AdminExecuteSequence table</span></span>](adminexecutesequence-table.md)
-   [<span data-ttu-id="65bdc-119">Таблица Адвтексекутесекуенце</span><span class="sxs-lookup"><span data-stu-id="65bdc-119">AdvtExecuteSequence table</span></span>](advtexecutesequence-table.md)
-   [<span data-ttu-id="65bdc-120">Таблица Админуисекуенце</span><span class="sxs-lookup"><span data-stu-id="65bdc-120">AdminUISequence table</span></span>](adminuisequence-table.md)

<span data-ttu-id="65bdc-121">Обратите внимание, что шесть таблиц последовательности действий содержат поля для условия.</span><span class="sxs-lookup"><span data-stu-id="65bdc-121">Note that the six action sequence tables have fields for a condition.</span></span> <span data-ttu-id="65bdc-122">Если условное выражение в этом поле имеет значение false, установщик пропускает это действие.</span><span class="sxs-lookup"><span data-stu-id="65bdc-122">If the conditional expression in this field evaluates to False, the installer skips that action.</span></span>

<span data-ttu-id="65bdc-123">Если задать [свойство Private](private-properties.md) в последовательности пользовательского интерфейса путем создания настраиваемого действия в одной из таблиц последовательности пользовательского интерфейса, это свойство не будет задано в последовательности выполнения.</span><span class="sxs-lookup"><span data-stu-id="65bdc-123">If you set a [private property](private-properties.md) in the UI sequence by authoring a custom action in one of the user interface sequence tables, that property is not set in the execution sequence.</span></span> <span data-ttu-id="65bdc-124">Чтобы задать свойство в последовательности выполнения, необходимо также добавить пользовательское действие в таблицу последовательности выполнения.</span><span class="sxs-lookup"><span data-stu-id="65bdc-124">To set the property in the execution sequence you must also put a custom action in an execution sequence table.</span></span> <span data-ttu-id="65bdc-125">Кроме того, можно сделать свойство [общедоступным](public-properties.md) и включить его в свойство [**секурекустомпропертиес**](securecustomproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="65bdc-125">Alternatively, you can make the property a [public property](public-properties.md) and include it in the [**SecureCustomProperties**](securecustomproperties.md) property.</span></span>

<span data-ttu-id="65bdc-126">Дополнительные сведения см. в разделе [Использование таблицы последовательностей](using-a-sequence-table.md) или [свойства](using-properties.md).</span><span class="sxs-lookup"><span data-stu-id="65bdc-126">For more information, see [Using a Sequence Table](using-a-sequence-table.md) or [Using Properties](using-properties.md).</span></span>

 

 



