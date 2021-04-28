---
description: Событие InkPicture. Таблетаддед — происходит при добавлении Иинктаблет в систему.
ms.assetid: 5df10efd-7055-43fa-881f-67eb5fd6adcf
title: Событие InkPicture. Таблетаддед (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81c5121b668f27034a04230311ee88ebb7564802
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113662"
---
# <a name="inkpicturetabletadded-event"></a><span data-ttu-id="d0480-103">Событие InkPicture. Таблетаддед</span><span class="sxs-lookup"><span data-stu-id="d0480-103">InkPicture.TabletAdded event</span></span>

<span data-ttu-id="d0480-104">Происходит при добавлении [**иинктаблет**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) в систему.</span><span class="sxs-lookup"><span data-stu-id="d0480-104">Occurs when a [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) is added to the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0480-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d0480-105">Syntax</span></span>


```C++
void TabletAdded(
  [in] IInkTablet *Tablet
);
```



## <a name="parameters"></a><span data-ttu-id="d0480-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d0480-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0480-107">*Планшетный ПК* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d0480-107">*Tablet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0480-108">Объект [**иинктаблет**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) , который был добавлен в систему.</span><span class="sxs-lookup"><span data-stu-id="d0480-108">The [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) object that has been added to the system.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0480-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d0480-109">Return value</span></span>

<span data-ttu-id="d0480-110">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="d0480-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0480-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="d0480-111">Remarks</span></span>

<span data-ttu-id="d0480-112">Этот метод события определен в интерфейсах диспетчеризации (DISP) **\_ иинкколлекторевентс**, **\_ иинковерлайевентс** и **\_ иинкпиктуривентс** с идентификатором DISPID \_ ицетаблетаддед.</span><span class="sxs-lookup"><span data-stu-id="d0480-112">This event method is defined in the **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICETabletAdded.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0480-113">Требования</span><span class="sxs-lookup"><span data-stu-id="d0480-113">Requirements</span></span>



| <span data-ttu-id="d0480-114">Требование</span><span class="sxs-lookup"><span data-stu-id="d0480-114">Requirement</span></span> | <span data-ttu-id="d0480-115">Значение</span><span class="sxs-lookup"><span data-stu-id="d0480-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0480-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d0480-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d0480-117">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="d0480-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="d0480-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d0480-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d0480-119">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="d0480-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="d0480-120">Header</span><span class="sxs-lookup"><span data-stu-id="d0480-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0480-121"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="d0480-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="d0480-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d0480-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="d0480-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d0480-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="d0480-124">См. также</span><span class="sxs-lookup"><span data-stu-id="d0480-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0480-125">InkPicture</span><span class="sxs-lookup"><span data-stu-id="d0480-125">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="d0480-126">**Интерфейс Иинктаблет**</span><span class="sxs-lookup"><span data-stu-id="d0480-126">**IInkTablet Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

 




