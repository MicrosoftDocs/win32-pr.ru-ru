---
description: Событие InkPicture. Курсораутофранже — происходит, когда курсор покидает диапазон физического обнаружения (близость) контекста планшета.
ms.assetid: 0c71a4ad-3c09-4134-b0e7-82f29e8913ed
title: Событие InkPicture. Курсораутофранже (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d80584eafb7f1e5222316507f08bd73efb12fae
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086572"
---
# <a name="inkpicturecursoroutofrange-event"></a><span data-ttu-id="f2cc9-103">Событие InkPicture. Курсораутофранже</span><span class="sxs-lookup"><span data-stu-id="f2cc9-103">InkPicture.CursorOutOfRange event</span></span>

<span data-ttu-id="f2cc9-104">Происходит, когда курсор покидает диапазон физического обнаружения (близость) контекста планшета.</span><span class="sxs-lookup"><span data-stu-id="f2cc9-104">Occurs when the cursor leaves the physical detection range (proximity) of the tablet context.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2cc9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f2cc9-105">Syntax</span></span>


```C++
void CursorOutOfRange(
  [in] IInkCursor *Cursor
);
```



## <a name="parameters"></a><span data-ttu-id="f2cc9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f2cc9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2cc9-107">*Курсор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f2cc9-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2cc9-108">Объект [**интерфейса иинккурсор**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) , создавший событие **курсораутофранже** .</span><span class="sxs-lookup"><span data-stu-id="f2cc9-108">The [**IInkCursor Interface**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **CursorOutOfRange** event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2cc9-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f2cc9-109">Return value</span></span>

<span data-ttu-id="f2cc9-110">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="f2cc9-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2cc9-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="f2cc9-111">Remarks</span></span>

<span data-ttu-id="f2cc9-112">Этот метод события определен в интерфейсах диспетчеризации (DISP) **\_ иинкколлекторевентс**, **\_ иинковерлайевентс** и **\_ иинкпиктуривентс** с идентификатором DISPID \_ ицекурсораутофранже.</span><span class="sxs-lookup"><span data-stu-id="f2cc9-112">This event method is defined in the **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICECursorOutOfRange.</span></span>

<span data-ttu-id="f2cc9-113">Событие **курсораутофранже** срабатывает даже в режиме выбора или стирания, а не только в режиме рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="f2cc9-113">The **CursorOutOfRange** event is fired even when in select or erase mode, not just when in ink mode.</span></span> <span data-ttu-id="f2cc9-114">Для этого необходимо наблюдать за режимом редактирования (который вы несете за параметром) и учитывать режим, прежде чем интерпретировать событие.</span><span class="sxs-lookup"><span data-stu-id="f2cc9-114">This requires that you monitor the editing mode (which you are responsible for setting) and be aware of the mode before interpreting the event.</span></span> <span data-ttu-id="f2cc9-115">Преимуществом этого требования является большая свобода для внедрения инноваций на платформе за счет большей осведомленности о событиях платформы.</span><span class="sxs-lookup"><span data-stu-id="f2cc9-115">The advantage of this requirement is greater freedom to innovate on the platform through greater awareness of platform events.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2cc9-116">Требования</span><span class="sxs-lookup"><span data-stu-id="f2cc9-116">Requirements</span></span>



| <span data-ttu-id="f2cc9-117">Требование</span><span class="sxs-lookup"><span data-stu-id="f2cc9-117">Requirement</span></span> | <span data-ttu-id="f2cc9-118">Значение</span><span class="sxs-lookup"><span data-stu-id="f2cc9-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2cc9-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f2cc9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f2cc9-120">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="f2cc9-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="f2cc9-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f2cc9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f2cc9-122">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f2cc9-122">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="f2cc9-123">Header</span><span class="sxs-lookup"><span data-stu-id="f2cc9-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2cc9-124"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="f2cc9-124"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="f2cc9-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f2cc9-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="f2cc9-126"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2cc9-126"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="f2cc9-127">См. также</span><span class="sxs-lookup"><span data-stu-id="f2cc9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2cc9-128">InkPicture</span><span class="sxs-lookup"><span data-stu-id="f2cc9-128">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="f2cc9-129">**Событие Курсоринранже**</span><span class="sxs-lookup"><span data-stu-id="f2cc9-129">**CursorInRange Event**</span></span>](inkpicture-cursorinrange.md)
</dt> <dt>

[<span data-ttu-id="f2cc9-130">**Интерфейс Иинккурсор**</span><span class="sxs-lookup"><span data-stu-id="f2cc9-130">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 




