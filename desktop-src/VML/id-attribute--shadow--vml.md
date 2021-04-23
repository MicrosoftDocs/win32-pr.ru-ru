---
title: Атрибут ID (shadow) (VML)
description: Атрибут ID (shadow) (VML)
ms.assetid: ca20b6b9-a41c-4073-9178-77eb0f918327
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d51a5917f9ef71e3c4acea7ec1ed2e5cf90aef8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792408"
---
# <a name="id-attribute-shadowvml"></a><span data-ttu-id="84f63-103">Атрибут ID (shadow) (VML)</span><span class="sxs-lookup"><span data-stu-id="84f63-103">ID Attribute (Shadow)(VML)</span></span>

<span data-ttu-id="84f63-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="84f63-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="84f63-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="84f63-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="84f63-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="84f63-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="84f63-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="84f63-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="84f63-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="84f63-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="84f63-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="84f63-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="84f63-110">Задает имя, которое предоставляет уникальный идентификатор для тени.</span><span class="sxs-lookup"><span data-stu-id="84f63-110">Specifies a name that provides a unique identifier for a shadow.</span></span> <span data-ttu-id="84f63-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="84f63-111">Read/write.</span></span> <span data-ttu-id="84f63-112">**Строка**.</span><span class="sxs-lookup"><span data-stu-id="84f63-112">**String**.</span></span>

<span data-ttu-id="84f63-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="84f63-113">**Applies To**</span></span>

[<span data-ttu-id="84f63-114">Shadow</span><span class="sxs-lookup"><span data-stu-id="84f63-114">Shadow</span></span>](msdn-online-vml-shadow-element.md)

<span data-ttu-id="84f63-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="84f63-115">**Tag Syntax**</span></span>

<span data-ttu-id="84f63-116"><v: *element* ID = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="84f63-116"><v: *element* id=" *expression* "></span></span>

<span data-ttu-id="84f63-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="84f63-117">**Script Syntax**</span></span>

<span data-ttu-id="84f63-118">*element* . ID = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="84f63-118">*element* .id="*expression*"</span></span>

<span data-ttu-id="84f63-119">*выражение* = *element*. ID</span><span class="sxs-lookup"><span data-stu-id="84f63-119">*expression*=*element*.id</span></span>

<span data-ttu-id="84f63-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="84f63-120">**Remarks**</span></span>

<span data-ttu-id="84f63-121">Используйте **идентификатор** для ссылки на определенную тень.</span><span class="sxs-lookup"><span data-stu-id="84f63-121">Use **ID** to refer to a specific shadow.</span></span> <span data-ttu-id="84f63-122">После создания тени и присвоения ей идентификатора можно использовать имя идентификатора, если вы хотите управлять тенью.</span><span class="sxs-lookup"><span data-stu-id="84f63-122">Once you have created a shadow and given it an ID, you can use the ID name when you want to manipulate the shadow.</span></span>

<span data-ttu-id="84f63-123">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="84f63-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="84f63-124">**Пример**</span><span class="sxs-lookup"><span data-stu-id="84f63-124">**Example**</span></span>

<span data-ttu-id="84f63-125">Фигура имеет теневой идентификатор с именем «мишадов».</span><span class="sxs-lookup"><span data-stu-id="84f63-125">The shape has a shadow ID called "myshadow".</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow id="myshadow" on="True"/>
   </v:shape>
```



 

 