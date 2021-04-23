---
description: Метод Чеккмедиатипе определяет, совместим ли предложенный тип мультимедиа с форматом вывода.
ms.assetid: 567663cf-c79f-4549-9fa9-b16da957d2b1
title: Цимажедисплай. Чеккмедиатипе, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a8ebcdbe6bbfe6538a2ea166be0816f31954c7d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105656947"
---
# <a name="cimagedisplaycheckmediatype-method"></a><span data-ttu-id="aa791-103">Цимажедисплай. Чеккмедиатипе, метод</span><span class="sxs-lookup"><span data-stu-id="aa791-103">CImageDisplay.CheckMediaType method</span></span>

<span data-ttu-id="aa791-104">`CheckMediaType`Метод определяет, совместим ли предложенный тип мультимедиа с форматом вывода.</span><span class="sxs-lookup"><span data-stu-id="aa791-104">The `CheckMediaType` method determines whether a proposed media type is compatible with the display format.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa791-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="aa791-105">Syntax</span></span>


```C++
HRESULT CheckMediaType(
   const CMediaType *pmtIn
);
```



## <a name="parameters"></a><span data-ttu-id="aa791-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="aa791-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa791-107">*пмтин*</span><span class="sxs-lookup"><span data-stu-id="aa791-107">*pmtIn*</span></span> 
</dt> <dd>

<span data-ttu-id="aa791-108">Указатель на объект [**кмедиатипе**](cmediatype.md) , который содержит тип мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="aa791-108">Pointer to a [**CMediaType**](cmediatype.md) object that contains the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa791-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="aa791-109">Return value</span></span>

<span data-ttu-id="aa791-110">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="aa791-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="aa791-111">Ниже приведены возможные значения.</span><span class="sxs-lookup"><span data-stu-id="aa791-111">Possible values include the following.</span></span>



| <span data-ttu-id="aa791-112">Код возврата</span><span class="sxs-lookup"><span data-stu-id="aa791-112">Return code</span></span>                                                                                  | <span data-ttu-id="aa791-113">Описание</span><span class="sxs-lookup"><span data-stu-id="aa791-113">Description</span></span>                              |
|----------------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <span data-ttu-id="aa791-114"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="aa791-114"><dt>**E\_FAIL**</dt></span></span> </dl>       | <span data-ttu-id="aa791-115">Недопустимый тип носителя.</span><span class="sxs-lookup"><span data-stu-id="aa791-115">Invalid media type.</span></span><br/>           |
| <dl> <span data-ttu-id="aa791-116"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="aa791-116"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="aa791-117">Недопустимый тип носителя.</span><span class="sxs-lookup"><span data-stu-id="aa791-117">Invalid media type.</span></span><br/>           |
| <dl> <span data-ttu-id="aa791-118"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="aa791-118"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="aa791-119">Тип мультимедиа является совместимым.</span><span class="sxs-lookup"><span data-stu-id="aa791-119">The media type is compatible.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="aa791-120">Требования</span><span class="sxs-lookup"><span data-stu-id="aa791-120">Requirements</span></span>



| <span data-ttu-id="aa791-121">Требование</span><span class="sxs-lookup"><span data-stu-id="aa791-121">Requirement</span></span> | <span data-ttu-id="aa791-122">Значение</span><span class="sxs-lookup"><span data-stu-id="aa791-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa791-123">Header</span><span class="sxs-lookup"><span data-stu-id="aa791-123">Header</span></span><br/>  | <dl> <span data-ttu-id="aa791-124"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="aa791-124"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="aa791-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="aa791-125">Library</span></span><br/> | <dl> <span data-ttu-id="aa791-126"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="aa791-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa791-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="aa791-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa791-128">**Класс Цимажедисплай**</span><span class="sxs-lookup"><span data-stu-id="aa791-128">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 




