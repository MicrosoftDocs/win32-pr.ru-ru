---
title: Атрибут ID (Fill) (VML)
description: Атрибут ID (Fill) (VML)
ms.assetid: 56865772-51bd-4729-8e56-6b00e3c6bed0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4820c4f7a23cf940c199f27243d8ad5601390a84
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070278"
---
# <a name="id-attribute-fillvml"></a><span data-ttu-id="1c566-103">Атрибут ID (Fill) (VML)</span><span class="sxs-lookup"><span data-stu-id="1c566-103">ID Attribute (Fill)(VML)</span></span>

<span data-ttu-id="1c566-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="1c566-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="1c566-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="1c566-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="1c566-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="1c566-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="1c566-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="1c566-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="1c566-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="1c566-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="1c566-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="1c566-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="1c566-110">Имя, которое предоставляет уникальный идентификатор для заливки.</span><span class="sxs-lookup"><span data-stu-id="1c566-110">A name that provides a unique identifier for a fill.</span></span> <span data-ttu-id="1c566-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="1c566-111">Read/write.</span></span> <span data-ttu-id="1c566-112">**Строка**.</span><span class="sxs-lookup"><span data-stu-id="1c566-112">**String**.</span></span>

<span data-ttu-id="1c566-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="1c566-113">**Applies To**</span></span>

[<span data-ttu-id="1c566-114">Заполнить</span><span class="sxs-lookup"><span data-stu-id="1c566-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="1c566-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="1c566-115">**Tag Syntax**</span></span>

<span data-ttu-id="1c566-116"><v: *element* ID = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="1c566-116"><v: *element* id=" *expression* "></span></span>

<span data-ttu-id="1c566-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="1c566-117">**Script Syntax**</span></span>

<span data-ttu-id="1c566-118">*element* . ID = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="1c566-118">*element* .id="*expression*"</span></span>

<span data-ttu-id="1c566-119">*выражение* = *element*. ID</span><span class="sxs-lookup"><span data-stu-id="1c566-119">*expression*=*element*.id</span></span>

<span data-ttu-id="1c566-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="1c566-120">**Remarks**</span></span>

<span data-ttu-id="1c566-121">Используйте **ID** для ссылки на определенную заливку.</span><span class="sxs-lookup"><span data-stu-id="1c566-121">Use **ID** to refer to a specific fill.</span></span> <span data-ttu-id="1c566-122">После создания заливки и присвоения ей идентификатора можно использовать имя идентификатора, если требуется управлять заливкой.</span><span class="sxs-lookup"><span data-stu-id="1c566-122">Once you have created a fill and given it an ID, you can use the ID name when you want to manipulate the fill.</span></span>

<span data-ttu-id="1c566-123">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="1c566-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="1c566-124">**Пример**</span><span class="sxs-lookup"><span data-stu-id="1c566-124">**Example**</span></span>

<span data-ttu-id="1c566-125">Фигура имеет идентификатор заполнения с именем «мифилл».</span><span class="sxs-lookup"><span data-stu-id="1c566-125">The shape has a fill ID called "myfill".</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill id="myfill"/>
   </v:shape>
```



 

 