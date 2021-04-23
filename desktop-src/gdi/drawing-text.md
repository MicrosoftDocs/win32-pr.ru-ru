---
description: Рисование текста
ms.assetid: 8a06f659-4e08-4738-b7a9-956b599c1344
title: Рисование текста (Windows GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7db44a756ff211bcae7605cb87bdac77005b34f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811968"
---
# <a name="drawing-text-windows-gdi"></a><span data-ttu-id="0581a-103">Рисование текста (Windows GDI)</span><span class="sxs-lookup"><span data-stu-id="0581a-103">Drawing Text (Windows GDI)</span></span>

<span data-ttu-id="0581a-104">После того как приложение выберет подходящий шрифт, задает необходимые параметры форматирования текста и вычислит необходимые значения ширины и высоты символов для строки текста, он может начать рисовать символы и символы, вызвав любую из функций вывода текста:</span><span class="sxs-lookup"><span data-stu-id="0581a-104">After an application selects the appropriate font, sets the required text-formatting options, and computes the necessary character width and height values for a string of text, it can begin drawing characters and symbols by calling any of the text-output functions:</span></span>

-   [<span data-ttu-id="0581a-105">DrawText</span><span class="sxs-lookup"><span data-stu-id="0581a-105">DrawText</span></span>](/windows/desktop/api/Winuser/nf-winuser-drawtext)
-   [<span data-ttu-id="0581a-106">дравтекстекс</span><span class="sxs-lookup"><span data-stu-id="0581a-106">DrawTextEx</span></span>](/windows/desktop/api/Winuser/nf-winuser-drawtextexa)
-   [<span data-ttu-id="0581a-107">ExtTextOut</span><span class="sxs-lookup"><span data-stu-id="0581a-107">ExtTextOut</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta)
-   [<span data-ttu-id="0581a-108">Текст</span><span class="sxs-lookup"><span data-stu-id="0581a-108">PolyTextOut</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polytextouta)
-   [<span data-ttu-id="0581a-109">таббедтекстаут</span><span class="sxs-lookup"><span data-stu-id="0581a-109">TabbedTextOut</span></span>](/windows/desktop/api/Winuser/nf-winuser-tabbedtextouta)
-   [<span data-ttu-id="0581a-110">TextOut</span><span class="sxs-lookup"><span data-stu-id="0581a-110">TextOut</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-textouta)

<span data-ttu-id="0581a-111">Когда приложение вызывает одну из этих функций, операционная система передает вызов модулю Graphics, который, в свою очередь, передает вызов соответствующему драйверу устройства.</span><span class="sxs-lookup"><span data-stu-id="0581a-111">When an application calls one of these functions, the operating system passes the call to the graphics engine, which in turn passes the call to the appropriate device driver.</span></span> <span data-ttu-id="0581a-112">На уровне драйвера устройства все эти вызовы поддерживаются одним или несколькими вызовами функции [ExtTextOut](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta) или [текста](/windows/desktop/api/Wingdi/nf-wingdi-textouta) драйвера.</span><span class="sxs-lookup"><span data-stu-id="0581a-112">At the device driver level, all of these calls are supported by one or more calls to the driver's own [ExtTextOut](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta) or [TextOut](/windows/desktop/api/Wingdi/nf-wingdi-textouta) function.</span></span> <span data-ttu-id="0581a-113">Приложение обеспечит самое быстрое выполнение путем вызова [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta), которое быстро преобразуется в вызов **ExtTextOut** для устройства.</span><span class="sxs-lookup"><span data-stu-id="0581a-113">An application will achieve the fastest execution by calling [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta), which is quickly converted into an **ExtTextOut** call for the device.</span></span> <span data-ttu-id="0581a-114">Однако существуют экземпляры, когда приложение должно вызвать одну из других трех функций. Например, чтобы нарисовать несколько строк текста внутри границ заданной прямоугольной области, более эффективно вызывать [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext).</span><span class="sxs-lookup"><span data-stu-id="0581a-114">However, there are instances when an application should call one of the other three functions; for example, to draw multiple lines of text within the borders of a specified rectangular region, it is more efficient to call [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext).</span></span> <span data-ttu-id="0581a-115">Чтобы создать таблицу с несколькими столбцами с выровненными столбцами текста, более эффективно вызывать [**таббедтекстаут**](/windows/win32/api/winuser/nf-winuser-tabbedtextouta).</span><span class="sxs-lookup"><span data-stu-id="0581a-115">To create a multicolumn table with justified columns of text, it is more efficient to call [**TabbedTextOut**](/windows/win32/api/winuser/nf-winuser-tabbedtextouta).</span></span>

 

 
