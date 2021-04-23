---
title: Атрибут Matrix (тень) (VML)
description: Атрибут Matrix (тень) (VML)
ms.assetid: 29bebd2f-7f66-4883-8c12-57fef4a0ac9e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d599aa817e87481aefdec43dbe345b7235fc54bd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413568"
---
# <a name="matrix-attribute-shadowvml"></a><span data-ttu-id="50fe1-103">Атрибут Matrix (тень) (VML)</span><span class="sxs-lookup"><span data-stu-id="50fe1-103">Matrix Attribute (Shadow)(VML)</span></span>

<span data-ttu-id="50fe1-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="50fe1-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="50fe1-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="50fe1-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="50fe1-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="50fe1-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="50fe1-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="50fe1-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="50fe1-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="50fe1-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="50fe1-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="50fe1-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="50fe1-110">Определяет преобразование перспективы для тени.</span><span class="sxs-lookup"><span data-stu-id="50fe1-110">Defines a perspective transform for a shadow.</span></span> <span data-ttu-id="50fe1-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="50fe1-111">Read/write.</span></span> <span data-ttu-id="50fe1-112">**Строка**.</span><span class="sxs-lookup"><span data-stu-id="50fe1-112">**String**.</span></span>

<span data-ttu-id="50fe1-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="50fe1-113">**Applies To**</span></span>

[<span data-ttu-id="50fe1-114">Shadow</span><span class="sxs-lookup"><span data-stu-id="50fe1-114">Shadow</span></span>](msdn-online-vml-shadow-element.md)

<span data-ttu-id="50fe1-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="50fe1-115">**Tag Syntax**</span></span>

<span data-ttu-id="50fe1-116"><v: *элемент* Matrix = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="50fe1-116"><v: *element* matrix=" *expression* "></span></span>

<span data-ttu-id="50fe1-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="50fe1-117">**Script Syntax**</span></span>

<span data-ttu-id="50fe1-118">*element* . Matrix = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="50fe1-118">*element* .matrix="*expression*"</span></span>

<span data-ttu-id="50fe1-119">*выражение* = *элемент*. Matrix</span><span class="sxs-lookup"><span data-stu-id="50fe1-119">*expression*=*element*.matrix</span></span>

<span data-ttu-id="50fe1-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="50fe1-120">**Remarks**</span></span>

<span data-ttu-id="50fe1-121">Матрица преобразования перспективы в форме "скскс, СКСИ, Сикс, сии, px, корректировка", где s = масштаб и p = перспектива.</span><span class="sxs-lookup"><span data-stu-id="50fe1-121">A perspective transform matrix in the form "sxx,sxy,syx,syy,px,py" where s= scale and p = perspective.</span></span> <span data-ttu-id="50fe1-122">Если значение offset в абсолютных единицах, то px, корректировка производится в 1 или единицах ЕС. в противном случае это обратная часть размера фигуры.</span><span class="sxs-lookup"><span data-stu-id="50fe1-122">If offset is in absolute units then px, py are in 1/emu units; otherwise they are an inverse fraction of the shape size.</span></span>

<span data-ttu-id="50fe1-123">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="50fe1-123">*VML Standard Attribute*</span></span>

 

 