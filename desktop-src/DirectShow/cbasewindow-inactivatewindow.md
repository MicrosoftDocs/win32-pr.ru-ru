---
description: Метод Инактиватевиндов деактивирует окно. В базовом классе этот метод скрывает окно.
ms.assetid: b575d4fd-dee1-4ae5-abb4-e92ae361e82a
title: Кбасевиндов. Инактиватевиндов, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.InactivateWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d1c5e925a3d9b510918636a221d5ad6e1b7da736
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675470"
---
# <a name="cbasewindowinactivatewindow-method"></a><span data-ttu-id="0973c-104">Кбасевиндов. Инактиватевиндов, метод</span><span class="sxs-lookup"><span data-stu-id="0973c-104">CBaseWindow.InactivateWindow method</span></span>

<span data-ttu-id="0973c-105">`InactivateWindow`Метод деактивирует окно.</span><span class="sxs-lookup"><span data-stu-id="0973c-105">The `InactivateWindow` method inactivates the window.</span></span> <span data-ttu-id="0973c-106">В базовом классе этот метод скрывает окно.</span><span class="sxs-lookup"><span data-stu-id="0973c-106">In the base class, this method hides the window.</span></span>

## <a name="syntax"></a><span data-ttu-id="0973c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0973c-107">Syntax</span></span>


```C++
virtual HRESULT InactivateWindow();
```



## <a name="parameters"></a><span data-ttu-id="0973c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="0973c-108">Parameters</span></span>

<span data-ttu-id="0973c-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="0973c-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0973c-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0973c-110">Return value</span></span>

<span data-ttu-id="0973c-111">Возвращает одно из значений **HRESULT** , приведенных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="0973c-111">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="0973c-112">Код возврата</span><span class="sxs-lookup"><span data-stu-id="0973c-112">Return code</span></span>                                                                             | <span data-ttu-id="0973c-113">Описание</span><span class="sxs-lookup"><span data-stu-id="0973c-113">Description</span></span>                            |
|-----------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <span data-ttu-id="0973c-114"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="0973c-114"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="0973c-115">Успешно.</span><span class="sxs-lookup"><span data-stu-id="0973c-115">Success.</span></span><br/>                    |
| <dl> <span data-ttu-id="0973c-116"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="0973c-116"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="0973c-117">Окно уже неактивно.</span><span class="sxs-lookup"><span data-stu-id="0973c-117">Window is already inactive.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="0973c-118">Требования</span><span class="sxs-lookup"><span data-stu-id="0973c-118">Requirements</span></span>



| <span data-ttu-id="0973c-119">Требование</span><span class="sxs-lookup"><span data-stu-id="0973c-119">Requirement</span></span> | <span data-ttu-id="0973c-120">Значение</span><span class="sxs-lookup"><span data-stu-id="0973c-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0973c-121">Header</span><span class="sxs-lookup"><span data-stu-id="0973c-121">Header</span></span><br/>  | <dl> <span data-ttu-id="0973c-122"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0973c-122"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0973c-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0973c-123">Library</span></span><br/> | <dl> <span data-ttu-id="0973c-124"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="0973c-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0973c-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0973c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0973c-126">**Класс Кбасевиндов**</span><span class="sxs-lookup"><span data-stu-id="0973c-126">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




