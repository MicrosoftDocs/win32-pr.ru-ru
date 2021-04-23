---
description: Функция Дбгинитиалисе инициализирует библиотеку отладки. Игнорируется в розничных сборках.
ms.assetid: d4ca739e-cd39-4692-81da-c5a88a09d546
title: Функция Дбгинитиалисе (Вксдебуг. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgInitialise
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 33a62c8dad7ef6e15b9b11461303b1bced977a96
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675403"
---
# <a name="dbginitialise-function"></a><span data-ttu-id="37ac2-104">Функция Дбгинитиалисе</span><span class="sxs-lookup"><span data-stu-id="37ac2-104">DbgInitialise function</span></span>

<span data-ttu-id="37ac2-105">Функция **дбгинитиалисе** инициализирует библиотеку отладки.</span><span class="sxs-lookup"><span data-stu-id="37ac2-105">The **DbgInitialise** function initializes the debug library.</span></span> <span data-ttu-id="37ac2-106">Игнорируется в розничных сборках.</span><span class="sxs-lookup"><span data-stu-id="37ac2-106">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="37ac2-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="37ac2-107">Syntax</span></span>


```C++
void DbgInitialise(
   HINSTANCE hInst
);
```



## <a name="parameters"></a><span data-ttu-id="37ac2-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="37ac2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37ac2-109">*хинст*</span><span class="sxs-lookup"><span data-stu-id="37ac2-109">*hInst*</span></span> 
</dt> <dd>

<span data-ttu-id="37ac2-110">Обработчик для экземпляра модуля.</span><span class="sxs-lookup"><span data-stu-id="37ac2-110">Handle to the module instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37ac2-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="37ac2-111">Return value</span></span>

<span data-ttu-id="37ac2-112">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="37ac2-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="37ac2-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="37ac2-113">Remarks</span></span>

<span data-ttu-id="37ac2-114">В исполняемом файле вызовите этот метод перед использованием средств отладки DirectShow.</span><span class="sxs-lookup"><span data-stu-id="37ac2-114">In an executable, call this method before using the DirectShow debug facilities.</span></span> <span data-ttu-id="37ac2-115">Перед завершением работы исполняемого файла вызовите функцию [**дбгтерминате**](dbgterminate.md) для очистки отладочной библиотеки.</span><span class="sxs-lookup"><span data-stu-id="37ac2-115">Before the executable quits, call the [**DbgTerminate**](dbgterminate.md) function to clean up the debug library.</span></span>

<span data-ttu-id="37ac2-116">В библиотеке DLL, которая ссылается на библиотеку базового класса (Стрмбасе. lib), нет необходимости вызывать эту функцию.</span><span class="sxs-lookup"><span data-stu-id="37ac2-116">In a DLL that links to the base-class library (Strmbase.lib), it is not necessary to call this function.</span></span> <span data-ttu-id="37ac2-117">Функция вызывается автоматически при загрузке библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="37ac2-117">The function is called automatically when the DLL is loaded.</span></span>

## <a name="requirements"></a><span data-ttu-id="37ac2-118">Требования</span><span class="sxs-lookup"><span data-stu-id="37ac2-118">Requirements</span></span>



| <span data-ttu-id="37ac2-119">Требование</span><span class="sxs-lookup"><span data-stu-id="37ac2-119">Requirement</span></span> | <span data-ttu-id="37ac2-120">Значение</span><span class="sxs-lookup"><span data-stu-id="37ac2-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37ac2-121">Header</span><span class="sxs-lookup"><span data-stu-id="37ac2-121">Header</span></span><br/>  | <dl> <span data-ttu-id="37ac2-122"><dt>Вксдебуг. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="37ac2-122"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="37ac2-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="37ac2-123">Library</span></span><br/> | <dl> <span data-ttu-id="37ac2-124"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="37ac2-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37ac2-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="37ac2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37ac2-126">Выходные функции отладки</span><span class="sxs-lookup"><span data-stu-id="37ac2-126">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 




