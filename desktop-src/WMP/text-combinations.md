---
title: Сочетания текста
description: Сочетания текста
ms.assetid: 0220b77e-5f1e-4569-a8fe-5085e0c16338
keywords:
- Обложки мобильных устройств проигрывателя Windows Media, области
- обложки, области
- Справочник по обложкам, бегущим строки
- области в обложках, сочетания текста
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5668a9e18555b871c82bae7ed1826766ec9429e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532225"
---
# <a name="text-combinations"></a><span data-ttu-id="f3a75-107">Сочетания текста</span><span class="sxs-lookup"><span data-stu-id="f3a75-107">Text Combinations</span></span>

<span data-ttu-id="f3a75-108">Это значение представляет собой список сочетаний текстовых полей, разделенных запятыми.</span><span class="sxs-lookup"><span data-stu-id="f3a75-108">This value is a list of text display box combinations, separated by commas.</span></span> <span data-ttu-id="f3a75-109">Текстовые поля можно объединить с помощью символа «плюс», чтобы создать новое отображаемое значение бегущей строки, а любой текстовый тип, определенный в разделе текстовый тип, можно будет использовать в вашей области.</span><span class="sxs-lookup"><span data-stu-id="f3a75-109">Text display boxes can be joined together by a plus character to create a new marquee display value and any text type defined in the Text Type section can be used in your marquee.</span></span>

<span data-ttu-id="f3a75-110">При определении того, что следует отображать, проигрыватель Windows Media Mobile проверяет каждый элемент в списке, чтобы узнать, доступны ли все части.</span><span class="sxs-lookup"><span data-stu-id="f3a75-110">When determining what to display, Windows Media Player Mobile evaluates each item in the list to see if all parts are available.</span></span> <span data-ttu-id="f3a75-111">В противном случае вычисляется следующий элемент и т. д., пока не будут найдены все доступные части.</span><span class="sxs-lookup"><span data-stu-id="f3a75-111">If not, the next item is evaluated, and so on, until all the available parts have been found.</span></span> <span data-ttu-id="f3a75-112">Например, если нужно отобразить сведения об авторе и заголовке, но вы не уверены, доступны ли оба варианта, используйте следующее значение:</span><span class="sxs-lookup"><span data-stu-id="f3a75-112">For example, if you want to display Author and Title, but you're not sure whether both are available, use the following value:</span></span>


```C++
Title+Author, Title, Author

```



<span data-ttu-id="f3a75-113">В предыдущем примере заголовок + Author будет отображаться, если для элемента мультимедиа было определено название и автор.</span><span class="sxs-lookup"><span data-stu-id="f3a75-113">In the preceding example, the Title+Author will be displayed if the title and author have been defined for the media item.</span></span> <span data-ttu-id="f3a75-114">Если оба не определены, заголовок вычисляется и отображается, если он определен.</span><span class="sxs-lookup"><span data-stu-id="f3a75-114">If both are not defined, the Title is evaluated and displayed if defined.</span></span> <span data-ttu-id="f3a75-115">Если заголовок не определен, автор отображается, если он определен.</span><span class="sxs-lookup"><span data-stu-id="f3a75-115">If the Title is not defined, the Author is displayed if defined.</span></span> <span data-ttu-id="f3a75-116">Если ни один из этих параметров не определен, ничего не отображается.</span><span class="sxs-lookup"><span data-stu-id="f3a75-116">If neither is defined, then nothing is displayed.</span></span>

<span data-ttu-id="f3a75-117">При использовании знака «плюс» для объединения убедитесь, что у вас нет пробелов с обеих сторон знака «плюс».</span><span class="sxs-lookup"><span data-stu-id="f3a75-117">When using the plus sign for concatenation, be sure you have no spaces on either side of the plus sign.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f3a75-118">См. также</span><span class="sxs-lookup"><span data-stu-id="f3a75-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f3a75-119">**Marquee**</span><span class="sxs-lookup"><span data-stu-id="f3a75-119">**Marquee**</span></span>](marquee.md)
</dt> <dt>

[<span data-ttu-id="f3a75-120">**Тип текста**</span><span class="sxs-lookup"><span data-stu-id="f3a75-120">**Text Type**</span></span>](text-type.md)
</dt> </dl>

 

 




