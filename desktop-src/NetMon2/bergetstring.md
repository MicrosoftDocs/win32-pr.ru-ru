---
description: Функция Бержетстринг декодирует строку в кодировке ЛИЧЕСТВО.
ms.assetid: 1f72f061-c0ed-4634-9709-e08c2b9468bb
title: Функция Бержетстринг (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BERGetString
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 6f8f864b8042ad49502ae53061e157575192e7bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909423"
---
# <a name="bergetstring-function"></a><span data-ttu-id="9487d-103">Функция Бержетстринг</span><span class="sxs-lookup"><span data-stu-id="9487d-103">BERGetString function</span></span>

<span data-ttu-id="9487d-104">Функция **бержетстринг** декодирует строку в кодировке личество.</span><span class="sxs-lookup"><span data-stu-id="9487d-104">The **BERGetString** function decodes a BER-encoded string.</span></span>

## <a name="syntax"></a><span data-ttu-id="9487d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9487d-105">Syntax</span></span>


```C++
BOOL BERGetString(
   LPBYTE  pCurrentPointer,
   LPBYTE  *ppValuePointer,
   LPDWORD pHeaderLength,
   LPDWORD pDataLength,
   LPBYTE  *ppNext
);
```



## <a name="parameters"></a><span data-ttu-id="9487d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9487d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9487d-107">*пкуррентпоинтер*</span><span class="sxs-lookup"><span data-stu-id="9487d-107">*pCurrentPointer*</span></span> 
</dt> <dd>

<span data-ttu-id="9487d-108">Указатель на декодированную строку.</span><span class="sxs-lookup"><span data-stu-id="9487d-108">Pointer to the string that is decoded.</span></span>

</dd> <dt>

<span data-ttu-id="9487d-109">*ппвалуепоинтер*</span><span class="sxs-lookup"><span data-stu-id="9487d-109">*ppValuePointer*</span></span> 
</dt> <dd>

<span data-ttu-id="9487d-110">Указатель на указатель декодированной строки.</span><span class="sxs-lookup"><span data-stu-id="9487d-110">Pointer to the pointer of the decoded string.</span></span>

</dd> <dt>

<span data-ttu-id="9487d-111">*феадерленгс*</span><span class="sxs-lookup"><span data-stu-id="9487d-111">*pHeaderLength*</span></span> 
</dt> <dd>

<span data-ttu-id="9487d-112">Указатель на возвращаемую длину заголовка.</span><span class="sxs-lookup"><span data-stu-id="9487d-112">Pointer to the returned header length.</span></span>

</dd> <dt>

<span data-ttu-id="9487d-113">*пдаталенгс*</span><span class="sxs-lookup"><span data-stu-id="9487d-113">*pDataLength*</span></span> 
</dt> <dd>

<span data-ttu-id="9487d-114">Указатель на длину строки.</span><span class="sxs-lookup"><span data-stu-id="9487d-114">Pointer to the string length.</span></span>

</dd> <dt>

<span data-ttu-id="9487d-115">*ппнекст*</span><span class="sxs-lookup"><span data-stu-id="9487d-115">*ppNext*</span></span> 
</dt> <dd>

<span data-ttu-id="9487d-116">Указатель на указатель следующей записи ЛИЧЕСТВО.</span><span class="sxs-lookup"><span data-stu-id="9487d-116">Pointer to the pointer of the next BER entry.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9487d-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9487d-117">Return value</span></span>

<span data-ttu-id="9487d-118">Если функция выполнена успешно (то есть при декодировании допустимой строки с ЛИЧЕСТВО кодировкой), возвращается значение **true**.</span><span class="sxs-lookup"><span data-stu-id="9487d-118">If the function is successful (that is, if a valid BER-encoded string is decoded), the return value is **TRUE**.</span></span>

<span data-ttu-id="9487d-119">Если функция завершилась неудачно, возвращается значение **false**.</span><span class="sxs-lookup"><span data-stu-id="9487d-119">If function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="9487d-120">Требования</span><span class="sxs-lookup"><span data-stu-id="9487d-120">Requirements</span></span>



| <span data-ttu-id="9487d-121">Требование</span><span class="sxs-lookup"><span data-stu-id="9487d-121">Requirement</span></span> | <span data-ttu-id="9487d-122">Значение</span><span class="sxs-lookup"><span data-stu-id="9487d-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9487d-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9487d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="9487d-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9487d-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="9487d-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9487d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="9487d-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9487d-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9487d-127">Заголовок</span><span class="sxs-lookup"><span data-stu-id="9487d-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="9487d-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="9487d-128"><dt>Netmon.h</dt></span></span> </dl>   |
| <span data-ttu-id="9487d-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9487d-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="9487d-130"><dt>Parser. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9487d-130"><dt>Parser.lib</dt></span></span> </dl> |
| <span data-ttu-id="9487d-131">DLL</span><span class="sxs-lookup"><span data-stu-id="9487d-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9487d-132"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9487d-132"><dt>Nmapi.dll</dt></span></span> </dl>  |



 

 




