---
title: макрос Max (Минвиндеф. h)
description: Макрос Max сравнивает два значения и возвращает значение большего. Тип данных может быть любым числовым типом данных, подписанным или неподписанным. Тип данных аргументов и возвращаемое значение одинаковы.
ms.assetid: 224d2ef7-6764-49c0-9782-51bfadbfb77f
keywords:
- Максимальное число мультимедийных окон макросов
topic_type:
- apiref
api_name:
- max
api_location:
- minwindef.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b484f2505958aca04745c63ca63a0dd131a51ed9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534019"
---
# <a name="max-macro"></a><span data-ttu-id="aaf19-106">max - макрос</span><span class="sxs-lookup"><span data-stu-id="aaf19-106">max macro</span></span>

<span data-ttu-id="aaf19-107">Макрос **Max** сравнивает два значения и возвращает значение большего.</span><span class="sxs-lookup"><span data-stu-id="aaf19-107">The **max** macro compares two values and returns the larger one.</span></span> <span data-ttu-id="aaf19-108">Тип данных может быть любым числовым типом данных, подписанным или неподписанным.</span><span class="sxs-lookup"><span data-stu-id="aaf19-108">The data type can be any numeric data type, signed or unsigned.</span></span> <span data-ttu-id="aaf19-109">Тип данных аргументов и возвращаемое значение одинаковы.</span><span class="sxs-lookup"><span data-stu-id="aaf19-109">The data type of the arguments and the return value is the same.</span></span>

## <a name="syntax"></a><span data-ttu-id="aaf19-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="aaf19-110">Syntax</span></span>


```C++
 max(
    value1,
    value2
);
```



## <a name="parameters"></a><span data-ttu-id="aaf19-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="aaf19-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aaf19-112">*value1*</span><span class="sxs-lookup"><span data-stu-id="aaf19-112">*value1*</span></span> 
</dt> <dd>

<span data-ttu-id="aaf19-113">Задает первое из двух значений.</span><span class="sxs-lookup"><span data-stu-id="aaf19-113">Specifies the first of two values.</span></span>

</dd> <dt>

<span data-ttu-id="aaf19-114">*value2*</span><span class="sxs-lookup"><span data-stu-id="aaf19-114">*value2*</span></span> 
</dt> <dd>

<span data-ttu-id="aaf19-115">Задает второе из двух значений.</span><span class="sxs-lookup"><span data-stu-id="aaf19-115">Specifies the second of two values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aaf19-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="aaf19-116">Return value</span></span>

<span data-ttu-id="aaf19-117">Возвращаемое значение — это большее из двух указанных значений.</span><span class="sxs-lookup"><span data-stu-id="aaf19-117">The return value is the greater of the two specified values.</span></span>

## <a name="remarks"></a><span data-ttu-id="aaf19-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="aaf19-118">Remarks</span></span>

<span data-ttu-id="aaf19-119">Макрос **Max** определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="aaf19-119">The **max** macro is defined as follows:</span></span>


```C++
#define max(a, b)  (((a) > (b)) ? (a) : (b)) 
```



## <a name="requirements"></a><span data-ttu-id="aaf19-120">Требования</span><span class="sxs-lookup"><span data-stu-id="aaf19-120">Requirements</span></span>



| <span data-ttu-id="aaf19-121">Требование</span><span class="sxs-lookup"><span data-stu-id="aaf19-121">Requirement</span></span> | <span data-ttu-id="aaf19-122">Значение</span><span class="sxs-lookup"><span data-stu-id="aaf19-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aaf19-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="aaf19-123">Minimum supported client</span></span><br/> | <span data-ttu-id="aaf19-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="aaf19-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="aaf19-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="aaf19-125">Minimum supported server</span></span><br/> | <span data-ttu-id="aaf19-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="aaf19-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="aaf19-127">Заголовок</span><span class="sxs-lookup"><span data-stu-id="aaf19-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="aaf19-128"><dt>Минвиндеф. h</dt></span><span class="sxs-lookup"><span data-stu-id="aaf19-128"><dt>Minwindef.h</dt></span></span> </dl> |



 

 





