---
description: Описывает форматы времени, поддерживаемые для использования в предложении языка WQL.
ms.assetid: d86bd2e3-f5cb-488f-9cd6-5105d82a1842
ms.tgt_platform: multiple
title: WQL-Supported форматы времени
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58b84d9e37de3529060dc3da6277b2cfb40f7cc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711723"
---
# <a name="wql-supported-time-formats"></a><span data-ttu-id="ea097-103">WQL-Supported форматы времени</span><span class="sxs-lookup"><span data-stu-id="ea097-103">WQL-Supported Time Formats</span></span>

<span data-ttu-id="ea097-104">Помимо формата DATETIME WMI, для использования в предложении WHERE WQL поддерживаются следующие форматы даты.</span><span class="sxs-lookup"><span data-stu-id="ea097-104">In addition to the WMI DATETIME format, the following date formats are supported for use in the WQL WHERE clause.</span></span>



| <span data-ttu-id="ea097-105">Формат</span><span class="sxs-lookup"><span data-stu-id="ea097-105">Format</span></span>                                    | <span data-ttu-id="ea097-106">Описание</span><span class="sxs-lookup"><span data-stu-id="ea097-106">Description</span></span>                                                                                                                                                                                            |
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea097-107">чч \[ \] {AP} м</span><span class="sxs-lookup"><span data-stu-id="ea097-107">hh\[ \]{AP}M</span></span><br/>                   | <span data-ttu-id="ea097-108">Час, как показано в 12-часовом формате, а также в режиме AM или PM.</span><span class="sxs-lookup"><span data-stu-id="ea097-108">Hour as shown on a twelve-hour clock, and AM or PM designation.</span></span><br/> <span data-ttu-id="ea097-109">16:00:00</span><span class="sxs-lookup"><span data-stu-id="ea097-109">4 PM</span></span><br/>                                                                                                             |
| <span data-ttu-id="ea097-110">чч:мм</span><span class="sxs-lookup"><span data-stu-id="ea097-110">hh:mm</span></span><br/>                          | <span data-ttu-id="ea097-111">Разделенные двоеточием часы и минуты.</span><span class="sxs-lookup"><span data-stu-id="ea097-111">Colon-delimited hour and minutes.</span></span> <span data-ttu-id="ea097-112">Нет заработок AM и PM.</span><span class="sxs-lookup"><span data-stu-id="ea097-112">No AM or PM designation.</span></span><br/> <span data-ttu-id="ea097-113">3:23</span><span class="sxs-lookup"><span data-stu-id="ea097-113">3:23</span></span><br/>                                                                                                                  |
| <span data-ttu-id="ea097-114">чч: мм \[ \] {AP} м</span><span class="sxs-lookup"><span data-stu-id="ea097-114">hh:mm\[ \]{AP}M</span></span><br/>                | <span data-ttu-id="ea097-115">Разделенные двоеточием часы и минуты, необязательное пространство, обозначение AM или PM.</span><span class="sxs-lookup"><span data-stu-id="ea097-115">Colon-delimited hour and minutes, optional space, and AM or PM designation.</span></span><br/> <span data-ttu-id="ea097-116">3:23 AM</span><span class="sxs-lookup"><span data-stu-id="ea097-116">3:23 AM</span></span><br/>                                                                                              |
| <span data-ttu-id="ea097-117">чч:мм:сс</span><span class="sxs-lookup"><span data-stu-id="ea097-117">hh:mm:ss</span></span><br/>                       | <span data-ttu-id="ea097-118">Разделенный двоеточием час, минуты и секунды.</span><span class="sxs-lookup"><span data-stu-id="ea097-118">Colon-delimited hour, minutes and seconds.</span></span> <span data-ttu-id="ea097-119">Нет заработок AM/PM.</span><span class="sxs-lookup"><span data-stu-id="ea097-119">No AM/PM designation.</span></span><br/> <span data-ttu-id="ea097-120">3:23:00</span><span class="sxs-lookup"><span data-stu-id="ea097-120">3:23:00</span></span><br/>                                                                                                         |
| <span data-ttu-id="ea097-121">чч: мм: СС \[ \] {AP} M</span><span class="sxs-lookup"><span data-stu-id="ea097-121">hh:mm:ss\[ \]{AP}M</span></span><br/>             | <span data-ttu-id="ea097-122">Разделенные двоеточием часы, минуты и секунды, необязательное пространство и обозначение AM/PM.</span><span class="sxs-lookup"><span data-stu-id="ea097-122">Colon-delimited hour, minutes and seconds, optional space, and AM/PM designation.</span></span><br/> <span data-ttu-id="ea097-123">3:23:12:00</span><span class="sxs-lookup"><span data-stu-id="ea097-123">3:23:00PM</span></span><br/>                                                                                      |
| <span data-ttu-id="ea097-124">чч: мм: СС: ууу</span><span class="sxs-lookup"><span data-stu-id="ea097-124">hh:mm:ss:uuu</span></span><br/>                   | <span data-ttu-id="ea097-125">Разделенные двоеточием часы, минуты и секунды, а также три цифры, указывающие количество минут, в течение которых исходящий часовой пояс отклоняется от времени в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="ea097-125">Colon-delimited hour, minutes and seconds, and three-digit offset that indicates the number of minutes that the originating time zone deviates from UTC.</span></span><br/>                                    |
| <span data-ttu-id="ea097-126">чч: мм: СС: \[ \[ u \] u \] u</span><span class="sxs-lookup"><span data-stu-id="ea097-126">hh:mm:ss:\[\[u\]u\]u</span></span><br/>           | <span data-ttu-id="ea097-127">Разделенный двоеточием час, минуты и секунды; и одно, два или три цифры, указывающие количество минут, в течение которых исходящий часовой пояс отклоняется от времени в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="ea097-127">Colon-delimited hour, minutes and seconds; and one, two, or three-digit offset that indicates the number of minutes that the originating time zone deviates from UTC.</span></span><br/>                       |
| <span data-ttu-id="ea097-128">чч: мм: СС: ууу \[ \] {AP} M</span><span class="sxs-lookup"><span data-stu-id="ea097-128">hh:mm:ss:uuu\[ \]{AP}M</span></span><br/>         | <span data-ttu-id="ea097-129">Интервал с разделителями-двоеточием, минуты и секунды, смещение из трех цифр, которое указывает количество минут, в течение которых исходящий часовой пояс отклоняется от времени в формате UTC, а также в режиме AM или PM.</span><span class="sxs-lookup"><span data-stu-id="ea097-129">Colon-delimited hour, minutes and seconds, three-digit offset that indicates the number of minutes that the originating time zone deviates from UTC, and AM or PM designation.</span></span><br/>              |
| <span data-ttu-id="ea097-130">чч: мм: СС: \[ \[ u \] u \] u \[ \] {AP} M</span><span class="sxs-lookup"><span data-stu-id="ea097-130">hh:mm:ss:\[\[u\]u\]u\[ \]{AP}M</span></span><br/> | <span data-ttu-id="ea097-131">Разделенный двоеточием час, минуты и секунды; одно, два или три цифры, указывающие количество минут, в течение которых исходящий часовой пояс отклоняется от времени в формате UTC; и AM или PM.</span><span class="sxs-lookup"><span data-stu-id="ea097-131">Colon-delimited hour, minutes and seconds; one, two, or three-digit offset that indicates the number of minutes that the originating time zone deviates from UTC; and AM or PM designation.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="ea097-132">См. также</span><span class="sxs-lookup"><span data-stu-id="ea097-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea097-133">Предложения WHERE</span><span class="sxs-lookup"><span data-stu-id="ea097-133">WHERE Clause</span></span>](where-clause.md)
</dt> </dl>

 

 




