---
description: Происходит при добавлении Иинктаблет в систему.
ms.assetid: 5df10efd-7055-43fa-881f-67eb5fd6adcf
title: Событие InkPicture. Таблетаддед (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d75cb3a67b00c5a26c0c3494fc752595954a23da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272640"
---
# <a name="inkpicturetabletadded-event"></a><span data-ttu-id="1ebc6-103">Событие InkPicture. Таблетаддед</span><span class="sxs-lookup"><span data-stu-id="1ebc6-103">InkPicture.TabletAdded event</span></span>

<span data-ttu-id="1ebc6-104">Происходит при добавлении [**иинктаблет**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) в систему.</span><span class="sxs-lookup"><span data-stu-id="1ebc6-104">Occurs when a [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) is added to the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ebc6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1ebc6-105">Syntax</span></span>


```C++
void TabletAdded(
  [in] IInkTablet *Tablet
);
```



## <a name="parameters"></a><span data-ttu-id="1ebc6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1ebc6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ebc6-107">*Планшетный ПК* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1ebc6-107">*Tablet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ebc6-108">Объект [**иинктаблет**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) , который был добавлен в систему.</span><span class="sxs-lookup"><span data-stu-id="1ebc6-108">The [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) object that has been added to the system.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ebc6-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1ebc6-109">Return value</span></span>

<span data-ttu-id="1ebc6-110">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="1ebc6-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ebc6-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1ebc6-111">Remarks</span></span>

<span data-ttu-id="1ebc6-112">Этот метод события определен в интерфейсах диспетчеризации (DISP) **\_ иинкколлекторевентс**, **\_ иинковерлайевентс** и **\_ иинкпиктуривентс** с идентификатором DISPID \_ ицетаблетаддед.</span><span class="sxs-lookup"><span data-stu-id="1ebc6-112">This event method is defined in the **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICETabletAdded.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ebc6-113">Требования</span><span class="sxs-lookup"><span data-stu-id="1ebc6-113">Requirements</span></span>



| <span data-ttu-id="1ebc6-114">Требование</span><span class="sxs-lookup"><span data-stu-id="1ebc6-114">Requirement</span></span> | <span data-ttu-id="1ebc6-115">Значение</span><span class="sxs-lookup"><span data-stu-id="1ebc6-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ebc6-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1ebc6-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1ebc6-117">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="1ebc6-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="1ebc6-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1ebc6-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1ebc6-119">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="1ebc6-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="1ebc6-120">Header</span><span class="sxs-lookup"><span data-stu-id="1ebc6-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ebc6-121"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="1ebc6-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="1ebc6-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1ebc6-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="1ebc6-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1ebc6-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="1ebc6-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1ebc6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ebc6-125">InkPicture</span><span class="sxs-lookup"><span data-stu-id="1ebc6-125">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="1ebc6-126">**Интерфейс Иинктаблет**</span><span class="sxs-lookup"><span data-stu-id="1ebc6-126">**IInkTablet Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

 




