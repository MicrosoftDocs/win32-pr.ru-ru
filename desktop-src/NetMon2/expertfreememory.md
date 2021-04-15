---
description: Функция Експертфримемори освобождает память, полученную с помощью вызовов функций Експерталлокмемори и Експертреаллокмемори.
ms.assetid: 0e7cc791-98dd-4522-afab-76ac9e74c715
title: Функция Експертфримемори (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertFreeMemory
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: cc26056a3ec3e8820c363d97f92c7eb382cd0622
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662205"
---
# <a name="expertfreememory-function"></a><span data-ttu-id="b6f24-103">Функция Експертфримемори</span><span class="sxs-lookup"><span data-stu-id="b6f24-103">ExpertFreeMemory function</span></span>

<span data-ttu-id="b6f24-104">Функция **експертфримемори** освобождает память, полученную с помощью вызовов функций [**експерталлокмемори**](expertallocmemory.md) и [**експертреаллокмемори**](expertreallocmemory.md) .</span><span class="sxs-lookup"><span data-stu-id="b6f24-104">The **ExpertFreeMemory** function frees memory acquired by calls to the [**ExpertAllocMemory**](expertallocmemory.md) and [**ExpertReallocMemory**](expertreallocmemory.md) functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6f24-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b6f24-105">Syntax</span></span>


```C++
SIZE_T WINAPI ExpertFreeMemory(
       HEXPERTKEY hExpertKey,
  _In_ LPVOID     pMemory
);
```



## <a name="parameters"></a><span data-ttu-id="b6f24-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b6f24-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6f24-107">*хексперткэй*</span><span class="sxs-lookup"><span data-stu-id="b6f24-107">*hExpertKey*</span></span> 
</dt> <dd>

<span data-ttu-id="b6f24-108">Уникальный идентификатор эксперта.</span><span class="sxs-lookup"><span data-stu-id="b6f24-108">Unique expert identifier.</span></span> <span data-ttu-id="b6f24-109">Сетевой монитор передает *хексперткэй* эксперту при вызове функции [Run](run.md) .</span><span class="sxs-lookup"><span data-stu-id="b6f24-109">Network Monitor passes *hExpertKey* to the expert when it calls the [Run](run.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="b6f24-110">*пмемори* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b6f24-110">*pMemory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6f24-111">Указатель на память, выделенную сетевой монитор.</span><span class="sxs-lookup"><span data-stu-id="b6f24-111">Pointer to the memory that Network Monitor allocates.</span></span> <span data-ttu-id="b6f24-112">Указатель *пмемори* может возвращаться предыдущим вызовом [**експерталлокмемори**](expertallocmemory.md) или [**експертреаллокмемори**](expertreallocmemory.md).</span><span class="sxs-lookup"><span data-stu-id="b6f24-112">The *pMemory* pointer can be returned by a previous call to [**ExpertAllocMemory**](expertallocmemory.md) or [**ExpertReallocMemory**](expertreallocmemory.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6f24-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b6f24-113">Return value</span></span>

<span data-ttu-id="b6f24-114">Значение, если функция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="b6f24-114">If the function is successful.</span></span> <span data-ttu-id="b6f24-115">Возвращаемое значение — НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="b6f24-115">the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="b6f24-116">Если функция завершается неудачно, возвращаемое значение указывает причину сбоя.</span><span class="sxs-lookup"><span data-stu-id="b6f24-116">If the function is unsuccessful, the return value indicates the reason for the failure.</span></span> <span data-ttu-id="b6f24-117">Если возвращаемое значение — НМЕРР \_ \_ , то эксперт немедленно очищается и возвращает результат.</span><span class="sxs-lookup"><span data-stu-id="b6f24-117">If the return value is NMERR\_EXPERT\_TERMINATE, the expert immediately cleans up and returns.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6f24-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b6f24-118">Remarks</span></span>

<span data-ttu-id="b6f24-119">Важно отметить, что эксперт должен использовать сетевой монитор функции выделения памяти для управления памятью.</span><span class="sxs-lookup"><span data-stu-id="b6f24-119">It is important to note that an expert should use the Network Monitor memory allocation functions for memory management.</span></span> <span data-ttu-id="b6f24-120">Если во время выполнения эксперт не работает, использование этих функций позволит сетевой монитор освободить выделенную память.</span><span class="sxs-lookup"><span data-stu-id="b6f24-120">If your expert fails during run time, using these functions will allow Network Monitor to free the memory it has allocated.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6f24-121">Требования</span><span class="sxs-lookup"><span data-stu-id="b6f24-121">Requirements</span></span>



| <span data-ttu-id="b6f24-122">Требование</span><span class="sxs-lookup"><span data-stu-id="b6f24-122">Requirement</span></span> | <span data-ttu-id="b6f24-123">Значение</span><span class="sxs-lookup"><span data-stu-id="b6f24-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b6f24-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b6f24-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b6f24-125">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b6f24-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="b6f24-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b6f24-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b6f24-127">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b6f24-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="b6f24-128">Заголовок</span><span class="sxs-lookup"><span data-stu-id="b6f24-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6f24-129"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6f24-129"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="b6f24-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b6f24-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="b6f24-131"><dt>Нмапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b6f24-131"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="b6f24-132">DLL</span><span class="sxs-lookup"><span data-stu-id="b6f24-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b6f24-133"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b6f24-133"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




