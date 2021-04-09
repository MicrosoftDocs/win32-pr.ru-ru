---
title: Атрибут Matrix (асимметрия) (VML)
description: Атрибут Matrix (асимметрия) (VML)
ms.assetid: 8d039865-2261-458b-8edf-01374af65cea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8327acfebfe4d968e673060f2f3cbef69d3e9db6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070528"
---
# <a name="matrix-attribute-skewvml"></a><span data-ttu-id="b616c-103">Атрибут Matrix (асимметрия) (VML)</span><span class="sxs-lookup"><span data-stu-id="b616c-103">Matrix Attribute (Skew)(VML)</span></span>

<span data-ttu-id="b616c-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="b616c-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="b616c-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="b616c-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="b616c-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="b616c-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="b616c-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="b616c-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="b616c-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="b616c-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="b616c-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="b616c-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="b616c-110">Определяет преобразование "Перспектива" для наклона.</span><span class="sxs-lookup"><span data-stu-id="b616c-110">Defines a perspective transform of a skew.</span></span> <span data-ttu-id="b616c-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="b616c-111">Read/write.</span></span> <span data-ttu-id="b616c-112">**Строка**.</span><span class="sxs-lookup"><span data-stu-id="b616c-112">**String**.</span></span>

<span data-ttu-id="b616c-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="b616c-113">**Applies To**</span></span>

[<span data-ttu-id="b616c-114">Отклонение</span><span class="sxs-lookup"><span data-stu-id="b616c-114">Skew</span></span>](msdn-online-vml-skew-element.md)

<span data-ttu-id="b616c-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="b616c-115">**Tag Syntax**</span></span>

<span data-ttu-id="b616c-116"><o: *элемент* Matrix = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="b616c-116"><o: *element* matrix=" *expression* "></span></span>

<span data-ttu-id="b616c-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="b616c-117">**Script Syntax**</span></span>

<span data-ttu-id="b616c-118">*element* . Matrix = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="b616c-118">*element* .matrix="*expression*"</span></span>

<span data-ttu-id="b616c-119">*выражение* = *элемент*. Matrix</span><span class="sxs-lookup"><span data-stu-id="b616c-119">*expression*=*element*.matrix</span></span>

<span data-ttu-id="b616c-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="b616c-120">**Remarks**</span></span>

<span data-ttu-id="b616c-121">Матрица представляет собой строку в форме "скскс, СКСИ, Сикс, сии, px, корректировка", где s — масштаб, p — перспектива, а x и y — значения x и y.</span><span class="sxs-lookup"><span data-stu-id="b616c-121">The matrix is a string in the form "sxx, sxy, syx, syy, px, py" where s is scale, p is perspective, and x and y are x and y values.</span></span> <span data-ttu-id="b616c-122">Если значение [offset](offset-attribute--skew--vml.md) в абсолютных единицах, то числа px и корректировки находятся в ЕС ^-1 [единиц](msdn-online-vml-units.md) (в противном случае это обратная часть размера фигуры).</span><span class="sxs-lookup"><span data-stu-id="b616c-122">If [Offset](offset-attribute--skew--vml.md) is in absolute units, then px and py are in emu^-1 [units](msdn-online-vml-units.md) (otherwise they are an inverse fraction of the shape size).</span></span> <span data-ttu-id="b616c-123">Значение по умолчанию — "1, 0, 0, 1, 0, 0".</span><span class="sxs-lookup"><span data-stu-id="b616c-123">The default value is "1,0,0,1,0,0".</span></span>

<span data-ttu-id="b616c-124">*Атрибут расширений Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="b616c-124">*Microsoft Office Extensions Attribute*</span></span>

 

 