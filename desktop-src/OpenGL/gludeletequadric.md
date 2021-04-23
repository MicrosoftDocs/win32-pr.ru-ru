---
title: Функция Глуделетекуадрик (GLU. h)
description: Функция Глуделетекуадрик уничтожает объект куадрик.
ms.assetid: 09efd887-0fe8-4a56-bc6f-2177a4930035
keywords:
- Функция Глуделетекуадрик OpenGL
topic_type:
- apiref
api_name:
- gluDeleteQuadric
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b5ee85e943cd958e394efb191932393d228d948
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802824"
---
# <a name="gludeletequadric-function"></a><span data-ttu-id="9e137-104">Функция Глуделетекуадрик</span><span class="sxs-lookup"><span data-stu-id="9e137-104">gluDeleteQuadric function</span></span>

<span data-ttu-id="9e137-105">Функция **глуделетекуадрик** уничтожает объект куадрик.</span><span class="sxs-lookup"><span data-stu-id="9e137-105">The **gluDeleteQuadric** function destroys a quadric object.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e137-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9e137-106">Syntax</span></span>


```C++
void WINAPI gluDeleteQuadric(
   GLUquadricObj *state
);
```



## <a name="parameters"></a><span data-ttu-id="9e137-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="9e137-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e137-108">*state*</span><span class="sxs-lookup"><span data-stu-id="9e137-108">*state*</span></span> 
</dt> <dd>

<span data-ttu-id="9e137-109">Объект куадрик для уничтожения (созданный с помощью [**глуневкуадрик**](glunewquadric.md)).</span><span class="sxs-lookup"><span data-stu-id="9e137-109">The quadric object to be destroyed (created with [**gluNewQuadric**](glunewquadric.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e137-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9e137-110">Return value</span></span>

<span data-ttu-id="9e137-111">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="9e137-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e137-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9e137-112">Remarks</span></span>

<span data-ttu-id="9e137-113">Функция **глуделетекуадрик** уничтожает объект куадрик и освобождает используемую память.</span><span class="sxs-lookup"><span data-stu-id="9e137-113">The **gluDeleteQuadric** function destroys the quadric object and frees any memory that it used.</span></span> <span data-ttu-id="9e137-114">После вызова **глуделетекуадрик** *состояние* нельзя использовать снова.</span><span class="sxs-lookup"><span data-stu-id="9e137-114">After you have called **gluDeleteQuadric**, you cannot use *state* again.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e137-115">Требования</span><span class="sxs-lookup"><span data-stu-id="9e137-115">Requirements</span></span>



| <span data-ttu-id="9e137-116">Требование</span><span class="sxs-lookup"><span data-stu-id="9e137-116">Requirement</span></span> | <span data-ttu-id="9e137-117">Значение</span><span class="sxs-lookup"><span data-stu-id="9e137-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9e137-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9e137-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9e137-119">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9e137-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="9e137-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9e137-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9e137-121">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9e137-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="9e137-122">Заголовок</span><span class="sxs-lookup"><span data-stu-id="9e137-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e137-123"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e137-123"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="9e137-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9e137-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="9e137-125"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9e137-125"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="9e137-126">DLL</span><span class="sxs-lookup"><span data-stu-id="9e137-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9e137-127"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e137-127"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e137-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9e137-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e137-129">**глуневкуадрик**</span><span class="sxs-lookup"><span data-stu-id="9e137-129">**gluNewQuadric**</span></span>](glunewquadric.md)
</dt> </dl>

 

 





