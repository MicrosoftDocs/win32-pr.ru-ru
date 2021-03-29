---
description: Метод ClassID определяет, соответствует ли CLSID этому шаблону класса.
ms.assetid: de560f7a-2ccb-44e2-ac32-3b0fea0d80b8
title: Метод Кфакторитемплате. ClassID (Комбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CFactoryTemplate.IsClassID
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 94564d7e9db52f8be22717a10f73fffb7fb6fa14
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657576"
---
# <a name="cfactorytemplateisclassid-method"></a><span data-ttu-id="550b7-103">Кфакторитемплате. ClassID, метод</span><span class="sxs-lookup"><span data-stu-id="550b7-103">CFactoryTemplate.IsClassID method</span></span>

<span data-ttu-id="550b7-104">`IsClassID`Метод определяет, соответствует ли CLSID этому шаблону класса.</span><span class="sxs-lookup"><span data-stu-id="550b7-104">The `IsClassID` method determines whether a CLSID matches this class template.</span></span>

## <a name="syntax"></a><span data-ttu-id="550b7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="550b7-105">Syntax</span></span>


```C++
BOOL IsClassID(
   REFCLSID rclsid
);
```



## <a name="parameters"></a><span data-ttu-id="550b7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="550b7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="550b7-107">*рклсид*</span><span class="sxs-lookup"><span data-stu-id="550b7-107">*rclsid*</span></span> 
</dt> <dd>

<span data-ttu-id="550b7-108">Ссылка на идентификатор CLSID.</span><span class="sxs-lookup"><span data-stu-id="550b7-108">Reference to a CLSID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="550b7-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="550b7-109">Return value</span></span>

<span data-ttu-id="550b7-110">Возвращает **значение true** , если параметр *рклсид* является тем же идентификатором CLSID, что и переменная-член [**\_ кфакторитемплате:: m**](cfactorytemplate-m-clsid.md) , или Else возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="550b7-110">Returns **TRUE** if the *rclsid* parameter is the same CLSID as the [**CFactoryTemplate::m\_ClsID**](cfactorytemplate-m-clsid.md) member variable, or else returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="550b7-111">Требования</span><span class="sxs-lookup"><span data-stu-id="550b7-111">Requirements</span></span>



| <span data-ttu-id="550b7-112">Требование</span><span class="sxs-lookup"><span data-stu-id="550b7-112">Requirement</span></span> | <span data-ttu-id="550b7-113">Значение</span><span class="sxs-lookup"><span data-stu-id="550b7-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="550b7-114">Header</span><span class="sxs-lookup"><span data-stu-id="550b7-114">Header</span></span><br/>  | <dl> <span data-ttu-id="550b7-115"><dt>Комбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="550b7-115"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="550b7-116">Библиотека</span><span class="sxs-lookup"><span data-stu-id="550b7-116">Library</span></span><br/> | <dl> <span data-ttu-id="550b7-117"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="550b7-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="550b7-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="550b7-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="550b7-119">**Класс Кфакторитемплате**</span><span class="sxs-lookup"><span data-stu-id="550b7-119">**CFactoryTemplate Class**</span></span>](cfactorytemplate.md)
</dt> </dl>

 

 




