---
title: Функция Глислист (GL. h)
description: Функция Гллслист проверяет наличие списка отображений.
ms.assetid: 86ef3684-8047-4ee4-befd-ec26bcd036c3
keywords:
- Функция Глислист OpenGL
topic_type:
- apiref
api_name:
- glIsList
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fdc67d0a7dad18f8850c283f0d5eb224ff9ebbd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341035"
---
# <a name="glislist-function"></a><span data-ttu-id="36f72-104">Функция Глислист</span><span class="sxs-lookup"><span data-stu-id="36f72-104">glIsList function</span></span>

<span data-ttu-id="36f72-105">Функция **гллслист** проверяет наличие списка отображений.</span><span class="sxs-lookup"><span data-stu-id="36f72-105">The **gllsList** function tests for display list existence.</span></span>

## <a name="syntax"></a><span data-ttu-id="36f72-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="36f72-106">Syntax</span></span>


```C++
GLboolean WINAPI glIsList(
   GLuint list
);
```



## <a name="parameters"></a><span data-ttu-id="36f72-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="36f72-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36f72-108">*list*</span><span class="sxs-lookup"><span data-stu-id="36f72-108">*list*</span></span> 
</dt> <dd>

<span data-ttu-id="36f72-109">Потенциальное имя списка дисплеев.</span><span class="sxs-lookup"><span data-stu-id="36f72-109">A potential display list name.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="36f72-110">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="36f72-110">Error codes</span></span>

<span data-ttu-id="36f72-111">С помощью функции [**глжетеррор**](glgeterror.md) можно получить следующий код ошибки.</span><span class="sxs-lookup"><span data-stu-id="36f72-111">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="36f72-112">Имя</span><span class="sxs-lookup"><span data-stu-id="36f72-112">Name</span></span>                                                                                                  | <span data-ttu-id="36f72-113">Значение</span><span class="sxs-lookup"><span data-stu-id="36f72-113">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="36f72-114"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="36f72-114"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="36f72-115">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="36f72-115">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="36f72-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="36f72-116">Remarks</span></span>

<span data-ttu-id="36f72-117">Функция **гллслист** ВОЗВРАЩАЕТ значение GL \_ true, если *List* является именем списка отображаемых данных, и возвращает \_ значение GL false в противном случае.</span><span class="sxs-lookup"><span data-stu-id="36f72-117">The **gllsList** function returns GL\_TRUE if *list* is the name of a display list and returns GL\_FALSE otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="36f72-118">Требования</span><span class="sxs-lookup"><span data-stu-id="36f72-118">Requirements</span></span>



| <span data-ttu-id="36f72-119">Требование</span><span class="sxs-lookup"><span data-stu-id="36f72-119">Requirement</span></span> | <span data-ttu-id="36f72-120">Значение</span><span class="sxs-lookup"><span data-stu-id="36f72-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="36f72-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="36f72-121">Minimum supported client</span></span><br/> | <span data-ttu-id="36f72-122">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="36f72-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="36f72-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="36f72-123">Minimum supported server</span></span><br/> | <span data-ttu-id="36f72-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="36f72-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="36f72-125">Заголовок</span><span class="sxs-lookup"><span data-stu-id="36f72-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="36f72-126"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="36f72-126"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="36f72-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="36f72-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="36f72-128"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="36f72-128"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="36f72-129">DLL</span><span class="sxs-lookup"><span data-stu-id="36f72-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="36f72-130"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="36f72-130"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36f72-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="36f72-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36f72-132">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="36f72-132">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="36f72-133">**глкалллист**</span><span class="sxs-lookup"><span data-stu-id="36f72-133">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="36f72-134">**глкалллистс**</span><span class="sxs-lookup"><span data-stu-id="36f72-134">**glCallLists**</span></span>](glcalllists.md)
</dt> <dt>

[<span data-ttu-id="36f72-135">**глделетелистс**</span><span class="sxs-lookup"><span data-stu-id="36f72-135">**glDeleteLists**</span></span>](gldeletelists.md)
</dt> <dt>

[<span data-ttu-id="36f72-136">**гленд**</span><span class="sxs-lookup"><span data-stu-id="36f72-136">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="36f72-137">**глженлистс**</span><span class="sxs-lookup"><span data-stu-id="36f72-137">**glGenLists**</span></span>](glgenlists.md)
</dt> <dt>

[<span data-ttu-id="36f72-138">**глневлист**</span><span class="sxs-lookup"><span data-stu-id="36f72-138">**glNewList**</span></span>](glnewlist.md)
</dt> </dl>

 

 





