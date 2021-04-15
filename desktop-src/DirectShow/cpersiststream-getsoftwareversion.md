---
description: Извлекает версию программного обеспечения для этого потока.
ms.assetid: f54153df-5593-4784-acc5-3e0dcef424b5
title: Кперсистстреам. Жетсофтвареверсион, метод (Пстреам. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.GetSoftwareVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f0954e9a113342217dd389c64ec4fc6c04a6f767
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675688"
---
# <a name="cpersiststreamgetsoftwareversion-method"></a><span data-ttu-id="9c11e-103">Кперсистстреам. Жетсофтвареверсион, метод</span><span class="sxs-lookup"><span data-stu-id="9c11e-103">CPersistStream.GetSoftwareVersion method</span></span>

<span data-ttu-id="9c11e-104">Извлекает версию программного обеспечения для этого потока.</span><span class="sxs-lookup"><span data-stu-id="9c11e-104">Retrieves the software version for this stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c11e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9c11e-105">Syntax</span></span>


```C++
virtual DWORD GetSoftwareVersion();
```



## <a name="parameters"></a><span data-ttu-id="9c11e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9c11e-106">Parameters</span></span>

<span data-ttu-id="9c11e-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="9c11e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9c11e-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9c11e-108">Return value</span></span>

<span data-ttu-id="9c11e-109">Возвращает значение **типа DWORD** , содержащее номер версии.</span><span class="sxs-lookup"><span data-stu-id="9c11e-109">Returns a **DWORD** containing the version number.</span></span> <span data-ttu-id="9c11e-110">При каждом изменении формата потока эта функция должна быть изменена для возврата большего числа, чем раньше.</span><span class="sxs-lookup"><span data-stu-id="9c11e-110">Each time the format of the stream is changed, this function should be altered to return a larger number than before.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c11e-111">Требования</span><span class="sxs-lookup"><span data-stu-id="9c11e-111">Requirements</span></span>



| <span data-ttu-id="9c11e-112">Требование</span><span class="sxs-lookup"><span data-stu-id="9c11e-112">Requirement</span></span> | <span data-ttu-id="9c11e-113">Значение</span><span class="sxs-lookup"><span data-stu-id="9c11e-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c11e-114">Header</span><span class="sxs-lookup"><span data-stu-id="9c11e-114">Header</span></span><br/>  | <dl> <span data-ttu-id="9c11e-115"><dt>Пстреам. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9c11e-115"><dt>Pstream.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9c11e-116">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9c11e-116">Library</span></span><br/> | <dl> <span data-ttu-id="9c11e-117"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="9c11e-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c11e-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9c11e-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c11e-119">**Класс Кперсистстреам**</span><span class="sxs-lookup"><span data-stu-id="9c11e-119">**CPersistStream Class**</span></span>](cpersiststream.md)
</dt> </dl>

 

 




