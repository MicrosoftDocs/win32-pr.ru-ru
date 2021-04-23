---
title: Рейтинги
description: Рейтинги
ms.assetid: babc9db5-2782-4261-a571-acb7be4ea770
keywords:
- Обложки мобильных устройств проигрывателя Windows Media, оценки
- обложки, оценки
- Справочник по обложек, Оценка
- оценки в обложках
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edb90908c725fcb525e0be1547c27c588a4220c6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105710123"
---
# <a name="ratings"></a><span data-ttu-id="de19d-107">Рейтинги</span><span class="sxs-lookup"><span data-stu-id="de19d-107">Ratings</span></span>

<span data-ttu-id="de19d-108">При создании обложки для проигрывателя Windows Media 10,1 Mobile можно отобразить рейтинг, связанный с содержимым Windows Media Audio, которое сейчас воспроизводится.</span><span class="sxs-lookup"><span data-stu-id="de19d-108">When you create a skin for Windows Media Player 10.1 Mobile, you can display the rating associated with Windows Media Audio-based content that is currently playing.</span></span> <span data-ttu-id="de19d-109">Оценка отображается в виде звезды с цифрой.</span><span class="sxs-lookup"><span data-stu-id="de19d-109">The rating is displayed as a star with a number on it.</span></span> <span data-ttu-id="de19d-110">Звездочка будет пронумерована от одной до пяти, обозначая текущую оценку этого содержимого.</span><span class="sxs-lookup"><span data-stu-id="de19d-110">The star will be numbered one through five, denoting the current rating for that content.</span></span> <span data-ttu-id="de19d-111">Если содержимое не оценивается, звездочка будет пронумерована нуль.</span><span class="sxs-lookup"><span data-stu-id="de19d-111">If the content is not rated, the star will be numbered zero.</span></span>

<span data-ttu-id="de19d-112">Раздел рейтингов файла определения обложки начинается со следующей строки:</span><span class="sxs-lookup"><span data-stu-id="de19d-112">The Ratings section of the skin definition file begins with this line:</span></span>


```C++
[ Ratings ]

```



<span data-ttu-id="de19d-113">Затем необходимо добавить строку, содержащую сведения о размере и расположении значка оценки в обложке.</span><span class="sxs-lookup"><span data-stu-id="de19d-113">You then must add a line that contains information about the size and location of your ratings icon in your skin.</span></span>


```C++
147, 3, 22, 21       ratings96S.gif

```



<span data-ttu-id="de19d-114">Для раздела рейтингов файла определения обложки можно использовать следующий шаблон:</span><span class="sxs-lookup"><span data-stu-id="de19d-114">You can use the following template for the Ratings section of your skin definition file:</span></span>


```C++
// <Location>           <Image>
// ---------------      --------------------
```



<span data-ttu-id="de19d-115">Можно также назначить значение оценки элементу мультимедиа с помощью пользовательского интерфейса проигрывателя Windows Media 10,1 Mobile, а при следующем синхронизации устройства с компьютером новое значение рейтинга будет распространяться на этот элемент мультимедиа, если он находится в библиотеке проигрывателя Windows Media 10.</span><span class="sxs-lookup"><span data-stu-id="de19d-115">You can also assign a ratings value to a media item through the user interface in Windows Media Player 10.1 Mobile, and the next time the device synchronizes with the a computer, the new ratings value will be propagated to that media item if it resides in the Windows Media Player 10 library.</span></span>

## <a name="related-topics"></a><span data-ttu-id="de19d-116">См. также</span><span class="sxs-lookup"><span data-stu-id="de19d-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="de19d-117">**Справочник по обложкам**</span><span class="sxs-lookup"><span data-stu-id="de19d-117">**Skin Reference**</span></span>](skin-reference.md)
</dt> </dl>

 

 




