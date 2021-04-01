---
title: Функция Глуделететесс (GLU. h)
description: Функция Глуделететесс уничтожает объект тесселяции.
ms.assetid: 7e1540f7-5e7d-4a3b-8c94-5a6800b17411
keywords:
- Функция Глуделететесс OpenGL
topic_type:
- apiref
api_name:
- gluDeleteTess
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee4625f0a9c2f51e9d7147c9564fcd4fb1fa7117
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801624"
---
# <a name="gludeletetess-function"></a><span data-ttu-id="bed28-104">Функция Глуделететесс</span><span class="sxs-lookup"><span data-stu-id="bed28-104">gluDeleteTess function</span></span>

<span data-ttu-id="bed28-105">Функция **глуделететесс** уничтожает объект тесселяции.</span><span class="sxs-lookup"><span data-stu-id="bed28-105">The **gluDeleteTess** function destroys a tessellation object.</span></span>

## <a name="syntax"></a><span data-ttu-id="bed28-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bed28-106">Syntax</span></span>


```C++
void WINAPI gluDeleteTess(
   GLUtesselator *tess
);
```



## <a name="parameters"></a><span data-ttu-id="bed28-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="bed28-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bed28-108">*тесс*</span><span class="sxs-lookup"><span data-stu-id="bed28-108">*tess*</span></span> 
</dt> <dd>

<span data-ttu-id="bed28-109">Объект тесселяции для уничтожения (создается с помощью [**глуневтесс**](glunewtess.md)).</span><span class="sxs-lookup"><span data-stu-id="bed28-109">The tessellation object to destroy (created with [**gluNewTess**](glunewtess.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bed28-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bed28-110">Return value</span></span>

<span data-ttu-id="bed28-111">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="bed28-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bed28-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bed28-112">Remarks</span></span>

<span data-ttu-id="bed28-113">Функция **глуделететесс** уничтожает указанный объект тесселяции и освобождает используемую память.</span><span class="sxs-lookup"><span data-stu-id="bed28-113">The **gluDeleteTess** function destroys the indicated tessellation object and frees any memory that it used.</span></span>

## <a name="requirements"></a><span data-ttu-id="bed28-114">Требования</span><span class="sxs-lookup"><span data-stu-id="bed28-114">Requirements</span></span>



| <span data-ttu-id="bed28-115">Требование</span><span class="sxs-lookup"><span data-stu-id="bed28-115">Requirement</span></span> | <span data-ttu-id="bed28-116">Значение</span><span class="sxs-lookup"><span data-stu-id="bed28-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="bed28-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bed28-117">Minimum supported client</span></span><br/> | <span data-ttu-id="bed28-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="bed28-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="bed28-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bed28-119">Minimum supported server</span></span><br/> | <span data-ttu-id="bed28-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="bed28-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="bed28-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="bed28-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="bed28-122"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="bed28-122"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="bed28-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="bed28-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="bed28-124"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bed28-124"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="bed28-125">DLL</span><span class="sxs-lookup"><span data-stu-id="bed28-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bed28-126"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bed28-126"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bed28-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bed28-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bed28-128">**глуневтесс**</span><span class="sxs-lookup"><span data-stu-id="bed28-128">**gluNewTess**</span></span>](glunewtess.md)
</dt> <dt>

[<span data-ttu-id="bed28-129">**глутессбегинполигон**</span><span class="sxs-lookup"><span data-stu-id="bed28-129">**gluTessBeginPolygon**</span></span>](glubeginpolygon.md)
</dt> <dt>

[<span data-ttu-id="bed28-130">*глутесскаллбакк*</span><span class="sxs-lookup"><span data-stu-id="bed28-130">*gluTessCallback*</span></span>](glutess.md)
</dt> </dl>

 

 





