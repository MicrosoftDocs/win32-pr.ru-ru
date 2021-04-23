---
description: 'Метод Коннектедто извлекает указатель на подключенный ПИН-код, если он есть. Этот метод реализует метод Ипин:: Коннектедто.'
ms.assetid: d8978c9a-e498-4411-a052-f3c2fca570ef
title: Кбасепин. Коннектедто, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.ConnectedTo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5003154011f93b2b70ddd49dab00dcc1659eb2f5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668515"
---
# <a name="cbasepinconnectedto-method"></a><span data-ttu-id="96703-104">Кбасепин. Коннектедто, метод</span><span class="sxs-lookup"><span data-stu-id="96703-104">CBasePin.ConnectedTo method</span></span>

<span data-ttu-id="96703-105">`ConnectedTo`Метод получает указатель на подключенный ПИН-код, если он есть.</span><span class="sxs-lookup"><span data-stu-id="96703-105">The `ConnectedTo` method retrieves a pointer to the connected pin, if any.</span></span> <span data-ttu-id="96703-106">Этот метод реализует метод [**Ипин:: коннектедто**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) .</span><span class="sxs-lookup"><span data-stu-id="96703-106">This method implements the [**IPin::ConnectedTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="96703-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="96703-107">Syntax</span></span>


```C++
HRESULT ConnectedTo(
   IPin **ppPin
);
```



## <a name="parameters"></a><span data-ttu-id="96703-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="96703-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96703-109">*пппин*</span><span class="sxs-lookup"><span data-stu-id="96703-109">*ppPin*</span></span> 
</dt> <dd>

<span data-ttu-id="96703-110">Адрес переменной, которая получает указатель на интерфейс [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin) другого ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="96703-110">Address of a variable that receives a pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the other pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96703-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="96703-111">Return value</span></span>

<span data-ttu-id="96703-112">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="96703-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="96703-113">Возможные значения перечислены в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="96703-113">Possible values include those in the following table.</span></span>



| <span data-ttu-id="96703-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="96703-114">Return code</span></span>                                                                                           | <span data-ttu-id="96703-115">Описание</span><span class="sxs-lookup"><span data-stu-id="96703-115">Description</span></span>                           |
|-------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="96703-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="96703-116"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="96703-117">Успешно.</span><span class="sxs-lookup"><span data-stu-id="96703-117">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="96703-118"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="96703-118"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="96703-119">**Пустой** аргумент указателя.</span><span class="sxs-lookup"><span data-stu-id="96703-119">**NULL** pointer argument.</span></span><br/> |
| <dl> <span data-ttu-id="96703-120"><dt>**VFW \_ E \_ не \_ подключен**</dt></span><span class="sxs-lookup"><span data-stu-id="96703-120"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="96703-121">ПИН-код не подключен.</span><span class="sxs-lookup"><span data-stu-id="96703-121">Pin is not connected.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="96703-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="96703-122">Remarks</span></span>

<span data-ttu-id="96703-123">Если метод завершается успешно, интерфейс **Ипин** , который он возвращает, имеет необработанный счетчик ссылок.</span><span class="sxs-lookup"><span data-stu-id="96703-123">If the method succeeds, the **IPin** interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="96703-124">Не забудьте освободить его по завершении.</span><span class="sxs-lookup"><span data-stu-id="96703-124">Be sure to release it when you are done.</span></span>

## <a name="requirements"></a><span data-ttu-id="96703-125">Требования</span><span class="sxs-lookup"><span data-stu-id="96703-125">Requirements</span></span>



| <span data-ttu-id="96703-126">Требование</span><span class="sxs-lookup"><span data-stu-id="96703-126">Requirement</span></span> | <span data-ttu-id="96703-127">Значение</span><span class="sxs-lookup"><span data-stu-id="96703-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96703-128">Header</span><span class="sxs-lookup"><span data-stu-id="96703-128">Header</span></span><br/>  | <dl> <span data-ttu-id="96703-129"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="96703-129"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="96703-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="96703-130">Library</span></span><br/> | <dl> <span data-ttu-id="96703-131"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="96703-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96703-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="96703-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96703-133">**Класс Кбасепин**</span><span class="sxs-lookup"><span data-stu-id="96703-133">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




