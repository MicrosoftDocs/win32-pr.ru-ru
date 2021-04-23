---
title: Marquee
description: Marquee
ms.assetid: 2715732a-25cc-4ba9-9aa6-181ebb9e1d1c
keywords:
- Обложки мобильных устройств проигрывателя Windows Media, области
- обложки, области
- Справочник по обложкам, бегущим строки
- области в обложках, о
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7efa2db2c6079d47d207240b18a57ebbf7e41ae1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411182"
---
# <a name="marquee"></a><span data-ttu-id="66845-107">Marquee</span><span class="sxs-lookup"><span data-stu-id="66845-107">Marquee</span></span>

<span data-ttu-id="66845-108">Бегущая строка — это текстовое поле с прокруткой, которое отображает информацию из одного или нескольких текстовых полей.</span><span class="sxs-lookup"><span data-stu-id="66845-108">A marquee is a scrolling text display box that displays information from one or more text display boxes.</span></span> <span data-ttu-id="66845-109">Добавлять области не нужно, но это может быть очень полезно при наличии подробных сведений, которые необходимо отобразить пользователю в ограниченном пространстве.</span><span class="sxs-lookup"><span data-stu-id="66845-109">You do not need to add a marquee, but it can be very useful when you have detailed information you want to display to the user in a limited space.</span></span>

<span data-ttu-id="66845-110">Текст в области будет прокручиваться, только если выполняются оба следующих условия.</span><span class="sxs-lookup"><span data-stu-id="66845-110">The text in the marquee will scroll only if both of the following conditions are met:</span></span>

-   <span data-ttu-id="66845-111">Имеется больше текста, отображаемого в области выделения, чем ширина поля "область экрана".</span><span class="sxs-lookup"><span data-stu-id="66845-111">You have more text to display in the marquee than the width of the marquee display box.</span></span>
-   <span data-ttu-id="66845-112">Элемент мультимедиа остановлен или приостановлен.</span><span class="sxs-lookup"><span data-stu-id="66845-112">The media item is either stopped or paused.</span></span>

<span data-ttu-id="66845-113">Раздел "область" в файле определения обложки должен начинаться с этой строки:</span><span class="sxs-lookup"><span data-stu-id="66845-113">The Marquee section of the skin definition file must begin with this line:</span></span>


```C++
[ Marquee ]

```



> [!Note]  
> <span data-ttu-id="66845-114">Для обеспечения совместимости с версиями проигрывателя Windows Media Mobile, более ранними, чем проигрыватель Windows Media 10 Mobile, использование "Маркуис" в файле определения обложки по-прежнему считается действительным.</span><span class="sxs-lookup"><span data-stu-id="66845-114">To maintain compatibility with versions of Windows Media Player Mobile older than Windows Media Player 10 Mobile, using "Marquis" in a skin definition file is still considered valid.</span></span>

 

<span data-ttu-id="66845-115">Затем необходимо добавить одну или несколько строк, содержащих сведения о каждом из окон «бегущая строка» в обложке.</span><span class="sxs-lookup"><span data-stu-id="66845-115">You then must add one or more lines that contain information about each of the marquee display boxes in your skin.</span></span>


```C++
    3,2,234,20   Tahoma,12,N  255,0,0    Playlist, Time, Filename

```



<span data-ttu-id="66845-116">Для раздела бегущей строки в файле определения обложки можно использовать следующий шаблон:</span><span class="sxs-lookup"><span data-stu-id="66845-116">You can use the following template for the Marquee section of your skin definition file:</span></span>


```C++
//  <Location>   <Font>       <Color>      <Text item combinations>
//  ----------   ------       -------      ------------------------

```



<span data-ttu-id="66845-117">Необходимо использовать следующий порядок для получения сведений в каждой строке раздела бегущая строка (каждая часть строки является обязательной):</span><span class="sxs-lookup"><span data-stu-id="66845-117">You must use the following order for information in each line of the Marquee section (each part of the line is required):</span></span>

1.  [<span data-ttu-id="66845-118">Расположение области</span><span class="sxs-lookup"><span data-stu-id="66845-118">Marquee Location</span></span>](marquee-location.md)
2.  [<span data-ttu-id="66845-119">Шрифт бегущей строки</span><span class="sxs-lookup"><span data-stu-id="66845-119">Marquee Font</span></span>](marquee-font.md)
3.  [<span data-ttu-id="66845-120">Цвет бегущей строки</span><span class="sxs-lookup"><span data-stu-id="66845-120">Marquee Color</span></span>](marquee-color.md)
4.  [<span data-ttu-id="66845-121">Сочетания текста</span><span class="sxs-lookup"><span data-stu-id="66845-121">Text Combinations</span></span>](text-combinations.md)

<span data-ttu-id="66845-122">Пример кода области см. в [разделе Sample Marquee](sample-marquee-section.md).</span><span class="sxs-lookup"><span data-stu-id="66845-122">For an example of Marquee code, see [Sample Marquee Section](sample-marquee-section.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="66845-123">См. также</span><span class="sxs-lookup"><span data-stu-id="66845-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="66845-124">**Справочник по обложкам**</span><span class="sxs-lookup"><span data-stu-id="66845-124">**Skin Reference**</span></span>](skin-reference.md)
</dt> </dl>

 

 




