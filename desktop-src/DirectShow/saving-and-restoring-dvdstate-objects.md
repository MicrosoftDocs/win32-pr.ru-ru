---
description: Сохранение и восстановление объектов Двдстате
ms.assetid: 65180fe2-0faf-47c0-bccd-728e01056c46
title: Сохранение и восстановление объектов Двдстате
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9640b20bc8d763054c15331017da343ef45f3c2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105673003"
---
# <a name="saving-and-restoring-dvdstate-objects"></a><span data-ttu-id="aceae-103">Сохранение и восстановление объектов Двдстате</span><span class="sxs-lookup"><span data-stu-id="aceae-103">Saving and Restoring DvdState Objects</span></span>

<span data-ttu-id="aceae-104">Объекты [**идвдстате**](/windows/desktop/api/Strmif/nn-strmif-idvdstate) позволяют приложениям сохранять моментальные снимки сеанса пользователя, в том числе такие сведения, как текущее место на диске, родительский уровень просмотра, выбранные потоки аудио и субтитров и т. д.</span><span class="sxs-lookup"><span data-stu-id="aceae-104">[**IDvdState**](/windows/desktop/api/Strmif/nn-strmif-idvdstate) objects enable applications to save a snapshot of the user session, including information such as the current location on the disc, the parental level of the person who is viewing, the selected audio and subpicture streams, and so on.</span></span> <span data-ttu-id="aceae-105">Это означает, что пользователи могут сохранить свое место на DVD-Video диске и смотреть их позже.</span><span class="sxs-lookup"><span data-stu-id="aceae-105">This means that users can save their place on a DVD-Video disc and watch it at a later time.</span></span>

<span data-ttu-id="aceae-106">Приложения не могут создавать объекты Двдстате.</span><span class="sxs-lookup"><span data-stu-id="aceae-106">Applications cannot create DvdState objects.</span></span> <span data-ttu-id="aceae-107">Эти объекты создаются внутренне навигатором DVD, когда приложение вызывает [**IDvdInfo2::-State**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getstate).</span><span class="sxs-lookup"><span data-stu-id="aceae-107">These objects are created internally by the DVD Navigator when an application calls [**IDvdInfo2::GetState**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getstate).</span></span> <span data-ttu-id="aceae-108">Объекты Двдстате предоставляют интерфейс [**идвдстате**](/windows/desktop/api/Strmif/nn-strmif-idvdstate) , позволяющий приложениям запрашивать определенные сведения.</span><span class="sxs-lookup"><span data-stu-id="aceae-108">DvdState objects expose the [**IDvdState**](/windows/desktop/api/Strmif/nn-strmif-idvdstate) interface to allow applications to query for certain information.</span></span>

<span data-ttu-id="aceae-109">В примере приложения DVD функции **кдвдкоре:: ресторебукмарк** и **Кдвдкоре:: савебукмарк** показывают, как сохранять и извлекать объекты двдстате.</span><span class="sxs-lookup"><span data-stu-id="aceae-109">In the DVD sample application, the **CDvdCore::RestoreBookmark** and **CDvdCore::SaveBookmark** functions show how to save and retrieve DvdState objects.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aceae-110">См. также</span><span class="sxs-lookup"><span data-stu-id="aceae-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aceae-111">DVD-приложения</span><span class="sxs-lookup"><span data-stu-id="aceae-111">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 



