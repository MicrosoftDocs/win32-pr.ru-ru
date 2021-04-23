---
title: Главный атрибут VML
description: Главный атрибут VML
ms.assetid: ec661dc6-8e1c-47a3-ad3a-e1ee7e64c840
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0d6c34fe49c107ed7ee1b4c1fb90d31bb07f17a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104134550"
---
# <a name="vml-master-attribute"></a><span data-ttu-id="98102-103">Главный атрибут VML</span><span class="sxs-lookup"><span data-stu-id="98102-103">VML Master Attribute</span></span>

<span data-ttu-id="98102-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="98102-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="98102-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="98102-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="98102-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="98102-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="98102-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="98102-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="98102-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="98102-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="98102-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="98102-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="98102-110">Определяет, является ли элемент **шапетипе** главным элементом.</span><span class="sxs-lookup"><span data-stu-id="98102-110">Determines whether a **ShapeType** element is a master element.</span></span> <span data-ttu-id="98102-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="98102-111">Read/write.</span></span> <span data-ttu-id="98102-112">**Вгтристате**.</span><span class="sxs-lookup"><span data-stu-id="98102-112">**VgTriState**.</span></span>

<span data-ttu-id="98102-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="98102-113">**Applies To**</span></span>

[<span data-ttu-id="98102-114">шапетипе</span><span class="sxs-lookup"><span data-stu-id="98102-114">ShapeType</span></span>](msdn-online-vml-shapetype-element.md)

<span data-ttu-id="98102-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="98102-115">**Tag Syntax**</span></span>

<span data-ttu-id="98102-116"><v: *element* о:Мастер = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="98102-116"><v: *element* o:master=" *expression* "></span></span>

<span data-ttu-id="98102-117">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="98102-117">**Remarks**</span></span>

<span data-ttu-id="98102-118">Если **значение — true**, фигура **шапетипе** подготавливается к просмотру модулем визуализации.</span><span class="sxs-lookup"><span data-stu-id="98102-118">If **True**, the **ShapeType** shape is rendered by the rendering engine.</span></span> <span data-ttu-id="98102-119">Значение по умолчанию равно **False**.</span><span class="sxs-lookup"><span data-stu-id="98102-119">The default value is **False**.</span></span>

<span data-ttu-id="98102-120">*Атрибут расширений Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="98102-120">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="98102-121">**Пример**</span><span class="sxs-lookup"><span data-stu-id="98102-121">**Example**</span></span>

<span data-ttu-id="98102-122">Элемент **шапетипе** является главной фигурой.</span><span class="sxs-lookup"><span data-stu-id="98102-122">The **ShapeType** element is a master shape.</span></span>


```HTML
   <v:shapetype id="laure"
   coordorigin= "0 0" coordsize="200 200"
   fillcolor= "red" o:master="True"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shapetype>
```



 

 