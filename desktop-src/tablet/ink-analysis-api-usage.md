---
description: 'Библиотека анализа рукописного ввода содержит четыре слоя: Windows Forms, WPF, COM и базовый слой. В этом разделе описывается, когда следует использовать каждый слой.'
ms.assetid: bd190606-5bd8-4280-ba2b-267588904ed3
title: Использование API анализа рукописного ввода
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24e291066d6cfd6ecdec319728b7394d730ba311
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990950"
---
# <a name="ink-analysis-api-usage"></a><span data-ttu-id="2964e-104">Использование API анализа рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="2964e-104">Ink Analysis API Usage</span></span>

<span data-ttu-id="2964e-105">Библиотека анализа рукописного ввода содержит четыре слоя: Windows Forms, WPF, COM и базовый слой.</span><span class="sxs-lookup"><span data-stu-id="2964e-105">There are four layers to the Ink Analysis library: Windows Forms, WPF, COM, and the base layer.</span></span> <span data-ttu-id="2964e-106">В этом разделе описывается, когда следует использовать каждый слой.</span><span class="sxs-lookup"><span data-stu-id="2964e-106">This section describes when to use each layer.</span></span>

## <a name="ink-analysis-api-overview"></a><span data-ttu-id="2964e-107">Общие сведения об API анализа рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="2964e-107">Ink Analysis API Overview</span></span>

<span data-ttu-id="2964e-108">Библиотеки анализа рукописного ввода предназначены для использования в различных поддерживаемых средах программирования.</span><span class="sxs-lookup"><span data-stu-id="2964e-108">The Ink Analysis libraries are designed to be used in a variety of supported programming environments.</span></span> <span data-ttu-id="2964e-109">Существует четыре основных уровня, с помощью которых приложение может использовать анализ рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="2964e-109">There are four basic layers through which your application can make use of Ink Analysis.</span></span> <span data-ttu-id="2964e-110">Эти слои:</span><span class="sxs-lookup"><span data-stu-id="2964e-110">These layers are:</span></span>

-   <span data-ttu-id="2964e-111">Слой Windows Forms</span><span class="sxs-lookup"><span data-stu-id="2964e-111">The Windows Forms layer</span></span>
-   <span data-ttu-id="2964e-112">Уровень WPF</span><span class="sxs-lookup"><span data-stu-id="2964e-112">The WPF layer</span></span>
-   <span data-ttu-id="2964e-113">Уровень COM</span><span class="sxs-lookup"><span data-stu-id="2964e-113">The COM layer</span></span>
-   <span data-ttu-id="2964e-114">Базовый уровень</span><span class="sxs-lookup"><span data-stu-id="2964e-114">The base layer</span></span>

### <a name="windows-forms-applications"></a><span data-ttu-id="2964e-115">Приложения Windows Forms</span><span class="sxs-lookup"><span data-stu-id="2964e-115">Windows Forms Applications</span></span>

<span data-ttu-id="2964e-116">Вы можете использовать API анализа рукописного ввода в управляемом проекте, добавив ссылку на следующие библиотеки:</span><span class="sxs-lookup"><span data-stu-id="2964e-116">You can use the Ink Analysis API in your managed project by adding a reference to the following libraries:</span></span>

-   <span data-ttu-id="2964e-117">Microsoft. Ink. Analysis (Microsoft.Ink.Analysis.dll)</span><span class="sxs-lookup"><span data-stu-id="2964e-117">Microsoft.Ink.Analysis (Microsoft.Ink.Analysis.dll)</span></span>
-   <span data-ttu-id="2964e-118">Библиотека анализа рукописных документов (IACore.dll)</span><span class="sxs-lookup"><span data-stu-id="2964e-118">Ink Document Analysis Library (IACore.dll)</span></span>

<span data-ttu-id="2964e-119">В Windows Forms приложениях, скорее всего, вы будете использовать библиотеки в сочетании со стандартными объектами платформы планшетных ПК, находящихся в сборке Microsoft Tablet PC API v 1.7.</span><span class="sxs-lookup"><span data-stu-id="2964e-119">In Windows Forms applications, you will most likely use the libraries in conjunction with the standard Tablet PC platform objects found in the Microsoft Tablet PC API v1.7 assembly.</span></span> <span data-ttu-id="2964e-120">Убедитесь, что у вас также есть ссылка на:</span><span class="sxs-lookup"><span data-stu-id="2964e-120">Be sure you also have a reference to:</span></span>

-   <span data-ttu-id="2964e-121">Microsoft Tablet PC API v 1.7.2600.2180 (Microsoft.Ink.dll)</span><span class="sxs-lookup"><span data-stu-id="2964e-121">Microsoft Tablet PC API v1.7.2600.2180 (Microsoft.Ink.dll)</span></span>

### <a name="windows-presentation-framework-applications"></a><span data-ttu-id="2964e-122">Приложения Windows Presentation Framework</span><span class="sxs-lookup"><span data-stu-id="2964e-122">Windows Presentation Framework Applications</span></span>

