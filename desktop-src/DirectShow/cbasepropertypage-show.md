---
description: 'Метод «Показать» показывает или скрывает диалоговое окно. Этот метод реализует метод Ипропертипаже:: демонстрации.'
ms.assetid: 03796779-ed41-4b68-852d-6b1849a9dc10
title: Метод Кбасепропертипаже. показывать (Кпроп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Show
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1dadd1c187773df3ca41ac0e1e4daf06fb54761b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668937"
---
# <a name="cbasepropertypageshow-method"></a><span data-ttu-id="5f397-104">Кбасепропертипаже. отобразить метод</span><span class="sxs-lookup"><span data-stu-id="5f397-104">CBasePropertyPage.Show method</span></span>

<span data-ttu-id="5f397-105">`Show`Метод показывает или скрывает диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="5f397-105">The `Show` method shows or hides the dialog box.</span></span> <span data-ttu-id="5f397-106">Этот метод реализует метод [ипропертипаже:: демонстрации](/windows/win32/api/ocidl/nf-ocidl-ipropertypage-show) .</span><span class="sxs-lookup"><span data-stu-id="5f397-106">This method implements the [IPropertyPage::Show](/windows/win32/api/ocidl/nf-ocidl-ipropertypage-show) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f397-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5f397-107">Syntax</span></span>

```C++
HRESULT Show(
   UINT nCmdShow
);
```
## <a name="parameters"></a><span data-ttu-id="5f397-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="5f397-108">Parameters</span></span>

<span data-ttu-id="5f397-109">*нкмдшов*</span><span class="sxs-lookup"><span data-stu-id="5f397-109">*nCmdShow*</span></span>

<span data-ttu-id="5f397-110">Тип: **[uint](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5f397-110">Type: **[UINT](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5f397-111">Значение, указывающее, следует ли отображать или скрывать окно.</span><span class="sxs-lookup"><span data-stu-id="5f397-111">Value that specifies whether to show or hide the window.</span></span> <span data-ttu-id="5f397-112">Дополнительные сведения см. в описании метода [ипропертипаже:: Показать](/windows/win32/api/ocidl/nf-ocidl-ipropertypage-show) .</span><span class="sxs-lookup"><span data-stu-id="5f397-112">For more information, see the [IPropertyPage::Show](/windows/win32/api/ocidl/nf-ocidl-ipropertypage-show) method.</span></span>

## <a name="return-value"></a><span data-ttu-id="5f397-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5f397-113">Return value</span></span>

<span data-ttu-id="5f397-114">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5f397-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="5f397-115">Ниже приведены возможные значения.</span><span class="sxs-lookup"><span data-stu-id="5f397-115">Possible values include the following.</span></span>

| <span data-ttu-id="5f397-116">Код возврата</span><span class="sxs-lookup"><span data-stu-id="5f397-116">Return code</span></span>                                                                                  | <span data-ttu-id="5f397-117">Описание</span><span class="sxs-lookup"><span data-stu-id="5f397-117">Description</span></span>                    |
|----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <span data-ttu-id="5f397-118"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="5f397-118"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="5f397-119">Успешно.</span><span class="sxs-lookup"><span data-stu-id="5f397-119">Success.</span></span><br/>            |
| <dl> <span data-ttu-id="5f397-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="5f397-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="5f397-121">Недопустимый аргумент.</span><span class="sxs-lookup"><span data-stu-id="5f397-121">Invalid argument.</span></span><br/>   |
| <dl> <span data-ttu-id="5f397-122"><dt>**\_непредвиденная E**</dt></span><span class="sxs-lookup"><span data-stu-id="5f397-122"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="5f397-123">Непредвиденный сбой.</span><span class="sxs-lookup"><span data-stu-id="5f397-123">Unexpected failure.</span></span><br/> |

## <a name="requirements"></a><span data-ttu-id="5f397-124">Требования</span><span class="sxs-lookup"><span data-stu-id="5f397-124">Requirements</span></span>

| <span data-ttu-id="5f397-125">Требование</span><span class="sxs-lookup"><span data-stu-id="5f397-125">Requirement</span></span> | <span data-ttu-id="5f397-126">Значение</span><span class="sxs-lookup"><span data-stu-id="5f397-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f397-127">Header</span><span class="sxs-lookup"><span data-stu-id="5f397-127">Header</span></span>  | <dl> <span data-ttu-id="5f397-128"><dt>Кпроп. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5f397-128"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="5f397-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5f397-129">Library</span></span> | <dl> <span data-ttu-id="5f397-130"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="5f397-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="5f397-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5f397-131">See also</span></span>

[<span data-ttu-id="5f397-132">Класс Кбасепропертипаже</span><span class="sxs-lookup"><span data-stu-id="5f397-132">CBasePropertyPage Class</span></span>](cbasepropertypage.md)
