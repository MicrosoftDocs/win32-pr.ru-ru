---
description: В этом разделе перечислены конструкторы класса Color. Полный список классов см. в разделе класс Color.
ms.assetid: ebd68c22-9b00-4a8e-9954-e8b0eda764f8
title: Конструкторы Color. Color
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 9d6fe2cdc790f87a69395cec5bfadaf653fc8acf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997635"
---
# <a name="colorcolor-constructors"></a><span data-ttu-id="e2730-104">Конструкторы Color. Color</span><span class="sxs-lookup"><span data-stu-id="e2730-104">Color.Color constructors</span></span>

<span data-ttu-id="e2730-105">В этом разделе перечислены конструкторы класса [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) .</span><span class="sxs-lookup"><span data-stu-id="e2730-105">This topic lists the constructors of the [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) class.</span></span> <span data-ttu-id="e2730-106">Полный список классов см. в разделе **класс Color**.</span><span class="sxs-lookup"><span data-stu-id="e2730-106">For a complete class listing, see **Color Class**.</span></span>

### <a name="overload-list"></a><span data-ttu-id="e2730-107">Список перегрузок</span><span class="sxs-lookup"><span data-stu-id="e2730-107">Overload list</span></span>



| <span data-ttu-id="e2730-108">Конструктор</span><span class="sxs-lookup"><span data-stu-id="e2730-108">Constructor</span></span>                                                               | <span data-ttu-id="e2730-109">Описание</span><span class="sxs-lookup"><span data-stu-id="e2730-109">Description</span></span>                                                                                                                                                                                                         |
|:--------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2730-110">[**Цвет (ARGB)**](/windows/win32/api/gdipluscolor/nf-gdipluscolor-color-color(inargb))</span><span class="sxs-lookup"><span data-stu-id="e2730-110">[**Color(ARGB)**](/windows/win32/api/gdipluscolor/nf-gdipluscolor-color-color(inargb))</span></span>                   | <span data-ttu-id="e2730-111">Создает объект [**Color:: Color**](/windows/win32/api/gdipluscolor/nf-gdipluscolor-color-color(inargb)) , используя значение **ARGB** .</span><span class="sxs-lookup"><span data-stu-id="e2730-111">Creates a [**Color::Color**](/windows/win32/api/gdipluscolor/nf-gdipluscolor-color-color(inargb)) object by using an **ARGB** value.</span></span><br/>                                                                                                    |
| <span data-ttu-id="e2730-112">[**Цвет (байт, байт, байт)**](/windows/win32/api/gdipluscolor/nf-gdipluscolor-color-color(inbyte_inbyte_inbyte))</span><span class="sxs-lookup"><span data-stu-id="e2730-112">[**Color(BYTE,BYTE,BYTE)**](/windows/win32/api/gdipluscolor/nf-gdipluscolor-color-color(inbyte_inbyte_inbyte))</span></span>        | <span data-ttu-id="e2730-113">Создает объект [**Color:: Color**](/windows/win32/api/gdipluscolor/nf-gdipluscolor-color-color(inbyte_inbyte_inbyte)) , используя указанные значения для красного, зеленого и синего компонентов.</span><span class="sxs-lookup"><span data-stu-id="e2730-113">Creates a [**Color::Color**](/windows/win32/api/gdipluscolor/nf-gdipluscolor-color-color(inbyte_inbyte_inbyte)) object by using specified values for the red, green, and blue components.</span></span> <span data-ttu-id="e2730-114">Этот конструктор задает для альфа-компонента значение 255 (непрозрачный).</span><span class="sxs-lookup"><span data-stu-id="e2730-114">This constructor sets the alpha component to 255 (opaque).</span></span><br/> |
| <span data-ttu-id="e2730-115">[**Цвет (байт, байт, байт)**](/windows/win32/api/gdipluscolor/nf-gdipluscolor-color-color(inbyte_inbyte_inbyte_inbyte))</span><span class="sxs-lookup"><span data-stu-id="e2730-115">[**Color(BYTE,BYTE,BYTE,BYTE)**](/windows/win32/api/gdipluscolor/nf-gdipluscolor-color-color(inbyte_inbyte_inbyte_inbyte))</span></span> | <span data-ttu-id="e2730-116">Создает объект [**Color:: Color**](/windows/win32/api/gdipluscolor/nf-gdipluscolor-color-color(inbyte_inbyte_inbyte_inbyte)) , используя указанные значения для альфа-, красного, зеленого и синего компонентов.</span><span class="sxs-lookup"><span data-stu-id="e2730-116">Creates a [**Color::Color**](/windows/win32/api/gdipluscolor/nf-gdipluscolor-color-color(inbyte_inbyte_inbyte_inbyte)) object by using specified values for the alpha, red, green, and blue components.</span></span><br/>                                                   |
| [<span data-ttu-id="e2730-117">**Color ()**</span><span class="sxs-lookup"><span data-stu-id="e2730-117">**Color()**</span></span>](/windows/win32/api/gdipluscolor/nf-gdipluscolor-color-color)                            | <span data-ttu-id="e2730-118">Создает объект [**Color:: Color**](/windows/win32/api/gdipluscolor/nf-gdipluscolor-color-color) и инициализирует его непрозрачным черным цветом.</span><span class="sxs-lookup"><span data-stu-id="e2730-118">Creates a [**Color::Color**](/windows/win32/api/gdipluscolor/nf-gdipluscolor-color-color) object and initializes it to opaque black.</span></span> <span data-ttu-id="e2730-119">Это конструктор по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e2730-119">This is the default constructor.</span></span><br/>                                                                |



 

 
