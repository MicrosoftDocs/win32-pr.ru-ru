---
title: Кэйбоардшорткут, свойство
description: Свойство Кэйбоардшорткут описывает сочетание клавиш или клавиш, которое активирует указанный доступный объект.
ms.assetid: 42587468-f069-4ef1-868e-ac6a285e1715
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 002c925151f3f1acc136190d7807d7bc814d30b9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104253300"
---
# <a name="keyboardshortcut-property"></a><span data-ttu-id="8455b-103">Кэйбоардшорткут, свойство</span><span class="sxs-lookup"><span data-stu-id="8455b-103">KeyboardShortcut Property</span></span>

<span data-ttu-id="8455b-104">Свойство **кэйбоардшорткут** описывает сочетание клавиш или клавиш, которое активирует указанный доступный объект.</span><span class="sxs-lookup"><span data-stu-id="8455b-104">The **KeyboardShortcut** property describes a key or key combination that activates a specified accessible object.</span></span>

<span data-ttu-id="8455b-105">Свойство **кэйбоардшорткут** извлекается путем вызова метода [**IAccessible:: Get \_ акккэйбоардшорткут**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut).</span><span class="sxs-lookup"><span data-stu-id="8455b-105">The **KeyboardShortcut** property is retrieved by calling [**IAccessible::get\_accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut).</span></span>

<span data-ttu-id="8455b-106">Извлеченная строка описывает *сочетание* клавиш (также называемое *ускорителем клавиатуры*) или *клавишу доступа* (также называемое *назначенной* клавишей).</span><span class="sxs-lookup"><span data-stu-id="8455b-106">The retrieved string describes a *shortcut key* (also called a *keyboard accelerator*) or an *access key* (also called a *mnemonic*).</span></span> <span data-ttu-id="8455b-107">Клавиша доступа — это подчеркнутый символ в тексте меню, пункт меню или метка элемента управления, например кнопка «Отправить».</span><span class="sxs-lookup"><span data-stu-id="8455b-107">An access key is an underlined character in the text of a menu, menu item, or label of a control such as a push button.</span></span>

<span data-ttu-id="8455b-108">Извлеченная строка должна содержать имя ключа, а также ключ или ключи модификатора.</span><span class="sxs-lookup"><span data-stu-id="8455b-108">The retrieved string must contain the name of the key along with the modifier key or keys.</span></span> <span data-ttu-id="8455b-109">Строка должна быть в следующем формате, чтобы клиенты могли легко его проанализировать: \[ \[ Клавиша модификатора.. \] + \[ . \] + \] имя ключа.</span><span class="sxs-lookup"><span data-stu-id="8455b-109">The string must be in the following format so that clients can easily parse it: \[\[modifier key\]+\[...\]+\] key name.</span></span>

<span data-ttu-id="8455b-110">Примеры: ALT + F, CTRL + ALT + 4, WIN + F1, CTRL + ALT + SHIFT + Backspace или просто Backspace.</span><span class="sxs-lookup"><span data-stu-id="8455b-110">Examples include ALT+F, CTRL+ALT+4, WIN+F1, CTRL+ALT+SHIFT+BACKSPACE, or simply BACKSPACE.</span></span>

<span data-ttu-id="8455b-111">В следующей таблице перечислены ключи модификаторов.</span><span class="sxs-lookup"><span data-stu-id="8455b-111">The following table lists modifier keys.</span></span>



| <span data-ttu-id="8455b-112">Клавиша-модификатор</span><span class="sxs-lookup"><span data-stu-id="8455b-112">Modifier key</span></span> | <span data-ttu-id="8455b-113">Описание</span><span class="sxs-lookup"><span data-stu-id="8455b-113">Description</span></span>                        |
|--------------|------------------------------------|
| <span data-ttu-id="8455b-114">ALT</span><span class="sxs-lookup"><span data-stu-id="8455b-114">ALT</span></span>          | <span data-ttu-id="8455b-115">Альтернативный ключ модификатора</span><span class="sxs-lookup"><span data-stu-id="8455b-115">Alternate modifier key</span></span>             |
| <span data-ttu-id="8455b-116">CTRL</span><span class="sxs-lookup"><span data-stu-id="8455b-116">CTRL</span></span>         | <span data-ttu-id="8455b-117">Клавиша модификатора Control</span><span class="sxs-lookup"><span data-stu-id="8455b-117">Control modifier key</span></span>               |
| <span data-ttu-id="8455b-118">МЕСТИ</span><span class="sxs-lookup"><span data-stu-id="8455b-118">SHIFT</span></span>        | <span data-ttu-id="8455b-119">Клавиша модификатора Shift</span><span class="sxs-lookup"><span data-stu-id="8455b-119">Shift modifier key</span></span>                 |
| <span data-ttu-id="8455b-120">WIN</span><span class="sxs-lookup"><span data-stu-id="8455b-120">WIN</span></span>          | <span data-ttu-id="8455b-121">Клавиша Windows</span><span class="sxs-lookup"><span data-stu-id="8455b-121">Windows logo key</span></span>                   |
| <span data-ttu-id="8455b-122">FN</span><span class="sxs-lookup"><span data-stu-id="8455b-122">FN</span></span>           | <span data-ttu-id="8455b-123">Функциональная клавиша на переносных компьютерах</span><span class="sxs-lookup"><span data-stu-id="8455b-123">Function key on portable computers</span></span> |



 

<span data-ttu-id="8455b-124">Не локализовать строки сочетаний клавиш.</span><span class="sxs-lookup"><span data-stu-id="8455b-124">Do not localize keyboard shortcut strings.</span></span>

## <a name="handling-objects-that-have-both-key-types"></a><span data-ttu-id="8455b-125">Обработка объектов, имеющих оба типа ключей</span><span class="sxs-lookup"><span data-stu-id="8455b-125">Handling Objects That Have Both Key Types</span></span>

<span data-ttu-id="8455b-126">Если у объекта есть и сочетание клавиш, и ключ доступа, свойство **кэйбоардшорткут** Возвращает ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="8455b-126">If an object has both a shortcut key and an access key, the **KeyboardShortcut** property returns the access key.</span></span> <span data-ttu-id="8455b-127">Клавиша доступа — это тот, который пользователь нажмет, когда объект или родительский объект объекта имеет фокус клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="8455b-127">The access key is the one a user would press when the object or the object's parent has the keyboard focus.</span></span> <span data-ttu-id="8455b-128">Например, элемент меню **Печать** может содержать сочетание клавиш (Ctrl + P) и клавишу доступа (P).</span><span class="sxs-lookup"><span data-stu-id="8455b-128">For example, the **Print** menu item might have both a shortcut key (CTRL+P) and an access key (P).</span></span> <span data-ttu-id="8455b-129">Если пользователь нажимает клавишу CTRL + P, когда меню активно, ничего не происходит.</span><span class="sxs-lookup"><span data-stu-id="8455b-129">If a user presses CTRL+P while the menu is active, nothing happens.</span></span> <span data-ttu-id="8455b-130">Но если пользователь нажимает клавишу P, когда меню активно, оно вызывает диалоговое окно **Печать** приложения.</span><span class="sxs-lookup"><span data-stu-id="8455b-130">But if a user presses P while the menu is active, it invokes the application's **Print** dialog box.</span></span> <span data-ttu-id="8455b-131">В этом случае свойство **кэйбоардшорткут** имеет значение «P» для отражения того, что пользователь должен нажать, когда меню имеет фокус клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="8455b-131">In this case, the **KeyboardShortcut** property is "P" to reflect what the user must press when the menu has the keyboard focus.</span></span>

 

 




