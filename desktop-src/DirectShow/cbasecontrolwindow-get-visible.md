---
description: Метод Get \_ Visible извлекает текущую видимость окна.
ms.assetid: 7e643569-1116-4562-be33-babd12a7e899
title: Метод CBaseControlWindow.get_Visible (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_Visible
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3bc38a0b35f46de223ed84174c3b10f5300cc94d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669236"
---
# <a name="cbasecontrolwindowget_visible-method"></a><span data-ttu-id="0028e-103">Кбасеконтролвиндов. получить \_ видимый метод</span><span class="sxs-lookup"><span data-stu-id="0028e-103">CBaseControlWindow.get\_Visible method</span></span>

<span data-ttu-id="0028e-104">`get_Visible`Метод получает текущую видимость окна.</span><span class="sxs-lookup"><span data-stu-id="0028e-104">The `get_Visible` method retrieves the current window visibility.</span></span>

## <a name="syntax"></a><span data-ttu-id="0028e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0028e-105">Syntax</span></span>


```C++
HRESULT get_Visible(
   long *pVisible
);
```



## <a name="parameters"></a><span data-ttu-id="0028e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0028e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0028e-107">*пвисибле*</span><span class="sxs-lookup"><span data-stu-id="0028e-107">*pVisible*</span></span> 
</dt> <dd>

<span data-ttu-id="0028e-108">Указатель на логический флаг автоматизации (0 — Off, 1 — включено).</span><span class="sxs-lookup"><span data-stu-id="0028e-108">Pointer to an Automation Boolean flag (0 is off,  1 is on).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0028e-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0028e-109">Return value</span></span>

<span data-ttu-id="0028e-110">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0028e-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0028e-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0028e-111">Remarks</span></span>

<span data-ttu-id="0028e-112">Эта функция – член возвращает значение 1, если окно имеет \_ стиль WS Visible; в противном случае — 0.</span><span class="sxs-lookup"><span data-stu-id="0028e-112">This member function returns  1 if the window has the WS\_VISIBLE style; 0 otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="0028e-113">Требования</span><span class="sxs-lookup"><span data-stu-id="0028e-113">Requirements</span></span>



| <span data-ttu-id="0028e-114">Требование</span><span class="sxs-lookup"><span data-stu-id="0028e-114">Requirement</span></span> | <span data-ttu-id="0028e-115">Значение</span><span class="sxs-lookup"><span data-stu-id="0028e-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0028e-116">Header</span><span class="sxs-lookup"><span data-stu-id="0028e-116">Header</span></span><br/>  | <dl> <span data-ttu-id="0028e-117"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0028e-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0028e-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0028e-118">Library</span></span><br/> | <dl> <span data-ttu-id="0028e-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="0028e-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0028e-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0028e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0028e-121">**Класс Кбасеконтролвиндов**</span><span class="sxs-lookup"><span data-stu-id="0028e-121">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




