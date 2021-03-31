---
title: Атрибут направления VML
description: Атрибут направления VML
ms.assetid: bf6e0169-f0d4-4dfb-b59e-b5601049fd7a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a5bd45d4baaed100537207a02fc4308b964dfa2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792774"
---
# <a name="vml-direction-attribute"></a><span data-ttu-id="9ee8e-103">Атрибут направления VML</span><span class="sxs-lookup"><span data-stu-id="9ee8e-103">VML Direction Attribute</span></span>

<span data-ttu-id="9ee8e-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="9ee8e-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="9ee8e-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="9ee8e-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="9ee8e-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="9ee8e-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="9ee8e-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="9ee8e-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="9ee8e-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="9ee8e-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="9ee8e-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="9ee8e-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="9ee8e-110">Определяет направление текста в текстовом поле.</span><span class="sxs-lookup"><span data-stu-id="9ee8e-110">Defines the direction of the text in the textbox.</span></span> <span data-ttu-id="9ee8e-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="9ee8e-111">Read/write.</span></span> <span data-ttu-id="9ee8e-112">**Строка**.</span><span class="sxs-lookup"><span data-stu-id="9ee8e-112">**String**.</span></span>

<span data-ttu-id="9ee8e-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="9ee8e-113">**Applies To**</span></span>

[<span data-ttu-id="9ee8e-114">TextBox</span><span class="sxs-lookup"><span data-stu-id="9ee8e-114">TextBox</span></span>](msdn-online-vml-textbox-element.md)

<span data-ttu-id="9ee8e-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="9ee8e-115">**Tag Syntax**</span></span>

<span data-ttu-id="9ee8e-116"><v: *элемент* Style = "направление: *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="9ee8e-116"><v: *element* style="direction: *expression* "></span></span>

<span data-ttu-id="9ee8e-117">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="9ee8e-117">**Remarks**</span></span>

<span data-ttu-id="9ee8e-118">К этим значениям относятся следующие.</span><span class="sxs-lookup"><span data-stu-id="9ee8e-118">Values include:</span></span>



| <span data-ttu-id="9ee8e-119">Значение</span><span class="sxs-lookup"><span data-stu-id="9ee8e-119">Value</span></span>   | <span data-ttu-id="9ee8e-120">Описание</span><span class="sxs-lookup"><span data-stu-id="9ee8e-120">Description</span></span>                                                                                |
|---------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ee8e-121">LTR</span><span class="sxs-lookup"><span data-stu-id="9ee8e-121">ltr</span></span>     | <span data-ttu-id="9ee8e-122">Текст отображается слева направо.</span><span class="sxs-lookup"><span data-stu-id="9ee8e-122">Text is displayed left-to-right.</span></span> <span data-ttu-id="9ee8e-123">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9ee8e-123">Default.</span></span>                                                  |
| <span data-ttu-id="9ee8e-124">направление</span><span class="sxs-lookup"><span data-stu-id="9ee8e-124">rtl</span></span>     | <span data-ttu-id="9ee8e-125">Текст отображается справа налево.</span><span class="sxs-lookup"><span data-stu-id="9ee8e-125">Text is displayed right-to-left.</span></span>                                                           |
| <span data-ttu-id="9ee8e-126">контекст</span><span class="sxs-lookup"><span data-stu-id="9ee8e-126">context</span></span> | <span data-ttu-id="9ee8e-127">Указывает, что тег **MSO-Direction-Alt** будет записан со значением context.</span><span class="sxs-lookup"><span data-stu-id="9ee8e-127">Indicates that the **MSO-Direction-Alt** tag will be written out with the value "context".</span></span> |



 

<span data-ttu-id="9ee8e-128">*Атрибут расширений Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="9ee8e-128">*Microsoft Office Extensions Attribute*</span></span>

 

 