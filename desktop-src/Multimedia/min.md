---
title: макрос min (Минвиндеф. h)
description: Макрос min сравнивает два значения и возвращает меньшее из них. Тип данных может быть любым числовым типом данных, подписанным или неподписанным. Тип данных аргументов и возвращаемое значение одинаковы.
ms.assetid: c7d5094c-6f26-4799-95c8-804a8b48d39e
keywords:
- Минимальное мультимедиа в Windows
topic_type:
- apiref
api_name:
- min
api_location:
- minwindef.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b50680d5902ae2dc895f53f023c4b229b03c7e86
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103804096"
---
# <a name="min-macro"></a><span data-ttu-id="68638-106">min - макрос</span><span class="sxs-lookup"><span data-stu-id="68638-106">min macro</span></span>

<span data-ttu-id="68638-107">Макрос **min** сравнивает два значения и возвращает меньшее из них.</span><span class="sxs-lookup"><span data-stu-id="68638-107">The **min** macro compares two values and returns the smaller one.</span></span> <span data-ttu-id="68638-108">Тип данных может быть любым числовым типом данных, подписанным или неподписанным.</span><span class="sxs-lookup"><span data-stu-id="68638-108">The data type can be any numeric data type, signed or unsigned.</span></span> <span data-ttu-id="68638-109">Тип данных аргументов и возвращаемое значение одинаковы.</span><span class="sxs-lookup"><span data-stu-id="68638-109">The data type of the arguments and the return value is the same.</span></span>

## <a name="syntax"></a><span data-ttu-id="68638-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="68638-110">Syntax</span></span>


```C++
 min(
    value1,
    value2
);
```



## <a name="parameters"></a><span data-ttu-id="68638-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="68638-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68638-112">*value1*</span><span class="sxs-lookup"><span data-stu-id="68638-112">*value1*</span></span> 
</dt> <dd>

<span data-ttu-id="68638-113">Задает первое из двух значений.</span><span class="sxs-lookup"><span data-stu-id="68638-113">Specifies the first of two values.</span></span>

</dd> <dt>

<span data-ttu-id="68638-114">*value2*</span><span class="sxs-lookup"><span data-stu-id="68638-114">*value2*</span></span> 
</dt> <dd>

<span data-ttu-id="68638-115">Задает второе из двух значений.</span><span class="sxs-lookup"><span data-stu-id="68638-115">Specifies the second of two values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68638-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="68638-116">Return value</span></span>

<span data-ttu-id="68638-117">Возвращаемое значение представляет собой меньшее из двух указанных значений.</span><span class="sxs-lookup"><span data-stu-id="68638-117">The return value is the smaller of the two specified values.</span></span>

## <a name="remarks"></a><span data-ttu-id="68638-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="68638-118">Remarks</span></span>

<span data-ttu-id="68638-119">Макрос **min** определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="68638-119">The **min** macro is defined as follows:</span></span>


```C++
#define min(a, b)  (((a) < (b)) ? (a) : (b)) 
```



## <a name="requirements"></a><span data-ttu-id="68638-120">Требования</span><span class="sxs-lookup"><span data-stu-id="68638-120">Requirements</span></span>



| <span data-ttu-id="68638-121">Требование</span><span class="sxs-lookup"><span data-stu-id="68638-121">Requirement</span></span> | <span data-ttu-id="68638-122">Значение</span><span class="sxs-lookup"><span data-stu-id="68638-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="68638-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="68638-123">Minimum supported client</span></span><br/> | <span data-ttu-id="68638-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="68638-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="68638-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="68638-125">Minimum supported server</span></span><br/> | <span data-ttu-id="68638-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="68638-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="68638-127">Заголовок</span><span class="sxs-lookup"><span data-stu-id="68638-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="68638-128"><dt>Минвиндеф. h</dt></span><span class="sxs-lookup"><span data-stu-id="68638-128"><dt>Minwindef.h</dt></span></span> </dl> |



 

 





