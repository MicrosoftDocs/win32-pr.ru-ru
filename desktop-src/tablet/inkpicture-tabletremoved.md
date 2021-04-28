---
description: Событие InkPicture. Таблетремовед — происходит при удалении Иинктаблет из системы.
ms.assetid: 9a4640a7-cbd9-4304-88c6-86036423628d
title: Событие InkPicture. Таблетремовед (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 929458c6b972143852b5921a8c8364a54a4b6f41
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113652"
---
# <a name="inkpicturetabletremoved-event"></a><span data-ttu-id="3cca8-103">Событие InkPicture. Таблетремовед</span><span class="sxs-lookup"><span data-stu-id="3cca8-103">InkPicture.TabletRemoved event</span></span>

<span data-ttu-id="3cca8-104">Происходит при удалении [**иинктаблет**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) из системы.</span><span class="sxs-lookup"><span data-stu-id="3cca8-104">Occurs when a [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) is removed from the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="3cca8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3cca8-105">Syntax</span></span>


```C++
void TabletRemoved(
  [in] long TabletId
);
```



## <a name="parameters"></a><span data-ttu-id="3cca8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3cca8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3cca8-107">*Таблетид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3cca8-107">*TabletId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3cca8-108">Значение типа Long, которое было использовано в качестве идентификатора удаленного объекта [**иинктаблет**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) .</span><span class="sxs-lookup"><span data-stu-id="3cca8-108">The long value that was used as the ID for the [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) object that was removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3cca8-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3cca8-109">Return value</span></span>

<span data-ttu-id="3cca8-110">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="3cca8-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3cca8-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="3cca8-111">Remarks</span></span>

<span data-ttu-id="3cca8-112">Этот метод события определен в интерфейсах диспетчеризации (DISP) **\_ иинкколлекторевентс**, **\_ иинковерлайевентс** и **\_ иинкпиктуривентс** с идентификатором DISPID \_ ицетаблетремовед.</span><span class="sxs-lookup"><span data-stu-id="3cca8-112">This event method is defined in the **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICETabletRemoved.</span></span>

## <a name="requirements"></a><span data-ttu-id="3cca8-113">Требования</span><span class="sxs-lookup"><span data-stu-id="3cca8-113">Requirements</span></span>



| <span data-ttu-id="3cca8-114">Требование</span><span class="sxs-lookup"><span data-stu-id="3cca8-114">Requirement</span></span> | <span data-ttu-id="3cca8-115">Значение</span><span class="sxs-lookup"><span data-stu-id="3cca8-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3cca8-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3cca8-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3cca8-117">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="3cca8-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="3cca8-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3cca8-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3cca8-119">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="3cca8-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="3cca8-120">Header</span><span class="sxs-lookup"><span data-stu-id="3cca8-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="3cca8-121"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="3cca8-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="3cca8-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3cca8-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="3cca8-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3cca8-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="3cca8-124">См. также</span><span class="sxs-lookup"><span data-stu-id="3cca8-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3cca8-125">InkPicture</span><span class="sxs-lookup"><span data-stu-id="3cca8-125">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="3cca8-126">**Интерфейс Иинктаблет**</span><span class="sxs-lookup"><span data-stu-id="3cca8-126">**IInkTablet Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

 




