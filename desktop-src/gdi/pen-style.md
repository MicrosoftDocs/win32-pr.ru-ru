---
description: Атрибут style указывает шаблон линии, который отображается при использовании определенного косметическиго или геометрического пера. Существует восемь стандартных стилей пера. На следующем рисунке показаны семь из этих стилей, определяемых системой.
ms.assetid: a9aaa999-529c-46e1-9a3f-b6fdcbeb5b51
title: Стиль пера
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f447839627f97d7662fdef35bd7088ef7b0dcba5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991491"
---
# <a name="pen-style"></a><span data-ttu-id="54c68-105">Стиль пера</span><span class="sxs-lookup"><span data-stu-id="54c68-105">Pen Style</span></span>

<span data-ttu-id="54c68-106">Атрибут style указывает шаблон линии, который отображается при использовании определенного косметическиго или геометрического пера.</span><span class="sxs-lookup"><span data-stu-id="54c68-106">The style attribute specifies the line pattern that appears when a particular cosmetic or geometric pen is used.</span></span> <span data-ttu-id="54c68-107">Существует восемь стандартных стилей пера.</span><span class="sxs-lookup"><span data-stu-id="54c68-107">There are eight predefined pen styles.</span></span> <span data-ttu-id="54c68-108">На следующем рисунке показаны семь из этих стилей, определяемых системой.</span><span class="sxs-lookup"><span data-stu-id="54c68-108">The following illustration shows the seven of these styles that are defined by the system.</span></span>

![Иллюстрация, в которой показаны семь строк, каждая из которых была выведена с использованием другого предопределенного стиля](images/cspen-01.png)

<span data-ttu-id="54c68-110">Стиль внутри фрейма идентичен сплошному стилю для косметических перьев.</span><span class="sxs-lookup"><span data-stu-id="54c68-110">The inside-frame style is identical to the solid style for cosmetic pens.</span></span> <span data-ttu-id="54c68-111">Однако при использовании с геометрическим пером он работает по-разному.</span><span class="sxs-lookup"><span data-stu-id="54c68-111">However, it operates differently when used with a geometric pen.</span></span> <span data-ttu-id="54c68-112">Если геометрическое перо шире одного пикселя, а функция рисования использует перо для рисования границы вокруг заполненного объекта, система рисует границу внутри рамки объекта.</span><span class="sxs-lookup"><span data-stu-id="54c68-112">If the geometric pen is wider than a single pixel and a drawing function uses the pen to draw a border around a filled object, the system draws the border inside the object's frame.</span></span> <span data-ttu-id="54c68-113">С помощью стиля внутри фрейма приложение может гарантировать, что объект отображается полностью в пределах указанных измерений, независимо от ширины геометрического пера.</span><span class="sxs-lookup"><span data-stu-id="54c68-113">By using the inside-frame style, an application can ensure that an object appears entirely within the specified dimensions, regardless of the geometric pen width.</span></span>

<span data-ttu-id="54c68-114">Помимо семи стилей, определенных системой, существует восьмой стиль, который определен пользователем (или приложением).</span><span class="sxs-lookup"><span data-stu-id="54c68-114">In addition to the seven styles defined by the system, there is an eighth style that is user (or application) defined.</span></span> <span data-ttu-id="54c68-115">Определяемый пользователем стиль создает строки с настроенными наборами штрихов и точек.</span><span class="sxs-lookup"><span data-stu-id="54c68-115">A user-defined style generates lines with a customized series of dashes and dots.</span></span>

<span data-ttu-id="54c68-116">Используйте функцию [**креатепен**](/windows/desktop/api/Wingdi/nf-wingdi-createpen), [**креатепениндирект**](/windows/desktop/api/Wingdi/nf-wingdi-createpenindirect)или [**ексткреатепен**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) , чтобы создать перо с определенными системой стилями.</span><span class="sxs-lookup"><span data-stu-id="54c68-116">Use the [**CreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-createpen), [**CreatePenIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createpenindirect), or [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) function to create a pen that has the system-defined styles.</span></span> <span data-ttu-id="54c68-117">Используйте функцию **ексткреатепен** , чтобы создать перо с определенным пользователем стилем.</span><span class="sxs-lookup"><span data-stu-id="54c68-117">Use the **ExtCreatePen** function to create a pen that has a user-defined style.</span></span>

 

 



