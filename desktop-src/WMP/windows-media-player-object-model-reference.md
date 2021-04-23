---
title: Справочник по объектной модели проигрывателя Windows Media
description: Справочник по объектной модели проигрывателя Windows Media
ms.assetid: af313b94-230b-47d7-a3ad-7e23b669886f
keywords:
- Проигрыватель Windows Media, объектная модель
- Проигрыватель Windows Media Mobile, объектная модель
- Объектная модель проигрывателя Windows Media, Справочник
- Объектная модель, Справочник
- Элемент управления ActiveX, Справочник
- Элемент управления ActiveX проигрывателя Windows Media, Справочник
- Элемент управления ActiveX проигрывателя Windows Media Mobile, Справочник
- Справочник по объектной модели, сведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6128ff3f69968ddf4f8a35955907a18876ef090
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068498"
---
# <a name="windows-media-player-object-model-reference"></a><span data-ttu-id="f0a6d-111">Справочник по объектной модели проигрывателя Windows Media</span><span class="sxs-lookup"><span data-stu-id="f0a6d-111">Windows Media Player Object Model Reference</span></span>

<span data-ttu-id="f0a6d-112">Справочные разделы объектной модели проигрывателя Windows Media содержат подробные сведения об объектной модели элемента управления ActiveX проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="f0a6d-112">The Windows Media Player Object Model Reference sections contain detailed information about the Windows Media Player ActiveX control object model.</span></span> <span data-ttu-id="f0a6d-113">Объектная модель предоставляет интерфейсы, позволяющие разработчикам добавлять функции проигрывателя Windows Media на веб-страницы, программы C++ и приложения .NET.</span><span class="sxs-lookup"><span data-stu-id="f0a6d-113">The object model provides interfaces that let developers add Windows Media Player functionality to webpages, C++ programs, and .NET applications.</span></span>

<span data-ttu-id="f0a6d-114">Справочник по объектной модели для сценариев представлен в стиле, предназначенном для использования с языками скриптов, такими как Microsoft JScript, и документирует объектную модель с точки зрения объектов со связанными свойствами, методами и событиями.</span><span class="sxs-lookup"><span data-stu-id="f0a6d-114">The Object Model Reference for Scripting is presented in a style designed for use with script languages like Microsoft JScript, and it documents the object model in terms of objects with their associated properties, methods, and events.</span></span>

<span data-ttu-id="f0a6d-115">Справочник по объектной модели для C++ содержит документацию по COM-интерфейсам, которые программисты C++ могут использовать для взаимодействия с элементом управления ActiveX проигрывателя Windows Media или мобильным элементом управления ActiveX проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="f0a6d-115">The Object Model Reference for C++ provides documentation for COM interfaces that C++ programmers can use to communicate with the Windows Media Player ActiveX control or the Windows Media Player Mobile ActiveX control.</span></span> <span data-ttu-id="f0a6d-116">Большая часть этих интерфейсов реализована в Windows Media Player Control и вызывается приложением C++.</span><span class="sxs-lookup"><span data-stu-id="f0a6d-116">Most of these interfaces are implemented by Windows Media Player control and called by the C++ application.</span></span> <span data-ttu-id="f0a6d-117">Однако некоторые интерфейсы (например, **ивмпевентс** и **ивмпремотемедиасервицес**) реализуются с помощью приложения C++ и вызываются элементом управления проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="f0a6d-117">However, some of the interfaces (for example, **IWMPEvents** and **IWMPRemoteMediaServices**) are implemented by the C++ application and called by the Windows Media Player control.</span></span>

<span data-ttu-id="f0a6d-118">В справочнике по объектной модели для Visual Basic .NET и C# представлена документация по свойствам, методам и событиям объекта **аксвиндовсмедиаплайер** , а также интерфейсам элемента управления ActiveX проигрывателя Windows Media, которые доступны через COM-взаимодействие в решении, закодированном в Visual Studio .NET 2002 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="f0a6d-118">The Object Model Reference for Visual Basic .NET and C# provides documentation for the properties, methods, and events of the **AxWindowsMediaPlayer** object and for interfaces to the Windows Media Player ActiveX control that are available through COM interoperability in a solution coded in Visual Studio .NET 2002 or later.</span></span>

