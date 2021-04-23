---
description: Проверяет, имеет ли вызывающий процесс доступ на чтение к строке ANSI. В противном случае макрос вызывает макрос Дбгбреак.
ms.assetid: 44be67f8-9896-4360-82de-083a5f28a3d0
title: Макрос Валидатестрингптра (Вксдебуг. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ValidateStringPtrA
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 94ce34393ec494f34cce621afc168a4d6bbe4325
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679982"
---
# <a name="validatestringptra-macro"></a><span data-ttu-id="ceb53-104">Макрос Валидатестрингптра</span><span class="sxs-lookup"><span data-stu-id="ceb53-104">ValidateStringPtrA macro</span></span>

<span data-ttu-id="ceb53-105">Проверяет, имеет ли вызывающий процесс доступ на чтение к строке ANSI.</span><span class="sxs-lookup"><span data-stu-id="ceb53-105">Verifies that the calling process has read access to an ANSI string.</span></span> <span data-ttu-id="ceb53-106">В противном случае макрос вызывает макрос [**дбгбреак**](dbgbreak.md) .</span><span class="sxs-lookup"><span data-stu-id="ceb53-106">If not, the macro calls the [**DbgBreak**](dbgbreak.md) macro.</span></span>

> [!Note]  
> <span data-ttu-id="ceb53-107">Этот макрос не рекомендуется к использованию.</span><span class="sxs-lookup"><span data-stu-id="ceb53-107">This macro is deprecated.</span></span> <span data-ttu-id="ceb53-108">В Windows SDK для Windows Vista (и более поздних версий) этот макрос не выполняет никаких действий.</span><span class="sxs-lookup"><span data-stu-id="ceb53-108">In the Windows SDK for Windows Vista (and later) this macro does not do anything.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="ceb53-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ceb53-109">Syntax</span></span>


```C++
void ValidateStringPtrA(
   LPCSTR p
);
```



## <a name="parameters"></a><span data-ttu-id="ceb53-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="ceb53-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ceb53-111">*ш*</span><span class="sxs-lookup"><span data-stu-id="ceb53-111">*p*</span></span> 
</dt> <dd>

<span data-ttu-id="ceb53-112">Указатель на строку ANSI, заканчивающуюся нулем.</span><span class="sxs-lookup"><span data-stu-id="ceb53-112">Pointer to a NULL-terminated ANSI string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ceb53-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ceb53-113">Return value</span></span>

<span data-ttu-id="ceb53-114">Этот макрос не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="ceb53-114">This macro does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ceb53-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ceb53-115">Remarks</span></span>

<span data-ttu-id="ceb53-116">Этот макрос игнорируется, если \_ при включении файла заголовков базового класса DirectShow не определена Отладка, отладка или вфвробуст.</span><span class="sxs-lookup"><span data-stu-id="ceb53-116">This macro is ignored unless DEBUG, \_DEBUG, or VFWROBUST is defined when the DirectShow base-class header file is included.</span></span>

## <a name="requirements"></a><span data-ttu-id="ceb53-117">Требования</span><span class="sxs-lookup"><span data-stu-id="ceb53-117">Requirements</span></span>



| <span data-ttu-id="ceb53-118">Требование</span><span class="sxs-lookup"><span data-stu-id="ceb53-118">Requirement</span></span> | <span data-ttu-id="ceb53-119">Значение</span><span class="sxs-lookup"><span data-stu-id="ceb53-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ceb53-120">Header</span><span class="sxs-lookup"><span data-stu-id="ceb53-120">Header</span></span><br/> | <dl> <span data-ttu-id="ceb53-121"><dt>Вксдебуг. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ceb53-121"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ceb53-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ceb53-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ceb53-123">Макросы проверки указателя</span><span class="sxs-lookup"><span data-stu-id="ceb53-123">Pointer Validation Macros</span></span>](pointer-validation-macros.md)
</dt> </dl>

 

 




