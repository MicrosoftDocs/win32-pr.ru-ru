---
description: Событие InkCollector. Таблетремовед — происходит при удалении Иинктаблет из системы.
ms.assetid: 659a9809-fe35-4d34-aa95-af353998c350
title: Событие InkCollector. Таблетремовед (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df76c27b1a0d47e456f69a789d17ef6343706284
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110002"
---
# <a name="inkcollectortabletremoved-event"></a><span data-ttu-id="5dde0-103">Событие InkCollector. Таблетремовед</span><span class="sxs-lookup"><span data-stu-id="5dde0-103">InkCollector.TabletRemoved event</span></span>

<span data-ttu-id="5dde0-104">Происходит при удалении [**иинктаблет**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) из системы.</span><span class="sxs-lookup"><span data-stu-id="5dde0-104">Occurs when a [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) is removed from the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="5dde0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5dde0-105">Syntax</span></span>


```C++
void TabletRemoved(
  [in] long TabletId
);
```



## <a name="parameters"></a><span data-ttu-id="5dde0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5dde0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5dde0-107">*Таблетид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5dde0-107">*TabletId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5dde0-108">Значение типа Long, которое было использовано в качестве идентификатора удаленного объекта [**иинктаблет**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) .</span><span class="sxs-lookup"><span data-stu-id="5dde0-108">The long value that was used as the ID for the [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) object that was removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5dde0-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5dde0-109">Return value</span></span>

<span data-ttu-id="5dde0-110">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="5dde0-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5dde0-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="5dde0-111">Remarks</span></span>

<span data-ttu-id="5dde0-112">Этот метод события определен в \_ \_ \_ интерфейсах диспетчеризации (DISP) иинкколлекторевентс, иинковерлайевентс и иинкпиктуривентс с идентификатором DISPID \_ ицетаблетремовед.</span><span class="sxs-lookup"><span data-stu-id="5dde0-112">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICETabletRemoved.</span></span>

## <a name="requirements"></a><span data-ttu-id="5dde0-113">Требования</span><span class="sxs-lookup"><span data-stu-id="5dde0-113">Requirements</span></span>



| <span data-ttu-id="5dde0-114">Требование</span><span class="sxs-lookup"><span data-stu-id="5dde0-114">Requirement</span></span> | <span data-ttu-id="5dde0-115">Значение</span><span class="sxs-lookup"><span data-stu-id="5dde0-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5dde0-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5dde0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5dde0-117">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="5dde0-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="5dde0-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5dde0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5dde0-119">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="5dde0-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="5dde0-120">Header</span><span class="sxs-lookup"><span data-stu-id="5dde0-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="5dde0-121"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="5dde0-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="5dde0-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5dde0-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="5dde0-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5dde0-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="5dde0-124">См. также</span><span class="sxs-lookup"><span data-stu-id="5dde0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5dde0-125">**Класс InkCollector**</span><span class="sxs-lookup"><span data-stu-id="5dde0-125">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="5dde0-126">**Интерфейс Иинктаблет**</span><span class="sxs-lookup"><span data-stu-id="5dde0-126">**IInkTablet Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

 




