---
title: Свойство справки
description: Свойство Help предоставляет сведения, которые сообщают пользователю о функции объекта.
ms.assetid: 3df0cc01-cc99-42a1-9d56-591e6e00e53d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b240475d4583826e08fd6ee43b5839bdfb451d4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329723"
---
# <a name="help-property"></a><span data-ttu-id="58804-103">Свойство справки</span><span class="sxs-lookup"><span data-stu-id="58804-103">Help Property</span></span>

<span data-ttu-id="58804-104">Свойство **Help** предоставляет сведения, которые сообщают пользователю о функции объекта.</span><span class="sxs-lookup"><span data-stu-id="58804-104">The **Help** property provides information that tells the user about the function of an object.</span></span>

<span data-ttu-id="58804-105">Свойство **Help** извлекается путем вызова метода [**IAccessible:: Get \_ акчелп**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp).</span><span class="sxs-lookup"><span data-stu-id="58804-105">The **Help** property is retrieved by calling [**IAccessible::get\_accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp).</span></span>

<span data-ttu-id="58804-106">Это свойство содержит сведения в стиле всплывающего окна (в подсказках), которые используются для описания того, что делает объект, или как его использовать.</span><span class="sxs-lookup"><span data-stu-id="58804-106">This property contains balloon-style information (as found in ToolTips) that is used either to describe what the object does or how to use it.</span></span> <span data-ttu-id="58804-107">Например, свойство **Help** для кнопки панели инструментов, показывающей принтер, может предоставить следующий текст: «печатает текущий документ».</span><span class="sxs-lookup"><span data-stu-id="58804-107">For example, the **Help** property for a toolbar button that shows a printer might provide the following text: "Prints the current document."</span></span>

<span data-ttu-id="58804-108">Текст для свойства **справки** не обязательно должен быть уникальным в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="58804-108">The text for the **Help** property does not have to be unique within the user interface.</span></span>

## <a name="when-to-support-the-help-property"></a><span data-ttu-id="58804-109">Когда следует поддерживать свойство Help</span><span class="sxs-lookup"><span data-stu-id="58804-109">When to Support the Help Property</span></span>

<span data-ttu-id="58804-110">Серверы не поддерживают свойство **Help** , если другие свойства предоставляют достаточно сведений о назначении объекта и действиях, выполняемых объектом.</span><span class="sxs-lookup"><span data-stu-id="58804-110">Servers do not support the **Help** property if other properties provide sufficient information about the object's purpose and the actions the object performs.</span></span> <span data-ttu-id="58804-111">Доступные объекты, которые предоставляют элементы управления, предоставляемые системой, не поддерживают свойство **Help** .</span><span class="sxs-lookup"><span data-stu-id="58804-111">Accessible objects that expose system-provided controls do not support the **Help** property.</span></span>

 

 




