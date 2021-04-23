---
description: Происходит, когда пользователь нажимает и отпускает ключ, когда элемент управления InkEdit имеет фокус.
ms.assetid: 8284ab41-dfac-4da2-b101-6968a43b15d7
title: Событие InkEdit. KeyPress (с. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e49264f82b2cfe3c6998666339f08340a540791
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712219"
---
# <a name="inkeditkeypress-event"></a><span data-ttu-id="a3dcb-103">Событие InkEdit. KeyPress</span><span class="sxs-lookup"><span data-stu-id="a3dcb-103">InkEdit.KeyPress event</span></span>

<span data-ttu-id="a3dcb-104">Происходит, когда пользователь нажимает и отпускает ключ, когда элемент управления [InkEdit](inkedit-control-reference.md) имеет фокус.</span><span class="sxs-lookup"><span data-stu-id="a3dcb-104">Occurs when the user presses and releases a key while the [InkEdit](inkedit-control-reference.md) control has focus.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3dcb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a3dcb-105">Syntax</span></span>


```C++
HRESULT KeyPress(
   Long *Char
);
```



## <a name="parameters"></a><span data-ttu-id="a3dcb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a3dcb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3dcb-107">*Char*</span><span class="sxs-lookup"><span data-stu-id="a3dcb-107">*Char*</span></span> 
</dt> <dd>

<span data-ttu-id="a3dcb-108">Целое число, возвращающее стандартное числовое значение ANSI KeyCode.</span><span class="sxs-lookup"><span data-stu-id="a3dcb-108">An integer that returns a standard numeric ANSI keycode.</span></span> <span data-ttu-id="a3dcb-109">Параметр *char* передается по ссылке; При изменении он отправляет элементу управления другой символ.</span><span class="sxs-lookup"><span data-stu-id="a3dcb-109">The *Char* parameter is passed by reference; changing it sends a different character to the control.</span></span> <span data-ttu-id="a3dcb-110">Изменение параметра *char* на 0 отменяет событие.</span><span class="sxs-lookup"><span data-stu-id="a3dcb-110">Changing the *Char* parameter to 0 cancels the event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3dcb-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a3dcb-111">Return value</span></span>

<span data-ttu-id="a3dcb-112">Если это событие завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="a3dcb-112">If this event succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a3dcb-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a3dcb-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3dcb-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a3dcb-114">Remarks</span></span>

<span data-ttu-id="a3dcb-115">Этот метод события определен в интерфейсе **\_ иинкедитевентс** .</span><span class="sxs-lookup"><span data-stu-id="a3dcb-115">This event method is defined in the **\_IInkEditEvents** interface.</span></span> <span data-ttu-id="a3dcb-116">Интерфейс **\_ иинкедитевентс** реализует интерфейс [**IDISPATCH**](/windows/win32/api/oaidl/nn-oaidl-idispatch) с идентификатором DISPID \_ иикэйпресс.</span><span class="sxs-lookup"><span data-stu-id="a3dcb-116">The **\_IInkEditEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IeeKeyPress.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3dcb-117">Требования</span><span class="sxs-lookup"><span data-stu-id="a3dcb-117">Requirements</span></span>



| <span data-ttu-id="a3dcb-118">Требование</span><span class="sxs-lookup"><span data-stu-id="a3dcb-118">Requirement</span></span> | <span data-ttu-id="a3dcb-119">Значение</span><span class="sxs-lookup"><span data-stu-id="a3dcb-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3dcb-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a3dcb-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a3dcb-121">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="a3dcb-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a3dcb-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a3dcb-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a3dcb-123">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="a3dcb-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="a3dcb-124">Header</span><span class="sxs-lookup"><span data-stu-id="a3dcb-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3dcb-125"><dt>«С». h (также требует \_ ввода i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="a3dcb-125"><dt>Inked.h (also requires inked\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="a3dcb-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a3dcb-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="a3dcb-127"><dt>InkEd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a3dcb-127"><dt>InkEd.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="a3dcb-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a3dcb-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3dcb-129">InkEdit</span><span class="sxs-lookup"><span data-stu-id="a3dcb-129">InkEdit</span></span>](inkedit-control-reference.md)
</dt> <dt>

<span data-ttu-id="a3dcb-130">[**\[Элемент управления InkEdit события KeyDown\]**](inkedit-keydown.md)</span><span class="sxs-lookup"><span data-stu-id="a3dcb-130">[**KeyDown Event \[InkEdit Control\]**](inkedit-keydown.md)</span></span>
</dt> <dt>

<span data-ttu-id="a3dcb-131">[**\[Элемент управления InkEdit для события KeyUp\]**](inkedit-keyup.md)</span><span class="sxs-lookup"><span data-stu-id="a3dcb-131">[**KeyUp Event \[InkEdit Control\]**](inkedit-keyup.md)</span></span>
</dt> </dl>

 

