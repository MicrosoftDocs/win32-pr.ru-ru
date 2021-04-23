---
title: Атрибут Рулеинитиатор VML
description: Атрибут Рулеинитиатор VML
ms.assetid: 2c9b1131-b088-4b70-b132-bdb4296433ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80201ad80fbb8dc5bbff2e8ed4e0b8db2863fdad
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104339105"
---
# <a name="vml-ruleinitiator-attribute"></a><span data-ttu-id="46712-103">Атрибут Рулеинитиатор VML</span><span class="sxs-lookup"><span data-stu-id="46712-103">VML RuleInitiator Attribute</span></span>

<span data-ttu-id="46712-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="46712-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="46712-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="46712-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="46712-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="46712-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="46712-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="46712-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="46712-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="46712-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="46712-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="46712-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="46712-110">Определяет, будет ли использоваться обработчик правил.</span><span class="sxs-lookup"><span data-stu-id="46712-110">Determines whether a rules engine will be used.</span></span> <span data-ttu-id="46712-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="46712-111">Read/write.</span></span> <span data-ttu-id="46712-112">**Вгтристате**.</span><span class="sxs-lookup"><span data-stu-id="46712-112">**VgTriState**.</span></span>

<span data-ttu-id="46712-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="46712-113">**Applies To**</span></span>

[<span data-ttu-id="46712-114">Фигурная</span><span class="sxs-lookup"><span data-stu-id="46712-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="46712-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="46712-115">**Tag Syntax**</span></span>

<span data-ttu-id="46712-116"><v: *element* о:рулеинитиатор = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="46712-116"><v: *element* o:ruleinitiator=" *expression* "></span></span>

<span data-ttu-id="46712-117">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="46712-117">**Remarks**</span></span>

<span data-ttu-id="46712-118">Значение по умолчанию равно **False**.</span><span class="sxs-lookup"><span data-stu-id="46712-118">The default value is **False**.</span></span> <span data-ttu-id="46712-119">Если значение равно **true**, используется обработчик правил.</span><span class="sxs-lookup"><span data-stu-id="46712-119">If the value is **True**, a rules engine is used.</span></span>

<span data-ttu-id="46712-120">*Атрибут расширений Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="46712-120">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="46712-121">**Пример**</span><span class="sxs-lookup"><span data-stu-id="46712-121">**Example**</span></span>

<span data-ttu-id="46712-122">Фигура будет обработана обработчиком правил.</span><span class="sxs-lookup"><span data-stu-id="46712-122">The shape will be processed by a rules engine.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red" rulesinitiator="True"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 