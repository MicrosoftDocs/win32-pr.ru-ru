---
title: Функция Глуневтесс (GLU. h)
description: Функция Глуневтесс создает объект тесселяции.
ms.assetid: dfc9fce8-ecab-493b-85ee-6d7487814186
keywords:
- Функция Глуневтесс OpenGL
topic_type:
- apiref
api_name:
- gluNewTess
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0573ead0cf9b81568c4bf2101e317bef7faf148
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661879"
---
# <a name="glunewtess-function"></a><span data-ttu-id="dedce-104">Функция Глуневтесс</span><span class="sxs-lookup"><span data-stu-id="dedce-104">gluNewTess function</span></span>

<span data-ttu-id="dedce-105">Функция **глуневтесс** создает объект тесселяции.</span><span class="sxs-lookup"><span data-stu-id="dedce-105">The **gluNewTess** function creates a tessellation object.</span></span>

## <a name="syntax"></a><span data-ttu-id="dedce-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dedce-106">Syntax</span></span>


```C++
GLUtesselator* WINAPI gluNewTess(void);
```



## <a name="parameters"></a><span data-ttu-id="dedce-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="dedce-107">Parameters</span></span>

<span data-ttu-id="dedce-108">У этой функции нет параметров.</span><span class="sxs-lookup"><span data-stu-id="dedce-108">This function has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="dedce-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dedce-109">Remarks</span></span>

<span data-ttu-id="dedce-110">Функция **глуневтесс** создает и возвращает указатель на новый объект тесселяции.</span><span class="sxs-lookup"><span data-stu-id="dedce-110">The **gluNewTess** function creates and returns a pointer to a new tessellation object.</span></span> <span data-ttu-id="dedce-111">Используйте этот объект при вызове функций тесселяции.</span><span class="sxs-lookup"><span data-stu-id="dedce-111">Refer to this object when calling tessellation functions.</span></span> <span data-ttu-id="dedce-112">Возвращаемое значение, равное нулю, означает, что недостаточно памяти для выделения объекту.</span><span class="sxs-lookup"><span data-stu-id="dedce-112">A return value of zero means there is not enough memory to allocate to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="dedce-113">Требования</span><span class="sxs-lookup"><span data-stu-id="dedce-113">Requirements</span></span>



| <span data-ttu-id="dedce-114">Требование</span><span class="sxs-lookup"><span data-stu-id="dedce-114">Requirement</span></span> | <span data-ttu-id="dedce-115">Значение</span><span class="sxs-lookup"><span data-stu-id="dedce-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="dedce-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dedce-116">Minimum supported client</span></span><br/> | <span data-ttu-id="dedce-117">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="dedce-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="dedce-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dedce-118">Minimum supported server</span></span><br/> | <span data-ttu-id="dedce-119">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="dedce-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="dedce-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="dedce-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="dedce-121"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="dedce-121"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="dedce-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="dedce-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="dedce-123"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dedce-123"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="dedce-124">DLL</span><span class="sxs-lookup"><span data-stu-id="dedce-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dedce-125"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dedce-125"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dedce-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dedce-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dedce-127">**глуделететесс**</span><span class="sxs-lookup"><span data-stu-id="dedce-127">**gluDeleteTess**</span></span>](gludeletetess.md)
</dt> <dt>

[<span data-ttu-id="dedce-128">**глутессбегинполигон**</span><span class="sxs-lookup"><span data-stu-id="dedce-128">**gluTessBeginPolygon**</span></span>](glubeginpolygon.md)
</dt> <dt>

[<span data-ttu-id="dedce-129">*глутесскаллбакк*</span><span class="sxs-lookup"><span data-stu-id="dedce-129">*gluTessCallback*</span></span>](glutess.md)
</dt> </dl>

 

 





