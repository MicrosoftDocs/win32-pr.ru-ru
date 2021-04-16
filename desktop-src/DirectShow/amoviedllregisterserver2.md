---
description: Функция AMovieDllRegisterServer2 регистрирует и отменяет регистрацию фильтров.
ms.assetid: 2122949d-0117-4c68-bfcd-c717b14dc970
title: Функция AMovieDllRegisterServer2 (Дллсетуп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AMovieDllRegisterServer2
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ec36290b7cad66b2b5f27633d30ae76c3331eba9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657839"
---
# <a name="amoviedllregisterserver2-function"></a><span data-ttu-id="b9194-103">Функция AMovieDllRegisterServer2</span><span class="sxs-lookup"><span data-stu-id="b9194-103">AMovieDllRegisterServer2 function</span></span>

<span data-ttu-id="b9194-104">Функция **AMovieDllRegisterServer2** регистрирует и отменяет регистрацию фильтров.</span><span class="sxs-lookup"><span data-stu-id="b9194-104">The **AMovieDllRegisterServer2** function registers and unregisters filters.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9194-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b9194-105">Syntax</span></span>


```C++
HRESULT AMovieDllRegisterServer2(
   BOOL bRegister
);
```



## <a name="parameters"></a><span data-ttu-id="b9194-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b9194-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9194-107">*брегистер*</span><span class="sxs-lookup"><span data-stu-id="b9194-107">*bRegister*</span></span> 
</dt> <dd>

<span data-ttu-id="b9194-108">**Значение true** указывает зарегистрировать фильтр, **значение false** — отменить регистрацию.</span><span class="sxs-lookup"><span data-stu-id="b9194-108">**TRUE** indicates register the filter, **FALSE** indicates unregister it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9194-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b9194-109">Return value</span></span>

<span data-ttu-id="b9194-110">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="b9194-110">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b9194-111">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b9194-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b9194-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b9194-112">Remarks</span></span>

<span data-ttu-id="b9194-113">Используйте эту функцию для настройки фильтров.</span><span class="sxs-lookup"><span data-stu-id="b9194-113">Use this function to set up your filters.</span></span> <span data-ttu-id="b9194-114">Дополнительные сведения см. [в разделе Регистрация фильтров DirectShow](how-to-register-directshow-filters.md).</span><span class="sxs-lookup"><span data-stu-id="b9194-114">For more information, see [How to Register DirectShow Filters](how-to-register-directshow-filters.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b9194-115">Требования</span><span class="sxs-lookup"><span data-stu-id="b9194-115">Requirements</span></span>



| <span data-ttu-id="b9194-116">Требование</span><span class="sxs-lookup"><span data-stu-id="b9194-116">Requirement</span></span> | <span data-ttu-id="b9194-117">Значение</span><span class="sxs-lookup"><span data-stu-id="b9194-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9194-118">Header</span><span class="sxs-lookup"><span data-stu-id="b9194-118">Header</span></span><br/>  | <dl> <span data-ttu-id="b9194-119"><dt>Дллсетуп. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b9194-119"><dt>Dllsetup.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="b9194-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b9194-120">Library</span></span><br/> | <dl> <span data-ttu-id="b9194-121"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="b9194-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9194-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b9194-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9194-123">**Функции установки DLL**</span><span class="sxs-lookup"><span data-stu-id="b9194-123">**DLL Setup Functions**</span></span>](dll-setup-functions.md)
</dt> </dl>

 

 




