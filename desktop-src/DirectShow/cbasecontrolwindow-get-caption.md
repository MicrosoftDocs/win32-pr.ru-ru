---
description: Метод получения \_ заголовка извлекает заголовок текущего окна.
ms.assetid: 51ce9cf8-0b2a-4459-b005-02dc45444fd8
title: Метод CBaseControlWindow.get_Caption (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_Caption
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b8d743c746f833007d91afd4346f7f48c6218dde
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657129"
---
# <a name="cbasecontrolwindowget_caption-method"></a><span data-ttu-id="79d88-103">Метод Кбасеконтролвиндов. Get \_ Caption</span><span class="sxs-lookup"><span data-stu-id="79d88-103">CBaseControlWindow.get\_Caption method</span></span>

<span data-ttu-id="79d88-104">`get_Caption`Метод извлекает заголовок текущего окна.</span><span class="sxs-lookup"><span data-stu-id="79d88-104">The `get_Caption` method retrieves the current window caption.</span></span>

## <a name="syntax"></a><span data-ttu-id="79d88-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="79d88-105">Syntax</span></span>


```C++
HRESULT get_Caption(
   BSTR *pstrCaption
);
```



## <a name="parameters"></a><span data-ttu-id="79d88-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="79d88-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79d88-107">*пстркаптион*</span><span class="sxs-lookup"><span data-stu-id="79d88-107">*pstrCaption*</span></span> 
</dt> <dd>

<span data-ttu-id="79d88-108">Указатель на заголовок текущего окна.</span><span class="sxs-lookup"><span data-stu-id="79d88-108">Pointer to the current window caption.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79d88-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="79d88-109">Return value</span></span>

<span data-ttu-id="79d88-110">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="79d88-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="79d88-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="79d88-111">Remarks</span></span>

<span data-ttu-id="79d88-112">Большинство окон верхнего уровня на рабочем столе под управлением Windows имеют заголовок (заголовок), связанный с ними.</span><span class="sxs-lookup"><span data-stu-id="79d88-112">Most top-level windows on a Windows-based desktop have a title (caption) associated with them.</span></span> <span data-ttu-id="79d88-113">Это свойство можно запрашивать и задавать с помощью интерфейса [**ивидеовиндов**](/windows/desktop/api/Control/nn-control-ivideowindow) .</span><span class="sxs-lookup"><span data-stu-id="79d88-113">This property can be queried and set through the [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) interface.</span></span> <span data-ttu-id="79d88-114">Любой набор заголовков будет виден только в том случае, если для окна \_ применен стиль «заголовок WS».</span><span class="sxs-lookup"><span data-stu-id="79d88-114">Any caption set will be visible only if the window has the WS\_CAPTION style applied.</span></span> <span data-ttu-id="79d88-115">Если это не так, заголовок можно по-прежнему задать (и получить), хотя он не будет виден пользователю.</span><span class="sxs-lookup"><span data-stu-id="79d88-115">If it does not, the caption can still be set (and retrieved), although it will not be visible to the user.</span></span>

## <a name="requirements"></a><span data-ttu-id="79d88-116">Требования</span><span class="sxs-lookup"><span data-stu-id="79d88-116">Requirements</span></span>



| <span data-ttu-id="79d88-117">Требование</span><span class="sxs-lookup"><span data-stu-id="79d88-117">Requirement</span></span> | <span data-ttu-id="79d88-118">Значение</span><span class="sxs-lookup"><span data-stu-id="79d88-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79d88-119">Header</span><span class="sxs-lookup"><span data-stu-id="79d88-119">Header</span></span><br/>  | <dl> <span data-ttu-id="79d88-120"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="79d88-120"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="79d88-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="79d88-121">Library</span></span><br/> | <dl> <span data-ttu-id="79d88-122"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="79d88-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79d88-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="79d88-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79d88-124">**Класс Кбасеконтролвиндов**</span><span class="sxs-lookup"><span data-stu-id="79d88-124">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




