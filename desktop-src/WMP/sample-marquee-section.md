---
title: Пример раздела бегущей строки
description: Пример раздела бегущей строки
ms.assetid: 44ed3257-2e1a-4b8d-9d55-a13b0400422d
keywords:
- Обложки мобильных устройств проигрывателя Windows Media, области
- обложки, области
- Справочник по обложкам, бегущим строки
- области в обложках, раздел бегущей строки
- файлы определения обложки, раздел бегущей строки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f66588d81b22051a9289a80c8733d5cfe154bed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486964"
---
# <a name="sample-marquee-section"></a><span data-ttu-id="df745-108">Пример раздела бегущей строки</span><span class="sxs-lookup"><span data-stu-id="df745-108">Sample Marquee Section</span></span>

<span data-ttu-id="df745-109">В следующих строках показан типичный раздел области в файле определения обложки:</span><span class="sxs-lookup"><span data-stu-id="df745-109">The following lines show a typical Marquee section of a skin definition file:</span></span>


```C++
//  <Location>   <Font>       <Color>      <Text item combinations>

//  ----------   ------       -------      ------------------------

    3,2,234,20   Tahoma,12,N  255,0,0    Title+Author, Title, Author


```



<span data-ttu-id="df745-110">Это определяет поле отображения области выделения, которое показывает заголовок и автора, если определены оба значения, заголовок, если определено только название, или имя автора, если определен только автор.</span><span class="sxs-lookup"><span data-stu-id="df745-110">This defines a marquee display box that shows the title and author if both are defined, the title if only Title is defined, or the name of the author if only Author is defined.</span></span> <span data-ttu-id="df745-111">Если ни один из этих параметров не определен, ничего не отображается.</span><span class="sxs-lookup"><span data-stu-id="df745-111">If neither is defined, nothing will be displayed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="df745-112">См. также</span><span class="sxs-lookup"><span data-stu-id="df745-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df745-113">**Marquee**</span><span class="sxs-lookup"><span data-stu-id="df745-113">**Marquee**</span></span>](marquee.md)
</dt> </dl>

 

 




