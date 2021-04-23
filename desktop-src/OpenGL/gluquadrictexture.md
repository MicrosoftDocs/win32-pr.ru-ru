---
title: Функция Глукуадриктекстуре (GLU. h)
description: Функция Глукуадриктекстуре указывает, следует ли затекстурировать куадрикс.
ms.assetid: 11681497-f099-4856-a0ac-6a44abd3e1a1
keywords:
- Функция Глукуадриктекстуре OpenGL
topic_type:
- apiref
api_name:
- gluQuadricTexture
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0cc395564b6c6f30f38a8c5129c489d0bfca6b80
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136731"
---
# <a name="gluquadrictexture-function"></a><span data-ttu-id="52691-104">Функция Глукуадриктекстуре</span><span class="sxs-lookup"><span data-stu-id="52691-104">gluQuadricTexture function</span></span>

<span data-ttu-id="52691-105">Функция **глукуадриктекстуре** указывает, следует ли затекстурировать куадрикс.</span><span class="sxs-lookup"><span data-stu-id="52691-105">The **gluQuadricTexture** function specifies whether quadrics are to be textured.</span></span>

## <a name="syntax"></a><span data-ttu-id="52691-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="52691-106">Syntax</span></span>


```C++
void WINAPI gluQuadricTexture(
   GLUquadric *quadObject,
   GLboolean  textureCoords
);
```



## <a name="parameters"></a><span data-ttu-id="52691-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="52691-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52691-108">*куадобжект*</span><span class="sxs-lookup"><span data-stu-id="52691-108">*quadObject*</span></span> 
</dt> <dd>

<span data-ttu-id="52691-109">Объект куадрик (созданный с помощью [**глуневкуадрик**](glunewquadric.md)).</span><span class="sxs-lookup"><span data-stu-id="52691-109">The quadric object (created with [**gluNewQuadric**](glunewquadric.md)).</span></span>

</dd> <dt>

<span data-ttu-id="52691-110">*текстурекурдс*</span><span class="sxs-lookup"><span data-stu-id="52691-110">*textureCoords*</span></span> 
</dt> <dd>

<span data-ttu-id="52691-111">Флаг, указывающий, должны ли создаваться координаты текстуры.</span><span class="sxs-lookup"><span data-stu-id="52691-111">A flag indicating whether texture coordinates are to be generated.</span></span> <span data-ttu-id="52691-112">Допустимы следующие значения.</span><span class="sxs-lookup"><span data-stu-id="52691-112">The following values are valid.</span></span>



| <span data-ttu-id="52691-113">Значение</span><span class="sxs-lookup"><span data-stu-id="52691-113">Value</span></span>                                                                                                                                          | <span data-ttu-id="52691-114">Значение</span><span class="sxs-lookup"><span data-stu-id="52691-114">Meaning</span></span>                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span id="GL_TRUE"></span><span id="gl_true"></span><dl> <span data-ttu-id="52691-115"><dt>**значение по ГК \_**</dt></span><span class="sxs-lookup"><span data-stu-id="52691-115"><dt>**GL\_TRUE**</dt></span></span> </dl>    | <span data-ttu-id="52691-116">Создание координат текстуры.</span><span class="sxs-lookup"><span data-stu-id="52691-116">Generate texture coordinates.</span></span><br/>                                   |
| <span id="GL_FALSE"></span><span id="gl_false"></span><dl> <span data-ttu-id="52691-117"><dt>**GL, \_ значение false**</dt></span><span class="sxs-lookup"><span data-stu-id="52691-117"><dt>**GL\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="52691-118">Не создавайте координаты текстуры.</span><span class="sxs-lookup"><span data-stu-id="52691-118">Do not generate texture coordinates.</span></span> <span data-ttu-id="52691-119">Это значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="52691-119">This is the default value.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52691-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="52691-120">Return value</span></span>

<span data-ttu-id="52691-121">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="52691-121">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="52691-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="52691-122">Remarks</span></span>

<span data-ttu-id="52691-123">Функция **глукуадриктекстуре** указывает, должны ли создаваться координаты текстуры для куадрикс, отображаемого с помощью **куадобжект**.</span><span class="sxs-lookup"><span data-stu-id="52691-123">The **gluQuadricTexture** function specifies whether texture coordinates are to be generated for quadrics rendered with **quadObject**.</span></span>

<span data-ttu-id="52691-124">Способ формирования координат текстуры зависит от конкретного куадрик, подготовленного к просмотру.</span><span class="sxs-lookup"><span data-stu-id="52691-124">The manner in which texture coordinates are generated depends upon the specific quadric rendered.</span></span>

## <a name="requirements"></a><span data-ttu-id="52691-125">Требования</span><span class="sxs-lookup"><span data-stu-id="52691-125">Requirements</span></span>



| <span data-ttu-id="52691-126">Требование</span><span class="sxs-lookup"><span data-stu-id="52691-126">Requirement</span></span> | <span data-ttu-id="52691-127">Значение</span><span class="sxs-lookup"><span data-stu-id="52691-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="52691-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="52691-128">Minimum supported client</span></span><br/> | <span data-ttu-id="52691-129">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="52691-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="52691-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="52691-130">Minimum supported server</span></span><br/> | <span data-ttu-id="52691-131">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="52691-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="52691-132">Заголовок</span><span class="sxs-lookup"><span data-stu-id="52691-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="52691-133"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="52691-133"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="52691-134">Библиотека</span><span class="sxs-lookup"><span data-stu-id="52691-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="52691-135"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="52691-135"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="52691-136">DLL</span><span class="sxs-lookup"><span data-stu-id="52691-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="52691-137"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="52691-137"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52691-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="52691-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52691-139">**глуневкуадрик**</span><span class="sxs-lookup"><span data-stu-id="52691-139">**gluNewQuadric**</span></span>](glunewquadric.md)
</dt> <dt>

[<span data-ttu-id="52691-140">**глукуадрикдравстиле**</span><span class="sxs-lookup"><span data-stu-id="52691-140">**gluQuadricDrawStyle**</span></span>](gluquadricdrawstyle.md)
</dt> <dt>

[<span data-ttu-id="52691-141">**глукуадрикнормалс**</span><span class="sxs-lookup"><span data-stu-id="52691-141">**gluQuadricNormals**</span></span>](gluquadricnormals.md)
</dt> </dl>

 

 