<span data-ttu-id="f0a6d-119">В справочнике по объектной модели проигрывателя Windows Media содержатся следующие разделы.</span><span class="sxs-lookup"><span data-stu-id="f0a6d-119">The Windows Media Player Object Model Reference contains the following sections.</span></span>



| <span data-ttu-id="f0a6d-120">Section</span><span class="sxs-lookup"><span data-stu-id="f0a6d-120">Section</span></span>                                                                                                        | <span data-ttu-id="f0a6d-121">Описание</span><span class="sxs-lookup"><span data-stu-id="f0a6d-121">Description</span></span>                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f0a6d-122">Справочник по объектной модели для создания сценариев</span><span class="sxs-lookup"><span data-stu-id="f0a6d-122">Object Model Reference for Scripting</span></span>](object-model-reference-for-scripting.md)                               | <span data-ttu-id="f0a6d-123">Содержит справочную документацию по свойствам, методам и событиям, которые объектная модель делает доступной для языков сценариев.</span><span class="sxs-lookup"><span data-stu-id="f0a6d-123">Provides reference documentation for the properties, methods, and events that the object model makes available to scripting languages.</span></span> <span data-ttu-id="f0a6d-124">Эти сведения также полезны для Visual Basicного программирования 6,0.</span><span class="sxs-lookup"><span data-stu-id="f0a6d-124">This information is also useful for Visual Basic 6.0 programming.</span></span> |
| [<span data-ttu-id="f0a6d-125">Справочник по объектной модели для C++</span><span class="sxs-lookup"><span data-stu-id="f0a6d-125">Object Model Reference for C++</span></span>](object-model-reference-for-c.md)                                             | <span data-ttu-id="f0a6d-126">Содержит справочную документацию по интерфейсам C++.</span><span class="sxs-lookup"><span data-stu-id="f0a6d-126">Provides reference documentation for C++ interfaces.</span></span>                                                                                                                                                     |
| [<span data-ttu-id="f0a6d-127">Справочник по объектной модели для Visual Basic .NET и C #</span><span class="sxs-lookup"><span data-stu-id="f0a6d-127">Object Model Reference for Visual Basic .NET and C#</span></span>](object-model-reference-for-visual-basic--net-and-c.md) | <span data-ttu-id="f0a6d-128">Справочная документация по объектам и интерфейсам, доступным для Visual Basic программистов .NET и C# с помощью COM-взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="f0a6d-128">Provides reference documentation for objects and interfaces available to Visual Basic .NET and C# programmers through COM interoperability.</span></span>                                                             |
| [<span data-ttu-id="f0a6d-129">Ссылка на атрибут</span><span class="sxs-lookup"><span data-stu-id="f0a6d-129">Attribute Reference</span></span>](attribute-reference.md)                                                                 | <span data-ttu-id="f0a6d-130">Содержит справочную документацию по атрибутам метаданных, представляющим интерес для разработчиков пакета SDK для проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="f0a6d-130">Provides reference documentation for metadata attributes that are of interest to Windows Media Player SDK developers.</span></span>                                                                                    |
| [<span data-ttu-id="f0a6d-131">Типы перечислений</span><span class="sxs-lookup"><span data-stu-id="f0a6d-131">Enumeration Types</span></span>](enumeration-types.md)                                                                     | <span data-ttu-id="f0a6d-132">Содержит справочную документацию по типам перечислений, используемым интерфейсами C++ и .NET.</span><span class="sxs-lookup"><span data-stu-id="f0a6d-132">Provides reference documentation for the enumeration types that are used by the C++ and .NET interfaces.</span></span>                                                                                                 |



 

## <a name="related-topics"></a><span data-ttu-id="f0a6d-133">См. также</span><span class="sxs-lookup"><span data-stu-id="f0a6d-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0a6d-134">**Объектная модель проигрывателя Windows Media**</span><span class="sxs-lookup"><span data-stu-id="f0a6d-134">**Windows Media Player Object Model**</span></span>](windows-media-player-object-model.md)
</dt> </dl>

 

 




