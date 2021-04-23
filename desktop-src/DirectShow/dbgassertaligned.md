---
description: Проверяет, соответствует ли указатель заданной границе. В противном случае этот макрос вызывает макрос ASSERT. Игнорируется в розничных сборках.
ms.assetid: 4d9ec3a9-7107-45a3-a7aa-28d6e38fa92a
title: Макрос Дбгассерталигнед (Вксдебуг. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgAssertAligned
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 22b357f7f28e9df04ce36636e3972dbadc3036a6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679874"
---
# <a name="dbgassertaligned-macro"></a><span data-ttu-id="80794-105">Макрос Дбгассерталигнед</span><span class="sxs-lookup"><span data-stu-id="80794-105">DbgAssertAligned macro</span></span>

<span data-ttu-id="80794-106">Проверяет, соответствует ли указатель заданной границе.</span><span class="sxs-lookup"><span data-stu-id="80794-106">Tests whether a pointer is aligned to a specified boundary.</span></span> <span data-ttu-id="80794-107">В противном случае этот макрос вызывает макрос [**Assert**](assert.md) .</span><span class="sxs-lookup"><span data-stu-id="80794-107">If not, this macro invokes the [**ASSERT**](assert.md) macro.</span></span> <span data-ttu-id="80794-108">Игнорируется в розничных сборках.</span><span class="sxs-lookup"><span data-stu-id="80794-108">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="80794-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="80794-109">Syntax</span></span>


```C++
void DbgAssertAligned(
    ptr,
    alignment
);
```



## <a name="parameters"></a><span data-ttu-id="80794-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="80794-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80794-111">*ptr*</span><span class="sxs-lookup"><span data-stu-id="80794-111">*ptr*</span></span> 
</dt> <dd>

<span data-ttu-id="80794-112">Переменная указателя.</span><span class="sxs-lookup"><span data-stu-id="80794-112">Pointer variable.</span></span>

</dd> <dt>

<span data-ttu-id="80794-113">*Выравнивание*</span><span class="sxs-lookup"><span data-stu-id="80794-113">*alignment*</span></span> 
</dt> <dd>

<span data-ttu-id="80794-114">Требуемое выравнивание.</span><span class="sxs-lookup"><span data-stu-id="80794-114">Required alignment.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80794-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="80794-115">Return value</span></span>

<span data-ttu-id="80794-116">Этот макрос не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="80794-116">This macro does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="80794-117">Требования</span><span class="sxs-lookup"><span data-stu-id="80794-117">Requirements</span></span>



| <span data-ttu-id="80794-118">Требование</span><span class="sxs-lookup"><span data-stu-id="80794-118">Requirement</span></span> | <span data-ttu-id="80794-119">Значение</span><span class="sxs-lookup"><span data-stu-id="80794-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80794-120">Header</span><span class="sxs-lookup"><span data-stu-id="80794-120">Header</span></span><br/> | <dl> <span data-ttu-id="80794-121"><dt>Вксдебуг. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="80794-121"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80794-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="80794-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80794-123">Макросы Assert и точка останова</span><span class="sxs-lookup"><span data-stu-id="80794-123">Assert and Breakpoint Macros</span></span>](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




