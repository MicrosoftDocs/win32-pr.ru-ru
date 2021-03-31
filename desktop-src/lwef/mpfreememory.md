---
title: Функция Мпфримемори (Мпклиент. h)
description: Освобождает память для диспетчера защиты от вредоносных программ.
ms.assetid: D0B43AE5-756F-4E86-B8A5-8268A41901BC
keywords:
- Функции Мпфримемори устаревшие функции среды Windows
topic_type:
- apiref
api_name:
- MpFreeMemory
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a15a2845b034a3aa739b1ba2f33a023b742b4b22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801907"
---
# <a name="mpfreememory-function"></a><span data-ttu-id="3a741-104">Функция Мпфримемори</span><span class="sxs-lookup"><span data-stu-id="3a741-104">MpFreeMemory function</span></span>

<span data-ttu-id="3a741-105">Освобождает память для диспетчера защиты от вредоносных программ.</span><span class="sxs-lookup"><span data-stu-id="3a741-105">Frees memory for the malware protection manager.</span></span> <span data-ttu-id="3a741-106">Все буферы, выделенные и возвращаемые функциями защиты от вредоносных программ, должны быть освобождены вызывающей стороной с помощью этой функции.</span><span class="sxs-lookup"><span data-stu-id="3a741-106">All buffers allocated and returned by malware protection functions must be freed by the caller using this function.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a741-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3a741-107">Syntax</span></span>


```C++
void WINAPI MpFreeMemory(
  _In_ PVOID pMemory
);
```



## <a name="parameters"></a><span data-ttu-id="3a741-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="3a741-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a741-109">*пмемори* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3a741-109">*pMemory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a741-110">Тип: **PVOID**</span><span class="sxs-lookup"><span data-stu-id="3a741-110">Type: **PVOID**</span></span>

<span data-ttu-id="3a741-111">Указатель на память, выделенную функцией защиты от вредоносных программ.</span><span class="sxs-lookup"><span data-stu-id="3a741-111">A pointer to memory allocated by a malware protection function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a741-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3a741-112">Return value</span></span>

<span data-ttu-id="3a741-113">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="3a741-113">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a741-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3a741-114">Remarks</span></span>

<span data-ttu-id="3a741-115">Чтобы упростить управление памятью для клиентов, диспетчер защиты от вредоносных программ также определяет макросы для освобождения памяти, связанной с различными структурами, возвращаемыми функциями защиты от вредоносных программ.</span><span class="sxs-lookup"><span data-stu-id="3a741-115">To facilitate memory management for clients, the malware protection manager also defines macros to free memory associated with various structures returned by malware protection functions.</span></span> <span data-ttu-id="3a741-116">В файле заголовка мпмемфри. h определены следующие макросы:</span><span class="sxs-lookup"><span data-stu-id="3a741-116">The following macros are defined in the header file mpmemfree.h:</span></span>



| <span data-ttu-id="3a741-117">Имя</span><span class="sxs-lookup"><span data-stu-id="3a741-117">Name</span></span>                            | <span data-ttu-id="3a741-118">Описание</span><span class="sxs-lookup"><span data-stu-id="3a741-118">Description</span></span>                                                                      |
|---------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="3a741-119">\_Бесплатная информация о мпресаурце \_</span><span class="sxs-lookup"><span data-stu-id="3a741-119">MPRESOURCE\_INFO\_FREE</span></span>          | <span data-ttu-id="3a741-120">Освобождает выделенные [**\_ сведения о мпресаурце**](mpresource-info.md).</span><span class="sxs-lookup"><span data-stu-id="3a741-120">Frees an allocated [**MPRESOURCE\_INFO**](mpresource-info.md).</span></span>                  |
| <span data-ttu-id="3a741-121">\_Бесплатная информация о мпсреат \_</span><span class="sxs-lookup"><span data-stu-id="3a741-121">MPTHREAT\_INFO\_FREE</span></span>            | <span data-ttu-id="3a741-122">Освобождает выделенные [**\_ сведения о мпсреат**](mpthreat-info.md).</span><span class="sxs-lookup"><span data-stu-id="3a741-122">Frees an allocated [**MPTHREAT\_INFO**](mpthreat-info.md).</span></span>                      |
| <span data-ttu-id="3a741-123">\_Бесплатные локализованные \_ сведения мпсреат \_</span><span class="sxs-lookup"><span data-stu-id="3a741-123">MPTHREAT\_LOCALIZED\_INFO\_FREE</span></span> | <span data-ttu-id="3a741-124">Освобождает выделенные [**\_ локализованные \_ сведения мпсреат**](mpthreat-localized-info.md).</span><span class="sxs-lookup"><span data-stu-id="3a741-124">Frees an allocated [**MPTHREAT\_LOCALIZED\_INFO**](mpthreat-localized-info.md).</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="3a741-125">Требования</span><span class="sxs-lookup"><span data-stu-id="3a741-125">Requirements</span></span>



| <span data-ttu-id="3a741-126">Требование</span><span class="sxs-lookup"><span data-stu-id="3a741-126">Requirement</span></span> | <span data-ttu-id="3a741-127">Значение</span><span class="sxs-lookup"><span data-stu-id="3a741-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3a741-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3a741-128">Minimum supported client</span></span><br/> | <span data-ttu-id="3a741-129">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="3a741-129">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="3a741-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3a741-130">Minimum supported server</span></span><br/> | <span data-ttu-id="3a741-131">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="3a741-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3a741-132">Header</span><span class="sxs-lookup"><span data-stu-id="3a741-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a741-133"><dt>Мпклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a741-133"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="3a741-134">DLL</span><span class="sxs-lookup"><span data-stu-id="3a741-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a741-135"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3a741-135"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a741-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3a741-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a741-137">**мперрормессажеформат**</span><span class="sxs-lookup"><span data-stu-id="3a741-137">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="3a741-138">**\_сведения о мпресаурце**</span><span class="sxs-lookup"><span data-stu-id="3a741-138">**MPRESOURCE\_INFO**</span></span>](mpresource-info.md)
</dt> <dt>

[<span data-ttu-id="3a741-139">**\_сведения о мпсреат**</span><span class="sxs-lookup"><span data-stu-id="3a741-139">**MPTHREAT\_INFO**</span></span>](mpthreat-info.md)
</dt> <dt>

[<span data-ttu-id="3a741-140">**\_локализованные \_ сведения мпсреат**</span><span class="sxs-lookup"><span data-stu-id="3a741-140">**MPTHREAT\_LOCALIZED\_INFO**</span></span>](mpthreat-localized-info.md)
</dt> </dl>

 

 





