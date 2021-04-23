---
title: Атрибут непрозрачности (Fill) (VML)
description: Атрибут непрозрачности (Fill) (VML)
ms.assetid: abd2fe4d-6391-4413-80f0-549bcc74f42e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03b913498705e65fa7211db4b4cef039894d573a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793752"
---
# <a name="opacity-attribute-fillvml"></a><span data-ttu-id="223c9-103">Атрибут непрозрачности (Fill) (VML)</span><span class="sxs-lookup"><span data-stu-id="223c9-103">Opacity Attribute (Fill)(VML)</span></span>

<span data-ttu-id="223c9-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="223c9-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="223c9-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="223c9-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="223c9-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="223c9-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="223c9-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="223c9-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="223c9-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="223c9-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="223c9-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="223c9-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="223c9-110">Определяет прозрачность заливки.</span><span class="sxs-lookup"><span data-stu-id="223c9-110">Defines the transparency of a fill.</span></span> <span data-ttu-id="223c9-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="223c9-111">Read/write.</span></span> <span data-ttu-id="223c9-112">[Вгфрактион](msdn-online-vml-vgfraction-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="223c9-112">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span></span>

<span data-ttu-id="223c9-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="223c9-113">**Applies To**</span></span>

[<span data-ttu-id="223c9-114">Заполнить</span><span class="sxs-lookup"><span data-stu-id="223c9-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="223c9-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="223c9-115">**Tag Syntax**</span></span>

<span data-ttu-id="223c9-116"><v: Opacity *элемента* = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="223c9-116"><v: *element* opacity=" *expression* "></span></span>

<span data-ttu-id="223c9-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="223c9-117">**Script Syntax**</span></span>

<span data-ttu-id="223c9-118">*element* . Opacity = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="223c9-118">*element* .opacity="*expression*"</span></span>

<span data-ttu-id="223c9-119">*выражение* = *элемент*. Opacity</span><span class="sxs-lookup"><span data-stu-id="223c9-119">*expression*=*element*.opacity</span></span>

<span data-ttu-id="223c9-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="223c9-120">**Remarks**</span></span>

<span data-ttu-id="223c9-121">Значение по умолчанию — 1,0.</span><span class="sxs-lookup"><span data-stu-id="223c9-121">The default value is 1.0.</span></span>

<span data-ttu-id="223c9-122">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="223c9-122">*VML Standard Attribute*</span></span>

<span data-ttu-id="223c9-123">**Пример**</span><span class="sxs-lookup"><span data-stu-id="223c9-123">**Example**</span></span>

<span data-ttu-id="223c9-124">Заливка фигуры будет закрашена на 50% прозрачна.</span><span class="sxs-lookup"><span data-stu-id="223c9-124">The fill of the shape will be 50% transparent.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill opacity="50%" color="red"/>
   </v:shape>
```



 

 