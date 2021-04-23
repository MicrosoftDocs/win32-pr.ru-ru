---
description: Функция Бержетинтежер декодирует целое число ЛИЧЕСТВО в кодировке.
ms.assetid: 1ab0dcec-05cf-4322-a44e-28aa9131495a
title: Функция Бержетинтежер (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BERGetInteger
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: c89cd5e3f4e4eb35157936f990939154f23966d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911644"
---
# <a name="bergetinteger-function"></a><span data-ttu-id="c01f8-103">Функция Бержетинтежер</span><span class="sxs-lookup"><span data-stu-id="c01f8-103">BERGetInteger function</span></span>

<span data-ttu-id="c01f8-104">Функция **бержетинтежер** декодирует целое число личество в кодировке.</span><span class="sxs-lookup"><span data-stu-id="c01f8-104">The **BERGetInteger** function decodes a BER-encoded integer.</span></span>

## <a name="syntax"></a><span data-ttu-id="c01f8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c01f8-105">Syntax</span></span>


```C++
BOOL BERGetInteger(
   LPBYTE  pCurrentPointer,
   LPBYTE  *ppValuePointer,
   LPDWORD pHeaderLength,
   LPDWORD pDataLength,
   LPBYTE  *ppNext
);
```



## <a name="parameters"></a><span data-ttu-id="c01f8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c01f8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c01f8-107">*пкуррентпоинтер*</span><span class="sxs-lookup"><span data-stu-id="c01f8-107">*pCurrentPointer*</span></span> 
</dt> <dd>

<span data-ttu-id="c01f8-108">Указатель на декодированное целое число.</span><span class="sxs-lookup"><span data-stu-id="c01f8-108">Pointer to the integer that is decoded.</span></span>

</dd> <dt>

<span data-ttu-id="c01f8-109">*ппвалуепоинтер*</span><span class="sxs-lookup"><span data-stu-id="c01f8-109">*ppValuePointer*</span></span> 
</dt> <dd>

<span data-ttu-id="c01f8-110">Указатель на возвращаемое значение указателя.</span><span class="sxs-lookup"><span data-stu-id="c01f8-110">Pointer to the pointer to returned value.</span></span>

</dd> <dt>

<span data-ttu-id="c01f8-111">*феадерленгс*</span><span class="sxs-lookup"><span data-stu-id="c01f8-111">*pHeaderLength*</span></span> 
</dt> <dd>

<span data-ttu-id="c01f8-112">Указатель на возвращаемую длину заголовка.</span><span class="sxs-lookup"><span data-stu-id="c01f8-112">Pointer to the returned header length.</span></span>

</dd> <dt>

<span data-ttu-id="c01f8-113">*пдаталенгс*</span><span class="sxs-lookup"><span data-stu-id="c01f8-113">*pDataLength*</span></span> 
</dt> <dd>

<span data-ttu-id="c01f8-114">Указатель на длину данных.</span><span class="sxs-lookup"><span data-stu-id="c01f8-114">Pointer to the data length.</span></span>

</dd> <dt>

<span data-ttu-id="c01f8-115">*ппнекст*</span><span class="sxs-lookup"><span data-stu-id="c01f8-115">*ppNext*</span></span> 
</dt> <dd>

<span data-ttu-id="c01f8-116">Указатель на указатель на следующую запись ЛИЧЕСТВО.</span><span class="sxs-lookup"><span data-stu-id="c01f8-116">Pointer to the pointer to the next BER entry.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c01f8-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c01f8-117">Return value</span></span>

<span data-ttu-id="c01f8-118">Если функция выполнена успешно (то есть при обнаружении и преобразовании допустимого целого числа в кодировке ЛИЧЕСТВО), возвращается значение **true**.</span><span class="sxs-lookup"><span data-stu-id="c01f8-118">If the function is successful (that is, if a valid BER encoded integer is found and converted), the return value is **TRUE**.</span></span>

<span data-ttu-id="c01f8-119">Если функция завершилась неудачно, возвращается значение **false**.</span><span class="sxs-lookup"><span data-stu-id="c01f8-119">If function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="c01f8-120">Требования</span><span class="sxs-lookup"><span data-stu-id="c01f8-120">Requirements</span></span>



| <span data-ttu-id="c01f8-121">Требование</span><span class="sxs-lookup"><span data-stu-id="c01f8-121">Requirement</span></span> | <span data-ttu-id="c01f8-122">Значение</span><span class="sxs-lookup"><span data-stu-id="c01f8-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c01f8-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c01f8-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c01f8-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c01f8-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="c01f8-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c01f8-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c01f8-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c01f8-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c01f8-127">Заголовок</span><span class="sxs-lookup"><span data-stu-id="c01f8-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="c01f8-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="c01f8-128"><dt>Netmon.h</dt></span></span> </dl>   |
| <span data-ttu-id="c01f8-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c01f8-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="c01f8-130"><dt>Parser. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c01f8-130"><dt>Parser.lib</dt></span></span> </dl> |
| <span data-ttu-id="c01f8-131">DLL</span><span class="sxs-lookup"><span data-stu-id="c01f8-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c01f8-132"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c01f8-132"><dt>Nmapi.dll</dt></span></span> </dl>  |



 

 




