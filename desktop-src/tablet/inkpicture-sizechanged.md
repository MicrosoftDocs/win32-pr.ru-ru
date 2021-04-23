---
description: Происходит после изменения размера элемента управления InkPicture, в частности после того, как изменяется значение свойства Width или Height.
ms.assetid: a5fc6c82-f9c8-4104-8abe-082c47c56be9
title: Событие InkPicture. SizeChanged (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5675d2a581d9e8973b88fa9fb6e213f54c0e283
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999428"
---
# <a name="inkpicturesizechanged-event"></a><span data-ttu-id="202df-103">Событие InkPicture. SizeChanged</span><span class="sxs-lookup"><span data-stu-id="202df-103">InkPicture.SizeChanged event</span></span>

<span data-ttu-id="202df-104">Происходит после изменения размера элемента управления [InkPicture](inkpicture-control-reference.md) , в частности после того, как изменяется значение свойства [**Width**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_width) или [**Height**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_height) .</span><span class="sxs-lookup"><span data-stu-id="202df-104">Occurs after the [InkPicture](inkpicture-control-reference.md) control has been resized, specifically, after the [**Width**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_width) or [**Height**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_height) property value changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="202df-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="202df-105">Syntax</span></span>


```C++
void SizeChanged(
  [in] long Left,
  [in] long Top,
  [in] long Right,
  [in] long Bottom
);
```



## <a name="parameters"></a><span data-ttu-id="202df-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="202df-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="202df-107">По *левому краю* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="202df-107">*Left* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="202df-108">Координата по оси x левой стороны элемента управления [InkPicture](inkpicture-control-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="202df-108">The x-coordinate of the left side of the [InkPicture](inkpicture-control-reference.md) control.</span></span>

</dd> <dt>

<span data-ttu-id="202df-109">В *Начало* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="202df-109">*Top* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="202df-110">Координата по оси y верхнего края элемента управления [InkPicture](inkpicture-control-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="202df-110">The y-coordinate of the top of the [InkPicture](inkpicture-control-reference.md) control.</span></span>

</dd> <dt>

<span data-ttu-id="202df-111">По *правому краю* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="202df-111">*Right* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="202df-112">Координата по оси x правой стороны элемента управления [InkPicture](inkpicture-control-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="202df-112">The x-coordinate of the right side of the [InkPicture](inkpicture-control-reference.md) control.</span></span>

</dd> <dt>

<span data-ttu-id="202df-113">По *нижнему краю* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="202df-113">*Bottom* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="202df-114">Координата по оси y нижней части элемента управления [InkPicture](inkpicture-control-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="202df-114">The y-coordinate of the bottom of the [InkPicture](inkpicture-control-reference.md) control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="202df-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="202df-115">Return value</span></span>

<span data-ttu-id="202df-116">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="202df-116">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="202df-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="202df-117">Remarks</span></span>

<span data-ttu-id="202df-118">Этот метод события определен в интерфейсе **\_ иинкпиктуривентс** .</span><span class="sxs-lookup"><span data-stu-id="202df-118">This event method is defined in the **\_IInkPictureEvents** interface.</span></span> <span data-ttu-id="202df-119">Интерфейс **\_ иинкпиктуривентс** реализует интерфейс [**IDISPATCH**](/windows/win32/api/oaidl/nn-oaidl-idispatch) с идентификатором DISPID \_ ипесизечанжед.</span><span class="sxs-lookup"><span data-stu-id="202df-119">The **\_IInkPictureEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IPESizeChanged.</span></span>

## <a name="requirements"></a><span data-ttu-id="202df-120">Требования</span><span class="sxs-lookup"><span data-stu-id="202df-120">Requirements</span></span>



| <span data-ttu-id="202df-121">Требование</span><span class="sxs-lookup"><span data-stu-id="202df-121">Requirement</span></span> | <span data-ttu-id="202df-122">Значение</span><span class="sxs-lookup"><span data-stu-id="202df-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="202df-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="202df-123">Minimum supported client</span></span><br/> | <span data-ttu-id="202df-124">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="202df-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="202df-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="202df-125">Minimum supported server</span></span><br/> | <span data-ttu-id="202df-126">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="202df-126">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="202df-127">Header</span><span class="sxs-lookup"><span data-stu-id="202df-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="202df-128"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="202df-128"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="202df-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="202df-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="202df-130"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="202df-130"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="202df-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="202df-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="202df-132">InkPicture</span><span class="sxs-lookup"><span data-stu-id="202df-132">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