<span data-ttu-id="2964e-123">Вы можете использовать API анализа рукописного ввода в проекте WPF, добавив ссылку на элементы анализа рукописного ввода, определенные в пространстве имен System. Windows. Ink в сборке IAWinFX.dll.</span><span class="sxs-lookup"><span data-stu-id="2964e-123">You can use the Ink Analysis API in your WPF project by adding a reference to the Ink Analysis members that are defined in the System.Windows.Ink namespace in the IAWinFX.dll assembly.</span></span> <span data-ttu-id="2964e-124">Эта сборка устанавливается пакетом SDK.</span><span class="sxs-lookup"><span data-stu-id="2964e-124">This assembly is installed by the SDK.</span></span>

### <a name="com-applications"></a><span data-ttu-id="2964e-125">Приложения COM</span><span class="sxs-lookup"><span data-stu-id="2964e-125">COM Applications</span></span>

<span data-ttu-id="2964e-126">Приложения COM, не относящиеся к автоматизации, должны использовать COM-уровень API анализа рукописного текста.</span><span class="sxs-lookup"><span data-stu-id="2964e-126">Non-Automation COM applications should use the COM layer of the Ink Analysis APIs.</span></span>

<span data-ttu-id="2964e-127">Введите определенные объекты [контекстноде](/previous-versions/ms551996(v=vs.100)) , такие как [параграфноде](/previous-versions/ms580136(v=vs.100)), [инквордноде](/previous-versions/ms580133(v=vs.100))и др., не используются на уровне com.</span><span class="sxs-lookup"><span data-stu-id="2964e-127">Type specific [ContextNode](/previous-versions/ms551996(v=vs.100)) objects-such as [ParagraphNode](/previous-versions/ms580136(v=vs.100)), [InkWordNode](/previous-versions/ms580133(v=vs.100)), and others-are not used in the COM layer.</span></span> <span data-ttu-id="2964e-128">Вместо этого следует использовать [**иконтекстноде:: аддпропертидата**](icontextnode-addpropertydata.md) в стандартном интерфейсе [**иконтекстноде**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="2964e-128">Rather, you should use the [**IContextNode::AddPropertyData**](icontextnode-addpropertydata.md) on the standard [**IContextNode**](icontextnode.md) interface.</span></span>

<span data-ttu-id="2964e-129">Необходимо \# включить "иаком. h".</span><span class="sxs-lookup"><span data-stu-id="2964e-129">You must \#include "IACom.h".</span></span> <span data-ttu-id="2964e-130">Скорее всего, вы будете использовать библиотеки в сочетании с объектом рукописного ввода платформы Tablet PC, поэтому необходимо также \# включить "мсинкаут. h".</span><span class="sxs-lookup"><span data-stu-id="2964e-130">You will most likely use the libraries in conjunction wit the Tablet PC platform Ink object, so you should also \#include "msinkaut.h".</span></span>

### <a name="rts-and-other-applications"></a><span data-ttu-id="2964e-131">RTS и другие приложения</span><span class="sxs-lookup"><span data-stu-id="2964e-131">RTS and Other Applications</span></span>

<span data-ttu-id="2964e-132">Уровень "базовый" анализа рукописного текста работает не так, как другие элементы, в которых он принимает данные точки для анализа, а не объекты- [штрихи](/previous-versions/ms552692(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="2964e-132">The Ink Analysis base layer works differently than the others in that it takes point data for analysis rather than [Stroke](/previous-versions/ms552692(v=vs.100)) objects.</span></span> <span data-ttu-id="2964e-133">Примерами того, где вы бы работали с базовым слоем напрямую, вместо использования уровней Windows Forms или COM являются приложения, которые не используют рукописные объекты первого поколения, или приложения, использующие интерфейсы API [**RealTimeStylus**](realtimestylus-class.md) для управления вводом с помощью пера, вместо [рукописных](/previous-versions/ms583670(v=vs.100)) объектов платформы Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="2964e-133">Examples of where you would work with the Base layer directly rather than using the Windows forms or COM layers include applications that do not use first generation Tablet PC Platform Ink objects, or applications that use the [**RealTimeStylus**](realtimestylus-class.md) APIs to manage stylus input rather than using the Tablet PC Platform [Ink](/previous-versions/ms583670(v=vs.100)) objects.</span></span>

## <a name="32-bit-support-only"></a><span data-ttu-id="2964e-134">Только 32-разрядная поддержка</span><span class="sxs-lookup"><span data-stu-id="2964e-134">32-bit Support Only</span></span>

<span data-ttu-id="2964e-135">Обратите внимание, что библиотеки анализа рукописного ввода поддерживаются только в 32-разрядных процессах.</span><span class="sxs-lookup"><span data-stu-id="2964e-135">Note that the Ink Analysis libraries are only supported in 32-bit processes.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2964e-136">См. также</span><span class="sxs-lookup"><span data-stu-id="2964e-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2964e-137">Обзор анализа рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="2964e-137">Ink Analysis Overview</span></span>](ink-analysis-overview.md)
</dt> <dt>

[<span data-ttu-id="2964e-138">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="2964e-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 
