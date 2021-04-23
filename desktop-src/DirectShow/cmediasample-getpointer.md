---
description: Метод-указатель извлекает указатель чтения/записи в буфер. Этот метод реализует метод Имедиасампле::/.
ms.assetid: dd797ad5-6066-4366-a56f-621132f2e6ea
title: Метод Кмедиасампле.-Point (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetPointer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fe8d8785bd52fbe601d9980f8fc146a2c6f41e40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675238"
---
# <a name="cmediasamplegetpointer-method"></a><span data-ttu-id="d6f83-104">Кмедиасампле. метод.</span><span class="sxs-lookup"><span data-stu-id="d6f83-104">CMediaSample.GetPointer method</span></span>

<span data-ttu-id="d6f83-105">`GetPointer`Метод извлекает указатель чтения/записи в буфер.</span><span class="sxs-lookup"><span data-stu-id="d6f83-105">The `GetPointer` method retrieves a read/write pointer to the buffer.</span></span> <span data-ttu-id="d6f83-106">Этот метод реализует метод [**имедиасампле::**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) /.</span><span class="sxs-lookup"><span data-stu-id="d6f83-106">This method implements the [**IMediaSample::GetPointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6f83-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d6f83-107">Syntax</span></span>


```C++
HRESULT GetPointer(
   BYTE **ppBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="d6f83-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d6f83-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6f83-109">*ppBuffer*</span><span class="sxs-lookup"><span data-stu-id="d6f83-109">*ppBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="d6f83-110">Адрес переменной, которая получает указатель на буфер.</span><span class="sxs-lookup"><span data-stu-id="d6f83-110">Address of a variable that receives a pointer to the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6f83-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d6f83-111">Return value</span></span>

<span data-ttu-id="d6f83-112">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="d6f83-112">Returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6f83-113">Требования</span><span class="sxs-lookup"><span data-stu-id="d6f83-113">Requirements</span></span>



| <span data-ttu-id="d6f83-114">Требование</span><span class="sxs-lookup"><span data-stu-id="d6f83-114">Requirement</span></span> | <span data-ttu-id="d6f83-115">Значение</span><span class="sxs-lookup"><span data-stu-id="d6f83-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6f83-116">Header</span><span class="sxs-lookup"><span data-stu-id="d6f83-116">Header</span></span><br/>  | <dl> <span data-ttu-id="d6f83-117"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d6f83-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d6f83-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d6f83-118">Library</span></span><br/> | <dl> <span data-ttu-id="d6f83-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="d6f83-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6f83-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d6f83-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6f83-121">**Класс Кмедиасампле**</span><span class="sxs-lookup"><span data-stu-id="d6f83-121">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




