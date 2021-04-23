---
description: Функция Експертмеморисизе Возвращает объем памяти, выделенной функцией Експерталлокмемори.
ms.assetid: 60d3f33d-dc03-4c39-98fa-ec093398b51b
title: Функция Експертмеморисизе (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertMemorySize
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 57c83bc3e9535550086c9732b33a71a357e4da42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896786"
---
# <a name="expertmemorysize-function"></a><span data-ttu-id="9aca5-103">Функция Експертмеморисизе</span><span class="sxs-lookup"><span data-stu-id="9aca5-103">ExpertMemorySize function</span></span>

<span data-ttu-id="9aca5-104">Функция **експертмеморисизе** Возвращает объем памяти, выделенной функцией [експерталлокмемори](expertallocmemory.md) .</span><span class="sxs-lookup"><span data-stu-id="9aca5-104">The **ExpertMemorySize** function returns the amount of memory allocated by the [ExpertAllocMemory](expertallocmemory.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="9aca5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9aca5-105">Syntax</span></span>


```C++
SIZE_T WINAPI ExpertMemorySize(
  _In_ HEXPERTKEY hExpertKey,
  _In_ LPVOID     pOriginalMemory
);
```



## <a name="parameters"></a><span data-ttu-id="9aca5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9aca5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9aca5-107">*хексперткэй* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9aca5-107">*hExpertKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9aca5-108">Уникальный идентификатор эксперта.</span><span class="sxs-lookup"><span data-stu-id="9aca5-108">Unique expert identifier.</span></span> <span data-ttu-id="9aca5-109">Сетевой монитор передает *хексперткэй* эксперту при вызове функции [Run](run.md) .</span><span class="sxs-lookup"><span data-stu-id="9aca5-109">Network Monitor passes *hExpertKey* to the expert when it calls the [Run](run.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="9aca5-110">*поригиналмемори* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9aca5-110">*pOriginalMemory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9aca5-111">Указатель на адрес в памяти эксперта, выделенного [експерталлокмемори](expertallocmemory.md).</span><span class="sxs-lookup"><span data-stu-id="9aca5-111">Pointer to the memory address of the expert allocated by [ExpertAllocMemory](expertallocmemory.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9aca5-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9aca5-112">Return value</span></span>

<span data-ttu-id="9aca5-113">Функция возвращает объем выделенной памяти в байтах.</span><span class="sxs-lookup"><span data-stu-id="9aca5-113">The function returns the amount of allocated memory   in bytes.</span></span>

## <a name="remarks"></a><span data-ttu-id="9aca5-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9aca5-114">Remarks</span></span>

<span data-ttu-id="9aca5-115">Сведения о типе данных «size», возвращаемом **експертмеморисизе** , см. в разделе Типы данных. **\_**</span><span class="sxs-lookup"><span data-stu-id="9aca5-115">For information on the **SIZE\_T** data type that **ExpertMemorySize** returns, see Data Types.</span></span>

## <a name="requirements"></a><span data-ttu-id="9aca5-116">Требования</span><span class="sxs-lookup"><span data-stu-id="9aca5-116">Requirements</span></span>



| <span data-ttu-id="9aca5-117">Требование</span><span class="sxs-lookup"><span data-stu-id="9aca5-117">Requirement</span></span> | <span data-ttu-id="9aca5-118">Значение</span><span class="sxs-lookup"><span data-stu-id="9aca5-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9aca5-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9aca5-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9aca5-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9aca5-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="9aca5-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9aca5-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9aca5-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9aca5-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="9aca5-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="9aca5-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9aca5-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="9aca5-124"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="9aca5-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9aca5-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="9aca5-126"><dt>Нмапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9aca5-126"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="9aca5-127">DLL</span><span class="sxs-lookup"><span data-stu-id="9aca5-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9aca5-128"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9aca5-128"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




