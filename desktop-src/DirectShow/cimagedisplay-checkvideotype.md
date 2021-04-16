---
description: Метод Чекквидеотипе проверяет, совместим ли указанный формат ВИДЕОИНФО с форматом вывода.
ms.assetid: a8593c7d-bde0-4c44-b450-10c129dd0007
title: Цимажедисплай. Чекквидеотипе, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CheckVideoType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7db198270804053993352c4969b924fa7edc891f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657817"
---
# <a name="cimagedisplaycheckvideotype-method"></a><span data-ttu-id="c5a29-103">Цимажедисплай. Чекквидеотипе, метод</span><span class="sxs-lookup"><span data-stu-id="c5a29-103">CImageDisplay.CheckVideoType method</span></span>

<span data-ttu-id="c5a29-104">`CheckVideoType`Метод проверяет, совместим ли указанный формат [**видеоинфо**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) с форматом вывода.</span><span class="sxs-lookup"><span data-stu-id="c5a29-104">The `CheckVideoType` method checks whether a specified [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) format is compatible with the display format.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5a29-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c5a29-105">Syntax</span></span>


```C++
HRESULT CheckVideoType(
   const VIDEOINFO *pInput
);
```



## <a name="parameters"></a><span data-ttu-id="c5a29-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c5a29-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5a29-107">*пинпут*</span><span class="sxs-lookup"><span data-stu-id="c5a29-107">*pInput*</span></span> 
</dt> <dd>

<span data-ttu-id="c5a29-108">Указатель на структуру **видеоинфо** .</span><span class="sxs-lookup"><span data-stu-id="c5a29-108">Pointer to a **VIDEOINFO** structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5a29-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c5a29-109">Return value</span></span>

<span data-ttu-id="c5a29-110">Возвращает значение S \_ , если формат совместим, или E \_ INVALIDARG в противном случае.</span><span class="sxs-lookup"><span data-stu-id="c5a29-110">Returns S\_OK if the format is compatible, or E\_INVALIDARG otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5a29-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c5a29-111">Remarks</span></span>

<span data-ttu-id="c5a29-112">Этот метод возвращает значение \_ ОК, если предложенный тип можно легко отобразить в текущих параметрах отображения.</span><span class="sxs-lookup"><span data-stu-id="c5a29-112">This method returns S\_OK if the proposed type can be displayed easily under the current display settings.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5a29-113">Требования</span><span class="sxs-lookup"><span data-stu-id="c5a29-113">Requirements</span></span>



| <span data-ttu-id="c5a29-114">Требование</span><span class="sxs-lookup"><span data-stu-id="c5a29-114">Requirement</span></span> | <span data-ttu-id="c5a29-115">Значение</span><span class="sxs-lookup"><span data-stu-id="c5a29-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5a29-116">Header</span><span class="sxs-lookup"><span data-stu-id="c5a29-116">Header</span></span><br/>  | <dl> <span data-ttu-id="c5a29-117"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c5a29-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c5a29-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c5a29-118">Library</span></span><br/> | <dl> <span data-ttu-id="c5a29-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="c5a29-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5a29-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c5a29-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5a29-121">**Класс Цимажедисплай**</span><span class="sxs-lookup"><span data-stu-id="c5a29-121">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 




