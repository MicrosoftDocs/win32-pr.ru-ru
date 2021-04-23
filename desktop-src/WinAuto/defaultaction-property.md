---
title: DefaultAction, свойство
description: Свойство DefaultAction объекта описывает основной метод обработки объекта из точки зрения пользователя. Свойство DefaultAction объекта должно быть глаголом или короткой глаголовой фразой.
ms.assetid: 8242c0af-b42e-44a4-8807-d6740fa1a24a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73dc032037c331a2022f227cb8e8547dd8bce9d2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328848"
---
# <a name="defaultaction-property"></a><span data-ttu-id="df1b3-104">DefaultAction, свойство</span><span class="sxs-lookup"><span data-stu-id="df1b3-104">DefaultAction Property</span></span>

<span data-ttu-id="df1b3-105">Свойство **DefaultAction** объекта описывает основной метод обработки объекта из точки зрения пользователя.</span><span class="sxs-lookup"><span data-stu-id="df1b3-105">An object's **DefaultAction** property describes the object's primary method of manipulation from the user's viewpoint.</span></span> <span data-ttu-id="df1b3-106">Свойство **DefaultAction** объекта должно быть глаголом или короткой глаголовой фразой.</span><span class="sxs-lookup"><span data-stu-id="df1b3-106">An object's **DefaultAction** property should be a verb or a short verb phrase.</span></span>

<span data-ttu-id="df1b3-107">Свойство **DefaultAction** извлекается путем вызова метода [**IAccessible:: Get \_ аккдефаултактион**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction).</span><span class="sxs-lookup"><span data-stu-id="df1b3-107">The **DefaultAction** property is retrieved by calling [**IAccessible::get\_accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction).</span></span>

<span data-ttu-id="df1b3-108">Чтобы выполнить действие по умолчанию для объекта, клиенты вызывают метод [**IAccessible:: аккдодефаултактион**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction).</span><span class="sxs-lookup"><span data-stu-id="df1b3-108">To perform an object's default action, clients call [**IAccessible::accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction).</span></span>

<span data-ttu-id="df1b3-109">Не все объекты имеют действия по умолчанию, а некоторые объекты имеют действие по умолчанию, связанное со свойством [**значения**](value-property.md) , как в следующих примерах:</span><span class="sxs-lookup"><span data-stu-id="df1b3-109">Not all objects have default actions, and some objects have a default action that is related to its [**Value**](value-property.md) property, such as in the following examples:</span></span>

-   <span data-ttu-id="df1b3-110">Установленный флажок имеет действие по умолчанию "снять флажок" и значение "Проверено".</span><span class="sxs-lookup"><span data-stu-id="df1b3-110">A selected check box has a default action of "Uncheck" and a value of "Checked."</span></span>
-   <span data-ttu-id="df1b3-111">Снятый флажок имеет действие по умолчанию "проверить" и значение "снят флажок".</span><span class="sxs-lookup"><span data-stu-id="df1b3-111">A cleared check box has a default action of "Check" and a value of "Unchecked."</span></span>
-   <span data-ttu-id="df1b3-112">Кнопка «Печать» имеет действие по умолчанию «Press» без значения.</span><span class="sxs-lookup"><span data-stu-id="df1b3-112">A button labeled "Print" has a default action of "Press," with no value.</span></span>
-   <span data-ttu-id="df1b3-113">Элемент управления "статический текст" или элемент управления "поле ввода", отображающий "принтер", не имеет действия по умолчанию, но имеет значение "принтер".</span><span class="sxs-lookup"><span data-stu-id="df1b3-113">A static text control or an edit control that shows "Printer" has no default action, but has a value of "Printer."</span></span>

 

 




