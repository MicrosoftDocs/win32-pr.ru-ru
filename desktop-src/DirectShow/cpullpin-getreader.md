---
description: Метод DataReader возвращает указатель на интерфейс Иасинкреадер выходного контакта.
ms.assetid: bb7ed3f2-a5bc-496c-8a52-f9915a75105e
title: Метод Кпуллпин. DataReader (Пуллпин. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.GetReader
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3a20bbb689c4ee5e3ac12c510098163d9fbb224e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669055"
---
# <a name="cpullpingetreader-method"></a><span data-ttu-id="2e449-103">Кпуллпин. DataReader, метод</span><span class="sxs-lookup"><span data-stu-id="2e449-103">CPullPin.GetReader method</span></span>

<span data-ttu-id="2e449-104">`GetReader`Метод возвращает указатель на интерфейс [**иасинкреадер**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) выходного контакта.</span><span class="sxs-lookup"><span data-stu-id="2e449-104">The `GetReader` method returns a pointer to the output pin's [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e449-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2e449-105">Syntax</span></span>


```C++
IAsyncReader* GetReader();
```



## <a name="parameters"></a><span data-ttu-id="2e449-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2e449-106">Parameters</span></span>

<span data-ttu-id="2e449-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="2e449-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2e449-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2e449-108">Return value</span></span>

<span data-ttu-id="2e449-109">Возвращает указатель на интерфейс [**иасинкреадер**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) .</span><span class="sxs-lookup"><span data-stu-id="2e449-109">Returns a pointer to the [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e449-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2e449-110">Remarks</span></span>

<span data-ttu-id="2e449-111">Возвращенный интерфейс имеет необработанный счетчик ссылок.</span><span class="sxs-lookup"><span data-stu-id="2e449-111">The returned interface has an outstanding reference count.</span></span> <span data-ttu-id="2e449-112">Вызывающий объект должен освободить интерфейс.</span><span class="sxs-lookup"><span data-stu-id="2e449-112">The caller must release the interface.</span></span>

<span data-ttu-id="2e449-113">Метод не проверяет значение указателя интерфейса перед вызовом **AddRef**, поэтому не вызывайте его до тех пор, пока не будет успешно вызван метод [**Кпуллпин:: Connect**](cpullpin-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="2e449-113">The method does not check the value of the interface pointer before calling **AddRef**, so do not call this until you have successfully called the [**CPullPin::Connect**](cpullpin-connect.md) method.</span></span> <span data-ttu-id="2e449-114">В противном случае указатель интерфейса может иметь **значение NULL** , а вызов **AddRef** выдаст исключение.</span><span class="sxs-lookup"><span data-stu-id="2e449-114">Otherwise, the interface pointer might be **NULL** and calling **AddRef** will throw an exception.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e449-115">Требования</span><span class="sxs-lookup"><span data-stu-id="2e449-115">Requirements</span></span>



| <span data-ttu-id="2e449-116">Требование</span><span class="sxs-lookup"><span data-stu-id="2e449-116">Requirement</span></span> | <span data-ttu-id="2e449-117">Значение</span><span class="sxs-lookup"><span data-stu-id="2e449-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e449-118">Header</span><span class="sxs-lookup"><span data-stu-id="2e449-118">Header</span></span><br/>  | <dl> <span data-ttu-id="2e449-119"><dt>Пуллпин. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e449-119"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="2e449-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2e449-120">Library</span></span><br/> | <dl> <span data-ttu-id="2e449-121"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="2e449-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e449-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2e449-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e449-123">**Класс Кпуллпин**</span><span class="sxs-lookup"><span data-stu-id="2e449-123">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




