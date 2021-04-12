---
title: Функция Глужеттесспроперти (GLU. h)
description: Функция Глужеттесспроперти возвращает свойство объекта тесселяции.
ms.assetid: 6aa565d8-2257-4259-a959-b7d806a7ed96
keywords:
- Функция Глужеттесспроперти OpenGL
topic_type:
- apiref
api_name:
- gluGetTessProperty
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 482f32b227dbcf0c2a62405e344aa719bb4b9e17
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415333"
---
# <a name="glugettessproperty-function"></a><span data-ttu-id="b97ba-104">Функция Глужеттесспроперти</span><span class="sxs-lookup"><span data-stu-id="b97ba-104">gluGetTessProperty function</span></span>

<span data-ttu-id="b97ba-105">Функция **глужеттесспроперти** возвращает свойство объекта тесселяции.</span><span class="sxs-lookup"><span data-stu-id="b97ba-105">The **gluGetTessProperty** function gets a tessellation object property.</span></span>

## <a name="syntax"></a><span data-ttu-id="b97ba-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b97ba-106">Syntax</span></span>


```C++
void WINAPI gluGetTessProperty(
   GLUtesselator *tess,
   GLenum        which,
   GLdouble      *value
);
```



## <a name="parameters"></a><span data-ttu-id="b97ba-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="b97ba-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b97ba-108">*тесс*</span><span class="sxs-lookup"><span data-stu-id="b97ba-108">*tess*</span></span> 
</dt> <dd>

<span data-ttu-id="b97ba-109">Объект тесселяции (созданный с помощью [**глуневтесс**](glunewtess.md)).</span><span class="sxs-lookup"><span data-stu-id="b97ba-109">The tessellation object (created with [**gluNewTess**](glunewtess.md)).</span></span>

</dd> <dt>

<span data-ttu-id="b97ba-110">*какую*</span><span class="sxs-lookup"><span data-stu-id="b97ba-110">*which*</span></span> 
</dt> <dd>

<span data-ttu-id="b97ba-111">Свойство, значение которого необходимо извлечь.</span><span class="sxs-lookup"><span data-stu-id="b97ba-111">The property whose value is to be retrieved.</span></span> <span data-ttu-id="b97ba-112">Допустимы следующие значения: GLU \_ Тесс \_ обмотка \_ , Glu \_ Тесс \_ \_ only и Glu \_ Тесс \_ .</span><span class="sxs-lookup"><span data-stu-id="b97ba-112">The following values are valid: GLU\_TESS\_WINDING\_RULE, GLU\_TESS\_BOUNDARY\_ONLY, and GLU\_TESS\_TOLERANCE.</span></span>

</dd> <dt>

<span data-ttu-id="b97ba-113">*value*</span><span class="sxs-lookup"><span data-stu-id="b97ba-113">*value*</span></span> 
</dt> <dd>

<span data-ttu-id="b97ba-114">Указатель на расположение, в которое записывается значение именованного свойства.</span><span class="sxs-lookup"><span data-stu-id="b97ba-114">A pointer to the location where the value of the named property is written.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b97ba-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b97ba-115">Return value</span></span>

<span data-ttu-id="b97ba-116">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="b97ba-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b97ba-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b97ba-117">Remarks</span></span>

<span data-ttu-id="b97ba-118">Используйте **глужеттесспроперти** для извлечения свойств, хранящихся в объекте тесселяции.</span><span class="sxs-lookup"><span data-stu-id="b97ba-118">Use **gluGetTessProperty** to retrieve properties stored in a tessellation object.</span></span> <span data-ttu-id="b97ba-119">Эти свойства влияют на способ интерпретации и отрисовки объектов тесселяции.</span><span class="sxs-lookup"><span data-stu-id="b97ba-119">These properties affect the way tessellation objects are interpreted and rendered.</span></span> <span data-ttu-id="b97ba-120">Сведения о свойствах и их возможностях см. в разделе [**глутесспроперти**](glutessproperty.md).</span><span class="sxs-lookup"><span data-stu-id="b97ba-120">For information about what the properties are and what they do, see [**gluTessProperty**](glutessproperty.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b97ba-121">Требования</span><span class="sxs-lookup"><span data-stu-id="b97ba-121">Requirements</span></span>



| <span data-ttu-id="b97ba-122">Требование</span><span class="sxs-lookup"><span data-stu-id="b97ba-122">Requirement</span></span> | <span data-ttu-id="b97ba-123">Значение</span><span class="sxs-lookup"><span data-stu-id="b97ba-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b97ba-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b97ba-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b97ba-125">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b97ba-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="b97ba-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b97ba-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b97ba-127">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b97ba-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="b97ba-128">Заголовок</span><span class="sxs-lookup"><span data-stu-id="b97ba-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="b97ba-129"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="b97ba-129"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="b97ba-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b97ba-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="b97ba-131"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b97ba-131"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="b97ba-132">DLL</span><span class="sxs-lookup"><span data-stu-id="b97ba-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b97ba-133"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b97ba-133"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b97ba-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b97ba-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b97ba-135">**глуневтесс**</span><span class="sxs-lookup"><span data-stu-id="b97ba-135">**gluNewTess**</span></span>](glunewtess.md)
</dt> <dt>

[<span data-ttu-id="b97ba-136">**глутесспроперти**</span><span class="sxs-lookup"><span data-stu-id="b97ba-136">**gluTessProperty**</span></span>](glutessproperty.md)
</dt> </dl>

 

 





