---
description: Можно указать, что драйвер обрезает кадры.
ms.assetid: a4f53568-684b-48cf-835b-915cefb45a5d
title: Обрезка рамки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1507b82ffedeb26939d5d954f116bb009ed0ab41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663027"
---
# <a name="clipping-a-frame"></a><span data-ttu-id="2946c-103">Обрезка рамки</span><span class="sxs-lookup"><span data-stu-id="2946c-103">Clipping a Frame</span></span>

<span data-ttu-id="2946c-104">Можно указать, что драйвер обрезает кадры.</span><span class="sxs-lookup"><span data-stu-id="2946c-104">You can specify that the driver clip the frames.</span></span> <span data-ttu-id="2946c-105">(Если другие разделы фильтра записи опущены, это может быть единственная функция фильтра записи).</span><span class="sxs-lookup"><span data-stu-id="2946c-105">(If the other capture filter sections are omitted, this may be the only function of your capture filter).</span></span> <span data-ttu-id="2946c-106">Если поле **нфрамебитестокопи** не равно нулю (0), его значение указывает, сколько байт каждого полученного кадра следует хранить.</span><span class="sxs-lookup"><span data-stu-id="2946c-106">If the **nFrameBytesToCopy** field is not zero (0), its value specifies how many bytes of each frame received to retain.</span></span> <span data-ttu-id="2946c-107">Если поле равно нулю, весь фрейм сохраняется.</span><span class="sxs-lookup"><span data-stu-id="2946c-107">If the field is zero, then the whole frame is retained.</span></span>

> [!Note]  
> <span data-ttu-id="2946c-108">Вы можете обрезать любой кадр, который передает другие части фильтра записи, установив **нфрамебитестокопи**.</span><span class="sxs-lookup"><span data-stu-id="2946c-108">You may clip any frame that passes the other portions of your capture filter by setting **nFrameBytesToCopy**.</span></span>

 

 

 



