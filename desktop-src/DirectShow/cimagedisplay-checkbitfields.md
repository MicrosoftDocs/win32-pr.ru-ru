---
description: Метод Чеккбитфиелдс проверяет цветовую маску в структуре ВИДЕОИНФО.
ms.assetid: b03455aa-8d90-4fab-999d-7408d8417021
title: Цимажедисплай. Чеккбитфиелдс, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CheckBitFields
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ade581dad5e53c2454df52e387653e44d6d4ad2f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105656948"
---
# <a name="cimagedisplaycheckbitfields-method"></a><span data-ttu-id="497c1-103">Цимажедисплай. Чеккбитфиелдс, метод</span><span class="sxs-lookup"><span data-stu-id="497c1-103">CImageDisplay.CheckBitFields method</span></span>

<span data-ttu-id="497c1-104">`CheckBitFields`Метод проверяет цветовую маску в структуре [**видеоинфо**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) .</span><span class="sxs-lookup"><span data-stu-id="497c1-104">The `CheckBitFields` method validates the color masks in a [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="497c1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="497c1-105">Syntax</span></span>


```C++
BOOL CheckBitFields(
   const VIDEOINFO *pInput
);
```



## <a name="parameters"></a><span data-ttu-id="497c1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="497c1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="497c1-107">*пинпут*</span><span class="sxs-lookup"><span data-stu-id="497c1-107">*pInput*</span></span> 
</dt> <dd>

<span data-ttu-id="497c1-108">Указатель на структуру **видеоинфо** .</span><span class="sxs-lookup"><span data-stu-id="497c1-108">Pointer to a **VIDEOINFO** structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="497c1-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="497c1-109">Return value</span></span>

<span data-ttu-id="497c1-110">Возвращает **значение true** , если цветовая маска является допустимой, или **значение false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="497c1-110">Returns **TRUE** if the color masks are valid, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="497c1-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="497c1-111">Remarks</span></span>

<span data-ttu-id="497c1-112">Этот метод проверяет, что цветовая маска для каждого компонента цвета находится в диапазоне от одного до восьми бит, и что каждая цветовая маска является непрерывной последовательностью битов.</span><span class="sxs-lookup"><span data-stu-id="497c1-112">This method verifies that the color mask for each color component is between one and eight bits long, and that each color mask is a contiguous sequence of bits.</span></span> <span data-ttu-id="497c1-113">Этот метод следует вызывать только в том случае, если для элемента **бикомпрессион** задано значение BI \_ битовых полей.</span><span class="sxs-lookup"><span data-stu-id="497c1-113">Call this method only when the **biCompression** member is set to BI\_BITFIELDS.</span></span>

## <a name="requirements"></a><span data-ttu-id="497c1-114">Требования</span><span class="sxs-lookup"><span data-stu-id="497c1-114">Requirements</span></span>



| <span data-ttu-id="497c1-115">Требование</span><span class="sxs-lookup"><span data-stu-id="497c1-115">Requirement</span></span> | <span data-ttu-id="497c1-116">Значение</span><span class="sxs-lookup"><span data-stu-id="497c1-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="497c1-117">Header</span><span class="sxs-lookup"><span data-stu-id="497c1-117">Header</span></span><br/>  | <dl> <span data-ttu-id="497c1-118"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="497c1-118"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="497c1-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="497c1-119">Library</span></span><br/> | <dl> <span data-ttu-id="497c1-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="497c1-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="497c1-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="497c1-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="497c1-122">**Класс Цимажедисплай**</span><span class="sxs-lookup"><span data-stu-id="497c1-122">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 




