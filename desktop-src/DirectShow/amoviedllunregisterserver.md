---
description: Амовиедллунрегистерсервер-функция устарела. Вместо этого используйте AMovieDllRegisterServer2.
ms.assetid: 80f52109-6239-4e3d-a395-eb69f5278cd2
title: Функция Амовиедллунрегистерсервер (Дллсетуп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AMovieDllUnregisterServer
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: df7fb34246249298efc143b7ccc8e6332540867c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099932"
---
# <a name="amoviedllunregisterserver-function"></a><span data-ttu-id="f1026-104">Функция Амовиедллунрегистерсервер</span><span class="sxs-lookup"><span data-stu-id="f1026-104">AMovieDllUnregisterServer function</span></span>

<span data-ttu-id="f1026-105">Является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="f1026-105">Obsolete.</span></span> <span data-ttu-id="f1026-106">Вместо этого используйте [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) .</span><span class="sxs-lookup"><span data-stu-id="f1026-106">Use [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1026-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f1026-107">Syntax</span></span>


```C++
HRESULT AMovieDllUnregisterServer(void);
```



## <a name="parameters"></a><span data-ttu-id="f1026-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f1026-108">Parameters</span></span>

<span data-ttu-id="f1026-109">У этой функции нет параметров.</span><span class="sxs-lookup"><span data-stu-id="f1026-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f1026-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f1026-110">Return value</span></span>

<span data-ttu-id="f1026-111">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="f1026-111">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f1026-112">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f1026-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1026-113">Требования</span><span class="sxs-lookup"><span data-stu-id="f1026-113">Requirements</span></span>



| <span data-ttu-id="f1026-114">Требование</span><span class="sxs-lookup"><span data-stu-id="f1026-114">Requirement</span></span> | <span data-ttu-id="f1026-115">Значение</span><span class="sxs-lookup"><span data-stu-id="f1026-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1026-116">Header</span><span class="sxs-lookup"><span data-stu-id="f1026-116">Header</span></span><br/>  | <dl> <span data-ttu-id="f1026-117"><dt>Дллсетуп. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f1026-117"><dt>Dllsetup.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f1026-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f1026-118">Library</span></span><br/> | <dl> <span data-ttu-id="f1026-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="f1026-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1026-120">См. также</span><span class="sxs-lookup"><span data-stu-id="f1026-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1026-121">**Функции установки DLL**</span><span class="sxs-lookup"><span data-stu-id="f1026-121">**DLL Setup Functions**</span></span>](dll-setup-functions.md)
</dt> </dl>

 

 




