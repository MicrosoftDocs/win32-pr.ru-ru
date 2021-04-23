---
description: Функция Варленсмаллинттодворд преобразует однострочное целое число с переменной длиной в тип DWORD.
ms.assetid: e26dc206-ac85-4346-9fcf-93ebc8948ced
title: Функция Варленсмаллинттодворд (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- VarLenSmallIntToDword
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 4b0e2fa0813c4b384b17ea45af45f9938bcd85c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673575"
---
# <a name="varlensmallinttodword-function"></a><span data-ttu-id="3f7f3-103">Функция Варленсмаллинттодворд</span><span class="sxs-lookup"><span data-stu-id="3f7f3-103">VarLenSmallIntToDword function</span></span>

<span data-ttu-id="3f7f3-104">Функция **варленсмаллинттодворд** преобразует однострочное целое число с переменной длиной в тип **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="3f7f3-104">The **VarLenSmallIntToDword** function converts a variable-length, small integer to a **DWORD**.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f7f3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3f7f3-105">Syntax</span></span>


```C++
LPDWORD WINAPI VarLenSmallIntToDword(
   LPBYTE  pValue,
   WORD    ValueLen,
   BOOL    fIsByteswapped,
   LPDWORD lpDword
);
```



## <a name="parameters"></a><span data-ttu-id="3f7f3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3f7f3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f7f3-107">*pValue*</span><span class="sxs-lookup"><span data-stu-id="3f7f3-107">*pValue*</span></span> 
</dt> <dd>

<span data-ttu-id="3f7f3-108">Указатель на однострочное целое число с переменной длиной.</span><span class="sxs-lookup"><span data-stu-id="3f7f3-108">Pointer to the variable-length, small integer.</span></span>

</dd> <dt>

<span data-ttu-id="3f7f3-109">*валуелен*</span><span class="sxs-lookup"><span data-stu-id="3f7f3-109">*ValueLen*</span></span> 
</dt> <dd>

<span data-ttu-id="3f7f3-110">Длина (в байтах) переменной длины с малым числом.</span><span class="sxs-lookup"><span data-stu-id="3f7f3-110">Length (in bytes) of the variable-length, small integer .</span></span>

</dd> <dt>

<span data-ttu-id="3f7f3-111">*фисбитесваппед*</span><span class="sxs-lookup"><span data-stu-id="3f7f3-111">*fIsByteswapped*</span></span> 
</dt> <dd>

<span data-ttu-id="3f7f3-112">Флаг, указывающий, является ли маленькое целое число переменной длины байтовым.</span><span class="sxs-lookup"><span data-stu-id="3f7f3-112">Flag that indicates whether the variable length small integer is byte-swapped.</span></span>

</dd> <dt>

<span data-ttu-id="3f7f3-113">*лпдворд*</span><span class="sxs-lookup"><span data-stu-id="3f7f3-113">*lpDword*</span></span> 
</dt> <dd>

<span data-ttu-id="3f7f3-114">Значение **типа DWORD** , в которое преобразуется целое число.</span><span class="sxs-lookup"><span data-stu-id="3f7f3-114">The **DWORD** that the integer is converted to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f7f3-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3f7f3-115">Return value</span></span>

<span data-ttu-id="3f7f3-116">Возвращаемое значение является указателем на **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="3f7f3-116">The return value is a pointer to the **DWORD**.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f7f3-117">Требования</span><span class="sxs-lookup"><span data-stu-id="3f7f3-117">Requirements</span></span>



| <span data-ttu-id="3f7f3-118">Требование</span><span class="sxs-lookup"><span data-stu-id="3f7f3-118">Requirement</span></span> | <span data-ttu-id="3f7f3-119">Значение</span><span class="sxs-lookup"><span data-stu-id="3f7f3-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3f7f3-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3f7f3-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3f7f3-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3f7f3-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="3f7f3-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3f7f3-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3f7f3-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3f7f3-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3f7f3-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="3f7f3-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="3f7f3-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f7f3-125"><dt>Netmon.h</dt></span></span> </dl>   |
| <span data-ttu-id="3f7f3-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3f7f3-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="3f7f3-127"><dt>Parser. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3f7f3-127"><dt>Parser.lib</dt></span></span> </dl> |
| <span data-ttu-id="3f7f3-128">DLL</span><span class="sxs-lookup"><span data-stu-id="3f7f3-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3f7f3-129"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3f7f3-129"><dt>Nmapi.dll</dt></span></span> </dl>  |



 

 




