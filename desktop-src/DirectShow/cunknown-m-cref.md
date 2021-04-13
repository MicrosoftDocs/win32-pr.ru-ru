---
description: Число ссылок.
ms.assetid: be619a85-ca73-4cee-9df7-20e7be21853b
title: 'Элемент Кункновн:: m_cRef (Комбасе. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_cRef
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 94ff5d88ca48feeb46a8b0411a55d6261aefcf6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657780"
---
# <a name="cunknownm_cref-member"></a><span data-ttu-id="6f154-103">Элемент cref Кункновн:: m \_</span><span class="sxs-lookup"><span data-stu-id="6f154-103">CUnknown::m\_cRef member</span></span>

<span data-ttu-id="6f154-104">Число ссылок.</span><span class="sxs-lookup"><span data-stu-id="6f154-104">Reference count.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f154-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6f154-105">Syntax</span></span>


```C++
LONG m_cRef;
```



## <a name="remarks"></a><span data-ttu-id="6f154-106">Примечания</span><span class="sxs-lookup"><span data-stu-id="6f154-106">Remarks</span></span>

<span data-ttu-id="6f154-107">Используйте эту переменную члена при переопределении метода [**нонделегатингаддреф**](cunknown-nondelegatingaddref.md) или [**нонделегатингрелеасе**](cunknown-nondelegatingrelease.md) .</span><span class="sxs-lookup"><span data-stu-id="6f154-107">Use this member variable if you override the [**NonDelegatingAddRef**](cunknown-nondelegatingaddref.md) or [**NonDelegatingRelease**](cunknown-nondelegatingrelease.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f154-108">Требования</span><span class="sxs-lookup"><span data-stu-id="6f154-108">Requirements</span></span>



| <span data-ttu-id="6f154-109">Требование</span><span class="sxs-lookup"><span data-stu-id="6f154-109">Requirement</span></span> | <span data-ttu-id="6f154-110">Значение</span><span class="sxs-lookup"><span data-stu-id="6f154-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f154-111">Header</span><span class="sxs-lookup"><span data-stu-id="6f154-111">Header</span></span><br/>  | <dl> <span data-ttu-id="6f154-112"><dt>Комбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6f154-112"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6f154-113">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6f154-113">Library</span></span><br/> | <dl> <span data-ttu-id="6f154-114"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="6f154-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




