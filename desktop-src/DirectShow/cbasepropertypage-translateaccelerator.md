---
description: 'Метод TranslateAccelerator указывает странице свойств обработать нажатие клавиши. Этот метод реализует метод Ипропертипаже:: TranslateAccelerator.'
ms.assetid: 2da214c9-35dc-470c-9b7f-2f4ef6bcd40a
title: Кбасепропертипаже. TranslateAccelerator, метод (Кпроп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.TranslateAccelerator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3116e85eec8fbf3a00bf434a1f88c8cac662ed0a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105656897"
---
# <a name="cbasepropertypagetranslateaccelerator-method"></a><span data-ttu-id="dde11-104">Кбасепропертипаже. TranslateAccelerator, метод</span><span class="sxs-lookup"><span data-stu-id="dde11-104">CBasePropertyPage.TranslateAccelerator method</span></span>

<span data-ttu-id="dde11-105">`TranslateAccelerator`Метод указывает странице свойств обработать нажатие клавиши.</span><span class="sxs-lookup"><span data-stu-id="dde11-105">The `TranslateAccelerator` method instructs the property page to process a keystroke.</span></span> <span data-ttu-id="dde11-106">Этот метод реализует метод **ипропертипаже:: TranslateAccelerator** .</span><span class="sxs-lookup"><span data-stu-id="dde11-106">This method implements the **IPropertyPage::TranslateAccelerator** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="dde11-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dde11-107">Syntax</span></span>


```C++
HRESULT TranslateAccelerator(
   LPMSG lpMsg
);
```



## <a name="parameters"></a><span data-ttu-id="dde11-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="dde11-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dde11-109">*лпмсг*</span><span class="sxs-lookup"><span data-stu-id="dde11-109">*lpMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="dde11-110">Указатель на структуру **MSG** , описывающую нажатие клавиши для обработки.</span><span class="sxs-lookup"><span data-stu-id="dde11-110">Pointer to a **MSG** structure describing the keystroke to process.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dde11-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dde11-111">Return value</span></span>

<span data-ttu-id="dde11-112">Возвращает E \_ нотимпл.</span><span class="sxs-lookup"><span data-stu-id="dde11-112">Returns E\_NOTIMPL.</span></span>

## <a name="remarks"></a><span data-ttu-id="dde11-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dde11-113">Remarks</span></span>

<span data-ttu-id="dde11-114">Переопределите этот метод, если требуется предоставить сочетания клавиш для страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="dde11-114">Override this method if you want to provide keyboard accelerators for the property page.</span></span>

## <a name="requirements"></a><span data-ttu-id="dde11-115">Требования</span><span class="sxs-lookup"><span data-stu-id="dde11-115">Requirements</span></span>



| <span data-ttu-id="dde11-116">Требование</span><span class="sxs-lookup"><span data-stu-id="dde11-116">Requirement</span></span> | <span data-ttu-id="dde11-117">Значение</span><span class="sxs-lookup"><span data-stu-id="dde11-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dde11-118">Header</span><span class="sxs-lookup"><span data-stu-id="dde11-118">Header</span></span><br/>  | <dl> <span data-ttu-id="dde11-119"><dt>Кпроп. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dde11-119"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="dde11-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="dde11-120">Library</span></span><br/> | <dl> <span data-ttu-id="dde11-121"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="dde11-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dde11-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dde11-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dde11-123">**Класс Кбасепропертипаже**</span><span class="sxs-lookup"><span data-stu-id="dde11-123">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




