---
description: Метод DataGridViewCell получает указатель на интерфейс IUnknown компонента-владельца. Для агрегированного компонента владельцем является внешний компонент. В противном случае компонент владеет самим собой.
ms.assetid: 7d8af9d1-52c0-4f2b-9d05-6ddff85ab508
title: Метод Кункновн. метод Owner (Комбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CUnknown.GetOwner
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e3cb1cd1d5b183857b6d75db79ee0fcdc6cb2d30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657781"
---
# <a name="cunknowngetowner-method"></a><span data-ttu-id="ee0bf-105">Кункновн. метод Owner</span><span class="sxs-lookup"><span data-stu-id="ee0bf-105">CUnknown.GetOwner method</span></span>

<span data-ttu-id="ee0bf-106">`GetOwner`Метод получает указатель на интерфейс **IUnknown** компонента-владельца.</span><span class="sxs-lookup"><span data-stu-id="ee0bf-106">The `GetOwner` method retrieves a pointer to the **IUnknown** interface of the owning component.</span></span> <span data-ttu-id="ee0bf-107">Для агрегированного компонента владельцем является внешний компонент.</span><span class="sxs-lookup"><span data-stu-id="ee0bf-107">For an aggregated component, the owner is the outer component.</span></span> <span data-ttu-id="ee0bf-108">В противном случае компонент владеет самим собой.</span><span class="sxs-lookup"><span data-stu-id="ee0bf-108">Otherwise, the component owns itself.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee0bf-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ee0bf-109">Syntax</span></span>


```C++
LPUNKNOWN GetOwner();
```



## <a name="parameters"></a><span data-ttu-id="ee0bf-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="ee0bf-110">Parameters</span></span>

<span data-ttu-id="ee0bf-111">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="ee0bf-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ee0bf-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ee0bf-112">Return value</span></span>

<span data-ttu-id="ee0bf-113">Возвращает указатель на управляющий интерфейс **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="ee0bf-113">Returns a pointer to the controlling **IUnknown** interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee0bf-114">Требования</span><span class="sxs-lookup"><span data-stu-id="ee0bf-114">Requirements</span></span>



| <span data-ttu-id="ee0bf-115">Требование</span><span class="sxs-lookup"><span data-stu-id="ee0bf-115">Requirement</span></span> | <span data-ttu-id="ee0bf-116">Значение</span><span class="sxs-lookup"><span data-stu-id="ee0bf-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee0bf-117">Header</span><span class="sxs-lookup"><span data-stu-id="ee0bf-117">Header</span></span><br/>  | <dl> <span data-ttu-id="ee0bf-118"><dt>Комбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ee0bf-118"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ee0bf-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ee0bf-119">Library</span></span><br/> | <dl> <span data-ttu-id="ee0bf-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="ee0bf-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




