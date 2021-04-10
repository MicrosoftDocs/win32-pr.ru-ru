---
description: Происходит при двойном щелчке объекта InkCollector или InkOverlay.
ms.assetid: 76ea40d4-82cf-420a-a9eb-66cb0492b43b
title: Событие InkOverlay. DoubleClick (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4baddc89e309b7d64ba2294827b58956b3e6c47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104266159"
---
# <a name="inkoverlaydoubleclick-event"></a><span data-ttu-id="012a9-103">Событие InkOverlay. DoubleClick</span><span class="sxs-lookup"><span data-stu-id="012a9-103">InkOverlay.DoubleClick event</span></span>

<span data-ttu-id="012a9-104">Происходит при двойном щелчке объекта [**InkCollector**](inkcollector-class.md) или [**InkOverlay**](inkoverlay-class.md) .</span><span class="sxs-lookup"><span data-stu-id="012a9-104">Occurs when the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object is double-clicked.</span></span>

## <a name="syntax"></a><span data-ttu-id="012a9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="012a9-105">Syntax</span></span>


```C++
void DoubleClick(
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="012a9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="012a9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="012a9-107">*Отмена* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="012a9-107">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="012a9-108">Следует ли отменять событие для родительского элемента управления.</span><span class="sxs-lookup"><span data-stu-id="012a9-108">Whether the event should be canceled for the parent control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="012a9-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="012a9-109">Return value</span></span>

<span data-ttu-id="012a9-110">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="012a9-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="012a9-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="012a9-111">Remarks</span></span>

<span data-ttu-id="012a9-112">Этот метод события определен в \_ \_ \_ интерфейсах диспетчеризации (DISP) иинкколлекторевентс, иинковерлайевентс и иинкпиктуривентс с идентификатором DISPID \_ ипедблкликк.</span><span class="sxs-lookup"><span data-stu-id="012a9-112">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEDblClick.</span></span>

## <a name="requirements"></a><span data-ttu-id="012a9-113">Требования</span><span class="sxs-lookup"><span data-stu-id="012a9-113">Requirements</span></span>



| <span data-ttu-id="012a9-114">Требование</span><span class="sxs-lookup"><span data-stu-id="012a9-114">Requirement</span></span> | <span data-ttu-id="012a9-115">Значение</span><span class="sxs-lookup"><span data-stu-id="012a9-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="012a9-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="012a9-116">Minimum supported client</span></span><br/> | <span data-ttu-id="012a9-117">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="012a9-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="012a9-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="012a9-118">Minimum supported server</span></span><br/> | <span data-ttu-id="012a9-119">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="012a9-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="012a9-120">Header</span><span class="sxs-lookup"><span data-stu-id="012a9-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="012a9-121"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="012a9-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="012a9-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="012a9-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="012a9-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="012a9-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="012a9-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="012a9-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="012a9-125">**Класс InkOverlay**</span><span class="sxs-lookup"><span data-stu-id="012a9-125">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> </dl>

 

 




