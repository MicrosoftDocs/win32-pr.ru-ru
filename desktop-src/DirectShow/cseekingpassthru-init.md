---
description: Метод init Инициализирует объект.
ms.assetid: a919adfa-0ffb-4241-b709-ad0e8d55476a
title: Метод CSeekingPassThru.Init (Сикпт. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSeekingPassThru.Init
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 78176a6966f379240b5b7edd1ef5b73d7fa75b3f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105656901"
---
# <a name="cseekingpassthruinit-method"></a><span data-ttu-id="8acc9-103">Метод CSeekingPassThru.Init</span><span class="sxs-lookup"><span data-stu-id="8acc9-103">CSeekingPassThru.Init method</span></span>

<span data-ttu-id="8acc9-104">`Init`Метод инициализирует объект.</span><span class="sxs-lookup"><span data-stu-id="8acc9-104">The `Init` method initializes the object.</span></span>

## <a name="syntax"></a><span data-ttu-id="8acc9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8acc9-105">Syntax</span></span>


```C++
HRESULT Init(
  [in] BOOL bSupportRendering,
       IPin *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="8acc9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8acc9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8acc9-107">*бсуппортрендеринг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8acc9-107">*bSupportRendering* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8acc9-108">Логическое значение, указывающее, является ли фильтр модулем подготовки отчетов.</span><span class="sxs-lookup"><span data-stu-id="8acc9-108">Boolean value that specifies whether the filter is a renderer.</span></span> <span data-ttu-id="8acc9-109">Используйте значение **true** , если фильтр является модулем подготовки отчетов, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="8acc9-109">Use the value **TRUE** if the filter is a renderer, or **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="8acc9-110">*ппин*</span><span class="sxs-lookup"><span data-stu-id="8acc9-110">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="8acc9-111">Указатель на интерфейс [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin) для входного ПИН-кода фильтра.</span><span class="sxs-lookup"><span data-stu-id="8acc9-111">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface on the filter's input pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8acc9-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8acc9-112">Return value</span></span>

<span data-ttu-id="8acc9-113">Возвращает одно из значений **HRESULT** , приведенных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="8acc9-113">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="8acc9-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="8acc9-114">Return code</span></span>                                                                                   | <span data-ttu-id="8acc9-115">Описание</span><span class="sxs-lookup"><span data-stu-id="8acc9-115">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="8acc9-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="8acc9-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="8acc9-117">Успешно.</span><span class="sxs-lookup"><span data-stu-id="8acc9-117">Success.</span></span><br/>                                |
| <dl> <span data-ttu-id="8acc9-118"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="8acc9-118"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="8acc9-119">Объект уже инициализирован.</span><span class="sxs-lookup"><span data-stu-id="8acc9-119">Object was already initialized.</span></span><br/>         |
| <dl> <span data-ttu-id="8acc9-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="8acc9-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="8acc9-121">Недостаточно памяти для создания объекта.</span><span class="sxs-lookup"><span data-stu-id="8acc9-121">Not enough memory to create the object.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8acc9-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8acc9-122">Remarks</span></span>

<span data-ttu-id="8acc9-123">Если значение *бсуппортрендеринг* равно **true**, этот метод создает экземпляр класса [**крендерерпоспасссру**](crendererpospassthru.md) .</span><span class="sxs-lookup"><span data-stu-id="8acc9-123">If the value of *bSupportRendering* is **TRUE**, this method creates an instance of the [**CRendererPosPassThru**](crendererpospassthru.md) class.</span></span> <span data-ttu-id="8acc9-124">В противном случае создается экземпляр класса [**кпоспасссру**](cpospassthru.md) .</span><span class="sxs-lookup"><span data-stu-id="8acc9-124">Otherwise, it creates an instance of the [**CPosPassThru**](cpospassthru.md) class.</span></span>

## <a name="requirements"></a><span data-ttu-id="8acc9-125">Требования</span><span class="sxs-lookup"><span data-stu-id="8acc9-125">Requirements</span></span>



| <span data-ttu-id="8acc9-126">Требование</span><span class="sxs-lookup"><span data-stu-id="8acc9-126">Requirement</span></span> | <span data-ttu-id="8acc9-127">Значение</span><span class="sxs-lookup"><span data-stu-id="8acc9-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8acc9-128">Header</span><span class="sxs-lookup"><span data-stu-id="8acc9-128">Header</span></span><br/>  | <dl> <span data-ttu-id="8acc9-129"><dt>Сикпт. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8acc9-129"><dt>Seekpt.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="8acc9-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8acc9-130">Library</span></span><br/> | <dl> <span data-ttu-id="8acc9-131"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="8acc9-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8acc9-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8acc9-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8acc9-133">**Класс Ксикингпасссру**</span><span class="sxs-lookup"><span data-stu-id="8acc9-133">**CSeekingPassThru Class**</span></span>](cseekingpassthru.md)
</dt> </dl>

 

 




