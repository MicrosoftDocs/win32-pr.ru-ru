---
title: монсдайстате
description: Тип данных МОНСДАЙСТАТЕ — это битовое поле, которое содержит состояние каждого дня месяца.
ms.assetid: eb3dd6cb-738e-424b-945b-1485798a444c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2286482460ec87982c46a564e8441edd9bf7bb43
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103887735"
---
# <a name="monthdaystate"></a><span data-ttu-id="f8f43-103">монсдайстате</span><span class="sxs-lookup"><span data-stu-id="f8f43-103">MONTHDAYSTATE</span></span>

<span data-ttu-id="f8f43-104">Тип данных МОНСДАЙСТАТЕ — это битовое поле, которое содержит состояние каждого дня месяца.</span><span class="sxs-lookup"><span data-stu-id="f8f43-104">The MONTHDAYSTATE data type is a bitfield that holds the state of each day in a month.</span></span> <span data-ttu-id="f8f43-105">Тип данных определяется в Коммктрл. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="f8f43-105">The data type is defined in Commctrl.h as follows:</span></span>


```
typedef DWORD MONTHDAYSTATE, *LPMONTHDAYSTATE;
```



<span data-ttu-id="f8f43-106">Каждый бит (от 0 до 30) представляет состояние дня в месяце.</span><span class="sxs-lookup"><span data-stu-id="f8f43-106">Each bit (0 through 30) represents the state of a day in a month.</span></span> <span data-ttu-id="f8f43-107">Если бит включен, соответствующий день будет отображаться полужирным шрифтом; в противном случае он будет отображаться без каких бы то ни было внимания.</span><span class="sxs-lookup"><span data-stu-id="f8f43-107">If a bit is on, the corresponding day will be displayed in bold; otherwise it will be displayed with no emphasis.</span></span>

<span data-ttu-id="f8f43-108">Этот тип данных используется с сообщением [**MCM \_ сетдайстате**](mcm-setdaystate.md) и соответствующим макросом, [**монскал \_ сетдайстате**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setdaystate).</span><span class="sxs-lookup"><span data-stu-id="f8f43-108">This data type is used with the [**MCM\_SETDAYSTATE**](mcm-setdaystate.md) message and the corresponding macro, [**MonthCal\_SetDayState**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setdaystate).</span></span> <span data-ttu-id="f8f43-109">Если значения МОНСДАЙСТАТЕ используются в ссылке на месяцы короче 31 день, будут доступны только необходимые биты.</span><span class="sxs-lookup"><span data-stu-id="f8f43-109">When MONTHDAYSTATE values are used in reference to months shorter than 31 days, only the needed bits will be accessed.</span></span>

<span data-ttu-id="f8f43-110">Этот тип данных был впервые определен в Comctl32.dll [версии 4,70](common-control-versions.md) .</span><span class="sxs-lookup"><span data-stu-id="f8f43-110">This data type was first defined in [Version 4.70](common-control-versions.md) of Comctl32.dll.</span></span>

 

 




