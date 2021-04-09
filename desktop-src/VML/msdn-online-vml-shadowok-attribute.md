---
title: Атрибут Шадовок VML
description: Атрибут Шадовок VML
ms.assetid: 88400bf5-f41c-4495-a5d0-9b35c1cae9f7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9e6b4ca6b98ce66208e906c45fd560324121e8a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070037"
---
# <a name="vml-shadowok-attribute"></a><span data-ttu-id="58fae-103">Атрибут Шадовок VML</span><span class="sxs-lookup"><span data-stu-id="58fae-103">VML ShadowOK Attribute</span></span>

<span data-ttu-id="58fae-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="58fae-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="58fae-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="58fae-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="58fae-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="58fae-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="58fae-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="58fae-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="58fae-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="58fae-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="58fae-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="58fae-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="58fae-110">Определяет, будет ли отображаться тень.</span><span class="sxs-lookup"><span data-stu-id="58fae-110">Determines whether a shadow will be displayed.</span></span> <span data-ttu-id="58fae-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="58fae-111">Read/write.</span></span> <span data-ttu-id="58fae-112">**Вгтристате**.</span><span class="sxs-lookup"><span data-stu-id="58fae-112">**VgTriState**.</span></span>

<span data-ttu-id="58fae-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="58fae-113">**Applies To**</span></span>

[<span data-ttu-id="58fae-114">Путь</span><span class="sxs-lookup"><span data-stu-id="58fae-114">Path</span></span>](msdn-online-vml-path-element.md)

<span data-ttu-id="58fae-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="58fae-115">**Tag Syntax**</span></span>

<span data-ttu-id="58fae-116"><v: *element* шадовок = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="58fae-116"><v: *element* shadowok=" *expression* "></span></span>

<span data-ttu-id="58fae-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="58fae-117">**Script Syntax**</span></span>

<span data-ttu-id="58fae-118">*element* . шадовок = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="58fae-118">*element* .shadowok="*expression*"</span></span>

<span data-ttu-id="58fae-119">*выражение* = *element*. шадовок</span><span class="sxs-lookup"><span data-stu-id="58fae-119">*expression*=*element*.shadowok</span></span>

<span data-ttu-id="58fae-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="58fae-120">**Remarks**</span></span>

<span data-ttu-id="58fae-121">Если **значение равно false**, то путь не может иметь тень.</span><span class="sxs-lookup"><span data-stu-id="58fae-121">If **False**, the path cannot have a shadow.</span></span> <span data-ttu-id="58fae-122">Значение по умолчанию равно **True**.</span><span class="sxs-lookup"><span data-stu-id="58fae-122">The default is **True**.</span></span> <span data-ttu-id="58fae-123">Этот атрибут переопределяет все другие теневые атрибуты в родительском или **скрытом** элементе.</span><span class="sxs-lookup"><span data-stu-id="58fae-123">This attribute overrides all other shadow attributes in the parent or **Shadow** element.</span></span>

<span data-ttu-id="58fae-124">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="58fae-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="58fae-125">**Пример**</span><span class="sxs-lookup"><span data-stu-id="58fae-125">**Example**</span></span>

<span data-ttu-id="58fae-126">Фигура не будет иметь тень.</span><span class="sxs-lookup"><span data-stu-id="58fae-126">The shape will not have a shadow.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="green"
   style="top:1;left:1;width:50;height:50">
   <v:shadow on="True" offset="5pt,5pt" color="blue"/>
   <v:path id= "myPath" shadowok="False" v="m 1,1 l 1,200, 200,200, 200,1 x e"/>
   </v:shape>
```



 

 