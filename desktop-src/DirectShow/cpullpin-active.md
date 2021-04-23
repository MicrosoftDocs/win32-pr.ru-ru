---
description: Активный метод создает рабочий поток, который извлекает данные из выходного ПИН-кода. Этот метод также фиксирует распределитель.
ms.assetid: 9efa20f3-7909-4d87-bfa8-314d055b80f8
title: Метод Кпуллпин. Active (Пуллпин. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 461f6554f828dc096029ee1e7a1832e12a7c262a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669493"
---
# <a name="cpullpinactive-method"></a><span data-ttu-id="8334c-104">Кпуллпин. активный метод</span><span class="sxs-lookup"><span data-stu-id="8334c-104">CPullPin.Active method</span></span>

<span data-ttu-id="8334c-105">**Активный** метод создает рабочий поток, который извлекает данные из выходного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="8334c-105">The **Active** method creates a worker thread that pulls data from the output pin.</span></span> <span data-ttu-id="8334c-106">Этот метод также фиксирует распределитель.</span><span class="sxs-lookup"><span data-stu-id="8334c-106">This method also commits the allocator.</span></span>

## <a name="syntax"></a><span data-ttu-id="8334c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8334c-107">Syntax</span></span>


```C++
HRESULT Active();
```



## <a name="parameters"></a><span data-ttu-id="8334c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="8334c-108">Parameters</span></span>

<span data-ttu-id="8334c-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="8334c-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8334c-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8334c-110">Return value</span></span>

<span data-ttu-id="8334c-111">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8334c-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="8334c-112">Ниже приведены возможные значения.</span><span class="sxs-lookup"><span data-stu-id="8334c-112">Possible values include the following.</span></span>



| <span data-ttu-id="8334c-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="8334c-113">Return code</span></span>                                                                                  | <span data-ttu-id="8334c-114">Описание</span><span class="sxs-lookup"><span data-stu-id="8334c-114">Description</span></span>                                                           |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <span data-ttu-id="8334c-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="8334c-115"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="8334c-116">Успешно.</span><span class="sxs-lookup"><span data-stu-id="8334c-116">Success.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="8334c-117"><dt>**\_непредвиденная E**</dt></span><span class="sxs-lookup"><span data-stu-id="8334c-117"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="8334c-118">Подключение к ПИН-коду установлено неправильно.</span><span class="sxs-lookup"><span data-stu-id="8334c-118">The pin connection was not established correctly.</span></span><br/>          |
| <dl> <span data-ttu-id="8334c-119"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="8334c-119"><dt>**E\_FAIL**</dt></span></span> </dl>       | <span data-ttu-id="8334c-120">Не удалось создать поток, или поток уже существует.</span><span class="sxs-lookup"><span data-stu-id="8334c-120">Could not create the thread, or the thread already exists.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8334c-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8334c-121">Remarks</span></span>

<span data-ttu-id="8334c-122">Вызывайте этот метод, когда фильтр владельца станет активным.</span><span class="sxs-lookup"><span data-stu-id="8334c-122">Call this method when the owning filter becomes active.</span></span> <span data-ttu-id="8334c-123">(Если входной ПИН-код является производным от [**кбасепин**](cbasepin.md), переопределите метод [**Кбасепин:: Active**](cbasepin-active.md) .)</span><span class="sxs-lookup"><span data-stu-id="8334c-123">(If your input pin derives from [**CBasePin**](cbasepin.md), override the [**CBasePin::Active**](cbasepin-active.md) method.)</span></span>

<span data-ttu-id="8334c-124">Перед вызовом этого метода вызовите метод [**кпуллпин:: Connect**](cpullpin-connect.md) , чтобы установить соединение с выходным закреплением.</span><span class="sxs-lookup"><span data-stu-id="8334c-124">Before calling this method, call the [**CPullPin::Connect**](cpullpin-connect.md) method to establish the connection with the output pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="8334c-125">Требования</span><span class="sxs-lookup"><span data-stu-id="8334c-125">Requirements</span></span>



| <span data-ttu-id="8334c-126">Требование</span><span class="sxs-lookup"><span data-stu-id="8334c-126">Requirement</span></span> | <span data-ttu-id="8334c-127">Значение</span><span class="sxs-lookup"><span data-stu-id="8334c-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8334c-128">Header</span><span class="sxs-lookup"><span data-stu-id="8334c-128">Header</span></span><br/>  | <dl> <span data-ttu-id="8334c-129"><dt>Пуллпин. h</dt></span><span class="sxs-lookup"><span data-stu-id="8334c-129"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="8334c-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8334c-130">Library</span></span><br/> | <dl> <span data-ttu-id="8334c-131"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="8334c-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8334c-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8334c-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8334c-133">**Класс Кпуллпин**</span><span class="sxs-lookup"><span data-stu-id="8334c-133">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




