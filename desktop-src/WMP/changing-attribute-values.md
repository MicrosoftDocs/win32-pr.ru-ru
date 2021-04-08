---
title: Изменение значений атрибутов
description: Изменение значений атрибутов
ms.assetid: c7dd7355-453c-44a5-9932-c41bb3ae2e40
keywords:
- Проигрыватель Windows Media, атрибуты для элементов мультимедиа
- Объектная модель проигрывателя Windows Media, атрибуты элементов мультимедиа
- Объектная модель, атрибуты элементов мультимедиа
- Проигрыватель Windows Media Mobile, атрибуты для элементов мультимедиа
- Элемент управления ActiveX проигрывателя Windows Media, атрибуты для элементов мультимедиа
- Элемент управления мобильными устройствами ActiveX проигрывателя Windows Media, атрибуты для элементов мультимедиа
- Элемент управления ActiveX, атрибуты для элементов мультимедиа
- Библиотека проигрывателя Windows Media, атрибуты для элементов мультимедиа
- Библиотека, атрибуты для элементов мультимедиа
- атрибуты, изменение значений
- изменение значений атрибутов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 133e004e1140bdaac19b22be8bc1c77fe9327601
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068125"
---
# <a name="changing-attribute-values"></a><span data-ttu-id="87030-114">Изменение значений атрибутов</span><span class="sxs-lookup"><span data-stu-id="87030-114">Changing Attribute Values</span></span>

<span data-ttu-id="87030-115">Можно изменить значение атрибута, если веб-страница или приложение имеет доступ на чтение и запись к библиотеке, а атрибут может быть как прочитанным, так и записанным.</span><span class="sxs-lookup"><span data-stu-id="87030-115">You can change the value of an attribute if your webpage or application has read/write access to the library and the attribute can be both read and written.</span></span>

<span data-ttu-id="87030-116">Можно изменить атрибут текущего элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="87030-116">You can change an attribute of the current media item.</span></span> <span data-ttu-id="87030-117">Чтобы изменить атрибуты нескольких элементов мультимедиа, можно назначить каждое из них в окне « *проигрыватель*». Свойство **куррентмедиа** .</span><span class="sxs-lookup"><span data-stu-id="87030-117">To change attributes of multiple media items, you can assign each one in turn to the *Player*.**currentMedia** property.</span></span>

<span data-ttu-id="87030-118">В этом разделе объект **Player** был определен следующим образом:</span><span class="sxs-lookup"><span data-stu-id="87030-118">Throughout this topic, the **Player** object was defined in the following manner:</span></span>


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



<span data-ttu-id="87030-119">Чтобы изменить атрибут, вызовите *проигрыватель*. *куррентмедиа*. метод **сетитеминфо** , как показано в следующем примере C#.</span><span class="sxs-lookup"><span data-stu-id="87030-119">To change an attribute, call the *Player*.*currentMedia*.**setItemInfo** method as shown in the following C# example.</span></span>


```C++
IWMPMedia3 media;
// Initialize the Media object
media = Player.currentMedia;
// Set the new genre value
media.setItemInfo("WM/Genre", "My New Genre");

```



<span data-ttu-id="87030-120">Рекомендуется вызывать *носитель*. метод **исреадонлитем** , позволяющий определить, можно ли изменить определенный атрибут.</span><span class="sxs-lookup"><span data-stu-id="87030-120">We recommend that you call the *Media*.**isReadOnlyItem** method to determine whether you can change a particular attribute.</span></span>

> [!Note]  
> <span data-ttu-id="87030-121">При внедрении элемента управления в приложение измененные атрибуты файла не будут записываться в файл мультимедиа до тех пор, пока пользователь не запустит проигрыватель Windows Media.</span><span class="sxs-lookup"><span data-stu-id="87030-121">If you embed the control in your application, file attributes that you change will not be written to the digital media file until the user runs Windows Media Player.</span></span> <span data-ttu-id="87030-122">При использовании элемента управления в удаленном приложении, написанном на языке C++, измененные атрибуты файла будут записаны в файл мультимедиа вскоре после внесения изменений.</span><span class="sxs-lookup"><span data-stu-id="87030-122">If you use the control in a remoted application written in C++, file attributes that you change will be written to the digital media file shortly after you make the changes.</span></span> <span data-ttu-id="87030-123">В любом случае изменения немедленно становятся доступными через библиотеку.</span><span class="sxs-lookup"><span data-stu-id="87030-123">In either case, the changes are immediately available to you through the library.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="87030-124">См. также</span><span class="sxs-lookup"><span data-stu-id="87030-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="87030-125">**Атрибуты элемента мультимедиа**</span><span class="sxs-lookup"><span data-stu-id="87030-125">**Media Item Attributes**</span></span>](media-item-attributes.md)
</dt> <dt>

[<span data-ttu-id="87030-126">**Доступ к библиотеке**</span><span class="sxs-lookup"><span data-stu-id="87030-126">**Library Access**</span></span>](library-access.md)
</dt> <dt>

[<span data-ttu-id="87030-127">**Объект мультимедиа**</span><span class="sxs-lookup"><span data-stu-id="87030-127">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="87030-128">**Считывание значений атрибутов**</span><span class="sxs-lookup"><span data-stu-id="87030-128">**Reading Attribute Values**</span></span>](reading-attribute-values.md)
</dt> </dl>

 

 




