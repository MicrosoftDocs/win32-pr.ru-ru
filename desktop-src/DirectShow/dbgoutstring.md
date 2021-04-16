---
description: Функция Дбгаутстринг отправляет строку в расположение выходных данных отладки. Игнорируется в розничных сборках.
ms.assetid: 644bf4f7-ec2d-466e-85c6-690dd44da702
title: Функция Дбгаутстринг (Вксдебуг. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgOutString
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bdc12d4b73080f00a3d32c80074a801146ea4a74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657222"
---
# <a name="dbgoutstring-function"></a><span data-ttu-id="e93a9-104">Функция Дбгаутстринг</span><span class="sxs-lookup"><span data-stu-id="e93a9-104">DbgOutString function</span></span>

<span data-ttu-id="e93a9-105">Функция **дбгаутстринг** отправляет строку в расположение выходных данных отладки.</span><span class="sxs-lookup"><span data-stu-id="e93a9-105">The **DbgOutString** function sends a string to the debug output location.</span></span> <span data-ttu-id="e93a9-106">Игнорируется в розничных сборках.</span><span class="sxs-lookup"><span data-stu-id="e93a9-106">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="e93a9-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e93a9-107">Syntax</span></span>


```C++
void DbgOutString(
   LPCTSTR psz
);
```



## <a name="parameters"></a><span data-ttu-id="e93a9-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e93a9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e93a9-109">*псз*</span><span class="sxs-lookup"><span data-stu-id="e93a9-109">*psz*</span></span> 
</dt> <dd>

<span data-ttu-id="e93a9-110">Строка для вывода.</span><span class="sxs-lookup"><span data-stu-id="e93a9-110">String to output.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e93a9-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e93a9-111">Return value</span></span>

<span data-ttu-id="e93a9-112">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="e93a9-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e93a9-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e93a9-113">Remarks</span></span>

<span data-ttu-id="e93a9-114">В отладочных сборках эта функция всегда выводит строку, независимо от текущих уровней выходных данных отладки.</span><span class="sxs-lookup"><span data-stu-id="e93a9-114">In debug builds, this function always outputs the string, regardless of the current debug output levels.</span></span> <span data-ttu-id="e93a9-115">Для более точного управления выходными данными используйте макрос [**дбглог**](dbglog.md) .</span><span class="sxs-lookup"><span data-stu-id="e93a9-115">For finer control over the output, use the [**DbgLog**](dbglog.md) macro.</span></span>

## <a name="examples"></a><span data-ttu-id="e93a9-116">Примеры</span><span class="sxs-lookup"><span data-stu-id="e93a9-116">Examples</span></span>


```C++
DbgOutString("Creating the filter graph...\n"); 
```



## <a name="requirements"></a><span data-ttu-id="e93a9-117">Требования</span><span class="sxs-lookup"><span data-stu-id="e93a9-117">Requirements</span></span>



| <span data-ttu-id="e93a9-118">Требование</span><span class="sxs-lookup"><span data-stu-id="e93a9-118">Requirement</span></span> | <span data-ttu-id="e93a9-119">Значение</span><span class="sxs-lookup"><span data-stu-id="e93a9-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e93a9-120">Header</span><span class="sxs-lookup"><span data-stu-id="e93a9-120">Header</span></span><br/>  | <dl> <span data-ttu-id="e93a9-121"><dt>Вксдебуг. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e93a9-121"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e93a9-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e93a9-122">Library</span></span><br/> | <dl> <span data-ttu-id="e93a9-123"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="e93a9-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e93a9-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e93a9-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e93a9-125">Выходные функции отладки</span><span class="sxs-lookup"><span data-stu-id="e93a9-125">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 




