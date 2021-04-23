---
title: Добавление BUTTONGROUP
description: Добавление BUTTONGROUP
ms.assetid: 07a4a347-b3da-4dcb-b3e4-bee0d002b2e2
keywords:
- Создание обложек, элемент BUTTONGROUP
- Обложки проигрывателя Windows Media, элемент BUTTONGROUP
- обложки, элемент BUTTONGROUP
- файлы определения обложки, элемент BUTTONGROUP
- BUTTONGROUP, элемент
- элементы, BUTTONGROUP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90659a2e867a65d2751532701b71810a532c8ce6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329080"
---
# <a name="adding-buttongroup"></a><span data-ttu-id="c4a21-109">Добавление BUTTONGROUP</span><span class="sxs-lookup"><span data-stu-id="c4a21-109">Adding BUTTONGROUP</span></span>

<span data-ttu-id="c4a21-110">В этом примере используется элемент **BUTTONGROUP** для написания кода в файле определения обложки.</span><span class="sxs-lookup"><span data-stu-id="c4a21-110">This example uses the **BUTTONGROUP** element for the coding in the skin definition file.</span></span> <span data-ttu-id="c4a21-111">**BUTTONGROUP** создает простой способ обработки событий мыши без необходимости вычисления точных расположений на экране и использует цвет вместо координат x и y.</span><span class="sxs-lookup"><span data-stu-id="c4a21-111">**BUTTONGROUP** creates an easy way to process mouse events without having to calculate exact locations on the screen and uses color instead of x and y-coordinates.</span></span>

<span data-ttu-id="c4a21-112">Сначала необходимо добавить теги **BUTTONGROUP** в созданный файл определения обложки.</span><span class="sxs-lookup"><span data-stu-id="c4a21-112">First you must add the **BUTTONGROUP** tags to the skin definition file you created.</span></span> <span data-ttu-id="c4a21-113">Вставьте их после атрибутов тега **темы** .</span><span class="sxs-lookup"><span data-stu-id="c4a21-113">Put them after the **THEME** tag attributes.</span></span>


```C++
        <BUTTONGROUP
            mappingImage = "map.bmp"
            hoverImage = "hover.bmp">


        </BUTTONGROUP>

```



<span data-ttu-id="c4a21-114">Оставьте несколько пустых строк над закрывающим тегом **BUTTONGROUP** для кнопок, которые будут добавлены далее.</span><span class="sxs-lookup"><span data-stu-id="c4a21-114">Leave a few blank lines above the closing **BUTTONGROUP** tag for the buttons you will add next.</span></span>

<span data-ttu-id="c4a21-115">Для определения **BUTTONGROUP** используются следующие атрибуты:</span><span class="sxs-lookup"><span data-stu-id="c4a21-115">The following attributes are used to define **BUTTONGROUP**:</span></span>

<span data-ttu-id="c4a21-116">**маппингимаже**</span><span class="sxs-lookup"><span data-stu-id="c4a21-116">**mappingImage**</span></span>

<span data-ttu-id="c4a21-117">Это имя файла сопоставленного рисунка, созданного ранее, с красной и зеленой окружностями.</span><span class="sxs-lookup"><span data-stu-id="c4a21-117">This is the file name of the mapping art file you created before, the one with the red and green circles.</span></span> <span data-ttu-id="c4a21-118">Этот атрибут является обязательным для любого **BUTTONGROUP**.</span><span class="sxs-lookup"><span data-stu-id="c4a21-118">This attribute is required for any **BUTTONGROUP**.</span></span>

<span data-ttu-id="c4a21-119">**ховеримаже**</span><span class="sxs-lookup"><span data-stu-id="c4a21-119">**hoverImage**</span></span>

<span data-ttu-id="c4a21-120">Это имя файла рисунка, который вы создали ранее, с двумя желтыми кнопками, которые считывают "Play" и "Close".</span><span class="sxs-lookup"><span data-stu-id="c4a21-120">This is the file name of the hover art file you created before, the one with the two yellow buttons that read "Play" and "Close".</span></span> <span data-ttu-id="c4a21-121">Это не является обязательным, но изображение для наведения помогает отправить отзыв пользователю.</span><span class="sxs-lookup"><span data-stu-id="c4a21-121">This is not required, but a hover image helps to provide feedback to the user.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c4a21-122">См. также</span><span class="sxs-lookup"><span data-stu-id="c4a21-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4a21-123">**Создание файла определения обложки**</span><span class="sxs-lookup"><span data-stu-id="c4a21-123">**Creating the Skin Definition File**</span></span>](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




