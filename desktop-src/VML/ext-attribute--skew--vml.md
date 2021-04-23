---
title: Атрибут ext (асимметрия) (VML)
description: Атрибут ext (асимметрия) (VML)
ms.assetid: ff1dfb2f-9098-4418-a2f7-c7159328bd09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 153273f613d188ae9e6fe733b2d0337c5010295d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104260936"
---
# <a name="ext-attribute-skewvml"></a><span data-ttu-id="e5663-103">Атрибут ext (асимметрия) (VML)</span><span class="sxs-lookup"><span data-stu-id="e5663-103">Ext Attribute (Skew)(VML)</span></span>

<span data-ttu-id="e5663-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="e5663-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="e5663-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="e5663-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="e5663-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="e5663-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="e5663-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="e5663-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="e5663-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="e5663-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="e5663-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="e5663-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="e5663-110">Определяет способ отображения наклона.</span><span class="sxs-lookup"><span data-stu-id="e5663-110">Defines the way a skew is displayed.</span></span> <span data-ttu-id="e5663-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="e5663-111">Read/write.</span></span> <span data-ttu-id="e5663-112">**Строка**.</span><span class="sxs-lookup"><span data-stu-id="e5663-112">**String**.</span></span>

<span data-ttu-id="e5663-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="e5663-113">**Applies To**</span></span>

[<span data-ttu-id="e5663-114">Отклонение</span><span class="sxs-lookup"><span data-stu-id="e5663-114">Skew</span></span>](msdn-online-vml-skew-element.md)

<span data-ttu-id="e5663-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="e5663-115">**Tag Syntax**</span></span>

<span data-ttu-id="e5663-116"><o: *element* в:екст = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="e5663-116"><o: *element* v:ext=" *expression* "></span></span>

<span data-ttu-id="e5663-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="e5663-117">**Script Syntax**</span></span>

<span data-ttu-id="e5663-118">*element* . ext = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="e5663-118">*element* .ext="*expression*"</span></span>

<span data-ttu-id="e5663-119">*выражение* = *element*. ext</span><span class="sxs-lookup"><span data-stu-id="e5663-119">*expression*=*element*.ext</span></span>

<span data-ttu-id="e5663-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="e5663-120">**Remarks**</span></span>

<span data-ttu-id="e5663-121">Этот атрибут используется, чтобы сообщить графическим редакторам, как обрабатывать элемент **асимметрии** .</span><span class="sxs-lookup"><span data-stu-id="e5663-121">This attribute is used to tell graphical editors how to process the **Skew** element.</span></span> <span data-ttu-id="e5663-122">К этим значениям относятся следующие.</span><span class="sxs-lookup"><span data-stu-id="e5663-122">Values include:</span></span>

-   <span data-ttu-id="e5663-123">**edit**</span><span class="sxs-lookup"><span data-stu-id="e5663-123">**edit**</span></span>
-   <span data-ttu-id="e5663-124">**представление** (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e5663-124">**view** (default)</span></span>
-   <span data-ttu-id="e5663-125">**бакквардкомпатибле**</span><span class="sxs-lookup"><span data-stu-id="e5663-125">**backwardCompatible**</span></span>

<span data-ttu-id="e5663-126">Если для расширения задано **изменение**, оно может игнорироваться средством просмотра программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="e5663-126">If an extension is set to **edit**, it can be ignored by a software viewer.</span></span> <span data-ttu-id="e5663-127">Если задано значение **Просмотр**, то средство просмотра должно отображать растровое представление.</span><span class="sxs-lookup"><span data-stu-id="e5663-127">If set to **view**, the viewer must render the bitmap representation instead.</span></span>

<span data-ttu-id="e5663-128">*Атрибут расширений Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="e5663-128">*Microsoft Office Extensions Attribute*</span></span>

 

 