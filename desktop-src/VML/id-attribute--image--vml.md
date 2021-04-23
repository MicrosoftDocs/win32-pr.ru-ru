---
title: Атрибут ID (Image) (VML)
description: Атрибут ID (Image) (VML)
ms.assetid: d85a6d56-5896-4ac0-85c7-0edc72928c62
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40ac489331699ca6fe040cddc0bebb408d524de7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413649"
---
# <a name="id-attribute-imagevml"></a><span data-ttu-id="2f00d-103">Атрибут ID (Image) (VML)</span><span class="sxs-lookup"><span data-stu-id="2f00d-103">ID Attribute (Image)(VML)</span></span>

<span data-ttu-id="2f00d-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="2f00d-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="2f00d-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="2f00d-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="2f00d-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="2f00d-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="2f00d-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="2f00d-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="2f00d-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="2f00d-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="2f00d-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="2f00d-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="2f00d-110">Определяет имя, которое предоставляет уникальный идентификатор для изображения.</span><span class="sxs-lookup"><span data-stu-id="2f00d-110">Defines a name that provides a unique identifier for an image.</span></span> <span data-ttu-id="2f00d-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="2f00d-111">Read/write.</span></span> <span data-ttu-id="2f00d-112">**Строка**.</span><span class="sxs-lookup"><span data-stu-id="2f00d-112">**String**.</span></span>

<span data-ttu-id="2f00d-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="2f00d-113">**Applies To**</span></span>

[<span data-ttu-id="2f00d-114">ImageData</span><span class="sxs-lookup"><span data-stu-id="2f00d-114">ImageData</span></span>](msdn-online-vml-imagedata-element.md)

<span data-ttu-id="2f00d-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="2f00d-115">**Tag Syntax**</span></span>

<span data-ttu-id="2f00d-116"><v: *element* ID = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="2f00d-116"><v: *element* id=" *expression* "></span></span>

<span data-ttu-id="2f00d-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="2f00d-117">**Script Syntax**</span></span>

<span data-ttu-id="2f00d-118">*element* . ID = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="2f00d-118">*element* .id="*expression*"</span></span>

<span data-ttu-id="2f00d-119">*выражение* = *element*. ID</span><span class="sxs-lookup"><span data-stu-id="2f00d-119">*expression*=*element*.id</span></span>

<span data-ttu-id="2f00d-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="2f00d-120">**Remarks**</span></span>

<span data-ttu-id="2f00d-121">Используйте **идентификатор** для ссылки на конкретный образ.</span><span class="sxs-lookup"><span data-stu-id="2f00d-121">Use **ID** to refer to a specific image.</span></span> <span data-ttu-id="2f00d-122">После создания образа и присвоения ему идентификатора можно использовать имя идентификатора, если требуется управлять изображением.</span><span class="sxs-lookup"><span data-stu-id="2f00d-122">Once you have created an image and given it an ID, you can use the ID name when you want to manipulate the image.</span></span>

<span data-ttu-id="2f00d-123">**Стандартный атрибут VML**</span><span class="sxs-lookup"><span data-stu-id="2f00d-123">**VML Standard Attribute**</span></span>

<span data-ttu-id="2f00d-124">**Пример**</span><span class="sxs-lookup"><span data-stu-id="2f00d-124">**Example**</span></span>

<span data-ttu-id="2f00d-125">Фигура имеет идентификатор **имажедата** с именем MyImage.</span><span class="sxs-lookup"><span data-stu-id="2f00d-125">The shape has an **ImageData** ID called "myimage".</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata id="myimage" src="kids.jpg"/>
   </v:shape>
```



 

 