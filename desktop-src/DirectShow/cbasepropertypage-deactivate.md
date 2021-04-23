---
description: Метод Deactivate уничтожает диалоговое окно. Этот метод реализует метод Ипропертипаже::D еактивате.
ms.assetid: f2d2f15f-15f6-4902-bafc-f58a684ff193
title: Метод Кбасепропертипаже. Deactivate (Кпроп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Deactivate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 63a843502fc735cc41ff3656e83ef3d6cb839a19
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657489"
---
# <a name="cbasepropertypagedeactivate-method"></a><span data-ttu-id="6d626-104">Кбасепропертипаже. Deactivate, метод</span><span class="sxs-lookup"><span data-stu-id="6d626-104">CBasePropertyPage.Deactivate method</span></span>

<span data-ttu-id="6d626-105">`Deactivate`Метод уничтожает диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="6d626-105">The `Deactivate` method destroys the dialog window.</span></span> <span data-ttu-id="6d626-106">Этот метод реализует метод **ипропертипаже::D еактивате** .</span><span class="sxs-lookup"><span data-stu-id="6d626-106">This method implements the **IPropertyPage::Deactivate** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d626-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6d626-107">Syntax</span></span>


```C++
HRESULT Deactivate();
```



## <a name="parameters"></a><span data-ttu-id="6d626-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="6d626-108">Parameters</span></span>

<span data-ttu-id="6d626-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="6d626-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6d626-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6d626-110">Return value</span></span>

<span data-ttu-id="6d626-111">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6d626-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="6d626-112">Ниже приведены возможные значения.</span><span class="sxs-lookup"><span data-stu-id="6d626-112">Possible values include the following.</span></span>



| <span data-ttu-id="6d626-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="6d626-113">Return code</span></span>                                                                                  | <span data-ttu-id="6d626-114">Описание</span><span class="sxs-lookup"><span data-stu-id="6d626-114">Description</span></span>                    |
|----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <span data-ttu-id="6d626-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="6d626-115"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="6d626-116">Успешно.</span><span class="sxs-lookup"><span data-stu-id="6d626-116">Success.</span></span><br/>            |
| <dl> <span data-ttu-id="6d626-117"><dt>**\_непредвиденная E**</dt></span><span class="sxs-lookup"><span data-stu-id="6d626-117"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="6d626-118">Непредвиденный сбой.</span><span class="sxs-lookup"><span data-stu-id="6d626-118">Unexpected failure.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="6d626-119">Требования</span><span class="sxs-lookup"><span data-stu-id="6d626-119">Requirements</span></span>



| <span data-ttu-id="6d626-120">Требование</span><span class="sxs-lookup"><span data-stu-id="6d626-120">Requirement</span></span> | <span data-ttu-id="6d626-121">Значение</span><span class="sxs-lookup"><span data-stu-id="6d626-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d626-122">Header</span><span class="sxs-lookup"><span data-stu-id="6d626-122">Header</span></span><br/>  | <dl> <span data-ttu-id="6d626-123"><dt>Кпроп. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6d626-123"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="6d626-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6d626-124">Library</span></span><br/> | <dl> <span data-ttu-id="6d626-125"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="6d626-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d626-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6d626-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d626-127">**Класс Кбасепропертипаже**</span><span class="sxs-lookup"><span data-stu-id="6d626-127">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> <dt>

[<span data-ttu-id="6d626-128">**Кбасепропертипаже:: OnDeactivate**</span><span class="sxs-lookup"><span data-stu-id="6d626-128">**CBasePropertyPage::OnDeactivate**</span></span>](cbasepropertypage-ondeactivate.md)
</dt> </dl>

 

 




