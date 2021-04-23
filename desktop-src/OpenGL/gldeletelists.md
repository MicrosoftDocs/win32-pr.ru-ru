---
title: Функция Глделетелистс (GL. h)
description: Функция Глделетелистс удаляет смежную группу списков вывода.
ms.assetid: 979ab352-99db-4822-922c-a1813b9fcfce
keywords:
- Функция Глделетелистс OpenGL
topic_type:
- apiref
api_name:
- glDeleteLists
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c11ae41273cba5bd050a62ea330cef9da0647769
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672689"
---
# <a name="gldeletelists-function"></a><span data-ttu-id="a3c8f-104">Функция Глделетелистс</span><span class="sxs-lookup"><span data-stu-id="a3c8f-104">glDeleteLists function</span></span>

<span data-ttu-id="a3c8f-105">Функция **глделетелистс** удаляет смежную группу списков вывода.</span><span class="sxs-lookup"><span data-stu-id="a3c8f-105">The **glDeleteLists** function deletes a contiguous group of display lists.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3c8f-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a3c8f-106">Syntax</span></span>


```C++
void WINAPI glDeleteLists(
   GLuint  list,
   GLsizei range
);
```



## <a name="parameters"></a><span data-ttu-id="a3c8f-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="a3c8f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3c8f-108">*list*</span><span class="sxs-lookup"><span data-stu-id="a3c8f-108">*list*</span></span> 
</dt> <dd>

<span data-ttu-id="a3c8f-109">Целочисленное имя первого списка отображаемых элементов для удаления.</span><span class="sxs-lookup"><span data-stu-id="a3c8f-109">The integer name of the first display list to delete.</span></span>

</dd> <dt>

<span data-ttu-id="a3c8f-110">*range*</span><span class="sxs-lookup"><span data-stu-id="a3c8f-110">*range*</span></span> 
</dt> <dd>

<span data-ttu-id="a3c8f-111">Число удаляемых списков вывода.</span><span class="sxs-lookup"><span data-stu-id="a3c8f-111">The number of display lists to delete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3c8f-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a3c8f-112">Return value</span></span>

<span data-ttu-id="a3c8f-113">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="a3c8f-113">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a3c8f-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="a3c8f-114">Error codes</span></span>

<span data-ttu-id="a3c8f-115">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="a3c8f-115">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="a3c8f-116">Имя</span><span class="sxs-lookup"><span data-stu-id="a3c8f-116">Name</span></span>                                                                                                  | <span data-ttu-id="a3c8f-117">Значение</span><span class="sxs-lookup"><span data-stu-id="a3c8f-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a3c8f-118"><dt>**\_недопустимое \_ значение GL**</dt></span><span class="sxs-lookup"><span data-stu-id="a3c8f-118"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="a3c8f-119">*диапазон* был отрицательным.</span><span class="sxs-lookup"><span data-stu-id="a3c8f-119">*range* was negative.</span></span><br/>                                                                                                      |
| <dl> <span data-ttu-id="a3c8f-120"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="a3c8f-120"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="a3c8f-121">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="a3c8f-121">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="a3c8f-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a3c8f-122">Remarks</span></span>

<span data-ttu-id="a3c8f-123">Функция **глделетелистс** приводит к удалению непрерывной группы списков вывода.</span><span class="sxs-lookup"><span data-stu-id="a3c8f-123">The **glDeleteLists** function causes a contiguous group of display lists to be deleted.</span></span> <span data-ttu-id="a3c8f-124">Параметр *List* — это имя первого списка, который необходимо удалить, а *Range* — число удаляемых списков.</span><span class="sxs-lookup"><span data-stu-id="a3c8f-124">The *list* parameter is the name of the first display list to be deleted, and *range* is the number of display lists to delete.</span></span> <span data-ttu-id="a3c8f-125">Все списки дисплеев  с   =    =    +  *диапазоном* list d List-1 удалены.</span><span class="sxs-lookup"><span data-stu-id="a3c8f-125">All display lists *d* with *list* = *d* = *list* + *range* - 1 are deleted.</span></span>

<span data-ttu-id="a3c8f-126">Освобождаются все места хранения, выделенные для указанных списков дисплеев, и имена, доступные для повторного использования, можно использовать позднее.</span><span class="sxs-lookup"><span data-stu-id="a3c8f-126">All storage locations allocated to the specified display lists are freed, and the names are available for reuse at a later time.</span></span> <span data-ttu-id="a3c8f-127">Имена в диапазоне, не имеющие связанного списка отображений, игнорируются.</span><span class="sxs-lookup"><span data-stu-id="a3c8f-127">Names within the range that do not have an associated display list are ignored.</span></span> <span data-ttu-id="a3c8f-128">Если *Range* равен нулю, ничего не происходит.</span><span class="sxs-lookup"><span data-stu-id="a3c8f-128">If *range* is zero, nothing happens.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3c8f-129">Требования</span><span class="sxs-lookup"><span data-stu-id="a3c8f-129">Requirements</span></span>



| <span data-ttu-id="a3c8f-130">Требование</span><span class="sxs-lookup"><span data-stu-id="a3c8f-130">Requirement</span></span> | <span data-ttu-id="a3c8f-131">Значение</span><span class="sxs-lookup"><span data-stu-id="a3c8f-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a3c8f-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a3c8f-132">Minimum supported client</span></span><br/> | <span data-ttu-id="a3c8f-133">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a3c8f-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a3c8f-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a3c8f-134">Minimum supported server</span></span><br/> | <span data-ttu-id="a3c8f-135">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a3c8f-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a3c8f-136">Заголовок</span><span class="sxs-lookup"><span data-stu-id="a3c8f-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3c8f-137"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3c8f-137"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="a3c8f-138">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a3c8f-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="a3c8f-139"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a3c8f-139"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="a3c8f-140">DLL</span><span class="sxs-lookup"><span data-stu-id="a3c8f-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a3c8f-141"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a3c8f-141"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3c8f-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a3c8f-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3c8f-143">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="a3c8f-143">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="a3c8f-144">**глкалллист**</span><span class="sxs-lookup"><span data-stu-id="a3c8f-144">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="a3c8f-145">**глкалллистс**</span><span class="sxs-lookup"><span data-stu-id="a3c8f-145">**glCallLists**</span></span>](glcalllists.md)
</dt> <dt>

[<span data-ttu-id="a3c8f-146">**гленд**</span><span class="sxs-lookup"><span data-stu-id="a3c8f-146">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="a3c8f-147">**глженлистс**</span><span class="sxs-lookup"><span data-stu-id="a3c8f-147">**glGenLists**</span></span>](glgenlists.md)
</dt> <dt>

[<span data-ttu-id="a3c8f-148">**глислист**</span><span class="sxs-lookup"><span data-stu-id="a3c8f-148">**glIsList**</span></span>](glislist.md)
</dt> <dt>

[<span data-ttu-id="a3c8f-149">**глневлист**</span><span class="sxs-lookup"><span data-stu-id="a3c8f-149">**glNewList**</span></span>](glnewlist.md)
</dt> </dl>

 

 





