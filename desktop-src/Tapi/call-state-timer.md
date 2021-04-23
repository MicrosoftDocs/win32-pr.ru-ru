---
description: В настоящее время все временные вызовы остаются в приложении.
ms.assetid: 9eb98b48-4bee-4f6d-b818-2f81b36591da
title: Таймер состояния вызова
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5d273d7f8439ebfee9d6668565745ed2c209f70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673357"
---
# <a name="call-state-timer"></a><span data-ttu-id="c2bcf-103">Таймер состояния вызова</span><span class="sxs-lookup"><span data-stu-id="c2bcf-103">Call State Timer</span></span>

<span data-ttu-id="c2bcf-104">В настоящее время все временные вызовы остаются в приложении.</span><span class="sxs-lookup"><span data-stu-id="c2bcf-104">Currently, all timing of calls is left up to applications.</span></span> <span data-ttu-id="c2bcf-105">Это может быть утомительным, если приложение наблюдает за большим количеством вызовов, и если имеется несколько приложений, которые, возможно, на нескольких серверах, они могут быть необходимы для поддержки таймеров в одних и тех же вызовах.</span><span class="sxs-lookup"><span data-stu-id="c2bcf-105">This can be burdensome if the application is monitoring a large number of calls, and if multiple applications are present, possibly on multiple servers, it can be necessary for them to all maintain timers on the same calls.</span></span> <span data-ttu-id="c2bcf-106">Поэтому он имеет более осмысленное значение для обработки времени вызова сервером.</span><span class="sxs-lookup"><span data-stu-id="c2bcf-106">It therefore makes more sense for call state timing to be handled by the server.</span></span>

<span data-ttu-id="c2bcf-107">Элемент **тстатинтритиме** в [**линекаллстатус**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) позволяет получать сведения о времени вызовов в состояниях.</span><span class="sxs-lookup"><span data-stu-id="c2bcf-107">The **tStateEntryTime** member in [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) allows timing of calls in states to be reported.</span></span> <span data-ttu-id="c2bcf-108">Элемент (типа **систиме**) указывает время, когда было введено текущее состояние.</span><span class="sxs-lookup"><span data-stu-id="c2bcf-108">The member (of type **SYSTIME**) indicates the time at which the current state was entered.</span></span>

 

 



