---
title: Функция Глиндексмаск (GL. h)
description: Функция Глиндексмаск управляет записью отдельных битов в буферах цветового индекса.
ms.assetid: f4b5df36-390f-4254-95fb-98589750a11b
keywords:
- Функция Глиндексмаск OpenGL
topic_type:
- apiref
api_name:
- glIndexMask
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d426cb1f4bb2e794bef53853d0336db1d64b263
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661840"
---
# <a name="glindexmask-function"></a><span data-ttu-id="a5091-104">Функция Глиндексмаск</span><span class="sxs-lookup"><span data-stu-id="a5091-104">glIndexMask function</span></span>

<span data-ttu-id="a5091-105">Функция **глиндексмаск** управляет записью отдельных битов в буферах цветового индекса.</span><span class="sxs-lookup"><span data-stu-id="a5091-105">The **glIndexMask** function controls the writing of individual bits in the color-index buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5091-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a5091-106">Syntax</span></span>


```C++
void WINAPI glIndexMask(
   GLuint mask
);
```



## <a name="parameters"></a><span data-ttu-id="a5091-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="a5091-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5091-108">*виде*</span><span class="sxs-lookup"><span data-stu-id="a5091-108">*mask*</span></span> 
</dt> <dd>

<span data-ttu-id="a5091-109">Битовая маска для включения и отключения записи отдельных битов в буферах цветового индекса.</span><span class="sxs-lookup"><span data-stu-id="a5091-109">A bit mask to enable and disable the writing of individual bits in the color-index buffers.</span></span> <span data-ttu-id="a5091-110">Изначально маска все равно.</span><span class="sxs-lookup"><span data-stu-id="a5091-110">Initially, the mask is all ones.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5091-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a5091-111">Return value</span></span>

<span data-ttu-id="a5091-112">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="a5091-112">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a5091-113">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="a5091-113">Error codes</span></span>

<span data-ttu-id="a5091-114">С помощью функции [**глжетеррор**](glgeterror.md) можно получить следующий код ошибки.</span><span class="sxs-lookup"><span data-stu-id="a5091-114">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="a5091-115">Имя</span><span class="sxs-lookup"><span data-stu-id="a5091-115">Name</span></span>                                                                                                  | <span data-ttu-id="a5091-116">Значение</span><span class="sxs-lookup"><span data-stu-id="a5091-116">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a5091-117"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="a5091-117"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="a5091-118">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="a5091-118">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="a5091-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a5091-119">Remarks</span></span>

<span data-ttu-id="a5091-120">Функция **глиндексмаск** управляет записью отдельных битов в буферах цветового индекса.</span><span class="sxs-lookup"><span data-stu-id="a5091-120">The **glIndexMask** function controls the writing of individual bits in the color-index buffers.</span></span> <span data-ttu-id="a5091-121">Наименее важные *n* бит *маски*, где *1* — число битов в буфере цветового индекса, укажите маску.</span><span class="sxs-lookup"><span data-stu-id="a5091-121">The least significant *n* bits of *mask*, where *1* is the number of bits in a color-index buffer, specify a mask.</span></span> <span data-ttu-id="a5091-122">Когда в маске появляется один из них, соответствующий бит в буфере цветового индекса (или в буферах) становится доступным для записи.</span><span class="sxs-lookup"><span data-stu-id="a5091-122">Wherever a one appears in the mask, the corresponding bit in the color-index buffer (or buffers) is made writable.</span></span> <span data-ttu-id="a5091-123">Если отображается ноль, бит защищен от записи.</span><span class="sxs-lookup"><span data-stu-id="a5091-123">Where a zero appears, the bit is write-protected.</span></span>

<span data-ttu-id="a5091-124">Эта маска используется только в режиме индексов цвета и влияет только на буферы, выбранные для записи (см. [**глдравбуффер**](gldrawbuffer.md)).</span><span class="sxs-lookup"><span data-stu-id="a5091-124">This mask is used only in color-index mode, and it affects only the buffers currently selected for writing (see [**glDrawBuffer**](gldrawbuffer.md)).</span></span> <span data-ttu-id="a5091-125">Изначально все биты включены для записи.</span><span class="sxs-lookup"><span data-stu-id="a5091-125">Initially, all bits are enabled for writing.</span></span>

<span data-ttu-id="a5091-126">Следующая функция получает сведения, связанные с **глиндексмаск**:</span><span class="sxs-lookup"><span data-stu-id="a5091-126">The following function retrieves information related to **glIndexMask**:</span></span>

<span data-ttu-id="a5091-127">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом GL \_ index \_ вритемаск</span><span class="sxs-lookup"><span data-stu-id="a5091-127">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_INDEX\_WRITEMASK</span></span>

## <a name="requirements"></a><span data-ttu-id="a5091-128">Требования</span><span class="sxs-lookup"><span data-stu-id="a5091-128">Requirements</span></span>



| <span data-ttu-id="a5091-129">Требование</span><span class="sxs-lookup"><span data-stu-id="a5091-129">Requirement</span></span> | <span data-ttu-id="a5091-130">Значение</span><span class="sxs-lookup"><span data-stu-id="a5091-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a5091-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a5091-131">Minimum supported client</span></span><br/> | <span data-ttu-id="a5091-132">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a5091-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a5091-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a5091-133">Minimum supported server</span></span><br/> | <span data-ttu-id="a5091-134">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a5091-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a5091-135">Заголовок</span><span class="sxs-lookup"><span data-stu-id="a5091-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5091-136"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5091-136"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="a5091-137">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a5091-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="a5091-138"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a5091-138"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="a5091-139">DLL</span><span class="sxs-lookup"><span data-stu-id="a5091-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a5091-140"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a5091-140"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5091-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a5091-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5091-142">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="a5091-142">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="a5091-143">**глдепсмаск**</span><span class="sxs-lookup"><span data-stu-id="a5091-143">**glDepthMask**</span></span>](gldepthmask.md)
</dt> <dt>

[<span data-ttu-id="a5091-144">**глдравбуффер**</span><span class="sxs-lookup"><span data-stu-id="a5091-144">**glDrawBuffer**</span></span>](gldrawbuffer.md)
</dt> <dt>

[<span data-ttu-id="a5091-145">**гленд**</span><span class="sxs-lookup"><span data-stu-id="a5091-145">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="a5091-146">**глиндекс**</span><span class="sxs-lookup"><span data-stu-id="a5091-146">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="a5091-147">**глстенЦилмаск**</span><span class="sxs-lookup"><span data-stu-id="a5091-147">**glStencilMask**</span></span>](glstencilmask.md)
</dt> </dl>

 

 





