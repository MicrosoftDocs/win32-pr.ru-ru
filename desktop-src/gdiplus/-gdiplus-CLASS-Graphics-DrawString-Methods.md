---
description: В этом разделе перечислены методы DrawString класса Graphics. Полный список методов для класса Graphics см. в разделе Graphics.
ms.assetid: b3568ed9-e359-4916-a83d-7553c021d197
title: Методы Graphics. DrawString (Гдиплусграфикс. h)
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 275c256ec2c7284401d37794bccf368538cbdd80
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "104987536"
---
# <a name="graphicsdrawstring-methods"></a><span data-ttu-id="dedfd-104">Методы Graphics. DrawString</span><span class="sxs-lookup"><span data-stu-id="dedfd-104">Graphics.DrawString methods</span></span>

<span data-ttu-id="dedfd-105">В этом разделе перечислены методы DrawString класса [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="dedfd-105">This topic lists the DrawString methods of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class.</span></span> <span data-ttu-id="dedfd-106">Полный список методов для класса **Graphics** см. в разделе [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics).</span><span class="sxs-lookup"><span data-stu-id="dedfd-106">For a complete list of methods for the **Graphics** class, see [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics).</span></span>

### <a name="overload-list"></a><span data-ttu-id="dedfd-107">Список перегрузок</span><span class="sxs-lookup"><span data-stu-id="dedfd-107">Overload list</span></span>



| <span data-ttu-id="dedfd-108">Метод</span><span class="sxs-lookup"><span data-stu-id="dedfd-108">Method</span></span>                                                                                                                                                       | <span data-ttu-id="dedfd-109">Описание</span><span class="sxs-lookup"><span data-stu-id="dedfd-109">Description</span></span>                                                                                                                                                                                                   |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dedfd-110">[**DrawString (WCHAR \* , int, Font \* , PointF&, кисть \* )**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush))</span><span class="sxs-lookup"><span data-stu-id="dedfd-110">[**DrawString(WCHAR\*,INT,Font\*,PointF&,Brush\*)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush))</span></span>                                | <span data-ttu-id="dedfd-111">Метод [**Graphics::D равстринг**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) рисует строку на основе шрифта и источника строки.</span><span class="sxs-lookup"><span data-stu-id="dedfd-111">The [**Graphics::DrawString**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) method draws a string based on a font and an origin for the string.</span></span><br/>                        |
| <span data-ttu-id="dedfd-112">[**DrawString (WCHAR \* , int, Font \* , ректф&, StringFormat \* , кисть \* )**](/previous-versions//ms535991(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="dedfd-112">[**DrawString(WCHAR\*,INT,Font\*,RectF&,StringFormat\*,Brush\*)**](/previous-versions//ms535991(v=vs.85))</span></span> | <span data-ttu-id="dedfd-113">Метод [**Graphics::D равстринг**](/previous-versions//ms535991(v=vs.85)) рисует строку на основе шрифта, прямоугольника макета и формата.</span><span class="sxs-lookup"><span data-stu-id="dedfd-113">The [**Graphics::DrawString**](/previous-versions//ms535991(v=vs.85)) method draws a string based on a font, a layout rectangle, and a format.</span></span> <br/> |
| <span data-ttu-id="dedfd-114">[**DrawString (WCHAR \* , int, Font \* , PointF&, StringFormat \* , кисть \* )**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush))</span><span class="sxs-lookup"><span data-stu-id="dedfd-114">[**DrawString(WCHAR\*,INT,Font\*,PointF&,StringFormat\*,Brush\*)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush))</span></span>    | <span data-ttu-id="dedfd-115">Метод [**Graphics::D равстринг**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) рисует строку на основе шрифта, источника строки и формата.</span><span class="sxs-lookup"><span data-stu-id="dedfd-115">The [**Graphics::DrawString**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) method draws a string based on a font, a string origin, and a format.</span></span><br/>         |



## <a name="requirements"></a><span data-ttu-id="dedfd-116">Требования</span><span class="sxs-lookup"><span data-stu-id="dedfd-116">Requirements</span></span>



| <span data-ttu-id="dedfd-117">Требование</span><span class="sxs-lookup"><span data-stu-id="dedfd-117">Requirement</span></span> | <span data-ttu-id="dedfd-118">Значение</span><span class="sxs-lookup"><span data-stu-id="dedfd-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="dedfd-119">Header</span><span class="sxs-lookup"><span data-stu-id="dedfd-119">Header</span></span><br/> | <dl> <span data-ttu-id="dedfd-120"><dt>Гдиплусграфикс. h</dt></span><span class="sxs-lookup"><span data-stu-id="dedfd-120"><dt>Gdiplusgraphics.h</dt></span></span> </dl> |



 

 
