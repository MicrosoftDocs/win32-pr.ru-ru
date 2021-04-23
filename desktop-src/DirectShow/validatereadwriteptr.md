---
description: Проверяет, что вызывающий процесс имеет доступ на чтение и запись к блоку памяти. В противном случае макрос вызывает макрос Дбгбреак.
ms.assetid: 215f6db9-67b6-47e1-bee1-dc37082ae2b8
title: Макрос Валидатереадвритептр (Вксдебуг. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ValidateReadWritePtr
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: b551f3c72a2480ea1f160b2b384fe87dbede51f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679983"
---
# <a name="validatereadwriteptr-macro"></a><span data-ttu-id="e1589-104">Макрос Валидатереадвритептр</span><span class="sxs-lookup"><span data-stu-id="e1589-104">ValidateReadWritePtr macro</span></span>

<span data-ttu-id="e1589-105">Проверяет, что вызывающий процесс имеет доступ на чтение и запись к блоку памяти.</span><span class="sxs-lookup"><span data-stu-id="e1589-105">Verifies that the calling process has read/write access to a memory block.</span></span> <span data-ttu-id="e1589-106">В противном случае макрос вызывает макрос [**дбгбреак**](dbgbreak.md) .</span><span class="sxs-lookup"><span data-stu-id="e1589-106">If not, the macro calls the [**DbgBreak**](dbgbreak.md) macro.</span></span>

> [!Note]  
> <span data-ttu-id="e1589-107">Этот макрос не рекомендуется к использованию.</span><span class="sxs-lookup"><span data-stu-id="e1589-107">This macro is deprecated.</span></span> <span data-ttu-id="e1589-108">В Windows SDK для Windows Vista (и более поздних версий) этот макрос не выполняет никаких действий.</span><span class="sxs-lookup"><span data-stu-id="e1589-108">In the Windows SDK for Windows Vista (and later) this macro does not do anything.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="e1589-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e1589-109">Syntax</span></span>


```C++
void ValidateReadWritePtr(
   const void *p,
         UINT cb
);
```



## <a name="parameters"></a><span data-ttu-id="e1589-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="e1589-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1589-111">*ш*</span><span class="sxs-lookup"><span data-stu-id="e1589-111">*p*</span></span> 
</dt> <dd>

<span data-ttu-id="e1589-112">Указатель на блок памяти.</span><span class="sxs-lookup"><span data-stu-id="e1589-112">Pointer to a memory block.</span></span>

</dd> <dt>

<span data-ttu-id="e1589-113">*CB*</span><span class="sxs-lookup"><span data-stu-id="e1589-113">*cb*</span></span> 
</dt> <dd>

<span data-ttu-id="e1589-114">Размер блока памяти в байтах.</span><span class="sxs-lookup"><span data-stu-id="e1589-114">Size of the memory block, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1589-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e1589-115">Return value</span></span>

<span data-ttu-id="e1589-116">Этот макрос не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="e1589-116">This macro does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1589-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e1589-117">Remarks</span></span>

<span data-ttu-id="e1589-118">Этот макрос игнорируется, если \_ при включении файла заголовков базового класса DirectShow не определена Отладка, отладка или вфвробуст.</span><span class="sxs-lookup"><span data-stu-id="e1589-118">This macro is ignored unless DEBUG, \_DEBUG, or VFWROBUST is defined when the DirectShow base-class header file is included.</span></span> <span data-ttu-id="e1589-119">Этот макрос может существенно постоить в производительности.</span><span class="sxs-lookup"><span data-stu-id="e1589-119">This macro can have a significant performance cost.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1589-120">Требования</span><span class="sxs-lookup"><span data-stu-id="e1589-120">Requirements</span></span>



| <span data-ttu-id="e1589-121">Требование</span><span class="sxs-lookup"><span data-stu-id="e1589-121">Requirement</span></span> | <span data-ttu-id="e1589-122">Значение</span><span class="sxs-lookup"><span data-stu-id="e1589-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1589-123">Header</span><span class="sxs-lookup"><span data-stu-id="e1589-123">Header</span></span><br/> | <dl> <span data-ttu-id="e1589-124"><dt>Вксдебуг. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e1589-124"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1589-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e1589-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1589-126">Макросы проверки указателя</span><span class="sxs-lookup"><span data-stu-id="e1589-126">Pointer Validation Macros</span></span>](pointer-validation-macros.md)
</dt> </dl>

 

 




