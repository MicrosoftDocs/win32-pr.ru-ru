---
description: Размеры косметических планшета указываются в единицах устройства.
ms.assetid: d4386681-3523-4872-b048-2a5cfbf7d039
title: Косметические перья
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbb312ed0b3825397ff79ebc32d363956ad04519
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811999"
---
# <a name="cosmetic-pens"></a><span data-ttu-id="b6695-103">Косметические перья</span><span class="sxs-lookup"><span data-stu-id="b6695-103">Cosmetic Pens</span></span>

<span data-ttu-id="b6695-104">Размеры косметических планшета указываются в единицах устройства.</span><span class="sxs-lookup"><span data-stu-id="b6695-104">The dimensions of a cosmetic pen are specified in device units.</span></span> <span data-ttu-id="b6695-105">Таким образом, линии, нарисованные с помощью косметических перьев, всегда имеют фиксированную ширину.</span><span class="sxs-lookup"><span data-stu-id="b6695-105">Therefore, lines drawn with a cosmetic pen always have a fixed width.</span></span> <span data-ttu-id="b6695-106">Линии, нарисованные с помощью косметических перьев, обычно выводятся 3 – 10 раз быстрее, чем линии, рисуемые с помощью геометрического пера.</span><span class="sxs-lookup"><span data-stu-id="b6695-106">Lines drawn with a cosmetic pen are generally drawn 3 to 10 times faster than lines drawn with a geometric pen.</span></span> <span data-ttu-id="b6695-107">Косметические перья имеют три атрибута: ширина, стиль и цвет.</span><span class="sxs-lookup"><span data-stu-id="b6695-107">Cosmetic pens have three attributes: width, style, and color.</span></span> <span data-ttu-id="b6695-108">Дополнительные сведения об этих атрибутах см. в разделе [атрибуты пера](pen-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="b6695-108">For more information about these attributes, see [Pen Attributes](pen-attributes.md).</span></span>

<span data-ttu-id="b6695-109">Чтобы создать косметический перо, используйте функцию [**креатепен**](/windows/desktop/api/Wingdi/nf-wingdi-createpen), [**креатепениндирект**](/windows/desktop/api/Wingdi/nf-wingdi-createpenindirect)или [**ексткреатепен**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) .</span><span class="sxs-lookup"><span data-stu-id="b6695-109">To create a cosmetic pen, use the [**CreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-createpen), [**CreatePenIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createpenindirect), or [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) function.</span></span> <span data-ttu-id="b6695-110">Чтобы получить один из трех перьевых косметических элементов, управляемых системой, используйте функцию [**жетстоккобжект**](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) .</span><span class="sxs-lookup"><span data-stu-id="b6695-110">To retrieve one of the three stock cosmetic pens managed by the system, use the [**GetStockObject**](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) function.</span></span>

<span data-ttu-id="b6695-111">После создания пера (или получения маркера для одного из геоакций) выберите перо в контексте устройства (DC) приложения с помощью функции [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) .</span><span class="sxs-lookup"><span data-stu-id="b6695-111">After you create a pen (or obtain a handle to one of the stock pens), select the pen into the application's device context (DC) using the [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) function.</span></span> <span data-ttu-id="b6695-112">С этого момента приложение использует это перо для любых операций рисования строк в клиентской области.</span><span class="sxs-lookup"><span data-stu-id="b6695-112">From this point on, the application uses this pen for any line-drawing operations in its client area.</span></span>

 

 



