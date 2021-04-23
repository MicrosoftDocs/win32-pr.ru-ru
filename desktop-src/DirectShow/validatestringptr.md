---
description: Проверяет, имеет ли вызывающий процесс доступ на чтение к строке. В противном случае макрос вызывает макрос Дбгбреак.
ms.assetid: 749a8c22-7a4a-49c2-a214-fc64dc5a0202
title: Макрос Валидатестрингптр (Вксдебуг. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ValidateReadPtr
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 19bf0b9e43ecbbbdea0e11284cd1cb4a058e22cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689457"
---
# <a name="validatestringptr-macro"></a><span data-ttu-id="54953-104">Макрос Валидатестрингптр</span><span class="sxs-lookup"><span data-stu-id="54953-104">ValidateStringPtr macro</span></span>

<span data-ttu-id="54953-105">Проверяет, имеет ли вызывающий процесс доступ на чтение к строке.</span><span class="sxs-lookup"><span data-stu-id="54953-105">Verifies that the calling process has read access to a string.</span></span> <span data-ttu-id="54953-106">В противном случае макрос вызывает макрос [**дбгбреак**](dbgbreak.md) .</span><span class="sxs-lookup"><span data-stu-id="54953-106">If not, the macro calls the [**DbgBreak**](dbgbreak.md) macro.</span></span>

> [!Note]  
> <span data-ttu-id="54953-107">Этот макрос не рекомендуется к использованию.</span><span class="sxs-lookup"><span data-stu-id="54953-107">This macro is deprecated.</span></span> <span data-ttu-id="54953-108">В Windows SDK для Windows Vista (и более поздних версий) этот макрос не выполняет никаких действий.</span><span class="sxs-lookup"><span data-stu-id="54953-108">In the Windows SDK for Windows Vista (and later) this macro does not do anything.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="54953-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="54953-109">Syntax</span></span>


```C++
void ValidateReadPtr(
   LPCTSTR p
);
```



## <a name="parameters"></a><span data-ttu-id="54953-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="54953-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54953-111">*ш*</span><span class="sxs-lookup"><span data-stu-id="54953-111">*p*</span></span> 
</dt> <dd>

<span data-ttu-id="54953-112">Указатель на строку **TCHAR** , заканчивающуюся нулем.</span><span class="sxs-lookup"><span data-stu-id="54953-112">Pointer to a NULL-terminated **TCHAR** string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54953-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="54953-113">Return value</span></span>

<span data-ttu-id="54953-114">Этот макрос не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="54953-114">This macro does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="54953-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="54953-115">Remarks</span></span>

<span data-ttu-id="54953-116">Этот макрос игнорируется, если \_ при включении файла заголовков базового класса DirectShow не определена Отладка, отладка или вфвробуст.</span><span class="sxs-lookup"><span data-stu-id="54953-116">This macro is ignored unless DEBUG, \_DEBUG, or VFWROBUST is defined when the DirectShow base-class header file is included.</span></span> <span data-ttu-id="54953-117">Этот макрос может существенно постоить в производительности.</span><span class="sxs-lookup"><span data-stu-id="54953-117">This macro can have a significant performance cost.</span></span>

## <a name="requirements"></a><span data-ttu-id="54953-118">Требования</span><span class="sxs-lookup"><span data-stu-id="54953-118">Requirements</span></span>



| <span data-ttu-id="54953-119">Требование</span><span class="sxs-lookup"><span data-stu-id="54953-119">Requirement</span></span> | <span data-ttu-id="54953-120">Значение</span><span class="sxs-lookup"><span data-stu-id="54953-120">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54953-121">Header</span><span class="sxs-lookup"><span data-stu-id="54953-121">Header</span></span><br/> | <dl> <span data-ttu-id="54953-122"><dt>Вксдебуг. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="54953-122"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54953-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="54953-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54953-124">Макросы проверки указателя</span><span class="sxs-lookup"><span data-stu-id="54953-124">Pointer Validation Macros</span></span>](pointer-validation-macros.md)
</dt> </dl>

 

 




