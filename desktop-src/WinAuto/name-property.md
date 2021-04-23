---
title: Свойство Name
description: Свойство Name — это строка, используемая клиентами для определения, поиска или объявления объекта для пользователя. Все объекты поддерживают свойство Name.
ms.assetid: 7533955a-9538-4ead-a6ca-f61dd1b4d5c5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e93d8b90190f81179d681600f4b1bfacf4665e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700570"
---
# <a name="name-property"></a><span data-ttu-id="4c984-104">Свойство Name</span><span class="sxs-lookup"><span data-stu-id="4c984-104">Name Property</span></span>

<span data-ttu-id="4c984-105">Свойство **Name** — это строка, используемая клиентами для определения, поиска или объявления объекта для пользователя.</span><span class="sxs-lookup"><span data-stu-id="4c984-105">The **Name** property is a string used by clients to identify, find, or announce an object for the user.</span></span> <span data-ttu-id="4c984-106">Все объекты поддерживают свойство **Name** .</span><span class="sxs-lookup"><span data-stu-id="4c984-106">All objects support the **Name** property.</span></span>

<span data-ttu-id="4c984-107">Например, текст элемента управления "Кнопка" — это имя, а имя для списка или элемента управления "поле ввода" — статический текст, непосредственно предшествующий элементу управления в порядке перехода.</span><span class="sxs-lookup"><span data-stu-id="4c984-107">For example, the text on a button control is its name, while the name for a list box or edit control is the static text that immediately precedes the control in the tabbing order.</span></span> <span data-ttu-id="4c984-108">Даже графические объекты, не отображающие имени, задают текст при запросе свойства **Name** .</span><span class="sxs-lookup"><span data-stu-id="4c984-108">Even graphic objects that do not display a name provide text when queried for the **Name** property.</span></span>

<span data-ttu-id="4c984-109">Свойство **Name** извлекается путем вызова метода [**IAccessible:: Get \_ аккнаме**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname).</span><span class="sxs-lookup"><span data-stu-id="4c984-109">The **Name** property is retrieved by calling [**IAccessible::get\_accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname).</span></span>

## <a name="selecting-names"></a><span data-ttu-id="4c984-110">Выбор имен</span><span class="sxs-lookup"><span data-stu-id="4c984-110">Selecting Names</span></span>

<span data-ttu-id="4c984-111">Имя объекта должно быть интуитивно понятным, чтобы пользователи понимали значение или назначение объекта.</span><span class="sxs-lookup"><span data-stu-id="4c984-111">An object's name should be intuitive so that users understand the object's meaning or purpose.</span></span> <span data-ttu-id="4c984-112">Кроме того, свойство **Name** должно быть уникальным относительно любого родственного объекта в родительском объекте.</span><span class="sxs-lookup"><span data-stu-id="4c984-112">Also, the **Name** property should be unique relative to any sibling objects in the parent.</span></span>

<span data-ttu-id="4c984-113">Переходы между таблицами представляют собой особенно сложные проблемы некоторых пользователей.</span><span class="sxs-lookup"><span data-stu-id="4c984-113">Navigation within tables presents especially difficult problems for some users.</span></span> <span data-ttu-id="4c984-114">Таким образом, разработчики сервера должны сделать имена ячеек таблицы как можно более описательными.</span><span class="sxs-lookup"><span data-stu-id="4c984-114">Therefore, server developers should make table cell names as descriptive as possible.</span></span> <span data-ttu-id="4c984-115">Например, можно создать имя ячейки, объединив имена строки и столбца, которые она занимает, например a1.</span><span class="sxs-lookup"><span data-stu-id="4c984-115">For example, you could create a cell name by combining the names of the row and column it occupies, such as "A1."</span></span> <span data-ttu-id="4c984-116">Однако обычно лучше использовать более описательные имена, такие как «Валентин, Февраль», где «Нэнси» — текущая строка, а «Февраль» — текущий столбец.</span><span class="sxs-lookup"><span data-stu-id="4c984-116">However, it is generally better to use more descriptive names, such as "Nancy, February" where "Nancy" is the current row and "February" is the current column.</span></span>

## <a name="delegating-requests"></a><span data-ttu-id="4c984-117">Делегирование запросов</span><span class="sxs-lookup"><span data-stu-id="4c984-117">Delegating Requests</span></span>

<span data-ttu-id="4c984-118">Если у объекта нет доступа к свойству **Name** , он делегирует запросы родительскому элементу, идентифицируя себя по его идентификатору дочернего элемента.</span><span class="sxs-lookup"><span data-stu-id="4c984-118">If an object does not have access to its **Name** property, it delegates requests to its parent, identifying itself by its child ID.</span></span> <span data-ttu-id="4c984-119">Например, если клиент вызывает свойство **имени** элемента управления Edit, элемент управления "поле ввода" делегирует запрос родительскому элементу, который возвращает значение элемента управления "статический текст", которое помечает элемент управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="4c984-119">For example, if a client calls an edit control's **Name** property, the edit control delegates the query to its parent, which returns the value of the static text control that labels the edit control.</span></span>

 

 




