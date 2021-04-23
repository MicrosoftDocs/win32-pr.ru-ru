---
description: 'Метод Move размещает и изменяет размер диалогового окна. Этот метод реализует метод Ипропертипаже:: Move.'
ms.assetid: b6cabb5c-196d-489b-9dd4-194d26f4de83
title: Метод Кбасепропертипаже. Move (Кпроп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Move
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4d293f6ccb6a1bcd730ce997367c179f1747f66e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668760"
---
# <a name="cbasepropertypagemove-method"></a><span data-ttu-id="c9abf-104">Кбасепропертипаже. Move, метод</span><span class="sxs-lookup"><span data-stu-id="c9abf-104">CBasePropertyPage.Move method</span></span>

<span data-ttu-id="c9abf-105">`Move`Метод размещает и изменяет размер диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="c9abf-105">The `Move` method positions and resizes the dialog box.</span></span> <span data-ttu-id="c9abf-106">Этот метод реализует метод **ипропертипаже:: Move** .</span><span class="sxs-lookup"><span data-stu-id="c9abf-106">This method implements the **IPropertyPage::Move** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9abf-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c9abf-107">Syntax</span></span>


```C++
HRESULT Move(
   LPCRECT prect
);
```



## <a name="parameters"></a><span data-ttu-id="c9abf-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c9abf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9abf-109">*прект*</span><span class="sxs-lookup"><span data-stu-id="c9abf-109">*prect*</span></span> 
</dt> <dd>

<span data-ttu-id="c9abf-110">Указатель на структуру **Rect** , содержащую сведения о размещении.</span><span class="sxs-lookup"><span data-stu-id="c9abf-110">Pointer to a **RECT** structure containing the positioning information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9abf-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c9abf-111">Return value</span></span>

<span data-ttu-id="c9abf-112">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c9abf-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="c9abf-113">Ниже приведены возможные значения.</span><span class="sxs-lookup"><span data-stu-id="c9abf-113">Possible values include the following.</span></span>



| <span data-ttu-id="c9abf-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="c9abf-114">Return code</span></span>                                                                                  | <span data-ttu-id="c9abf-115">Описание</span><span class="sxs-lookup"><span data-stu-id="c9abf-115">Description</span></span>                           |
|----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="c9abf-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="c9abf-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="c9abf-117">Успешно.</span><span class="sxs-lookup"><span data-stu-id="c9abf-117">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="c9abf-118"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="c9abf-118"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="c9abf-119">**Пустой** аргумент указателя.</span><span class="sxs-lookup"><span data-stu-id="c9abf-119">**NULL** pointer argument.</span></span><br/> |
| <dl> <span data-ttu-id="c9abf-120"><dt>**\_непредвиденная E**</dt></span><span class="sxs-lookup"><span data-stu-id="c9abf-120"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="c9abf-121">Непредвиденный сбой.</span><span class="sxs-lookup"><span data-stu-id="c9abf-121">Unexpected failure.</span></span><br/>        |



 

## <a name="requirements"></a><span data-ttu-id="c9abf-122">Требования</span><span class="sxs-lookup"><span data-stu-id="c9abf-122">Requirements</span></span>



| <span data-ttu-id="c9abf-123">Требование</span><span class="sxs-lookup"><span data-stu-id="c9abf-123">Requirement</span></span> | <span data-ttu-id="c9abf-124">Значение</span><span class="sxs-lookup"><span data-stu-id="c9abf-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9abf-125">Header</span><span class="sxs-lookup"><span data-stu-id="c9abf-125">Header</span></span><br/>  | <dl> <span data-ttu-id="c9abf-126"><dt>Кпроп. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c9abf-126"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="c9abf-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c9abf-127">Library</span></span><br/> | <dl> <span data-ttu-id="c9abf-128"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="c9abf-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9abf-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c9abf-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9abf-130">**Класс Кбасепропертипаже**</span><span class="sxs-lookup"><span data-stu-id="c9abf-130">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




