---
description: Указатель на функцию, которая вызывается из точки входа библиотеки DLL. Может иметь значение NULL.
ms.assetid: 0769f55b-6f0d-4a89-9d3f-64f211426342
title: 'Элемент Кфакторитемплате:: m_lpfnInit (Комбасе. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_lpfnInit
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b44181f926f77ecc7cc22673622d4a0d3dcb7d26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657570"
---
# <a name="cfactorytemplatem_lpfninit-member"></a><span data-ttu-id="12a8c-104">Элемент Кфакторитемплате:: m \_ лпфнинит</span><span class="sxs-lookup"><span data-stu-id="12a8c-104">CFactoryTemplate::m\_lpfnInit member</span></span>

<span data-ttu-id="12a8c-105">Указатель на функцию, которая вызывается из точки входа библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="12a8c-105">Pointer to a function that gets called from the DLL entry point.</span></span> <span data-ttu-id="12a8c-106">Может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="12a8c-106">Can be **NULL**.</span></span>

## <a name="syntax"></a><span data-ttu-id="12a8c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="12a8c-107">Syntax</span></span>


```C++
LPFNInitRoutine m_lpfnInit;
```



## <a name="remarks"></a><span data-ttu-id="12a8c-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="12a8c-108">Remarks</span></span>

<span data-ttu-id="12a8c-109">Тип указателя функции — [**лпфнинитраутине**](lpfninitroutine.md).</span><span class="sxs-lookup"><span data-stu-id="12a8c-109">The function pointer type is [**LPFNInitRoutine**](lpfninitroutine.md).</span></span> <span data-ttu-id="12a8c-110">При предоставлении этой функции в библиотеке DLL функция точки входа DLL вызывает ее со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="12a8c-110">If you provide this function in your DLL, the DLL entry-point function calls it with following parameters:</span></span>

-   <span data-ttu-id="12a8c-111">*блоадинг*: **true** при загрузке библиотеки DLL, **значение false** при выгрузке библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="12a8c-111">*bLoading*: **TRUE** when the DLL is loaded, **FALSE** when the DLL is unloaded.</span></span>
-   <span data-ttu-id="12a8c-112">*рклсид*: указатель на clisd инициализированного объекта, указанный в переменной члена [**\_ CLSID кфакторитемплате:: m**](cfactorytemplate-m-clsid.md) .</span><span class="sxs-lookup"><span data-stu-id="12a8c-112">*rclsid*: Pointer to the object's CLISD, specified in the [**CFactoryTemplate::m\_ClsID**](cfactorytemplate-m-clsid.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="12a8c-113">Требования</span><span class="sxs-lookup"><span data-stu-id="12a8c-113">Requirements</span></span>



| <span data-ttu-id="12a8c-114">Требование</span><span class="sxs-lookup"><span data-stu-id="12a8c-114">Requirement</span></span> | <span data-ttu-id="12a8c-115">Значение</span><span class="sxs-lookup"><span data-stu-id="12a8c-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12a8c-116">Header</span><span class="sxs-lookup"><span data-stu-id="12a8c-116">Header</span></span><br/>  | <dl> <span data-ttu-id="12a8c-117"><dt>Комбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="12a8c-117"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="12a8c-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="12a8c-118">Library</span></span><br/> | <dl> <span data-ttu-id="12a8c-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="12a8c-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12a8c-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="12a8c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12a8c-121">**Класс Кфакторитемплате**</span><span class="sxs-lookup"><span data-stu-id="12a8c-121">**CFactoryTemplate Class**</span></span>](cfactorytemplate.md)
</dt> </dl>

 

 




