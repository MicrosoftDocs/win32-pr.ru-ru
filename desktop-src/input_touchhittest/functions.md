---
title: Функции (проверка нажатия касания)
description: В подразделах этого раздела приводятся справочные сведения по функциям проверки попадания в касание.
ms.assetid: C7275A12-4F76-485D-896F-3CCB8CE92F8E
keywords:
- взаимодействие с пользователем
- input
- указатель
- Сенсорный ввод
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: 03fcb4fb3fbe4f56e288703316f4b6e3ff02bba4
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/26/2021
ms.locfileid: "105721074"
---
# <a name="touch-hit-testing-functions"></a><span data-ttu-id="de500-107">Функции проверки нажатия касания</span><span class="sxs-lookup"><span data-stu-id="de500-107">Touch Hit Testing functions</span></span>

<span data-ttu-id="de500-108">В подразделах этого раздела приводятся справочные сведения по [функциям проверки попадания в касание](functions.md).</span><span class="sxs-lookup"><span data-stu-id="de500-108">The topics in this section provide the reference specifications for [Touch Hit Testing functions](functions.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="de500-109">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="de500-109">In this section</span></span>

| <span data-ttu-id="de500-110">Раздел</span><span class="sxs-lookup"><span data-stu-id="de500-110">Topic</span></span> | <span data-ttu-id="de500-111">Описание</span><span class="sxs-lookup"><span data-stu-id="de500-111">Description</span></span> |
| --- | --- |
| [<span data-ttu-id="de500-112">**евалуатепроксимититополигон**</span><span class="sxs-lookup"><span data-stu-id="de500-112">**EvaluateProximityToPolygon**</span></span>](/windows/win32/api/winuser/nf-winuser-evaluateproximitytopolygon)<br/> | <span data-ttu-id="de500-113">Возвращает оценку многоугольника как вероятного сенсорного объекта (по сравнению со всеми другими многоугольниками, пересекающимися с контактной областью касания) и настроенной сенсорной точке многоугольника.</span><span class="sxs-lookup"><span data-stu-id="de500-113">Returns the score of a polygon as the probable touch target (compared to all other polygons that intersect the touch contact area) and an adjusted touch point within the polygon.</span></span> <br/> |
| [<span data-ttu-id="de500-114">**евалуатепроксимититорект**</span><span class="sxs-lookup"><span data-stu-id="de500-114">**EvaluateProximityToRect**</span></span>](/windows/win32/api/winuser/nf-winuser-evaluateproximitytorect)<br/> | <span data-ttu-id="de500-115">Возвращает оценку прямоугольника как вероятного сенсорного объекта, по сравнению с другими прямоугольниками, пересекающимися с контактной областью касания, и скорректированной сенсорной точкой внутри прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="de500-115">Returns the score of a rectangle as the probable touch target, compared to all other rectangles that intersect the touch contact area, and an adjusted touch point within the rectangle.</span></span> <br/> |
| [<span data-ttu-id="de500-116">**пакктаучхиттестингпроксимитевалуатион**</span><span class="sxs-lookup"><span data-stu-id="de500-116">**PackTouchHitTestingProximityEvaluation**</span></span>](/windows/win32/api/winuser/nf-winuser-packtouchhittestingproximityevaluation)<br/> | <span data-ttu-id="de500-117">Возвращает оценку оценки близости, а также скорректированные координаты сенсорной точки в виде упакованного значения для обратного вызова [WM_TOUCHHITTESTINGного сообщения](../inputmsg/wm-touchhittesting.md) .</span><span class="sxs-lookup"><span data-stu-id="de500-117">Returns the proximity evaluation score and the adjusted touch-point coordinates as a packed value for the [WM_TOUCHHITTESTING message](../inputmsg/wm-touchhittesting.md) callback.</span></span> <br/> |
| [<span data-ttu-id="de500-118">**регистертаучхиттестингвиндов**</span><span class="sxs-lookup"><span data-stu-id="de500-118">**RegisterTouchHitTestingWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow)<br/> | <span data-ttu-id="de500-119">Регистрирует окно для обработки уведомления [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md)</span><span class="sxs-lookup"><span data-stu-id="de500-119">Registers a window to process the [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) notification</span></span><br/> |

## <a name="related-topics"></a><span data-ttu-id="de500-120">См. также</span><span class="sxs-lookup"><span data-stu-id="de500-120">Related topics</span></span>

[<span data-ttu-id="de500-121">Ссылка на проверку нажатия касания</span><span class="sxs-lookup"><span data-stu-id="de500-121">Touch Hit Testing Reference</span></span>](touchhittest-reference.md)
