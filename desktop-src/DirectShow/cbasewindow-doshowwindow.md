---
description: Метод Дошоввиндов задает режим отображения окна.
ms.assetid: 4180de9d-ef40-40e3-aa37-be54283b1f97
title: Кбасевиндов. Дошоввиндов, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.DoShowWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a2a1f7d4cd9bc4600733d5d33f9df6d3b6998f57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675480"
---
# <a name="cbasewindowdoshowwindow-method"></a><span data-ttu-id="6b249-103">Кбасевиндов. Дошоввиндов, метод</span><span class="sxs-lookup"><span data-stu-id="6b249-103">CBaseWindow.DoShowWindow method</span></span>

<span data-ttu-id="6b249-104">Метод **дошоввиндов** задает режим отображения окна.</span><span class="sxs-lookup"><span data-stu-id="6b249-104">The **DoShowWindow** method sets the window's show state.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b249-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6b249-105">Syntax</span></span>


```C++
HRESULT DoShowWindow(
   LONG ShowCmd
);
```



## <a name="parameters"></a><span data-ttu-id="6b249-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6b249-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b249-107">*шовкмд*</span><span class="sxs-lookup"><span data-stu-id="6b249-107">*ShowCmd*</span></span> 
</dt> <dd>

<span data-ttu-id="6b249-108">Флаг, указывающий способ отображения окна.</span><span class="sxs-lookup"><span data-stu-id="6b249-108">Flag that specifies how the window is to be shown.</span></span> <span data-ttu-id="6b249-109">Значением может быть любая константа, определенная для параметра *нкмдшов* функции [**ShowWindow**](/windows/desktop/api/winuser/nf-winuser-showwindow) .</span><span class="sxs-lookup"><span data-stu-id="6b249-109">The value can be any constant defined for the *nCmdShow* parameter of the [**ShowWindow**](/windows/desktop/api/winuser/nf-winuser-showwindow) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b249-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6b249-110">Return value</span></span>

<span data-ttu-id="6b249-111">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="6b249-111">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6b249-112">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6b249-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b249-113">Требования</span><span class="sxs-lookup"><span data-stu-id="6b249-113">Requirements</span></span>



| <span data-ttu-id="6b249-114">Требование</span><span class="sxs-lookup"><span data-stu-id="6b249-114">Requirement</span></span> | <span data-ttu-id="6b249-115">Значение</span><span class="sxs-lookup"><span data-stu-id="6b249-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b249-116">Header</span><span class="sxs-lookup"><span data-stu-id="6b249-116">Header</span></span><br/>  | <dl> <span data-ttu-id="6b249-117"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6b249-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6b249-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6b249-118">Library</span></span><br/> | <dl> <span data-ttu-id="6b249-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="6b249-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b249-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6b249-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b249-121">**Класс Кбасевиндов**</span><span class="sxs-lookup"><span data-stu-id="6b249-121">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

