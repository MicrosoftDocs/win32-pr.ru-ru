---
description: Метод Сетформаттипе задает тип формата.
ms.assetid: e8ed9190-7169-4d51-ace7-597f43ff083e
title: Кмедиатипе. Сетформаттипе, метод (Мтипе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetFormatType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7843c5a9788545909ef4297accfa342c08b71e88
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668893"
---
# <a name="cmediatypesetformattype-method"></a><span data-ttu-id="fd76a-103">Кмедиатипе. Сетформаттипе, метод</span><span class="sxs-lookup"><span data-stu-id="fd76a-103">CMediaType.SetFormatType method</span></span>

<span data-ttu-id="fd76a-104">Метод Сетформаттипе задает тип формата.</span><span class="sxs-lookup"><span data-stu-id="fd76a-104">The \`\`SetFormatType method specifies the format type.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd76a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fd76a-105">Syntax</span></span>


```C++
void SetFormatType(
   const GUID *pformattype
);
```



## <a name="parameters"></a><span data-ttu-id="fd76a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fd76a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd76a-107">*пформаттипе*</span><span class="sxs-lookup"><span data-stu-id="fd76a-107">*pformattype*</span></span> 
</dt> <dd>

<span data-ttu-id="fd76a-108">Указатель на **идентификатор GUID** , указывающий тип формата.</span><span class="sxs-lookup"><span data-stu-id="fd76a-108">Pointer to a **GUID** that specifies the format type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd76a-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fd76a-109">Return value</span></span>

<span data-ttu-id="fd76a-110">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="fd76a-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd76a-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fd76a-111">Remarks</span></span>

<span data-ttu-id="fd76a-112">Этот метод задает элемент **форматтипе** .</span><span class="sxs-lookup"><span data-stu-id="fd76a-112">This method sets the **formattype** member.</span></span> <span data-ttu-id="fd76a-113">Тип формата определяет макет блока форматирования.</span><span class="sxs-lookup"><span data-stu-id="fd76a-113">The format type defines the layout of the format block.</span></span> <span data-ttu-id="fd76a-114">Например, если тип формата — FORMAT \_ видеоинфо, блок формата должен содержать структуру **видеоинфохеадер** .</span><span class="sxs-lookup"><span data-stu-id="fd76a-114">For example, if the format type is FORMAT\_VideoInfo, the format block should contain a **VIDEOINFOHEADER** structure.</span></span> <span data-ttu-id="fd76a-115">Чтобы задать блок формата, вызовите метод [**кмедиатипе:: сетформат**](cmediatype-setformat.md) .</span><span class="sxs-lookup"><span data-stu-id="fd76a-115">To set the format block, call the [**CMediaType::SetFormat**](cmediatype-setformat.md) method.</span></span> <span data-ttu-id="fd76a-116">Вызывающий объект отвечает за обеспечение соответствия блока формата типу формата.</span><span class="sxs-lookup"><span data-stu-id="fd76a-116">The caller is responsible for making sure that the format block matches the format type.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd76a-117">Требования</span><span class="sxs-lookup"><span data-stu-id="fd76a-117">Requirements</span></span>



| <span data-ttu-id="fd76a-118">Требование</span><span class="sxs-lookup"><span data-stu-id="fd76a-118">Requirement</span></span> | <span data-ttu-id="fd76a-119">Значение</span><span class="sxs-lookup"><span data-stu-id="fd76a-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd76a-120">Header</span><span class="sxs-lookup"><span data-stu-id="fd76a-120">Header</span></span><br/>  | <dl> <span data-ttu-id="fd76a-121"><dt>Мтипе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fd76a-121"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="fd76a-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="fd76a-122">Library</span></span><br/> | <dl> <span data-ttu-id="fd76a-123"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="fd76a-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd76a-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fd76a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd76a-125">**Класс Кмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="fd76a-125">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 


``
