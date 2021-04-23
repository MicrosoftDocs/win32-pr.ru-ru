---
description: Происходит при завершении перерисовки элемента управления InkPicture.
ms.assetid: a8194cff-ed94-402e-8564-08d370f958b4
title: Событие InkPicture. окрашено (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60188ef87d88ba7412a07300e708718bedc947fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712210"
---
# <a name="inkpicturepainted-event"></a><span data-ttu-id="f48f2-103">Событие InkPicture. окрашено</span><span class="sxs-lookup"><span data-stu-id="f48f2-103">InkPicture.Painted event</span></span>

<span data-ttu-id="f48f2-104">Происходит при завершении перерисовки элемента управления [InkPicture](inkpicture-control-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="f48f2-104">Occurs when the [InkPicture](inkpicture-control-reference.md) control has completed redrawing itself.</span></span>

## <a name="syntax"></a><span data-ttu-id="f48f2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f48f2-105">Syntax</span></span>


```C++
void Painted(
  [in] long         hDC,
  [in] InkRectangle *Rect
);
```



## <a name="parameters"></a><span data-ttu-id="f48f2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f48f2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f48f2-107">*HDC* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f48f2-107">*hDC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f48f2-108">Контекст устройства, в котором произошло событие.</span><span class="sxs-lookup"><span data-stu-id="f48f2-108">The device context on which the event occurred.</span></span>

</dd> <dt>

<span data-ttu-id="f48f2-109">*Rect* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f48f2-109">*Rect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f48f2-110">Перерисовка [**инкректангле**](inkrectangle-class.md) .</span><span class="sxs-lookup"><span data-stu-id="f48f2-110">The [**InkRectangle**](inkrectangle-class.md) that was repainted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f48f2-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f48f2-111">Return value</span></span>

<span data-ttu-id="f48f2-112">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="f48f2-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f48f2-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f48f2-113">Remarks</span></span>

<span data-ttu-id="f48f2-114">Этот метод события определен в DISP-интерфейсах **\_ иинковерлайевентс** и **\_ иинкпиктуривентс** с идентификатором DISPID \_ иоепаинтед.</span><span class="sxs-lookup"><span data-stu-id="f48f2-114">This event method is defined in the **\_IInkOverlayEvents** and **\_IInkPictureEvents** dispinterfaces with an ID of DISPID\_IOEPainted.</span></span>

## <a name="requirements"></a><span data-ttu-id="f48f2-115">Требования</span><span class="sxs-lookup"><span data-stu-id="f48f2-115">Requirements</span></span>



| <span data-ttu-id="f48f2-116">Требование</span><span class="sxs-lookup"><span data-stu-id="f48f2-116">Requirement</span></span> | <span data-ttu-id="f48f2-117">Значение</span><span class="sxs-lookup"><span data-stu-id="f48f2-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f48f2-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f48f2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f48f2-119">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="f48f2-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="f48f2-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f48f2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f48f2-121">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f48f2-121">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="f48f2-122">Header</span><span class="sxs-lookup"><span data-stu-id="f48f2-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f48f2-123"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="f48f2-123"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="f48f2-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f48f2-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="f48f2-125"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f48f2-125"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="f48f2-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f48f2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f48f2-127">InkPicture</span><span class="sxs-lookup"><span data-stu-id="f48f2-127">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

 




