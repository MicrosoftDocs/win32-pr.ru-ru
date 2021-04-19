---
description: Является устаревшей. Вместо этого используйте AMovieDllRegisterServer2.
ms.assetid: d3be5fe0-f993-4a15-a3b8-3d761d51f289
title: Функция Амовиедллрегистерсервер (Дллсетуп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AMovieDllRegisterServer
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d93724c0f1ea6ed8b6cd2fa2b683a5ba9d45f0d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689050"
---
# <a name="amoviedllregisterserver-function"></a><span data-ttu-id="80deb-104">Функция Амовиедллрегистерсервер</span><span class="sxs-lookup"><span data-stu-id="80deb-104">AMovieDllRegisterServer function</span></span>

<span data-ttu-id="80deb-105">Является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="80deb-105">Obsolete.</span></span> <span data-ttu-id="80deb-106">Вместо этого используйте [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) .</span><span class="sxs-lookup"><span data-stu-id="80deb-106">Use [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="80deb-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="80deb-107">Syntax</span></span>


```C++
HRESULT AMovieDllRegisterServer(void);
```



## <a name="parameters"></a><span data-ttu-id="80deb-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="80deb-108">Parameters</span></span>

<span data-ttu-id="80deb-109">У этой функции нет параметров.</span><span class="sxs-lookup"><span data-stu-id="80deb-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="80deb-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="80deb-110">Return value</span></span>

<span data-ttu-id="80deb-111">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="80deb-111">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="80deb-112">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="80deb-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="80deb-113">Требования</span><span class="sxs-lookup"><span data-stu-id="80deb-113">Requirements</span></span>



| <span data-ttu-id="80deb-114">Требование</span><span class="sxs-lookup"><span data-stu-id="80deb-114">Requirement</span></span> | <span data-ttu-id="80deb-115">Значение</span><span class="sxs-lookup"><span data-stu-id="80deb-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80deb-116">Header</span><span class="sxs-lookup"><span data-stu-id="80deb-116">Header</span></span><br/>  | <dl> <span data-ttu-id="80deb-117"><dt>Дллсетуп. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="80deb-117"><dt>Dllsetup.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="80deb-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="80deb-118">Library</span></span><br/> | <dl> <span data-ttu-id="80deb-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="80deb-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80deb-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="80deb-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80deb-121">**Функции установки DLL**</span><span class="sxs-lookup"><span data-stu-id="80deb-121">**DLL Setup Functions**</span></span>](dll-setup-functions.md)
</dt> </dl>

 

 




