---
title: Функция Аллоккаунтедстринг (Напутил. h)
description: Выделяет память для строки, завершающейся нулем, и возвращает ее в структуре Каунтедстринг.
ms.assetid: 6dd503bf-8853-499b-adcd-54de696f01d6
keywords:
- Аллоккаунтедстринг функция NAP
topic_type:
- apiref
api_name:
- AllocCountedString
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ab2980ce5eefdd7743907bdcc947cdce1c74823
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672491"
---
# <a name="alloccountedstring-function"></a><span data-ttu-id="7b858-104">Функция Аллоккаунтедстринг</span><span class="sxs-lookup"><span data-stu-id="7b858-104">AllocCountedString function</span></span>

> [!Note]  
> <span data-ttu-id="7b858-105">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="7b858-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="7b858-106">Функция **аллоккаунтедстринг** выделяет память для строки, завершающейся нулем, и возвращает ее в структуре [**каунтедстринг**](/windows/win32/api/naptypes/ns-naptypes-countedstring) .</span><span class="sxs-lookup"><span data-stu-id="7b858-106">The **AllocCountedString** function allocates memory for a null-terminated string and returns it in a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b858-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7b858-107">Syntax</span></span>


```C++
NAPAPI HRESULT WINAPI AllocCountedString(
  _Inout_       CountedString **countedString,
  _In_    const WCHAR         *string
);
```



## <a name="parameters"></a><span data-ttu-id="7b858-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7b858-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b858-109">*каунтедстринг* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="7b858-109">*countedString* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7b858-110">Указатель на адрес вновь выделенной структуры [**каунтедстринг**](/windows/win32/api/naptypes/ns-naptypes-countedstring) .</span><span class="sxs-lookup"><span data-stu-id="7b858-110">A pointer to the address of a newly allocated [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) structure.</span></span>

</dd> <dt>

<span data-ttu-id="7b858-111">*строка* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7b858-111">*string* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b858-112">Указатель на строку, завершающуюся нулем и возвращаемую в *каунтедстринг*.</span><span class="sxs-lookup"><span data-stu-id="7b858-112">A pointer to the null-terminated string that is to be returned in *countedString*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b858-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7b858-113">Return value</span></span>



| <span data-ttu-id="7b858-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="7b858-114">Return code</span></span>                                                                                   | <span data-ttu-id="7b858-115">Описание</span><span class="sxs-lookup"><span data-stu-id="7b858-115">Description</span></span>                                                                |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7b858-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="7b858-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="7b858-117">Операция успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="7b858-117">The operation has completed successfully.</span></span><br/>                       |
| <dl> <span data-ttu-id="7b858-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="7b858-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="7b858-119">Передан недопустимый аргумент.</span><span class="sxs-lookup"><span data-stu-id="7b858-119">An invalid argument was passed.</span></span><br/>                                 |
| <dl> <span data-ttu-id="7b858-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="7b858-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="7b858-121">В системе исчерпана виртуальная память.</span><span class="sxs-lookup"><span data-stu-id="7b858-121">The system is out of virtual memory.</span></span> <span data-ttu-id="7b858-122">Не удалось выполнить операцию.</span><span class="sxs-lookup"><span data-stu-id="7b858-122">This operation has failed.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7b858-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7b858-123">Remarks</span></span>

<span data-ttu-id="7b858-124">Все COM-интерфейсы, поддерживаемые системой защиты доступа к сети, используют стандартные правила управления памятью COM и распределителя памяти COM (**CoTaskMemAlloc** и **CoTaskMemFree**):</span><span class="sxs-lookup"><span data-stu-id="7b858-124">All the COM interfaces supported by the NAP system use standard COM memory management rules and the COM memory allocators (**CoTaskMemAlloc** and **CoTaskMemFree**):</span></span>

-   <span data-ttu-id="7b858-125">**Входные** параметры выделяются и освобождаются вызывающей стороной.</span><span class="sxs-lookup"><span data-stu-id="7b858-125">**In** parameters are allocated and freed by the caller.</span></span>
-   <span data-ttu-id="7b858-126">**Выходные** параметры выделяются вызываемым методом и освобождаются вызывающей стороной с помощью **котаскмем**.</span><span class="sxs-lookup"><span data-stu-id="7b858-126">**Out** parameters are allocated by the callee and freed by the caller using **CoTaskMem**.</span></span>
-   <span data-ttu-id="7b858-127">**Входные и выходные** параметры выделяются вызывающим объектом, освобождаются и перераспределяются вызываемым объектом, и в итоге освобождаются вызывающей стороной с помощью **котаскмем**.</span><span class="sxs-lookup"><span data-stu-id="7b858-127">**In/out** parameters are allocated by the caller, freed and reallocated by the callee, and ultimately freed by the caller, using **CoTaskMem**.</span></span>

<span data-ttu-id="7b858-128">Все функции NAP для освобождения памяти также освобождают все внедренные указатели.</span><span class="sxs-lookup"><span data-stu-id="7b858-128">All NAP functions for freeing memory also free all embedded pointers.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b858-129">Требования</span><span class="sxs-lookup"><span data-stu-id="7b858-129">Requirements</span></span>



| <span data-ttu-id="7b858-130">Требование</span><span class="sxs-lookup"><span data-stu-id="7b858-130">Requirement</span></span> | <span data-ttu-id="7b858-131">Значение</span><span class="sxs-lookup"><span data-stu-id="7b858-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7b858-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7b858-132">Minimum supported client</span></span><br/> | <span data-ttu-id="7b858-133">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7b858-133">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="7b858-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7b858-134">Minimum supported server</span></span><br/> | <span data-ttu-id="7b858-135">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7b858-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="7b858-136">Header</span><span class="sxs-lookup"><span data-stu-id="7b858-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b858-137"><dt>Напутил. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b858-137"><dt>NapUtil.h</dt></span></span> </dl> |
| <span data-ttu-id="7b858-138">DLL</span><span class="sxs-lookup"><span data-stu-id="7b858-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b858-139"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b858-139"><dt>Qutil.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b858-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7b858-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b858-141">**фрикаунтедстринг**</span><span class="sxs-lookup"><span data-stu-id="7b858-141">**FreeCountedString**</span></span>](freecountedstring-func.md)
</dt> </dl>

 

 





