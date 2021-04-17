---
title: Атрибут переключателя VML
description: Атрибут переключателя VML
ms.assetid: fc099c0a-6789-41e8-ab08-36f4fd2d3bfa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9d102d6af20e698d8ec281cb1be6fae9690de4e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105672292"
---
# <a name="vml-switch-attribute"></a><span data-ttu-id="bd879-103">Атрибут переключателя VML</span><span class="sxs-lookup"><span data-stu-id="bd879-103">VML Switch Attribute</span></span>

<span data-ttu-id="bd879-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="bd879-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="bd879-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="bd879-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="bd879-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="bd879-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="bd879-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="bd879-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="bd879-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="bd879-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="bd879-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="bd879-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="bd879-110">Определяет, меняются ли направления обработчиков.</span><span class="sxs-lookup"><span data-stu-id="bd879-110">Determines whether the handle directions are swapped.</span></span> <span data-ttu-id="bd879-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="bd879-111">Read/write.</span></span> <span data-ttu-id="bd879-112">**Вгтристате**.</span><span class="sxs-lookup"><span data-stu-id="bd879-112">**VgTriState**.</span></span>

<span data-ttu-id="bd879-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="bd879-113">**Applies To**</span></span>

<span data-ttu-id="bd879-114">[H](msdn-online-vml-h-element.md) (вложенный элемент [дескрипторов](msdn-online-vml-handles-element.md))</span><span class="sxs-lookup"><span data-stu-id="bd879-114">[H](msdn-online-vml-h-element.md) (subelement of [Handles](msdn-online-vml-handles-element.md))</span></span>

<span data-ttu-id="bd879-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="bd879-115">**Tag Syntax**</span></span>

<span data-ttu-id="bd879-116"><v: Switch *элемента* = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="bd879-116"><v: *element* switch=" *expression* "></span></span>

<span data-ttu-id="bd879-117">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="bd879-117">**Remarks**</span></span>

<span data-ttu-id="bd879-118">Если **значение равно true**, то маркер переключается между направлениями x и y, если размер фигуры превышает ширину.</span><span class="sxs-lookup"><span data-stu-id="bd879-118">If **True**, the handle is switched between the x and y directions if the shape is taller than it is wide.</span></span> <span data-ttu-id="bd879-119">Значение по умолчанию равно **False**.</span><span class="sxs-lookup"><span data-stu-id="bd879-119">The default value is **False**.</span></span>

<span data-ttu-id="bd879-120">Этот атрибут используется для фигур с поведением растяжения Лимо.</span><span class="sxs-lookup"><span data-stu-id="bd879-120">This attribute is used for shapes with limo stretch behavior.</span></span>

<span data-ttu-id="bd879-121">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="bd879-121">*VML Standard Attribute*</span></span>

 

 