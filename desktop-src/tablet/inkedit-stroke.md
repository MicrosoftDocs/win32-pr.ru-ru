---
description: Происходит, когда пользователь рисует новый объект Иинкстрокедисп для любого объекта Иинктаблет.
ms.assetid: fac5104d-d0da-40b1-a4a6-00a34718d09f
title: Событие InkEdit. Stroke (рисование. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d21abde9deb565f207a44ddd44b51681f1bfa6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103817744"
---
# <a name="inkeditstroke-event"></a><span data-ttu-id="cc1f2-103">Событие InkEdit. Stroke</span><span class="sxs-lookup"><span data-stu-id="cc1f2-103">InkEdit.Stroke event</span></span>

<span data-ttu-id="cc1f2-104">Происходит, когда пользователь рисует новый объект [**иинкстрокедисп**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) для любого объекта [**иинктаблет**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) .</span><span class="sxs-lookup"><span data-stu-id="cc1f2-104">Occurs when the user draws a new [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object on any [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc1f2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cc1f2-105">Syntax</span></span>


```C++
HRESULT Stroke(
  [in]      IInkCursor     *Cursor,
  [in]      IInkStrokeDisp *Stroke,
  [in, out] VARIANT_BOOL   *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="cc1f2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cc1f2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc1f2-107">*Курсор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cc1f2-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc1f2-108">Объект [**иинккурсор**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) .</span><span class="sxs-lookup"><span data-stu-id="cc1f2-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object.</span></span>

</dd> <dt>

<span data-ttu-id="cc1f2-109">*Штриховая линия* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cc1f2-109">*Stroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc1f2-110">Собранный объект [**иинкстрокедисп**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) .</span><span class="sxs-lookup"><span data-stu-id="cc1f2-110">The collected [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object.</span></span>

</dd> <dt>

<span data-ttu-id="cc1f2-111">*Отмена* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="cc1f2-111">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="cc1f2-112">**Вариант \_ Значение TRUE** , чтобы отменить коллекцию объекта [**иинкстрокедисп**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) ; **Вариант \_ Значение FALSE** , чтобы получить объект **иинкстрокедисп** и продолжить **штрих** .</span><span class="sxs-lookup"><span data-stu-id="cc1f2-112">**VARIANT\_TRUE** to cancel the collection of the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object; **VARIANT\_FALSE** to collect the **IInkStrokeDisp** object and continue with the **Stroke** even.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc1f2-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cc1f2-113">Return value</span></span>

<span data-ttu-id="cc1f2-114">Если это событие завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="cc1f2-114">If this event succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="cc1f2-115">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cc1f2-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc1f2-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cc1f2-116">Remarks</span></span>

<span data-ttu-id="cc1f2-117">Этот метод события определен в интерфейсе **\_ иинкедитевентс** .</span><span class="sxs-lookup"><span data-stu-id="cc1f2-117">This event method is defined in the **\_IInkEditEvents** interface.</span></span> <span data-ttu-id="cc1f2-118">Интерфейс **\_ иинкедитевентс** реализует интерфейс [**IDISPATCH**](/windows/win32/api/oaidl/nn-oaidl-idispatch) с идентификатором DISPID \_ иистроке.</span><span class="sxs-lookup"><span data-stu-id="cc1f2-118">The **\_IInkEditEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IeeStroke.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc1f2-119">Требования</span><span class="sxs-lookup"><span data-stu-id="cc1f2-119">Requirements</span></span>



| <span data-ttu-id="cc1f2-120">Требование</span><span class="sxs-lookup"><span data-stu-id="cc1f2-120">Requirement</span></span> | <span data-ttu-id="cc1f2-121">Значение</span><span class="sxs-lookup"><span data-stu-id="cc1f2-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc1f2-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cc1f2-122">Minimum supported client</span></span><br/> | <span data-ttu-id="cc1f2-123">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="cc1f2-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="cc1f2-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cc1f2-124">Minimum supported server</span></span><br/> | <span data-ttu-id="cc1f2-125">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="cc1f2-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="cc1f2-126">Header</span><span class="sxs-lookup"><span data-stu-id="cc1f2-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc1f2-127"><dt>«С». h (также требует \_ ввода i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="cc1f2-127"><dt>Inked.h (also requires inked\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="cc1f2-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="cc1f2-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="cc1f2-129"><dt>InkEd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cc1f2-129"><dt>InkEd.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="cc1f2-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cc1f2-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc1f2-131">InkEdit</span><span class="sxs-lookup"><span data-stu-id="cc1f2-131">InkEdit</span></span>](inkedit-control-reference.md)
</dt> <dt>

[<span data-ttu-id="cc1f2-132">**Интерфейс Иинккурсор**</span><span class="sxs-lookup"><span data-stu-id="cc1f2-132">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="cc1f2-133">**Интерфейс Иинкстрокедисп**</span><span class="sxs-lookup"><span data-stu-id="cc1f2-133">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

