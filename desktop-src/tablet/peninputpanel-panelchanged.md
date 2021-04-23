---
description: Не рекомендуется. Пенинпутпанел был заменен панелью ввода текста (TIP). Происходит при изменении объекта Пенинпутпанел между макетами.
ms.assetid: 21d38406-7ed9-4741-a092-ed3a369dc0dc
title: Событие Пенинпутпанел. Панелчанжед (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d6ff0f415e12131221a8dad1c0775a347ef96cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347872"
---
# <a name="peninputpanelpanelchanged-event"></a><span data-ttu-id="d5592-104">Пенинпутпанел. Панелчанжед, событие</span><span class="sxs-lookup"><span data-stu-id="d5592-104">PenInputPanel.PanelChanged event</span></span>

<span data-ttu-id="d5592-105">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="d5592-105">Deprecated.</span></span> <span data-ttu-id="d5592-106">[**Пенинпутпанел**](peninputpanel-class.md) был заменен [панелью ввода текста (TIP)](text-input-panel-reference.md).</span><span class="sxs-lookup"><span data-stu-id="d5592-106">The [**PenInputPanel**](peninputpanel-class.md) has been replaced by the [Text Input Panel (TIP)](text-input-panel-reference.md).</span></span>

<span data-ttu-id="d5592-107">Происходит при изменении объекта [**пенинпутпанел**](peninputpanel-class.md) между макетами.</span><span class="sxs-lookup"><span data-stu-id="d5592-107">Occurs when the [**PenInputPanel**](peninputpanel-class.md) object changes between layouts.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5592-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d5592-108">Syntax</span></span>


```C++
HRESULT PanelChanged(
  [in] PanelType NewPanelType
);
```



## <a name="parameters"></a><span data-ttu-id="d5592-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="d5592-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5592-110">*Невпанелтипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d5592-110">*NewPanelType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5592-111">Новый тип панели, используемый для входных данных в объекте [**пенинпутпанел**](peninputpanel-class.md) после срабатывания события **панелчанжед** .</span><span class="sxs-lookup"><span data-stu-id="d5592-111">The new panel type used for input within the [**PenInputPanel**](peninputpanel-class.md) object, after the **PanelChanged** event fires.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5592-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d5592-112">Return value</span></span>

<span data-ttu-id="d5592-113">Если это событие завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="d5592-113">If this event succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d5592-114">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d5592-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5592-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d5592-115">Remarks</span></span>

<span data-ttu-id="d5592-116">При создании объекта [**пенинпутпанел**](peninputpanel-class.md) используется [**Рукописный ввод**](/windows/win32/api/peninputpanel/ne-peninputpanel-paneltype) по умолчанию **панелтипе**.</span><span class="sxs-lookup"><span data-stu-id="d5592-116">When creating a [**PenInputPanel**](peninputpanel-class.md) object, [**Handwriting**](/windows/win32/api/peninputpanel/ne-peninputpanel-paneltype) is the default **PanelType**.</span></span> <span data-ttu-id="d5592-117">Если изменить панель, установив свойство [**куррентпанел**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_currentpanel) до того, как панель ввода пера станет активной в первый раз, происходит событие **панелчанжед** .</span><span class="sxs-lookup"><span data-stu-id="d5592-117">If you change the panel by setting the [**CurrentPanel**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_currentpanel) property before the pen input panel becomes active for the first time, a **PanelChanged** event occurs.</span></span>

<span data-ttu-id="d5592-118">Событие **панелчанжед** не возникает, когда пользователь изменяет между линией с текстом и упакованным Pad.</span><span class="sxs-lookup"><span data-stu-id="d5592-118">The **PanelChanged** event is not raised when the user changes between Lined and Boxed writing pads.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5592-119">Требования</span><span class="sxs-lookup"><span data-stu-id="d5592-119">Requirements</span></span>



| <span data-ttu-id="d5592-120">Требование</span><span class="sxs-lookup"><span data-stu-id="d5592-120">Requirement</span></span> | <span data-ttu-id="d5592-121">Значение</span><span class="sxs-lookup"><span data-stu-id="d5592-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5592-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d5592-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d5592-123">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="d5592-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="d5592-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d5592-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d5592-125">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="d5592-125">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="d5592-126">Header</span><span class="sxs-lookup"><span data-stu-id="d5592-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5592-127"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="d5592-127"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="d5592-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d5592-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="d5592-129"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d5592-129"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="d5592-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d5592-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5592-131">**пенинпутпанел**</span><span class="sxs-lookup"><span data-stu-id="d5592-131">**PenInputPanel**</span></span>](peninputpanel-class.md)
</dt> </dl>

 

 
