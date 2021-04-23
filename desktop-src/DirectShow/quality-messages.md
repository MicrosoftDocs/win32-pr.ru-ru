---
description: Сообщения о контроле качества
ms.assetid: ff98cb51-6300-470d-b696-5e27591c6b3f
title: Сообщения о контроле качества
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b290833be7550e255590a5bcda449ce19743c0b4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537148"
---
# <a name="quality-messages"></a><span data-ttu-id="e484f-103">Сообщения о контроле качества</span><span class="sxs-lookup"><span data-stu-id="e484f-103">Quality Messages</span></span>

<span data-ttu-id="e484f-104">Сообщения качества определяются структурой [**качества**](/windows/win32/api/strmif/ns-strmif-quality) .</span><span class="sxs-lookup"><span data-stu-id="e484f-104">Quality messages are defined with the [**Quality**](/windows/win32/api/strmif/ns-strmif-quality) structure.</span></span> <span data-ttu-id="e484f-105">Эта структура содержит следующие члены:</span><span class="sxs-lookup"><span data-stu-id="e484f-105">This structure contains the following members:</span></span>

-   <span data-ttu-id="e484f-106">**Тип:** Определяется перечислением [**куалитимессажетипе**](/windows/win32/api/strmif/ne-strmif-qualitymessagetype) ; либо Фамине, указывающее, что фильтр получает слишком мало данных, или переполнение, указывающее, что фильтр получает слишком много данных.</span><span class="sxs-lookup"><span data-stu-id="e484f-106">**Type:** Defined by the [**QualityMessageType**](/windows/win32/api/strmif/ne-strmif-qualitymessagetype) enumeration; either Famine, indicating that the filter is receiving too little data, or Flood, indicating that the filter is receiving too much data.</span></span>
-   <span data-ttu-id="e484f-107">**Пропорции:** Запрошенная коррекция скорости передачи данных от базового плана 1000.</span><span class="sxs-lookup"><span data-stu-id="e484f-107">**Proportion:** The requested adjustment in the data rate, from a baseline of 1000.</span></span> <span data-ttu-id="e484f-108">Например, 750 означает 75%, а 1500 — 150%.</span><span class="sxs-lookup"><span data-stu-id="e484f-108">For example, 750 indicates 75% and 1500 indicates 150%.</span></span>
-   <span data-ttu-id="e484f-109">**Позднее:** Справочное время, указывающее, как поступил последний пример.</span><span class="sxs-lookup"><span data-stu-id="e484f-109">**Late:** Reference time indicating how late the most recent sample arrived.</span></span> <span data-ttu-id="e484f-110">Значение является отрицательным, если пример приступил на ранних этапах.</span><span class="sxs-lookup"><span data-stu-id="e484f-110">The value is negative if the sample arrived early.</span></span>
-   <span data-ttu-id="e484f-111">**Отметка времени:** Метка времени для последнего примера.</span><span class="sxs-lookup"><span data-stu-id="e484f-111">**TimeStamp:** The time stamp on the most recent sample.</span></span>

<span data-ttu-id="e484f-112">Например, предположим, что пример с меткой времени 240 миллисекунд (МС) достигает модуля подготовки отчетов 280 МС, потоковое время.</span><span class="sxs-lookup"><span data-stu-id="e484f-112">For example, suppose that a sample with a time stamp of 240 milliseconds (ms) reaches the renderer at 280 ms, stream time.</span></span> <span data-ttu-id="e484f-113">Модуль подготовки отчетов создает сообщение качества типа Фамине.</span><span class="sxs-lookup"><span data-stu-id="e484f-113">The renderer creates a quality message of type Famine.</span></span> <span data-ttu-id="e484f-114">Пример приступил к 40 мс в конце, поэтому **последний** член равен 400000.</span><span class="sxs-lookup"><span data-stu-id="e484f-114">The sample arrived 40 ms late, so the **Late** member is 400000.</span></span> <span data-ttu-id="e484f-115">(Все значения времени ссылки находятся в 100-наносекундных единицах.) Элемент **timestamp** имеет значение 2400000.</span><span class="sxs-lookup"><span data-stu-id="e484f-115">(All reference times are in 100-nanosecond units.) The **TimeStamp** member is 2400000.</span></span>

<span data-ttu-id="e484f-116">Для элемента с **пропорциями** модуль подготовки отчетов может использовать скользящее среднее для вычисления значения.</span><span class="sxs-lookup"><span data-stu-id="e484f-116">For the **Proportion** member, the renderer might use a running average to calculate the value.</span></span> <span data-ttu-id="e484f-117">Возможно, примеры поступают на момент времени, и этот пример является аномалией.</span><span class="sxs-lookup"><span data-stu-id="e484f-117">Perhaps samples have been arriving on time, and this sample is an anomaly.</span></span> <span data-ttu-id="e484f-118">В этом случае модуль подготовки отчетов может запросить только небольшое исправление.</span><span class="sxs-lookup"><span data-stu-id="e484f-118">In that case the renderer might request only a small correction.</span></span> <span data-ttu-id="e484f-119">С другой стороны, если выборки постоянно поздно, модуль подготовки отчетов может запросить более крупную коррекцию.</span><span class="sxs-lookup"><span data-stu-id="e484f-119">On the other hand, if samples are consistently late, the renderer might request a larger correction.</span></span>

<span data-ttu-id="e484f-120">Контроль качества обрабатывается через интерфейс [**икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) .</span><span class="sxs-lookup"><span data-stu-id="e484f-120">Quality control is handled through the [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) interface.</span></span> <span data-ttu-id="e484f-121">Он содержит два метода.</span><span class="sxs-lookup"><span data-stu-id="e484f-121">It contains two methods.</span></span>

-   <span data-ttu-id="e484f-122">[**Уведомлять**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify): отправляет сообщение с качеством.</span><span class="sxs-lookup"><span data-stu-id="e484f-122">[**Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify): Sends a quality message.</span></span>
-   <span data-ttu-id="e484f-123">[**Сетсинк**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink): указывает пользовательский диспетчер качества.</span><span class="sxs-lookup"><span data-stu-id="e484f-123">[**SetSink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink): Specifies a custom quality manager.</span></span>

<span data-ttu-id="e484f-124">Объект, реализующий **икуалитиконтрол** , получает сообщения о повышении качества с помощью метода **Notify** .</span><span class="sxs-lookup"><span data-stu-id="e484f-124">An object that implements **IQualityControl** receives quality messages through its **Notify** method.</span></span> <span data-ttu-id="e484f-125">Он может либо обрабатывать сообщение, либо передавать сообщение другому объекту.</span><span class="sxs-lookup"><span data-stu-id="e484f-125">It can either handle the message or pass the message to another object.</span></span> <span data-ttu-id="e484f-126">Если приложение вызывает метод **сетсинк** объекта, объект должен передать управление качеством указанному диспетчеру качества.</span><span class="sxs-lookup"><span data-stu-id="e484f-126">If the application calls the object's **SetSink** method, the object should delegate quality control to the specified quality manager.</span></span>

 

 



