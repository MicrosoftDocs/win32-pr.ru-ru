---
title: Атрибут ID (TextBox) (VML)
description: Атрибут ID (TextBox) (VML)
ms.assetid: b9eb75cc-4d0a-4e83-a897-e35995ae7c53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b39ac566e7b619c31cb12f4657bd86020dc12cb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103890800"
---
# <a name="id-attribute-textboxvml"></a><span data-ttu-id="1228e-103">Атрибут ID (TextBox) (VML)</span><span class="sxs-lookup"><span data-stu-id="1228e-103">ID Attribute (TextBox)(VML)</span></span>

<span data-ttu-id="1228e-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="1228e-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="1228e-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="1228e-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="1228e-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="1228e-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="1228e-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="1228e-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="1228e-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="1228e-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="1228e-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="1228e-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="1228e-110">Имя, которое предоставляет уникальный идентификатор для текстового поля.</span><span class="sxs-lookup"><span data-stu-id="1228e-110">A name that provides a unique identifier for a textbox.</span></span> <span data-ttu-id="1228e-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="1228e-111">Read/write.</span></span> <span data-ttu-id="1228e-112">**Строка**.</span><span class="sxs-lookup"><span data-stu-id="1228e-112">**String**.</span></span>

<span data-ttu-id="1228e-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="1228e-113">**Applies To**</span></span>

[<span data-ttu-id="1228e-114">TextBox</span><span class="sxs-lookup"><span data-stu-id="1228e-114">TextBox</span></span>](msdn-online-vml-textbox-element.md)

<span data-ttu-id="1228e-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="1228e-115">**Tag Syntax**</span></span>

<span data-ttu-id="1228e-116"><v: *element* ID = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="1228e-116"><v: *element* id=" *expression* "></span></span>

<span data-ttu-id="1228e-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="1228e-117">**Script Syntax**</span></span>

<span data-ttu-id="1228e-118">*element* . ID = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="1228e-118">*element* .id="*expression*"</span></span>

<span data-ttu-id="1228e-119">*выражение* = *element*. ID</span><span class="sxs-lookup"><span data-stu-id="1228e-119">*expression*=*element*.id</span></span>

<span data-ttu-id="1228e-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="1228e-120">**Remarks**</span></span>

<span data-ttu-id="1228e-121">Используйте **ID** для ссылки на конкретное текстовое поле.</span><span class="sxs-lookup"><span data-stu-id="1228e-121">Use **ID** to refer to a specific textbox.</span></span> <span data-ttu-id="1228e-122">После создания текстового поля и присвоения ему идентификатора можно использовать имя идентификатора, если вы хотите управлять текстовым полем.</span><span class="sxs-lookup"><span data-stu-id="1228e-122">Once you have created a textbox and given it an ID, you can use the ID name when you want to manipulate the textbox.</span></span>

<span data-ttu-id="1228e-123">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="1228e-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="1228e-124">**Пример**</span><span class="sxs-lookup"><span data-stu-id="1228e-124">**Example**</span></span>

<span data-ttu-id="1228e-125">Фигура имеет идентификатор TextBox с именем "митекстбокс".</span><span class="sxs-lookup"><span data-stu-id="1228e-125">The shape has a textbox ID called "mytextbox".</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:10pt;left:10pt;width:50pt;height:50pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:textbox id="mytextbox">
   VML
   </v:textbox/>
   </v:shape>
```



 

 