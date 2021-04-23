---
title: Text (Windows Media Player SDK)
description: Текст
ms.assetid: 8c10cefb-d0d0-4214-8712-d171a76de95d
keywords:
- Обложки Windows Media Player для мобильных устройств, текст
- обложки, текст
- Справочник по обложек, тексту
- текст в обложках, сведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c801d93698bc7a17eea34df71514dd88b485f0d9
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "103891365"
---
# <a name="text-windows-media-player-sdk"></a><span data-ttu-id="ea8e0-107">Text (Windows Media Player SDK)</span><span class="sxs-lookup"><span data-stu-id="ea8e0-107">Text (Windows Media Player SDK)</span></span>

<span data-ttu-id="ea8e0-108">Может потребоваться использовать одно или несколько текстовых полей в обложке.</span><span class="sxs-lookup"><span data-stu-id="ea8e0-108">You may want to use one or more text display boxes in your skin.</span></span> <span data-ttu-id="ea8e0-109">Каждое используемое текстовое поле должно быть определено в файле определения обложки.</span><span class="sxs-lookup"><span data-stu-id="ea8e0-109">Each text display box you use must be defined in the skin definition file.</span></span> <span data-ttu-id="ea8e0-110">Если в этом разделе не определено текстовое поле для вывода, Обложка не сможет ее использовать.</span><span class="sxs-lookup"><span data-stu-id="ea8e0-110">If you do not define a text display box in this section, your skin will not be able to use it.</span></span>

<span data-ttu-id="ea8e0-111">Текст, содержащийся в файле определения обложки, начинается со следующей строки:</span><span class="sxs-lookup"><span data-stu-id="ea8e0-111">The Text section of the skin definition file begins with this line:</span></span>


```C++
[ Text ]

```



<span data-ttu-id="ea8e0-112">Затем необходимо добавить одну или несколько строк, содержащих сведения о каждом из текстовых полей, отображаемых в обложке.</span><span class="sxs-lookup"><span data-stu-id="ea8e0-112">You then must add one or more lines that contain information about each of the text display boxes in your skin</span></span>


```C++
    Time         180,46,50,30   Right    Tahoma,16,N     255,255,255

```



<span data-ttu-id="ea8e0-113">Для текстового раздела файла определения обложки можно использовать следующий шаблон:</span><span class="sxs-lookup"><span data-stu-id="ea8e0-113">You can use the following template for the Text section of your skin definition file:</span></span>


```C++
//  <Type>       <Location>     <Align> <Font>          <Color>
//  ------       ----------     ------- ------          -------

```



<span data-ttu-id="ea8e0-114">Необходимо использовать порядок, показанный в предыдущем шаблоне, для отображения данных в поле текст для каждой строки в разделе текст.</span><span class="sxs-lookup"><span data-stu-id="ea8e0-114">You must use the order shown in the preceding template for text display box information for each line in the Text section.</span></span> <span data-ttu-id="ea8e0-115">Каждая часть строки является обязательной.</span><span class="sxs-lookup"><span data-stu-id="ea8e0-115">Each part of the line is required.</span></span> <span data-ttu-id="ea8e0-116">В следующих разделах подробно описывается каждый элемент.</span><span class="sxs-lookup"><span data-stu-id="ea8e0-116">The following sections describe each item in detail.</span></span>

1.  [<span data-ttu-id="ea8e0-117">Тип текста</span><span class="sxs-lookup"><span data-stu-id="ea8e0-117">Text Type</span></span>](text-type.md)
2.  [<span data-ttu-id="ea8e0-118">Расположение текста</span><span class="sxs-lookup"><span data-stu-id="ea8e0-118">Text Location</span></span>](text-location.md)
3.  [<span data-ttu-id="ea8e0-119">Выравнивание текста</span><span class="sxs-lookup"><span data-stu-id="ea8e0-119">Text Alignment</span></span>](text-alignment.md)
4.  [<span data-ttu-id="ea8e0-120">Шрифт текста</span><span class="sxs-lookup"><span data-stu-id="ea8e0-120">Text Font</span></span>](text-font.md)
5.  [<span data-ttu-id="ea8e0-121">Цвет текста</span><span class="sxs-lookup"><span data-stu-id="ea8e0-121">Text Color</span></span>](text-color.md)

<span data-ttu-id="ea8e0-122">Пример текстового кода см. в [разделе Образец текста](sample-text-section.md).</span><span class="sxs-lookup"><span data-stu-id="ea8e0-122">For an example of Text code, see [Sample Text Section](sample-text-section.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ea8e0-123">См. также</span><span class="sxs-lookup"><span data-stu-id="ea8e0-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea8e0-124">**Справочник по обложкам**</span><span class="sxs-lookup"><span data-stu-id="ea8e0-124">**Skin Reference**</span></span>](skin-reference.md)
</dt> </dl>

 

 




