---
title: Раздел описания
description: Раздел описания
ms.assetid: 280a9a4d-935f-440d-a606-94aeba0007db
keywords:
- Обложки мобильных устройств проигрывателя Windows Media, раздел описания
- обложки, раздел описания
- Создание обложек, раздел описания
- Написание кода для обложек, раздел описания
- Раздел описания в обложках
- файлы определения обложки, раздел описания
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce9518b6b1de128457dc3e6b3738ddab9be2a873
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103889032"
---
# <a name="description-section"></a><span data-ttu-id="d753a-109">Раздел описания</span><span class="sxs-lookup"><span data-stu-id="d753a-109">Description Section</span></span>

<span data-ttu-id="d753a-110">Далее необходимо предоставить раздел, описывающий размер и ориентацию обложки при создании обложки для проигрывателя Windows Media 9 для Windows Mobile 2003 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="d753a-110">Next, you must provide a section that describes the size and orientation of the skin when creating a skin for Windows Media Player 9 Series for Windows Mobile 2003 and later versions:</span></span>


```C++
[ Description ]
//              <X,Y>       <DPI>
//              ------      -----
    Dimensions  240, 320    96

//    <Orientation>
//    -------------
    Orientation Portrait

```



<span data-ttu-id="d753a-111">Раздел Description должен начинаться с описания слова в квадратных скобках, а затем включать строку, указывающую размеры и разрешение экрана для обложки.</span><span class="sxs-lookup"><span data-stu-id="d753a-111">The Description section must begin with the word Description in brackets, and then include a line that specifies the dimensions and display resolution for the skin.</span></span>

<span data-ttu-id="d753a-112">Строки, начинающиеся с двух косых черт, не обрабатываются и могут использоваться для комментариев или, как показано в предыдущем коде, с помощью шаблона, помогающего запомнить, что происходит в разделе.</span><span class="sxs-lookup"><span data-stu-id="d753a-112">Lines beginning with two forward slashes are not processed, and can be used for comments or, as shown in the previous code, a template to help you remember what goes in a section.</span></span> <span data-ttu-id="d753a-113">Кроме того, можно использовать шаблоны для совмещения всех столбцов.</span><span class="sxs-lookup"><span data-stu-id="d753a-113">You can also use templates to help align everything into columns.</span></span>

<span data-ttu-id="d753a-114">Дополнительные сведения см. в разделе [Описание](description.md) в справочнике по обложкам.</span><span class="sxs-lookup"><span data-stu-id="d753a-114">For more information about the Description section, see [Description](description.md) in the Skin Reference.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d753a-115">См. также</span><span class="sxs-lookup"><span data-stu-id="d753a-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d753a-116">**Написание кода**</span><span class="sxs-lookup"><span data-stu-id="d753a-116">**Writing the Code**</span></span>](writing-the-code.md)
</dt> </dl>

 

 




