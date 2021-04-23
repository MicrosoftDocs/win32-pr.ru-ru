---
description: Является устаревшей. Вместо этого используйте AMovieDllRegisterServer2.
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
ms.openlocfilehash: 4cab526a69f14cdd4c4f48767ca34722f61002eb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689221"
---
# <a name="amoviedllunregisterserver-function"></a><span data-ttu-id="a3a8f-104">Функция Амовиедллунрегистерсервер</span><span class="sxs-lookup"><span data-stu-id="a3a8f-104">AMovieDllUnregisterServer function</span></span>

<span data-ttu-id="a3a8f-105">Является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="a3a8f-105">Obsolete.</span></span> <span data-ttu-id="a3a8f-106">Вместо этого используйте [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) .</span><span class="sxs-lookup"><span data-stu-id="a3a8f-106">Use [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3a8f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a3a8f-107">Syntax</span></span>


```C++
HRESULT AMovieDllUnregisterServer(void);
```



## <a name="parameters"></a><span data-ttu-id="a3a8f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a3a8f-108">Parameters</span></span>

<span data-ttu-id="a3a8f-109">У этой функции нет параметров.</span><span class="sxs-lookup"><span data-stu-id="a3a8f-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a3a8f-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a3a8f-110">Return value</span></span>

<span data-ttu-id="a3a8f-111">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="a3a8f-111">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a3a8f-112">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a3a8f-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3a8f-113">Требования</span><span class="sxs-lookup"><span data-stu-id="a3a8f-113">Requirements</span></span>



| <span data-ttu-id="a3a8f-114">Требование</span><span class="sxs-lookup"><span data-stu-id="a3a8f-114">Requirement</span></span> | <span data-ttu-id="a3a8f-115">Значение</span><span class="sxs-lookup"><span data-stu-id="a3a8f-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3a8f-116">Header</span><span class="sxs-lookup"><span data-stu-id="a3a8f-116">Header</span></span><br/>  | <dl> <span data-ttu-id="a3a8f-117"><dt>Дллсетуп. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a3a8f-117"><dt>Dllsetup.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a3a8f-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a3a8f-118">Library</span></span><br/> | <dl> <span data-ttu-id="a3a8f-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="a3a8f-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3a8f-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a3a8f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3a8f-121">**Функции установки DLL**</span><span class="sxs-lookup"><span data-stu-id="a3a8f-121">**DLL Setup Functions**</span></span>](dll-setup-functions.md)
</dt> </dl>

 

 




