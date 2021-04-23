---
description: 'Метод Activate создает окно диалогового окна. Этот метод реализует метод Ипропертипаже:: Activate.'
ms.assetid: 8f030dc5-1d14-46b5-9d40-7f07a1177dbe
title: Метод Кбасепропертипаже. Activate (Кпроп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Activate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4b851cfc4490d25e7e30dfd2cf0e7c33b0e76224
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668513"
---
# <a name="cbasepropertypageactivate-method"></a><span data-ttu-id="882f7-104">Кбасепропертипаже. Activate, метод</span><span class="sxs-lookup"><span data-stu-id="882f7-104">CBasePropertyPage.Activate method</span></span>

<span data-ttu-id="882f7-105">`Activate`Метод создает окно диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="882f7-105">The `Activate` method creates the dialog box window.</span></span> <span data-ttu-id="882f7-106">Этот метод реализует метод **ипропертипаже:: Activate** .</span><span class="sxs-lookup"><span data-stu-id="882f7-106">This method implements the **IPropertyPage::Activate** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="882f7-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="882f7-107">Syntax</span></span>


```C++
HRESULT Activate(
   HWND    hwndParent,
   LPCRECT prect,
   BOOL    fModal
);
```



## <a name="parameters"></a><span data-ttu-id="882f7-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="882f7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="882f7-109">*хвндпарент*</span><span class="sxs-lookup"><span data-stu-id="882f7-109">*hwndParent*</span></span> 
</dt> <dd>

<span data-ttu-id="882f7-110">Обработано с родительским окном диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="882f7-110">Handle to the parent window of the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="882f7-111">*прект*</span><span class="sxs-lookup"><span data-stu-id="882f7-111">*prect*</span></span> 
</dt> <dd>

<span data-ttu-id="882f7-112">Указатель на структуру **Rect** , которая содержит сведения о размещении для диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="882f7-112">Pointer to a **RECT** structure that contains positioning information for the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="882f7-113">*фмодал*</span><span class="sxs-lookup"><span data-stu-id="882f7-113">*fModal*</span></span> 
</dt> <dd>

<span data-ttu-id="882f7-114">Логическое значение, указывающее, является ли фрейм диалогового окна модальным (**true**) или немодальным (**false**).</span><span class="sxs-lookup"><span data-stu-id="882f7-114">Boolean value indicating whether the dialog box frame is modal (**TRUE**) or modeless (**FALSE**).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="882f7-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="882f7-115">Return value</span></span>

<span data-ttu-id="882f7-116">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="882f7-116">Returns an **HRESULT** value.</span></span> <span data-ttu-id="882f7-117">Ниже приведены возможные значения.</span><span class="sxs-lookup"><span data-stu-id="882f7-117">Possible values include the following.</span></span>



| <span data-ttu-id="882f7-118">Код возврата</span><span class="sxs-lookup"><span data-stu-id="882f7-118">Return code</span></span>                                                                                   | <span data-ttu-id="882f7-119">Описание</span><span class="sxs-lookup"><span data-stu-id="882f7-119">Description</span></span>                           |
|-----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="882f7-120"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="882f7-120"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="882f7-121">Успешно.</span><span class="sxs-lookup"><span data-stu-id="882f7-121">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="882f7-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="882f7-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="882f7-123">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="882f7-123">Insufficient memory.</span></span><br/>       |
| <dl> <span data-ttu-id="882f7-124"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="882f7-124"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="882f7-125">**Пустой** аргумент указателя.</span><span class="sxs-lookup"><span data-stu-id="882f7-125">**NULL** pointer argument.</span></span><br/> |
| <dl> <span data-ttu-id="882f7-126"><dt>**\_непредвиденная E**</dt></span><span class="sxs-lookup"><span data-stu-id="882f7-126"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>  | <span data-ttu-id="882f7-127">Непредвиденный сбой.</span><span class="sxs-lookup"><span data-stu-id="882f7-127">Unexpected failure.</span></span><br/>        |



 

## <a name="requirements"></a><span data-ttu-id="882f7-128">Требования</span><span class="sxs-lookup"><span data-stu-id="882f7-128">Requirements</span></span>



| <span data-ttu-id="882f7-129">Требование</span><span class="sxs-lookup"><span data-stu-id="882f7-129">Requirement</span></span> | <span data-ttu-id="882f7-130">Значение</span><span class="sxs-lookup"><span data-stu-id="882f7-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="882f7-131">Header</span><span class="sxs-lookup"><span data-stu-id="882f7-131">Header</span></span><br/>  | <dl> <span data-ttu-id="882f7-132"><dt>Кпроп. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="882f7-132"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="882f7-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="882f7-133">Library</span></span><br/> | <dl> <span data-ttu-id="882f7-134"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="882f7-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="882f7-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="882f7-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="882f7-136">**Класс Кбасепропертипаже**</span><span class="sxs-lookup"><span data-stu-id="882f7-136">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> <dt>

[<span data-ttu-id="882f7-137">**Кбасепропертипаже:: OnActivate**</span><span class="sxs-lookup"><span data-stu-id="882f7-137">**CBasePropertyPage::OnActivate**</span></span>](cbasepropertypage-onactivate.md)
</dt> </dl>

 

 




