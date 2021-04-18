---
description: С кистью используются следующие функции.
ms.assetid: 617eb778-876c-4bbb-90da-c5f13359becb
title: Функции кисти (Windows GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2170ff5c4b743e19da669bd76b340ca95ac2ef9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544551"
---
# <a name="brush-functions-windows-gdi"></a><span data-ttu-id="88113-103">Функции кисти (Windows GDI)</span><span class="sxs-lookup"><span data-stu-id="88113-103">Brush Functions (Windows GDI)</span></span>

<span data-ttu-id="88113-104">С кистью используются следующие функции.</span><span class="sxs-lookup"><span data-stu-id="88113-104">The following functions are used with brushes.</span></span>



| <span data-ttu-id="88113-105">Функция</span><span class="sxs-lookup"><span data-stu-id="88113-105">Function</span></span>                                                   | <span data-ttu-id="88113-106">Описание</span><span class="sxs-lookup"><span data-stu-id="88113-106">Description</span></span>                                                |
|------------------------------------------------------------|------------------------------------------------------------|
| [<span data-ttu-id="88113-107">**креатебрушиндирект**</span><span class="sxs-lookup"><span data-stu-id="88113-107">**CreateBrushIndirect**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createbrushindirect)         | <span data-ttu-id="88113-108">Создает кисть с указанным стилем, цветом и шаблоном.</span><span class="sxs-lookup"><span data-stu-id="88113-108">Creates a brush with a specified style, color, and pattern</span></span> |
| [<span data-ttu-id="88113-109">**креатедибпаттернбрушпт**</span><span class="sxs-lookup"><span data-stu-id="88113-109">**CreateDIBPatternBrushPt**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createdibpatternbrushpt) | <span data-ttu-id="88113-110">Создает кисть с шаблоном из рисунка DIB</span><span class="sxs-lookup"><span data-stu-id="88113-110">Creates a brush with the pattern from a DIB</span></span>                |
| [<span data-ttu-id="88113-111">**креатехатчбруш**</span><span class="sxs-lookup"><span data-stu-id="88113-111">**CreateHatchBrush**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createhatchbrush)               | <span data-ttu-id="88113-112">Создает кисть с шаблоном штриховки и цветом</span><span class="sxs-lookup"><span data-stu-id="88113-112">Creates a brush with a hatch pattern and color</span></span>             |
| [<span data-ttu-id="88113-113">**креатепаттернбруш**</span><span class="sxs-lookup"><span data-stu-id="88113-113">**CreatePatternBrush**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createpatternbrush)           | <span data-ttu-id="88113-114">Создает кисть с шаблоном точечного рисунка</span><span class="sxs-lookup"><span data-stu-id="88113-114">Creates a brush with a bitmap pattern</span></span>                      |
| [<span data-ttu-id="88113-115">**креатесолидбруш**</span><span class="sxs-lookup"><span data-stu-id="88113-115">**CreateSolidBrush**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createsolidbrush)               | <span data-ttu-id="88113-116">Создает кисть с сплошным цветом</span><span class="sxs-lookup"><span data-stu-id="88113-116">Creates a brush with a solid color</span></span>                         |
| [<span data-ttu-id="88113-117">**жетбрушоржекс**</span><span class="sxs-lookup"><span data-stu-id="88113-117">**GetBrushOrgEx**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getbrushorgex)                     | <span data-ttu-id="88113-118">Возвращает источник кисти для контекста устройства</span><span class="sxs-lookup"><span data-stu-id="88113-118">Gets the brush origin for a device context</span></span>                 |
| [<span data-ttu-id="88113-119">**жетсисколорбруш**</span><span class="sxs-lookup"><span data-stu-id="88113-119">**GetSysColorBrush**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getsyscolorbrush)               | <span data-ttu-id="88113-120">Возвращает дескриптор кисти, соответствующей цвету индексу.</span><span class="sxs-lookup"><span data-stu-id="88113-120">Gets a handle to a brush that corresponds to a color index</span></span> |
| [<span data-ttu-id="88113-121">**патблт**</span><span class="sxs-lookup"><span data-stu-id="88113-121">**PatBlt**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-patblt)                                   | <span data-ttu-id="88113-122">Закрашивает прямоугольник</span><span class="sxs-lookup"><span data-stu-id="88113-122">Paints a rectangle</span></span>                                         |
| [<span data-ttu-id="88113-123">**сетбрушоржекс**</span><span class="sxs-lookup"><span data-stu-id="88113-123">**SetBrushOrgEx**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setbrushorgex)                     | <span data-ttu-id="88113-124">Задает источник кисти для контекста устройства</span><span class="sxs-lookup"><span data-stu-id="88113-124">Sets the brush origin for a device context</span></span>                 |
| [<span data-ttu-id="88113-125">**сетдкбрушколор**</span><span class="sxs-lookup"><span data-stu-id="88113-125">**SetDCBrushColor**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor)                 | <span data-ttu-id="88113-126">Задает цвет кисти контекста текущего устройства.</span><span class="sxs-lookup"><span data-stu-id="88113-126">Sets the current device context brush color.</span></span>               |



 

## <a name="obsolete-functions"></a><span data-ttu-id="88113-127">Устаревшие функции</span><span class="sxs-lookup"><span data-stu-id="88113-127">Obsolete Functions</span></span>

<span data-ttu-id="88113-128">Следующие функции предоставляются только для обеспечения совместимости с 16-разрядными версиями Windows.</span><span class="sxs-lookup"><span data-stu-id="88113-128">The following functions are provided only for compatibility with 16-bit versions of Windows.</span></span>

[<span data-ttu-id="88113-129">**креатедибпаттернбруш**</span><span class="sxs-lookup"><span data-stu-id="88113-129">**CreateDIBPatternBrush**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createdibpatternbrush)

 

 



