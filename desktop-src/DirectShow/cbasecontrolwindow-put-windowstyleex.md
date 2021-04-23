---
description: Метод размещения \_ виндовстиликс задает расширенные стили окна.
ms.assetid: 3c5928fe-7cd3-4e1c-9a3f-fa6d7a73dbc3
title: Метод CBaseControlWindow.put_WindowStyleEx (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_WindowStyleEx
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7ee04cf2d2b2dcaafdaf4e989fd1118abf447698
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105658061"
---
# <a name="cbasecontrolwindowput_windowstyleex-method"></a><span data-ttu-id="5974e-103">Кбасеконтролвиндов. размещение \_ метода виндовстиликс</span><span class="sxs-lookup"><span data-stu-id="5974e-103">CBaseControlWindow.put\_WindowStyleEx method</span></span>

<span data-ttu-id="5974e-104">`put_WindowStyleEx`Метод задает расширенные стили окна.</span><span class="sxs-lookup"><span data-stu-id="5974e-104">The `put_WindowStyleEx` method sets the extended window styles.</span></span>

## <a name="syntax"></a><span data-ttu-id="5974e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5974e-105">Syntax</span></span>


```C++
HRESULT put_WindowStyleEx(
  [in] long WindowStyleEx
);
```



## <a name="parameters"></a><span data-ttu-id="5974e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5974e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5974e-107">*Виндовстиликс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5974e-107">*WindowStyleEx* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5974e-108">Значение, указывающее стиль окна элемента управления.</span><span class="sxs-lookup"><span data-stu-id="5974e-108">Value that specifies the style of the control window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5974e-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5974e-109">Return value</span></span>

<span data-ttu-id="5974e-110">Возвращает значение "ошибка".</span><span class="sxs-lookup"><span data-stu-id="5974e-110">Returns NOERROR.</span></span>

## <a name="remarks"></a><span data-ttu-id="5974e-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5974e-111">Remarks</span></span>

<span data-ttu-id="5974e-112">Этот метод использует расширенные стили окна.</span><span class="sxs-lookup"><span data-stu-id="5974e-112">This method uses extended window styles.</span></span> <span data-ttu-id="5974e-113">Полный список расширенных стилей окон см. в разделе функция Microsoft Win32 **CreateWindowEx** .</span><span class="sxs-lookup"><span data-stu-id="5974e-113">For a complete list of extended window styles, see the Microsoft Win32 **CreateWindowEx** function.</span></span> <span data-ttu-id="5974e-114">Чтобы изменить стиль окна, извлеките текущий стиль окна, а затем добавьте или удалите необходимые битовые поля.</span><span class="sxs-lookup"><span data-stu-id="5974e-114">To change the window style, retrieve the current window style, and then add or remove the necessary bit fields.</span></span>

<span data-ttu-id="5974e-115">Не используйте следующие стили окна, так как они не проверены.</span><span class="sxs-lookup"><span data-stu-id="5974e-115">Do not use the following window styles because they are not validated.</span></span>

-   <span data-ttu-id="5974e-116">протокол WS \_ отключен</span><span class="sxs-lookup"><span data-stu-id="5974e-116">WS\_DISABLED</span></span>
-   <span data-ttu-id="5974e-117">\_HSCROLL WS</span><span class="sxs-lookup"><span data-stu-id="5974e-117">WS\_HSCROLL</span></span>
-   <span data-ttu-id="5974e-118">\_значок WS</span><span class="sxs-lookup"><span data-stu-id="5974e-118">WS\_ICONIC</span></span>
-   <span data-ttu-id="5974e-119">\_развернуть WS</span><span class="sxs-lookup"><span data-stu-id="5974e-119">WS\_MAXIMIZE</span></span>
-   <span data-ttu-id="5974e-120">WS \_ Minimize</span><span class="sxs-lookup"><span data-stu-id="5974e-120">WS\_MINIMIZE</span></span>
-   <span data-ttu-id="5974e-121">\_VSCROLL WS</span><span class="sxs-lookup"><span data-stu-id="5974e-121">WS\_VSCROLL</span></span>

<span data-ttu-id="5974e-122">С некоторыми исключениями (отмеченными здесь) допустимые флаги совпадают с допустимыми для функции Win32 **CreateWindow** .</span><span class="sxs-lookup"><span data-stu-id="5974e-122">With some exceptions (noted here), the acceptable flags are the same as those allowed by the Win32 **CreateWindow** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="5974e-123">Требования</span><span class="sxs-lookup"><span data-stu-id="5974e-123">Requirements</span></span>



| <span data-ttu-id="5974e-124">Требование</span><span class="sxs-lookup"><span data-stu-id="5974e-124">Requirement</span></span> | <span data-ttu-id="5974e-125">Значение</span><span class="sxs-lookup"><span data-stu-id="5974e-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5974e-126">Header</span><span class="sxs-lookup"><span data-stu-id="5974e-126">Header</span></span><br/>  | <dl> <span data-ttu-id="5974e-127"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5974e-127"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5974e-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5974e-128">Library</span></span><br/> | <dl> <span data-ttu-id="5974e-129"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="5974e-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5974e-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5974e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5974e-131">**Класс Кбасеконтролвиндов**</span><span class="sxs-lookup"><span data-stu-id="5974e-131">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




