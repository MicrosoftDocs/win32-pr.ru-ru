---
description: Проверяет, имеет ли вызывающий процесс доступ на чтение к строке расширенных символов. В противном случае макрос вызывает макрос Дбгбреак.
ms.assetid: 526e8027-31e5-428d-856d-9fc6698693c3
title: Макрос Валидатестрингптрв (Вксдебуг. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ValidateStringPtrW
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 1ece2caa0f2263c038121cd1ffd031cbe42d336a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689456"
---
# <a name="validatestringptrw-macro"></a><span data-ttu-id="c6792-104">Макрос Валидатестрингптрв</span><span class="sxs-lookup"><span data-stu-id="c6792-104">ValidateStringPtrW macro</span></span>

<span data-ttu-id="c6792-105">Проверяет, имеет ли вызывающий процесс доступ на чтение к строке расширенных символов.</span><span class="sxs-lookup"><span data-stu-id="c6792-105">Verifies that the calling process has read access to a wide-character string.</span></span> <span data-ttu-id="c6792-106">В противном случае макрос вызывает макрос [**дбгбреак**](dbgbreak.md) .</span><span class="sxs-lookup"><span data-stu-id="c6792-106">If not, the macro calls the [**DbgBreak**](dbgbreak.md) macro.</span></span>

> [!Note]  
> <span data-ttu-id="c6792-107">Этот макрос не рекомендуется к использованию.</span><span class="sxs-lookup"><span data-stu-id="c6792-107">This macro is deprecated.</span></span> <span data-ttu-id="c6792-108">В Windows SDK для Windows Vista (и более поздних версий) этот макрос не выполняет никаких действий.</span><span class="sxs-lookup"><span data-stu-id="c6792-108">In the Windows SDK for Windows Vista (and later) this macro does not do anything.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="c6792-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c6792-109">Syntax</span></span>


```C++
void ValidateStringPtrW(
   LPCWSTR p
);
```



## <a name="parameters"></a><span data-ttu-id="c6792-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="c6792-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6792-111">*ш*</span><span class="sxs-lookup"><span data-stu-id="c6792-111">*p*</span></span> 
</dt> <dd>

<span data-ttu-id="c6792-112">Указатель на строку расширенных символов, заканчивающуюся НУЛЕМ.</span><span class="sxs-lookup"><span data-stu-id="c6792-112">Pointer to a NULL-terminated wide-character string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6792-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c6792-113">Return value</span></span>

<span data-ttu-id="c6792-114">Этот макрос не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="c6792-114">This macro does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6792-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c6792-115">Remarks</span></span>

<span data-ttu-id="c6792-116">Этот макрос игнорируется, если \_ при включении файла заголовков базового класса DirectShow не определена Отладка, отладка или вфвробуст.</span><span class="sxs-lookup"><span data-stu-id="c6792-116">This macro is ignored unless DEBUG, \_DEBUG, or VFWROBUST is defined when the DirectShow base-class header file is included.</span></span> <span data-ttu-id="c6792-117">Этот макрос может существенно постоить в производительности.</span><span class="sxs-lookup"><span data-stu-id="c6792-117">This macro can have a significant performance cost.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6792-118">Требования</span><span class="sxs-lookup"><span data-stu-id="c6792-118">Requirements</span></span>



| <span data-ttu-id="c6792-119">Требование</span><span class="sxs-lookup"><span data-stu-id="c6792-119">Requirement</span></span> | <span data-ttu-id="c6792-120">Значение</span><span class="sxs-lookup"><span data-stu-id="c6792-120">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6792-121">Header</span><span class="sxs-lookup"><span data-stu-id="c6792-121">Header</span></span><br/> | <dl> <span data-ttu-id="c6792-122"><dt>Вксдебуг. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c6792-122"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6792-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c6792-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6792-124">Макросы проверки указателя</span><span class="sxs-lookup"><span data-stu-id="c6792-124">Pointer Validation Macros</span></span>](pointer-validation-macros.md)
</dt> </dl>

 

 




