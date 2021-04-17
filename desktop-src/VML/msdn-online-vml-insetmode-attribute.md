---
title: Атрибут Инсетмоде VML
description: Атрибут Инсетмоде VML
ms.assetid: 3cdce299-a490-43b9-93f5-09aca443e98b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8f3ddee2a3c8060a9aa89dbd17bca329c1a105c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105691566"
---
# <a name="vml-insetmode-attribute"></a><span data-ttu-id="52197-103">Атрибут Инсетмоде VML</span><span class="sxs-lookup"><span data-stu-id="52197-103">VML InsetMode Attribute</span></span>

<span data-ttu-id="52197-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="52197-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="52197-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="52197-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="52197-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="52197-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="52197-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="52197-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="52197-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="52197-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="52197-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="52197-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="52197-110">Определяет, как приложение будет допускать значения настраиваемых отступов.</span><span class="sxs-lookup"><span data-stu-id="52197-110">Defines how the application will allow custom inset values.</span></span> <span data-ttu-id="52197-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="52197-111">Read/write.</span></span> <span data-ttu-id="52197-112">**Строка**.</span><span class="sxs-lookup"><span data-stu-id="52197-112">**String**.</span></span>

<span data-ttu-id="52197-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="52197-113">**Applies To**</span></span>

[<span data-ttu-id="52197-114">TextBox</span><span class="sxs-lookup"><span data-stu-id="52197-114">TextBox</span></span>](msdn-online-vml-textbox-element.md)

<span data-ttu-id="52197-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="52197-115">**Tag Syntax**</span></span>

<span data-ttu-id="52197-116"><v: *element* о:инсетмоде = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="52197-116"><v: *element* o:insetmode=" *expression* "></span></span>

<span data-ttu-id="52197-117">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="52197-117">**Remarks**</span></span>

<span data-ttu-id="52197-118">К этим значениям относятся следующие.</span><span class="sxs-lookup"><span data-stu-id="52197-118">Values include:</span></span>

-   <span data-ttu-id="52197-119">auto</span><span class="sxs-lookup"><span data-stu-id="52197-119">auto</span></span>
-   <span data-ttu-id="52197-120">Custom (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="52197-120">custom (default)</span></span>

<span data-ttu-id="52197-121">Если значение равно **Auto**, значения пользовательского отступа не допускаются, а приложение определяет внутреннее текстовое поле текстового поля.</span><span class="sxs-lookup"><span data-stu-id="52197-121">If the value is **auto**, custom inset values are not allowed, and the application determines the inner text margin of a textbox.</span></span>

<span data-ttu-id="52197-122">*Атрибут расширений Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="52197-122">*Microsoft Office Extensions Attribute*</span></span>

 

 