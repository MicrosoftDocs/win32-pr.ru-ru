---
description: 'Кункновн:: m_cRef число ссылок на элементы.'
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
ms.openlocfilehash: a3f6be7d09149f651bce8d1042b7f3e3a5dc9307
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084582"
---
# <a name="cunknownm_cref-member"></a><span data-ttu-id="66f3a-103">Элемент cref Кункновн:: m \_</span><span class="sxs-lookup"><span data-stu-id="66f3a-103">CUnknown::m\_cRef member</span></span>

<span data-ttu-id="66f3a-104">Число ссылок.</span><span class="sxs-lookup"><span data-stu-id="66f3a-104">Reference count.</span></span>

## <a name="syntax"></a><span data-ttu-id="66f3a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="66f3a-105">Syntax</span></span>


```C++
LONG m_cRef;
```



## <a name="remarks"></a><span data-ttu-id="66f3a-106">Remarks</span><span class="sxs-lookup"><span data-stu-id="66f3a-106">Remarks</span></span>

<span data-ttu-id="66f3a-107">Используйте эту переменную члена при переопределении метода [**нонделегатингаддреф**](cunknown-nondelegatingaddref.md) или [**нонделегатингрелеасе**](cunknown-nondelegatingrelease.md) .</span><span class="sxs-lookup"><span data-stu-id="66f3a-107">Use this member variable if you override the [**NonDelegatingAddRef**](cunknown-nondelegatingaddref.md) or [**NonDelegatingRelease**](cunknown-nondelegatingrelease.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="66f3a-108">Требования</span><span class="sxs-lookup"><span data-stu-id="66f3a-108">Requirements</span></span>



| <span data-ttu-id="66f3a-109">Требование</span><span class="sxs-lookup"><span data-stu-id="66f3a-109">Requirement</span></span> | <span data-ttu-id="66f3a-110">Значение</span><span class="sxs-lookup"><span data-stu-id="66f3a-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66f3a-111">Header</span><span class="sxs-lookup"><span data-stu-id="66f3a-111">Header</span></span><br/>  | <dl> <span data-ttu-id="66f3a-112"><dt>Комбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="66f3a-112"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="66f3a-113">Библиотека</span><span class="sxs-lookup"><span data-stu-id="66f3a-113">Library</span></span><br/> | <dl> <span data-ttu-id="66f3a-114"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="66f3a-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




