---
description: Функция "интерфейс" получает указатель интерфейса.
ms.assetid: 75fe8849-c779-4d47-a5ff-5a23308c8a21
title: Функция-интерфейс (Комбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetInterface
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 317f08af2a4ff0e9410c61da8b19d14735a14f6c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679583"
---
# <a name="getinterface-function"></a><span data-ttu-id="db2d2-103">Функция "интерфейс</span><span class="sxs-lookup"><span data-stu-id="db2d2-103">GetInterface function</span></span>

<span data-ttu-id="db2d2-104">`GetInterface`Функция получает указатель интерфейса.</span><span class="sxs-lookup"><span data-stu-id="db2d2-104">The `GetInterface` function retrieves an interface pointer.</span></span>

## <a name="syntax"></a><span data-ttu-id="db2d2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="db2d2-105">Syntax</span></span>


```C++
HRESULT GetInterface(
   LPUNKNOWN pUnk,
   void      **ppv
);
```



## <a name="parameters"></a><span data-ttu-id="db2d2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="db2d2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db2d2-107">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="db2d2-107">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="db2d2-108">Указатель на интерфейс **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="db2d2-108">Pointer to the **IUnknown** interface.</span></span>

</dd> <dt>

<span data-ttu-id="db2d2-109">*ппв*</span><span class="sxs-lookup"><span data-stu-id="db2d2-109">*ppv*</span></span> 
</dt> <dd>

<span data-ttu-id="db2d2-110">Адрес указателя на полученный интерфейс.</span><span class="sxs-lookup"><span data-stu-id="db2d2-110">Address of a pointer to the retrieved interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db2d2-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="db2d2-111">Return value</span></span>

<span data-ttu-id="db2d2-112">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="db2d2-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="db2d2-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="db2d2-113">Remarks</span></span>

<span data-ttu-id="db2d2-114">Эта функция-член выполняет поточно-ориентированное приращение счетчика ссылок.</span><span class="sxs-lookup"><span data-stu-id="db2d2-114">This member function performs a thread-safe increment of the reference count.</span></span> <span data-ttu-id="db2d2-115">Чтобы получить интерфейс и добавить ссылку, вызовите эту функцию из переопределяющей реализации метода **инонделегатингункновн:: нонделегатингкуеринтерфаце** .</span><span class="sxs-lookup"><span data-stu-id="db2d2-115">To retrieve the interface and add a reference, call this function from your overriding implementation of the **INonDelegatingUnknown::NonDelegatingQueryInterface** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="db2d2-116">Требования</span><span class="sxs-lookup"><span data-stu-id="db2d2-116">Requirements</span></span>



| <span data-ttu-id="db2d2-117">Требование</span><span class="sxs-lookup"><span data-stu-id="db2d2-117">Requirement</span></span> | <span data-ttu-id="db2d2-118">Значение</span><span class="sxs-lookup"><span data-stu-id="db2d2-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db2d2-119">Header</span><span class="sxs-lookup"><span data-stu-id="db2d2-119">Header</span></span><br/>  | <dl> <span data-ttu-id="db2d2-120"><dt>Комбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="db2d2-120"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="db2d2-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="db2d2-121">Library</span></span><br/> | <dl> <span data-ttu-id="db2d2-122"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="db2d2-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db2d2-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="db2d2-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db2d2-124">**Вспомогательные функции COM**</span><span class="sxs-lookup"><span data-stu-id="db2d2-124">**COM Helper Functions**</span></span>](com-helper-functions.md)
</dt> <dt>

[<span data-ttu-id="db2d2-125">**инонделегатингункновн**</span><span class="sxs-lookup"><span data-stu-id="db2d2-125">**INonDelegatingUnknown**</span></span>](inondelegatingunknown.md)
</dt> </dl>

 

 




