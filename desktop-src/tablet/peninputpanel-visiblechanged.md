---
description: Не рекомендуется. Пенинпутпанел был заменен панелью ввода текста (TIP). Происходит при отображении или скрытии объекта Пенинпутпанел.
ms.assetid: bf4651f4-2cf4-4952-a93e-3c6ba4846722
title: Событие Пенинпутпанел. Висиблечанжед (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c739f3517ad9739f1d1ba95af9e5001dfbe659a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693722"
---
# <a name="peninputpanelvisiblechanged-event"></a><span data-ttu-id="01841-104">Пенинпутпанел. Висиблечанжед, событие</span><span class="sxs-lookup"><span data-stu-id="01841-104">PenInputPanel.VisibleChanged event</span></span>

<span data-ttu-id="01841-105">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="01841-105">Deprecated.</span></span> <span data-ttu-id="01841-106">[**Пенинпутпанел**](peninputpanel-class.md) был заменен [панелью ввода текста (TIP)](text-input-panel-reference.md).</span><span class="sxs-lookup"><span data-stu-id="01841-106">The [**PenInputPanel**](peninputpanel-class.md) has been replaced by the [Text Input Panel (TIP)](text-input-panel-reference.md).</span></span>

<span data-ttu-id="01841-107">Происходит при отображении или скрытии объекта [**пенинпутпанел**](peninputpanel-class.md) .</span><span class="sxs-lookup"><span data-stu-id="01841-107">Occurs when the [**PenInputPanel**](peninputpanel-class.md) object has shown or hidden itself.</span></span>

## <a name="syntax"></a><span data-ttu-id="01841-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="01841-108">Syntax</span></span>


```C++
HRESULT VisibleChanged(
  [in] VARIANT_BOOL NewVisibility
);
```



## <a name="parameters"></a><span data-ttu-id="01841-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="01841-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01841-110">*Неввисибилити* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="01841-110">*NewVisibility* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01841-111">**Вариант \_ Значение TRUE** , чтобы объект [**пенинпутпанел**](peninputpanel-class.md) стал видимым; в противном случае — **\_ значение false**.</span><span class="sxs-lookup"><span data-stu-id="01841-111">**VARIANT\_TRUE** to cause the [**PenInputPanel**](peninputpanel-class.md) object to become visible; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01841-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="01841-112">Return value</span></span>

<span data-ttu-id="01841-113">Если это событие завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="01841-113">If this event succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="01841-114">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="01841-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="01841-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="01841-115">Remarks</span></span>

<span data-ttu-id="01841-116">Событие **висиблечанжед** применяется к нацеливанию на панель ввода Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="01841-116">The **VisibleChanged** event applies to the Tablet PC Input Panel hover target.</span></span> <span data-ttu-id="01841-117">Однако он не вызывается, когда нацеливание наводится на панель ввода для отображения всей панели вводов Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="01841-117">However, it is not raised when the hover target expands to show the full Tablet PC Input Panel.</span></span>

## <a name="requirements"></a><span data-ttu-id="01841-118">Требования</span><span class="sxs-lookup"><span data-stu-id="01841-118">Requirements</span></span>



| <span data-ttu-id="01841-119">Требование</span><span class="sxs-lookup"><span data-stu-id="01841-119">Requirement</span></span> | <span data-ttu-id="01841-120">Значение</span><span class="sxs-lookup"><span data-stu-id="01841-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01841-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="01841-121">Minimum supported client</span></span><br/> | <span data-ttu-id="01841-122">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="01841-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="01841-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="01841-123">Minimum supported server</span></span><br/> | <span data-ttu-id="01841-124">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="01841-124">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="01841-125">Header</span><span class="sxs-lookup"><span data-stu-id="01841-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="01841-126"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="01841-126"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="01841-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="01841-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="01841-128"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01841-128"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="01841-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="01841-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01841-130">**пенинпутпанел**</span><span class="sxs-lookup"><span data-stu-id="01841-130">**PenInputPanel**</span></span>](peninputpanel-class.md)
</dt> </dl>

 

 




