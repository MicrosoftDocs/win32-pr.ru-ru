---
description: Метод Онрецеивемессаже вызывается, когда диалоговое окно получает сообщение.
ms.assetid: ea93500d-fd0f-4820-a54a-a186c40899ad
title: Кбасепропертипаже. Онрецеивемессаже, метод (Кпроп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.OnReceiveMessage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 69d9da708d45524d15f735273d47f242104ee22f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665249"
---
# <a name="cbasepropertypageonreceivemessage-method"></a><span data-ttu-id="f94c7-103">Кбасепропертипаже. Онрецеивемессаже, метод</span><span class="sxs-lookup"><span data-stu-id="f94c7-103">CBasePropertyPage.OnReceiveMessage method</span></span>

<span data-ttu-id="f94c7-104">`OnReceiveMessage`Метод вызывается, когда диалоговое окно получает сообщение.</span><span class="sxs-lookup"><span data-stu-id="f94c7-104">The `OnReceiveMessage` method is called when the dialog box receives a message.</span></span>

## <a name="syntax"></a><span data-ttu-id="f94c7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f94c7-105">Syntax</span></span>


```C++
virtual INT_PTR OnReceiveMessage(
   HWND   hwnd,
   UINT   uMsg,
   WPARAM wParam,
   LPARAM lParam
);
```



## <a name="parameters"></a><span data-ttu-id="f94c7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f94c7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f94c7-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="f94c7-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="f94c7-108">Обработчик для окна.</span><span class="sxs-lookup"><span data-stu-id="f94c7-108">Handle to the window.</span></span>

</dd> <dt>

<span data-ttu-id="f94c7-109">*Uiacp*</span><span class="sxs-lookup"><span data-stu-id="f94c7-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="f94c7-110">Message.</span><span class="sxs-lookup"><span data-stu-id="f94c7-110">Message.</span></span>

</dd> <dt>

<span data-ttu-id="f94c7-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f94c7-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f94c7-112">Первый параметр сообщения.</span><span class="sxs-lookup"><span data-stu-id="f94c7-112">First message parameter.</span></span>

</dd> <dt>

<span data-ttu-id="f94c7-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f94c7-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f94c7-114">Второй параметр сообщения.</span><span class="sxs-lookup"><span data-stu-id="f94c7-114">Second message parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f94c7-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f94c7-115">Return value</span></span>

<span data-ttu-id="f94c7-116">Возвращает логическое значение.</span><span class="sxs-lookup"><span data-stu-id="f94c7-116">Returns a Boolean value.</span></span> <span data-ttu-id="f94c7-117">Процедура диалогового окна возвращает это значение. Дополнительные сведения см. в документации по пакету Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="f94c7-117">The dialog procedure returns this value; for more information, see the Platform SDK documentation.</span></span>

## <a name="remarks"></a><span data-ttu-id="f94c7-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f94c7-118">Remarks</span></span>

<span data-ttu-id="f94c7-119">Реализация базового класса вызывает **дефвиндовпрок**.</span><span class="sxs-lookup"><span data-stu-id="f94c7-119">The base-class implementation calls **DefWindowProc**.</span></span> <span data-ttu-id="f94c7-120">Переопределите этот метод, чтобы он обрабатывал сообщения, связанные с элементами управления диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="f94c7-120">Override this method to handle messages that relate to the dialog controls.</span></span> <span data-ttu-id="f94c7-121">Если переопределяющий метод не обрабатывает конкретное сообщение, он должен вызвать метод базового класса.</span><span class="sxs-lookup"><span data-stu-id="f94c7-121">If the overriding method does not handle a particular message, it should call the base-class method.</span></span>

<span data-ttu-id="f94c7-122">Если пользователь изменяет свойства через диалоговые элементы управления, установите для флага [**кбасепропертипаже:: m \_ Бдирти**](cbasepropertypage-m-bdirty.md) **значение true**.</span><span class="sxs-lookup"><span data-stu-id="f94c7-122">If the user changes any properties via the dialog controls, set the [**CBasePropertyPage::m\_bDirty**](cbasepropertypage-m-bdirty.md) flag to **TRUE**.</span></span> <span data-ttu-id="f94c7-123">Затем вызовите метод **ипропертипажесите:: онстатусчанже** в указателе [**кбасепропертипаже:: m \_ ппажесите**](cbasepropertypage-m-ppagesite.md) , чтобы проинформировать кадр.</span><span class="sxs-lookup"><span data-stu-id="f94c7-123">Then call the **IPropertyPageSite::OnStatusChange** method on the [**CBasePropertyPage::m\_pPageSite**](cbasepropertypage-m-ppagesite.md) pointer to inform the frame.</span></span>

## <a name="examples"></a><span data-ttu-id="f94c7-124">Примеры</span><span class="sxs-lookup"><span data-stu-id="f94c7-124">Examples</span></span>

<span data-ttu-id="f94c7-125">Следующий пример реагирует на нажатие кнопки, обновляя переменную-член, которая предполагается определить в производном классе.</span><span class="sxs-lookup"><span data-stu-id="f94c7-125">The following example responds to a button click by updating a member variable, which is assumed to be defined in the derived class.</span></span> <span data-ttu-id="f94c7-126">В этом примере также показана вспомогательная функция для задания состояния "грязной" страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="f94c7-126">This example also shows a helper function for setting the property page's dirty status.</span></span>


```C++
INT_PTR CMyProp::OnReceiveMessage(HWND hwnd,
  UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
    case WM_COMMAND:
        if (LOWORD(wParam) == IDC_BUTTON1)
        {
            m_lNewVal = GetDlgItemInt(m_Dlg, IDC_EDIT1, 0, TRUE);
            SetDirty();
            return (INT_PTR)TRUE;
        }
        break;
    } // switch

    // Did not handle the message.
    return CBasePropertyPage::OnReceiveMessage(hwnd, uMsg, wParam, lParam);
}

// Helper function to update the dirty status.
void CMyProp::SetDirty()
{
    m_bDirty = TRUE;
    if (m_pPageSite)
    {
        m_pPageSite->OnStatusChange(PROPPAGESTATUS_DIRTY);
    }
}
```



## <a name="requirements"></a><span data-ttu-id="f94c7-127">Требования</span><span class="sxs-lookup"><span data-stu-id="f94c7-127">Requirements</span></span>



| <span data-ttu-id="f94c7-128">Требование</span><span class="sxs-lookup"><span data-stu-id="f94c7-128">Requirement</span></span> | <span data-ttu-id="f94c7-129">Значение</span><span class="sxs-lookup"><span data-stu-id="f94c7-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f94c7-130">Header</span><span class="sxs-lookup"><span data-stu-id="f94c7-130">Header</span></span><br/>  | <dl> <span data-ttu-id="f94c7-131"><dt>Кпроп. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f94c7-131"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="f94c7-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f94c7-132">Library</span></span><br/> | <dl> <span data-ttu-id="f94c7-133"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="f94c7-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f94c7-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f94c7-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f94c7-135">**Класс Кбасепропертипаже**</span><span class="sxs-lookup"><span data-stu-id="f94c7-135">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




