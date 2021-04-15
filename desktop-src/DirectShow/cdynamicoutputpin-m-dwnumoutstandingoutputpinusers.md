---
description: Число потоков потоковой передачи, использующих этот ПИН-код.
ms.assetid: f8650a17-edab-4d69-91da-78107c3c60b9
title: 'Элемент Кдинамикаутпутпин:: m_dwNumOutstandingOutputPinUsers (Амфилтер. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_dwNumOutstandingOutputPinUsers
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2ba214a2c1c6d3d056147db54c936cb61b73dcfc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669424"
---
# <a name="cdynamicoutputpinm_dwnumoutstandingoutputpinusers-member"></a><span data-ttu-id="8ad45-103">Элемент Кдинамикаутпутпин:: m \_ двнумаутстандингаутпутпинусерс</span><span class="sxs-lookup"><span data-stu-id="8ad45-103">CDynamicOutputPin::m\_dwNumOutstandingOutputPinUsers member</span></span>

<span data-ttu-id="8ad45-104">Число потоков потоковой передачи, использующих этот ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="8ad45-104">Number of streaming threads using this pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ad45-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8ad45-105">Syntax</span></span>


```C++
DWORD m_dwNumOutstandingOutputPinUsers;
```



## <a name="remarks"></a><span data-ttu-id="8ad45-106">Примечания</span><span class="sxs-lookup"><span data-stu-id="8ad45-106">Remarks</span></span>

<span data-ttu-id="8ad45-107">Метод [**кдинамикаутпутпин:: стартусингаутпутпин**](cdynamicoutputpin-startusingoutputpin.md) увеличивает эту переменную, а метод [**Кдинамикаутпутпин:: стопусингаутпутпин**](cdynamicoutputpin-stopusingoutputpin.md) уменьшает его.</span><span class="sxs-lookup"><span data-stu-id="8ad45-107">The [**CDynamicOutputPin::StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) method increments this variable, and the [**CDynamicOutputPin::StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) method decrements it.</span></span> <span data-ttu-id="8ad45-108">Если значение больше нуля, то некоторый поток использует этот ПИН-код для потоковой передачи данных или для изменения типа соединения.</span><span class="sxs-lookup"><span data-stu-id="8ad45-108">When the value is greater than zero, some thread is using this pin to stream data or to change the connection type.</span></span> <span data-ttu-id="8ad45-109">ПИН-код не может быть заблокирован, пока это так.</span><span class="sxs-lookup"><span data-stu-id="8ad45-109">The pin cannot be blocked while this is the case.</span></span>

<span data-ttu-id="8ad45-110">Прежде чем обращаться к этой переменной, удерживайте критический раздел [**кдинамикаутпутпин:: m \_ блоккстателокк**](cdynamicoutputpin-m-blockstatelock.md) .</span><span class="sxs-lookup"><span data-stu-id="8ad45-110">Before accessing this variable, hold the [**CDynamicOutputPin::m\_BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) critical section.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ad45-111">Требования</span><span class="sxs-lookup"><span data-stu-id="8ad45-111">Requirements</span></span>



| <span data-ttu-id="8ad45-112">Требование</span><span class="sxs-lookup"><span data-stu-id="8ad45-112">Requirement</span></span> | <span data-ttu-id="8ad45-113">Значение</span><span class="sxs-lookup"><span data-stu-id="8ad45-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ad45-114">Header</span><span class="sxs-lookup"><span data-stu-id="8ad45-114">Header</span></span><br/>  | <dl> <span data-ttu-id="8ad45-115"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8ad45-115"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="8ad45-116">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8ad45-116">Library</span></span><br/> | <dl> <span data-ttu-id="8ad45-117"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="8ad45-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ad45-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8ad45-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ad45-119">**Класс Кдинамикаутпутпин**</span><span class="sxs-lookup"><span data-stu-id="8ad45-119">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> <dt>

[<span data-ttu-id="8ad45-120">**Кдинамикаутпутпин:: Стреамингсреадусингаутпутпин**</span><span class="sxs-lookup"><span data-stu-id="8ad45-120">**CDynamicOutputPin::StreamingThreadUsingOutputPin**</span></span>](cdynamicoutputpin-streamingthreadusingoutputpin.md)
</dt> </dl>

 

 




