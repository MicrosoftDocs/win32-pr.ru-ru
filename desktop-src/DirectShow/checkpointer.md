---
description: Проверяет, имеет ли указатель значение NULL. Если указатель имеет значение NULL, функция или метод, в которых отображается макрос, возвращает указанное значение.
ms.assetid: eca73fbf-5fd8-4b76-af06-ca0c22510b55
title: Макрос контрольной точки (Вксдебуг. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CheckPointer
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 04f442303e520ef758a3576d21c2df810ef26fb2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657548"
---
# <a name="checkpointer-macro"></a><span data-ttu-id="1caed-104">Макрос контрольной точки</span><span class="sxs-lookup"><span data-stu-id="1caed-104">CheckPointer macro</span></span>

<span data-ttu-id="1caed-105">Проверяет, имеет ли указатель **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="1caed-105">Checks whether a pointer is **NULL**.</span></span> <span data-ttu-id="1caed-106">Если указатель имеет **значение NULL**, функция или метод, в которых отображается макрос, возвращает указанное значение.</span><span class="sxs-lookup"><span data-stu-id="1caed-106">If the pointer is **NULL**, the function or method in which the macro appears returns the specified value.</span></span>

## <a name="syntax"></a><span data-ttu-id="1caed-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1caed-107">Syntax</span></span>


```C++
HRESULT CheckPointer(
    p,
    ret
);
```



## <a name="parameters"></a><span data-ttu-id="1caed-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="1caed-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1caed-109">*ш*</span><span class="sxs-lookup"><span data-stu-id="1caed-109">*p*</span></span> 
</dt> <dd>

<span data-ttu-id="1caed-110">Указатель на проверку.</span><span class="sxs-lookup"><span data-stu-id="1caed-110">Pointer to check.</span></span>

</dd> <dt>

<span data-ttu-id="1caed-111">*обратно*</span><span class="sxs-lookup"><span data-stu-id="1caed-111">*ret*</span></span> 
</dt> <dd>

<span data-ttu-id="1caed-112">Значение, возвращаемое функцией или методом, если *p* имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="1caed-112">Value that the function or method returns if *p* is **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1caed-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1caed-113">Return value</span></span>

<span data-ttu-id="1caed-114">Окружающая функция возвращает *RET* , если *p* имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="1caed-114">The surrounding function returns *ret* if *p* is **NULL**.</span></span> <span data-ttu-id="1caed-115">В противном случае макрос не будет возвращать окружающую функцию.</span><span class="sxs-lookup"><span data-stu-id="1caed-115">Otherwise, the macro does not cause the surrounding function to return.</span></span>

## <a name="examples"></a><span data-ttu-id="1caed-116">Примеры</span><span class="sxs-lookup"><span data-stu-id="1caed-116">Examples</span></span>


```
HRESULT MyFunction(VOID *pSomeParameter)
{
    // Return E_INVALIDARG if pSomeParameter is NULL.
    CheckPointer(pSomeParameter, E_INVALIDARG)

    // Rest of the function (not shown).
}
```



## <a name="requirements"></a><span data-ttu-id="1caed-117">Требования</span><span class="sxs-lookup"><span data-stu-id="1caed-117">Requirements</span></span>



| <span data-ttu-id="1caed-118">Требование</span><span class="sxs-lookup"><span data-stu-id="1caed-118">Requirement</span></span> | <span data-ttu-id="1caed-119">Значение</span><span class="sxs-lookup"><span data-stu-id="1caed-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1caed-120">Header</span><span class="sxs-lookup"><span data-stu-id="1caed-120">Header</span></span><br/> | <dl> <span data-ttu-id="1caed-121"><dt>Вксдебуг. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1caed-121"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1caed-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1caed-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1caed-123">Макросы проверки указателя</span><span class="sxs-lookup"><span data-stu-id="1caed-123">Pointer Validation Macros</span></span>](pointer-validation-macros.md)
</dt> </dl>

 

 




