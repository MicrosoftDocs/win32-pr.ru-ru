---
description: В этом разделе перечислены конструкторы класса Region. Полный список классов см. в разделе Класс Region.
ms.assetid: 94f4971c-defa-43e0-a0c0-4000557b0a5c
title: Конструкторы регионов. Region
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name: ''
api_type:
- NA
api_location: ''
ms.openlocfilehash: 98663587fab3722d689c9d34578d60daad922a2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156211"
---
# <a name="regionregion-constructors"></a><span data-ttu-id="122c0-104">Конструкторы регионов. Region</span><span class="sxs-lookup"><span data-stu-id="122c0-104">Region.Region constructors</span></span>

<span data-ttu-id="122c0-105">В этом разделе перечислены конструкторы класса [**Region**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-region) .</span><span class="sxs-lookup"><span data-stu-id="122c0-105">This topic lists the constructors of the [**Region**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-region) class.</span></span> <span data-ttu-id="122c0-106">Полный список классов см. в разделе **Класс Region**.</span><span class="sxs-lookup"><span data-stu-id="122c0-106">For a complete class listing, see **Region Class**.</span></span>

### <a name="overload-list"></a><span data-ttu-id="122c0-107">Список перегрузок</span><span class="sxs-lookup"><span data-stu-id="122c0-107">Overload list</span></span>



| <span data-ttu-id="122c0-108">Конструктор</span><span class="sxs-lookup"><span data-stu-id="122c0-108">Constructor</span></span>                                                                 | <span data-ttu-id="122c0-109">Описание</span><span class="sxs-lookup"><span data-stu-id="122c0-109">Description</span></span>                                                                                                                                                                                      |
|:----------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="122c0-110">[**Регион (ХРГН)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(inhrgn))</span><span class="sxs-lookup"><span data-stu-id="122c0-110">[**Region(HRGN)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(inhrgn))</span></span>                  | <span data-ttu-id="122c0-111">Создает регион, идентичный региону, заданному с помощью маркера, в регион GDI.</span><span class="sxs-lookup"><span data-stu-id="122c0-111">Creates a region that is identical to the region that is specified by a handle to a GDI region.</span></span><br/>                                                                                       |
| <span data-ttu-id="122c0-112">[**Регион (Rect&)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(inconstrect_))</span><span class="sxs-lookup"><span data-stu-id="122c0-112">[**Region(Rect&)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(inconstrect_))</span></span>            | <span data-ttu-id="122c0-113">Создает область, определяемую прямоугольником.</span><span class="sxs-lookup"><span data-stu-id="122c0-113">Creates a region that is defined by a rectangle.</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="122c0-114">[**Регион (Ректф&)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(inconstrectf_))</span><span class="sxs-lookup"><span data-stu-id="122c0-114">[**Region(RectF&)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(inconstrectf_))</span></span>          | <span data-ttu-id="122c0-115">Создает область, определяемую прямоугольником.</span><span class="sxs-lookup"><span data-stu-id="122c0-115">Creates a region that is defined by a rectangle.</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="122c0-116">[**Регион (BYTE \* , int)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(inconstbyte_inint))</span><span class="sxs-lookup"><span data-stu-id="122c0-116">[**Region(BYTE\*,INT)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(inconstbyte_inint))</span></span> | <span data-ttu-id="122c0-117">Создает регион, определенный данными, полученными из другого региона.</span><span class="sxs-lookup"><span data-stu-id="122c0-117">Creates a region that is defined by data obtained from another region.</span></span> <br/>                                                                                                               |
| <span data-ttu-id="122c0-118">[**Регион (GraphicsPath \* )**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(inconstgraphicspath))</span><span class="sxs-lookup"><span data-stu-id="122c0-118">[**Region(GraphicsPath\*)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(inconstgraphicspath))</span></span>        | <span data-ttu-id="122c0-119">Создает регион, определяемый путем (объект [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) ) и имеющий режим заполнения, содержащийся в объекте **GraphicsPath** .</span><span class="sxs-lookup"><span data-stu-id="122c0-119">Creates a region that is defined by a path (a [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) object) and has a fill mode that is contained in the **GraphicsPath** object.</span></span><br/> |
| <span data-ttu-id="122c0-120">[**Region ()**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(constregion_))</span><span class="sxs-lookup"><span data-stu-id="122c0-120">[**Region()**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(constregion_))</span></span>                           | <span data-ttu-id="122c0-121">Создает неограниченный регион.</span><span class="sxs-lookup"><span data-stu-id="122c0-121">Creates a region that is infinite.</span></span> <span data-ttu-id="122c0-122">Это конструктор по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="122c0-122">This is the default constructor.</span></span> <br/>                                                                                                                  |



 

 
