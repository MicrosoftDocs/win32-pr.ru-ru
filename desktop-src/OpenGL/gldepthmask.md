---
title: Функция Глдепсмаск (GL. h)
description: Функция Глдепсмаск включает или отключает запись в буфер глубины.
ms.assetid: 067b18e2-f21a-4dde-8fa6-dd975746e189
keywords:
- Функция Глдепсмаск OpenGL
topic_type:
- apiref
api_name:
- glDepthMask
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5873d517770f1ce61f9a2eaad3ea7cce7b4fd7ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415692"
---
# <a name="gldepthmask-function"></a><span data-ttu-id="19d75-104">Функция Глдепсмаск</span><span class="sxs-lookup"><span data-stu-id="19d75-104">glDepthMask function</span></span>

<span data-ttu-id="19d75-105">Функция **глдепсмаск** включает или отключает запись в буфер глубины.</span><span class="sxs-lookup"><span data-stu-id="19d75-105">The **glDepthMask** function enables or disables writing into the depth buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="19d75-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="19d75-106">Syntax</span></span>


```C++
void WINAPI glDepthMask(
   GLboolean flag
);
```



## <a name="parameters"></a><span data-ttu-id="19d75-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="19d75-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19d75-108">*flag*</span><span class="sxs-lookup"><span data-stu-id="19d75-108">*flag*</span></span> 
</dt> <dd>

<span data-ttu-id="19d75-109">Указывает, разрешена ли запись в буфер глубины.</span><span class="sxs-lookup"><span data-stu-id="19d75-109">Specifies whether the depth buffer is enabled for writing.</span></span> <span data-ttu-id="19d75-110">Если *флаг* равен нулю, запись в буфер глубины отключена.</span><span class="sxs-lookup"><span data-stu-id="19d75-110">If *flag* is zero, depth-buffer writing is disabled.</span></span> <span data-ttu-id="19d75-111">В противном случае он будет включен.</span><span class="sxs-lookup"><span data-stu-id="19d75-111">Otherwise, it is enabled.</span></span> <span data-ttu-id="19d75-112">Изначально запись в буфере глубины включена.</span><span class="sxs-lookup"><span data-stu-id="19d75-112">Initially, depth-buffer writing is enabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19d75-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="19d75-113">Return value</span></span>

<span data-ttu-id="19d75-114">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="19d75-114">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="19d75-115">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="19d75-115">Error codes</span></span>

<span data-ttu-id="19d75-116">С помощью функции [**глжетеррор**](glgeterror.md) можно получить следующий код ошибки.</span><span class="sxs-lookup"><span data-stu-id="19d75-116">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="19d75-117">Имя</span><span class="sxs-lookup"><span data-stu-id="19d75-117">Name</span></span>                                                                                                  | <span data-ttu-id="19d75-118">Значение</span><span class="sxs-lookup"><span data-stu-id="19d75-118">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="19d75-119"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="19d75-119"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="19d75-120">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="19d75-120">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="19d75-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="19d75-121">Remarks</span></span>

<span data-ttu-id="19d75-122">Следующая функция получает сведения, связанные с **глдепсмаск**:</span><span class="sxs-lookup"><span data-stu-id="19d75-122">The following function retrieves information related to **glDepthMask**:</span></span>

<span data-ttu-id="19d75-123">**глжет** с аргументом GL \_ Depth \_ вритемаск</span><span class="sxs-lookup"><span data-stu-id="19d75-123">**glGet** with argument GL\_DEPTH\_WRITEMASK</span></span>

## <a name="requirements"></a><span data-ttu-id="19d75-124">Требования</span><span class="sxs-lookup"><span data-stu-id="19d75-124">Requirements</span></span>



| <span data-ttu-id="19d75-125">Требование</span><span class="sxs-lookup"><span data-stu-id="19d75-125">Requirement</span></span> | <span data-ttu-id="19d75-126">Значение</span><span class="sxs-lookup"><span data-stu-id="19d75-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="19d75-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="19d75-127">Minimum supported client</span></span><br/> | <span data-ttu-id="19d75-128">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="19d75-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="19d75-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="19d75-129">Minimum supported server</span></span><br/> | <span data-ttu-id="19d75-130">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="19d75-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="19d75-131">Заголовок</span><span class="sxs-lookup"><span data-stu-id="19d75-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="19d75-132"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="19d75-132"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="19d75-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="19d75-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="19d75-134"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="19d75-134"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="19d75-135">DLL</span><span class="sxs-lookup"><span data-stu-id="19d75-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19d75-136"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19d75-136"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19d75-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="19d75-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19d75-138">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="19d75-138">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="19d75-139">**глколормаск**</span><span class="sxs-lookup"><span data-stu-id="19d75-139">**glColorMask**</span></span>](glcolormask.md)
</dt> <dt>

[<span data-ttu-id="19d75-140">**глдепсфунк**</span><span class="sxs-lookup"><span data-stu-id="19d75-140">**glDepthFunc**</span></span>](gldepthfunc.md)
</dt> <dt>

[<span data-ttu-id="19d75-141">**глдепсранже**</span><span class="sxs-lookup"><span data-stu-id="19d75-141">**glDepthRange**</span></span>](gldepthrange.md)
</dt> <dt>

[<span data-ttu-id="19d75-142">**гленд**</span><span class="sxs-lookup"><span data-stu-id="19d75-142">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="19d75-143">**глжет**</span><span class="sxs-lookup"><span data-stu-id="19d75-143">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="19d75-144">**глиндексмаск**</span><span class="sxs-lookup"><span data-stu-id="19d75-144">**glIndexMask**</span></span>](glindexmask.md)
</dt> <dt>

[<span data-ttu-id="19d75-145">**глстенЦилмаск**</span><span class="sxs-lookup"><span data-stu-id="19d75-145">**glStencilMask**</span></span>](glstencilmask.md)
</dt> </dl>

 

 





