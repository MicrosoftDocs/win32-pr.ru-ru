---
description: Происходит при удалении Иинктаблет из системы.
ms.assetid: 9a4640a7-cbd9-4304-88c6-86036423628d
title: Событие InkPicture. Таблетремовед (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e05b097b4dcf15c618e3316066be962b52803e27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272639"
---
# <a name="inkpicturetabletremoved-event"></a><span data-ttu-id="dd60b-103">Событие InkPicture. Таблетремовед</span><span class="sxs-lookup"><span data-stu-id="dd60b-103">InkPicture.TabletRemoved event</span></span>

<span data-ttu-id="dd60b-104">Происходит при удалении [**иинктаблет**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) из системы.</span><span class="sxs-lookup"><span data-stu-id="dd60b-104">Occurs when a [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) is removed from the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd60b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dd60b-105">Syntax</span></span>


```C++
void TabletRemoved(
  [in] long TabletId
);
```



## <a name="parameters"></a><span data-ttu-id="dd60b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="dd60b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd60b-107">*Таблетид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dd60b-107">*TabletId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd60b-108">Значение типа Long, которое было использовано в качестве идентификатора удаленного объекта [**иинктаблет**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) .</span><span class="sxs-lookup"><span data-stu-id="dd60b-108">The long value that was used as the ID for the [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) object that was removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd60b-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dd60b-109">Return value</span></span>

<span data-ttu-id="dd60b-110">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="dd60b-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="dd60b-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dd60b-111">Remarks</span></span>

<span data-ttu-id="dd60b-112">Этот метод события определен в интерфейсах диспетчеризации (DISP) **\_ иинкколлекторевентс**, **\_ иинковерлайевентс** и **\_ иинкпиктуривентс** с идентификатором DISPID \_ ицетаблетремовед.</span><span class="sxs-lookup"><span data-stu-id="dd60b-112">This event method is defined in the **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICETabletRemoved.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd60b-113">Требования</span><span class="sxs-lookup"><span data-stu-id="dd60b-113">Requirements</span></span>



| <span data-ttu-id="dd60b-114">Требование</span><span class="sxs-lookup"><span data-stu-id="dd60b-114">Requirement</span></span> | <span data-ttu-id="dd60b-115">Значение</span><span class="sxs-lookup"><span data-stu-id="dd60b-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd60b-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dd60b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="dd60b-117">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="dd60b-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="dd60b-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dd60b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="dd60b-119">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="dd60b-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="dd60b-120">Header</span><span class="sxs-lookup"><span data-stu-id="dd60b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd60b-121"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="dd60b-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="dd60b-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="dd60b-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="dd60b-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd60b-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="dd60b-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dd60b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd60b-125">InkPicture</span><span class="sxs-lookup"><span data-stu-id="dd60b-125">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="dd60b-126">**Интерфейс Иинктаблет**</span><span class="sxs-lookup"><span data-stu-id="dd60b-126">**IInkTablet Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

 




