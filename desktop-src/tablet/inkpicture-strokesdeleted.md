---
description: Происходит после удаления объектов Иинкстрокедисп из свойства Ink.
ms.assetid: 395544e1-dc93-45d3-ac7a-d54712f3c027
title: Событие InkPicture. Строкесделетед (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf98e51196d760f467d507c133429201883b340e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712817"
---
# <a name="inkpicturestrokesdeleted-event"></a><span data-ttu-id="5cf2b-103">Событие InkPicture. Строкесделетед</span><span class="sxs-lookup"><span data-stu-id="5cf2b-103">InkPicture.StrokesDeleted event</span></span>

<span data-ttu-id="5cf2b-104">Происходит после удаления объектов [**иинкстрокедисп**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) из свойства [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink) .</span><span class="sxs-lookup"><span data-stu-id="5cf2b-104">Occurs after [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) objects have been deleted from the [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="5cf2b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5cf2b-105">Syntax</span></span>


```C++
void StrokesDeleted();
```



## <a name="parameters"></a><span data-ttu-id="5cf2b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5cf2b-106">Parameters</span></span>

<span data-ttu-id="5cf2b-107">У этого события нет параметров.</span><span class="sxs-lookup"><span data-stu-id="5cf2b-107">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5cf2b-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5cf2b-108">Return value</span></span>

<span data-ttu-id="5cf2b-109">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="5cf2b-109">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5cf2b-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5cf2b-110">Remarks</span></span>

<span data-ttu-id="5cf2b-111">Данные событий отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="5cf2b-111">There is no event data.</span></span>

<span data-ttu-id="5cf2b-112">Этот метод события определен в интерфейсах диспетчеризации **\_ иинковерлайевентс** и **\_ ИИНКПИКТУРИВЕНТС** (DISP) с идентификатором DISPID \_ иоестрокесделетед.</span><span class="sxs-lookup"><span data-stu-id="5cf2b-112">This event method is defined in the **\_IInkOverlayEvents** and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOEStrokesDeleted.</span></span>

## <a name="requirements"></a><span data-ttu-id="5cf2b-113">Требования</span><span class="sxs-lookup"><span data-stu-id="5cf2b-113">Requirements</span></span>



| <span data-ttu-id="5cf2b-114">Требование</span><span class="sxs-lookup"><span data-stu-id="5cf2b-114">Requirement</span></span> | <span data-ttu-id="5cf2b-115">Значение</span><span class="sxs-lookup"><span data-stu-id="5cf2b-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5cf2b-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5cf2b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5cf2b-117">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="5cf2b-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="5cf2b-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5cf2b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5cf2b-119">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="5cf2b-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="5cf2b-120">Header</span><span class="sxs-lookup"><span data-stu-id="5cf2b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="5cf2b-121"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="5cf2b-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="5cf2b-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5cf2b-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="5cf2b-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5cf2b-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="5cf2b-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5cf2b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5cf2b-125">InkPicture</span><span class="sxs-lookup"><span data-stu-id="5cf2b-125">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

 




