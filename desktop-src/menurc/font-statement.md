---
title: FONT, инструкция
description: Определяет шрифт, с помощью которого система будет рисовать текст в диалоговом окне. Шрифт должен быть ранее загружен; Например, путем вызова функции Лоадресаурце.
ms.assetid: d7b0f382-bc45-4405-a30e-0b571fdfd1db
keywords:
- Меню инструкций шрифтов и другие ресурсы
topic_type:
- apiref
api_name:
- FONT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4b31b280a5a973301e8410f1f74340138af07ba
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487688"
---
# <a name="font-statement"></a><span data-ttu-id="60661-105">FONT, инструкция</span><span class="sxs-lookup"><span data-stu-id="60661-105">FONT statement</span></span>

<span data-ttu-id="60661-106">Определяет шрифт, с помощью которого система будет рисовать текст в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="60661-106">Defines the font with which the system will draw text in the dialog box.</span></span> <span data-ttu-id="60661-107">Шрифт должен быть ранее загружен; Например, путем вызова функции [**лоадресаурце**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource) .</span><span class="sxs-lookup"><span data-stu-id="60661-107">The font must have been previously loaded; for example, by calling the [**LoadResource**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource) function.</span></span>

``` syntax
FONT pointsize, "typeface", weight, italic, charset
```

<dl> <dt>

<span data-ttu-id="60661-108"><span id="pointsize"></span><span id="POINTSIZE"></span>*PointSize*</span><span class="sxs-lookup"><span data-stu-id="60661-108"><span id="pointsize"></span><span id="POINTSIZE"></span>*pointsize*</span></span>
</dt> <dd>

<span data-ttu-id="60661-109">Размер шрифта в пунктах.</span><span class="sxs-lookup"><span data-stu-id="60661-109">The size of the font, in points.</span></span>

</dd> <dt>

<span data-ttu-id="60661-110"><span id="typeface"></span><span id="TYPEFACE"></span>*начертан*</span><span class="sxs-lookup"><span data-stu-id="60661-110"><span id="typeface"></span><span id="TYPEFACE"></span>*typeface*</span></span>
</dt> <dd>

<span data-ttu-id="60661-111">Имя гарнитуры.</span><span class="sxs-lookup"><span data-stu-id="60661-111">The name of the typeface.</span></span> <span data-ttu-id="60661-112">Этот параметр должен быть заключен в кавычки (").</span><span class="sxs-lookup"><span data-stu-id="60661-112">This parameter must be enclosed in quotes (").</span></span>

</dd> <dt>

<span data-ttu-id="60661-113"><span id="weight"></span><span id="WEIGHT"></span>*оценку*</span><span class="sxs-lookup"><span data-stu-id="60661-113"><span id="weight"></span><span id="WEIGHT"></span>*weight*</span></span>
</dt> <dd>

<span data-ttu-id="60661-114">Вес шрифта в диапазоне от 0 до 1000.</span><span class="sxs-lookup"><span data-stu-id="60661-114">The weight of the font in the range 0 through 1000.</span></span> <span data-ttu-id="60661-115">Например, 400 является нормальным, а 700 — полужирным.</span><span class="sxs-lookup"><span data-stu-id="60661-115">For example, 400 is normal and 700 is bold.</span></span> <span data-ttu-id="60661-116">Если это значение равно 0, используется вес по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="60661-116">If this value is 0, the default weight is used.</span></span> <span data-ttu-id="60661-117">Список предварительно определенных значений см. в разделе **значения \_ \* FW** , определенные в вингди. h.</span><span class="sxs-lookup"><span data-stu-id="60661-117">For a list of predefined values, see the **FW\_\*** values defined in WinGDI.h.</span></span>

</dd> <dt>

<span data-ttu-id="60661-118"><span id="italic"></span><span id="ITALIC"></span>*деле*</span><span class="sxs-lookup"><span data-stu-id="60661-118"><span id="italic"></span><span id="ITALIC"></span>*italic*</span></span>
</dt> <dd>

<span data-ttu-id="60661-119">Обозначает курсив, если задано значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="60661-119">Indicates an italic font if set to TRUE.</span></span>

</dd> <dt>

<span data-ttu-id="60661-120"><span id="charset"></span><span id="CHARSET"></span>*charset*</span><span class="sxs-lookup"><span data-stu-id="60661-120"><span id="charset"></span><span id="CHARSET"></span>*charset*</span></span>
</dt> <dd>

<span data-ttu-id="60661-121">Набор символов.</span><span class="sxs-lookup"><span data-stu-id="60661-121">The character set.</span></span> <span data-ttu-id="60661-122">Список значений см. в описании элемента **лфчарсет** структуры [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) .</span><span class="sxs-lookup"><span data-stu-id="60661-122">For a list of values, see the **lfCharSet** member of the [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="60661-123">Примеры</span><span class="sxs-lookup"><span data-stu-id="60661-123">Examples</span></span>

<span data-ttu-id="60661-124">В следующем примере показано использование оператора **Font** :</span><span class="sxs-lookup"><span data-stu-id="60661-124">The following example demonstrates the use of the **FONT** statement:</span></span>

``` syntax
FONT 12, "MS Shell Dlg"
```

## <a name="see-also"></a><span data-ttu-id="60661-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="60661-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60661-126">**лоадресаурце**</span><span class="sxs-lookup"><span data-stu-id="60661-126">**LoadResource**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource)
</dt> </dl>

 

 