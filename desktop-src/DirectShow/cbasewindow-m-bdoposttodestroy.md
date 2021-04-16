---
description: Флаг, указывающий, отправляет ли окно сообщение об уничтожении.
ms.assetid: 553a372e-1abe-4661-bfa5-b8a63be63c72
title: 'Элемент Кбасевиндов:: m_bDoPostToDestroy (Винутил. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bDoPostToDestroy
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 804d0910760ddac5ea4d74979293f43e5b189225
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657694"
---
# <a name="cbasewindowm_bdoposttodestroy-member"></a><span data-ttu-id="3b15f-103">Элемент Кбасевиндов:: m \_ бдопосттодестрой</span><span class="sxs-lookup"><span data-stu-id="3b15f-103">CBaseWindow::m\_bDoPostToDestroy member</span></span>

<span data-ttu-id="3b15f-104">Флаг, указывающий, отправляет ли окно сообщение об уничтожении.</span><span class="sxs-lookup"><span data-stu-id="3b15f-104">Flag that specifies whether the window posts or sends its destruction message.</span></span> <span data-ttu-id="3b15f-105">Если **значение — true**, метод [**Кбасевиндов::D оневисвиндов**](cbasewindow-donewithwindow.md) использует функцию посылки **сообщений** для отправки частного сообщения об уничтожении.</span><span class="sxs-lookup"><span data-stu-id="3b15f-105">If **TRUE**, the [**CBaseWindow::DoneWithWindow**](cbasewindow-donewithwindow.md) method uses the **PostMessage** function to send itself a private destruction message.</span></span> <span data-ttu-id="3b15f-106">Если **значение равно false**, **Доневисвиндов** использует функцию **SendMessage** для отправки сообщения.</span><span class="sxs-lookup"><span data-stu-id="3b15f-106">If **FALSE**, **DoneWithWindow** uses the **SendMessage** function to send the message.</span></span> <span data-ttu-id="3b15f-107">По умолчанию используется значение **false**.</span><span class="sxs-lookup"><span data-stu-id="3b15f-107">By default, the value is **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b15f-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3b15f-108">Syntax</span></span>


```C++
BOOL m_bDoPostToDestroy;
```



## <a name="requirements"></a><span data-ttu-id="3b15f-109">Требования</span><span class="sxs-lookup"><span data-stu-id="3b15f-109">Requirements</span></span>



| <span data-ttu-id="3b15f-110">Требование</span><span class="sxs-lookup"><span data-stu-id="3b15f-110">Requirement</span></span> | <span data-ttu-id="3b15f-111">Значение</span><span class="sxs-lookup"><span data-stu-id="3b15f-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b15f-112">Header</span><span class="sxs-lookup"><span data-stu-id="3b15f-112">Header</span></span><br/>  | <dl> <span data-ttu-id="3b15f-113"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3b15f-113"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3b15f-114">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3b15f-114">Library</span></span><br/> | <dl> <span data-ttu-id="3b15f-115"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="3b15f-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b15f-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3b15f-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b15f-117">**Класс Кбасевиндов**</span><span class="sxs-lookup"><span data-stu-id="3b15f-117">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




