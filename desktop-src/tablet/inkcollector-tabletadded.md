---
description: Событие InkCollector. Таблетаддед — возникает при добавлении Иинктаблет в систему.
ms.assetid: c5f90fce-faf7-411b-a4d6-deb5d0f22f4a
title: Событие InkCollector. Таблетаддед (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad3088eff151d9857f8a1449d3c99805c949b790
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110012"
---
# <a name="inkcollectortabletadded-event"></a><span data-ttu-id="d97bc-103">Событие InkCollector. Таблетаддед</span><span class="sxs-lookup"><span data-stu-id="d97bc-103">InkCollector.TabletAdded event</span></span>

<span data-ttu-id="d97bc-104">Происходит при добавлении [**иинктаблет**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) в систему.</span><span class="sxs-lookup"><span data-stu-id="d97bc-104">Occurs when a [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) is added to the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="d97bc-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d97bc-105">Syntax</span></span>


```C++
void TabletAdded(
  [in] IInkTablet *Tablet
);
```



## <a name="parameters"></a><span data-ttu-id="d97bc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d97bc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d97bc-107">*Планшетный ПК* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d97bc-107">*Tablet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d97bc-108">Объект [**иинктаблет**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) , который был добавлен в систему.</span><span class="sxs-lookup"><span data-stu-id="d97bc-108">The [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) object that has been added to the system.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d97bc-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d97bc-109">Return value</span></span>

<span data-ttu-id="d97bc-110">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="d97bc-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d97bc-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="d97bc-111">Remarks</span></span>

<span data-ttu-id="d97bc-112">Этот метод события определен в \_ \_ \_ интерфейсах диспетчеризации (DISP) иинкколлекторевентс, иинковерлайевентс и иинкпиктуривентс с идентификатором DISPID \_ ицетаблетаддед.</span><span class="sxs-lookup"><span data-stu-id="d97bc-112">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICETabletAdded.</span></span>

## <a name="requirements"></a><span data-ttu-id="d97bc-113">Требования</span><span class="sxs-lookup"><span data-stu-id="d97bc-113">Requirements</span></span>



| <span data-ttu-id="d97bc-114">Требование</span><span class="sxs-lookup"><span data-stu-id="d97bc-114">Requirement</span></span> | <span data-ttu-id="d97bc-115">Значение</span><span class="sxs-lookup"><span data-stu-id="d97bc-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d97bc-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d97bc-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d97bc-117">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="d97bc-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="d97bc-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d97bc-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d97bc-119">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="d97bc-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="d97bc-120">Header</span><span class="sxs-lookup"><span data-stu-id="d97bc-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d97bc-121"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="d97bc-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="d97bc-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d97bc-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="d97bc-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d97bc-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="d97bc-124">См. также</span><span class="sxs-lookup"><span data-stu-id="d97bc-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d97bc-125">**Класс InkCollector**</span><span class="sxs-lookup"><span data-stu-id="d97bc-125">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="d97bc-126">**Интерфейс Иинктаблет**</span><span class="sxs-lookup"><span data-stu-id="d97bc-126">**IInkTablet Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

 




