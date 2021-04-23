---
description: 'Извлекает указатель интерфейса и увеличивает счетчик ссылок. Этот метод реализует метод Инонделегатингункновн:: Нонделегатингкуеринтерфаце.'
ms.assetid: 451ca350-f40b-4cbf-ac39-e86dadb48a24
title: Кункновн. Нонделегатингкуеринтерфаце, метод (Комбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CUnknown.NonDelegatingQueryInterface
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b41810eb52db38644bda472907228cd812f76f6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679693"
---
# <a name="cunknownnondelegatingqueryinterface-method"></a><span data-ttu-id="c5a53-104">Кункновн. Нонделегатингкуеринтерфаце, метод</span><span class="sxs-lookup"><span data-stu-id="c5a53-104">CUnknown.NonDelegatingQueryInterface method</span></span>

<span data-ttu-id="c5a53-105">Извлекает указатель интерфейса и увеличивает счетчик ссылок.</span><span class="sxs-lookup"><span data-stu-id="c5a53-105">Retrieves an interface pointer and increments the reference count.</span></span> <span data-ttu-id="c5a53-106">Этот метод реализует метод **инонделегатингункновн:: нонделегатингкуеринтерфаце** .</span><span class="sxs-lookup"><span data-stu-id="c5a53-106">This method implements the **INonDelegatingUnknown::NonDelegatingQueryInterface** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5a53-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c5a53-107">Syntax</span></span>


```C++
HRESULT NonDelegatingQueryInterface(
   REFIID riid,
   void   **ppv
);
```



## <a name="parameters"></a><span data-ttu-id="c5a53-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c5a53-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5a53-109">*riid*</span><span class="sxs-lookup"><span data-stu-id="c5a53-109">*riid*</span></span> 
</dt> <dd>

<span data-ttu-id="c5a53-110">Идентификатор интерфейса.</span><span class="sxs-lookup"><span data-stu-id="c5a53-110">Identifier of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="c5a53-111">*ппв*</span><span class="sxs-lookup"><span data-stu-id="c5a53-111">*ppv*</span></span> 
</dt> <dd>

<span data-ttu-id="c5a53-112">Адрес указателя для получения интерфейса.</span><span class="sxs-lookup"><span data-stu-id="c5a53-112">Address of a pointer to receive the interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5a53-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c5a53-113">Return value</span></span>

<span data-ttu-id="c5a53-114">Возвращает одно из значений **HRESULT** , приведенных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="c5a53-114">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="c5a53-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="c5a53-115">Return code</span></span>                                                                                   | <span data-ttu-id="c5a53-116">Описание</span><span class="sxs-lookup"><span data-stu-id="c5a53-116">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="c5a53-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="c5a53-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="c5a53-118">Успешно.</span><span class="sxs-lookup"><span data-stu-id="c5a53-118">Success.</span></span><br/>                                |
| <dl> <span data-ttu-id="c5a53-119"><dt>**\_интерфейс E**</dt></span><span class="sxs-lookup"><span data-stu-id="c5a53-119"><dt>**E\_NOINTERFACE**</dt></span></span> </dl> | <span data-ttu-id="c5a53-120">Объект не поддерживает этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="c5a53-120">Object does not support this interface.</span></span><br/> |
| <dl> <span data-ttu-id="c5a53-121"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="c5a53-121"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="c5a53-122">**Пустой** аргумент указателя.</span><span class="sxs-lookup"><span data-stu-id="c5a53-122">**NULL** pointer argument.</span></span><br/>              |



 

## <a name="remarks"></a><span data-ttu-id="c5a53-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c5a53-123">Remarks</span></span>

<span data-ttu-id="c5a53-124">Класс **кункновн** предоставляет только интерфейс **иукновн** .</span><span class="sxs-lookup"><span data-stu-id="c5a53-124">The **CUnknown** class exposes only the **IUknown** interface.</span></span> <span data-ttu-id="c5a53-125">Переопределите этот метод, чтобы предоставить дополнительные интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="c5a53-125">Override this method to expose additional interfaces.</span></span> <span data-ttu-id="c5a53-126">Сведения о том, как переопределить этот метод, см. [в разделе Реализация IUnknown](how-to-implement-iunknown.md).</span><span class="sxs-lookup"><span data-stu-id="c5a53-126">For information on how to override this method, see [How to Implement IUnknown](how-to-implement-iunknown.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c5a53-127">Требования</span><span class="sxs-lookup"><span data-stu-id="c5a53-127">Requirements</span></span>



| <span data-ttu-id="c5a53-128">Требование</span><span class="sxs-lookup"><span data-stu-id="c5a53-128">Requirement</span></span> | <span data-ttu-id="c5a53-129">Значение</span><span class="sxs-lookup"><span data-stu-id="c5a53-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5a53-130">Header</span><span class="sxs-lookup"><span data-stu-id="c5a53-130">Header</span></span><br/>  | <dl> <span data-ttu-id="c5a53-131"><dt>Комбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c5a53-131"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c5a53-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c5a53-132">Library</span></span><br/> | <dl> <span data-ttu-id="c5a53-133"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="c5a53-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




