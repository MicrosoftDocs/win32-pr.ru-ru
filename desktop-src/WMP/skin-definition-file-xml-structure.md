---
title: XML-структура файла определения обложки
description: XML-структура файла определения обложки
ms.assetid: 93325b94-667a-42a6-92f8-78288d36da81
keywords:
- Создание обложек, файлы определения обложки
- Обложки проигрывателя Windows Media, файлы определения обложки
- обложки, файлы определения обложки
- файлы для обложек, определение обложки
- файлы определения обложки, структура XML
- XML-структура для файлов определения обложки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8508f1a458930bc2b60d564a45ef08a9f9f5a9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068240"
---
# <a name="skin-definition-file-xml-structure"></a><span data-ttu-id="c557d-109">XML-структура файла определения обложки</span><span class="sxs-lookup"><span data-stu-id="c557d-109">Skin Definition File XML Structure</span></span>

<span data-ttu-id="c557d-110">Файл определения обложки записывается в формате XML.</span><span class="sxs-lookup"><span data-stu-id="c557d-110">The skin definition file is written in XML.</span></span> <span data-ttu-id="c557d-111">Одной из важных функций XML является то, что она полностью структурирована и похожа на структуру.</span><span class="sxs-lookup"><span data-stu-id="c557d-111">One of the important features of XML is that it is completely structured, and is similar to an outline.</span></span> <span data-ttu-id="c557d-112">XML-код — это просто ряд элементов, таких как **View** и **BUTTONGROUP**.</span><span class="sxs-lookup"><span data-stu-id="c557d-112">The XML code is simply a series of elements such as **VIEW** and **BUTTONGROUP**.</span></span> <span data-ttu-id="c557d-113">Сначала вы начнете с элементов, а затем определите их с помощью атрибутов.</span><span class="sxs-lookup"><span data-stu-id="c557d-113">You will start with the elements and then define them with attributes.</span></span> <span data-ttu-id="c557d-114">В оставшейся части этого руководства вы получите подробные сведения об атрибутах, но ниже приведена структура элементов, которые будут использоваться:</span><span class="sxs-lookup"><span data-stu-id="c557d-114">The rest of this tutorial will give you details on the attributes, but here is the outline of the elements that will be used:</span></span>


```C++
<THEME>
    <VIEW>
        <BUTTONGROUP>
            <BUTTONELEMENT/>
            <BUTTONELEMENT/>
        </BUTTONGROUP>
    </VIEW>
<THEME>

```



<span data-ttu-id="c557d-115">Учитывая простую структуру элементов, можно присвоить смысл атрибутам, которые делают каждый элемент уникальным.</span><span class="sxs-lookup"><span data-stu-id="c557d-115">By keeping in mind the simple structure of the elements, you can make sense of the attributes that make each element unique.</span></span> <span data-ttu-id="c557d-116">Сведения о каждом элементе будут рассмотрены в остальных разделах этого раздела.</span><span class="sxs-lookup"><span data-stu-id="c557d-116">Details of each element will be covered in the remaining topics of this section.</span></span> <span data-ttu-id="c557d-117">Дополнительные сведения об элементах и атрибутах см. в [справочнике по программированию для обложки](skin-programming-reference.md).</span><span class="sxs-lookup"><span data-stu-id="c557d-117">For more information about elements and attributes, see the [Skin Programming Reference](skin-programming-reference.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c557d-118">См. также</span><span class="sxs-lookup"><span data-stu-id="c557d-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c557d-119">**Создание файла определения обложки**</span><span class="sxs-lookup"><span data-stu-id="c557d-119">**Creating the Skin Definition File**</span></span>](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




