---
description: Функция Бержесеадер декодирует заголовок Choice.
ms.assetid: 2574a9b3-c28e-43d1-904f-d45888617584
title: Функция Бержесеадер (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BERGetHeader
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 5e2213b15b6b4d2cbaa15b3b9aa9de028e20a62d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673645"
---
# <a name="bergetheader-function"></a><span data-ttu-id="85770-103">Функция Бержесеадер</span><span class="sxs-lookup"><span data-stu-id="85770-103">BERGetHeader function</span></span>

<span data-ttu-id="85770-104">Функция **бержесеадер** декодирует заголовок Choice.</span><span class="sxs-lookup"><span data-stu-id="85770-104">The **BERGetHeader** function decodes a choice header.</span></span>

## <a name="syntax"></a><span data-ttu-id="85770-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="85770-105">Syntax</span></span>


```C++
BOOL BERGetHeader(
   LPBYTE  pCurrentPointer,
   LPBYTE  pTag,
   LPDWORD pHeaderLength,
   LPDWORD pDataLength,
   LPBYTE  *ppNext
);
```



## <a name="parameters"></a><span data-ttu-id="85770-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="85770-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85770-107">*пкуррентпоинтер*</span><span class="sxs-lookup"><span data-stu-id="85770-107">*pCurrentPointer*</span></span> 
</dt> <dd>

<span data-ttu-id="85770-108">Указатель на заголовок Choice.</span><span class="sxs-lookup"><span data-stu-id="85770-108">Pointer to the choice header.</span></span>

</dd> <dt>

<span data-ttu-id="85770-109">*птаг*</span><span class="sxs-lookup"><span data-stu-id="85770-109">*pTag*</span></span> 
</dt> <dd>

<span data-ttu-id="85770-110">Указатель на возвращаемый тег.</span><span class="sxs-lookup"><span data-stu-id="85770-110">Pointer to the returned tag.</span></span>

</dd> <dt>

<span data-ttu-id="85770-111">*феадерленгс*</span><span class="sxs-lookup"><span data-stu-id="85770-111">*pHeaderLength*</span></span> 
</dt> <dd>

<span data-ttu-id="85770-112">Указатель на возвращаемую длину заголовка.</span><span class="sxs-lookup"><span data-stu-id="85770-112">Pointer to the returned header length.</span></span>

</dd> <dt>

<span data-ttu-id="85770-113">*пдаталенгс*</span><span class="sxs-lookup"><span data-stu-id="85770-113">*pDataLength*</span></span> 
</dt> <dd>

<span data-ttu-id="85770-114">Указатель на возвращаемую длину данных.</span><span class="sxs-lookup"><span data-stu-id="85770-114">Pointer to the returned data length.</span></span>

</dd> <dt>

<span data-ttu-id="85770-115">*ппнекст*</span><span class="sxs-lookup"><span data-stu-id="85770-115">*ppNext*</span></span> 
</dt> <dd>

<span data-ttu-id="85770-116">Указатель на содержимое заголовка.</span><span class="sxs-lookup"><span data-stu-id="85770-116">Pointer to the header contents.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85770-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="85770-117">Return value</span></span>

<span data-ttu-id="85770-118">Если функция выполнена успешно (то есть найден допустимый заголовок выбора ЛИЧЕСТВО), возвращается значение **true**.</span><span class="sxs-lookup"><span data-stu-id="85770-118">If the function is successful (that is, a valid BER choice header is found) the return value is **TRUE**.</span></span>

<span data-ttu-id="85770-119">Если функция завершается неудачно, возвращается значение **false**.</span><span class="sxs-lookup"><span data-stu-id="85770-119">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="85770-120">Требования</span><span class="sxs-lookup"><span data-stu-id="85770-120">Requirements</span></span>



| <span data-ttu-id="85770-121">Требование</span><span class="sxs-lookup"><span data-stu-id="85770-121">Requirement</span></span> | <span data-ttu-id="85770-122">Значение</span><span class="sxs-lookup"><span data-stu-id="85770-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="85770-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="85770-123">Minimum supported client</span></span><br/> | <span data-ttu-id="85770-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="85770-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="85770-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="85770-125">Minimum supported server</span></span><br/> | <span data-ttu-id="85770-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="85770-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="85770-127">Заголовок</span><span class="sxs-lookup"><span data-stu-id="85770-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="85770-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="85770-128"><dt>Netmon.h</dt></span></span> </dl>   |
| <span data-ttu-id="85770-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="85770-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="85770-130"><dt>Parser. lib</dt></span><span class="sxs-lookup"><span data-stu-id="85770-130"><dt>Parser.lib</dt></span></span> </dl> |
| <span data-ttu-id="85770-131">DLL</span><span class="sxs-lookup"><span data-stu-id="85770-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="85770-132"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="85770-132"><dt>Nmapi.dll</dt></span></span> </dl>  |



 

 




