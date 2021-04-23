---
title: Функция Глженлистс (GL. h)
description: Функция Глженлистс создает непрерывный набор пустых списков вывода.
ms.assetid: 07a97e89-1fbe-4405-b1b0-c4c47b098633
keywords:
- Функция Глженлистс OpenGL
topic_type:
- apiref
api_name:
- glGenLists
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc556e789da9c768a7ed1aef6880ad48022a1ee4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801510"
---
# <a name="glgenlists-function"></a><span data-ttu-id="f54ba-104">Функция Глженлистс</span><span class="sxs-lookup"><span data-stu-id="f54ba-104">glGenLists function</span></span>

<span data-ttu-id="f54ba-105">Функция **глженлистс** создает непрерывный набор пустых списков вывода.</span><span class="sxs-lookup"><span data-stu-id="f54ba-105">The **glGenLists** function generates a contiguous set of empty display lists.</span></span>

## <a name="syntax"></a><span data-ttu-id="f54ba-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f54ba-106">Syntax</span></span>


```C++
GLuint WINAPI glGenLists(
   GLsizei range
);
```



## <a name="parameters"></a><span data-ttu-id="f54ba-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="f54ba-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f54ba-108">*range*</span><span class="sxs-lookup"><span data-stu-id="f54ba-108">*range*</span></span> 
</dt> <dd>

<span data-ttu-id="f54ba-109">Количество смежных пустых списков вывода, которые должны быть созданы.</span><span class="sxs-lookup"><span data-stu-id="f54ba-109">The number of contiguous empty display lists to be generated.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="f54ba-110">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="f54ba-110">Error codes</span></span>

<span data-ttu-id="f54ba-111">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="f54ba-111">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="f54ba-112">Имя</span><span class="sxs-lookup"><span data-stu-id="f54ba-112">Name</span></span>                                                                                                  | <span data-ttu-id="f54ba-113">Значение</span><span class="sxs-lookup"><span data-stu-id="f54ba-113">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f54ba-114"><dt>**\_недопустимое \_ значение GL**</dt></span><span class="sxs-lookup"><span data-stu-id="f54ba-114"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="f54ba-115">*диапазон* был отрицательным.</span><span class="sxs-lookup"><span data-stu-id="f54ba-115">*range* was negative.</span></span><br/>                                                                                                      |
| <dl> <span data-ttu-id="f54ba-116"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="f54ba-116"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="f54ba-117">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="f54ba-117">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="f54ba-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f54ba-118">Remarks</span></span>

<span data-ttu-id="f54ba-119">Функция **глженлистс** имеет один аргумент, *Range*.</span><span class="sxs-lookup"><span data-stu-id="f54ba-119">The **glGenLists** function has one argument, *range*.</span></span> <span data-ttu-id="f54ba-120">Он возвращает целое число *n* , такое как *диапазон* смежных пустых списков вывода с именами *n*, *n* + 1,.</span><span class="sxs-lookup"><span data-stu-id="f54ba-120">It returns an integer *n* such that *range* contiguous empty display lists, named *n*, *n* + 1, .</span></span> <span data-ttu-id="f54ba-121">.</span><span class="sxs-lookup"><span data-stu-id="f54ba-121">.</span></span> <span data-ttu-id="f54ba-122">., *n* + (*Range* -1) создаются.</span><span class="sxs-lookup"><span data-stu-id="f54ba-122">., *n* + (*range* - 1), are created.</span></span> <span data-ttu-id="f54ba-123">Если значение *Range* равно нулю, то при отсутствии доступной группы из *диапазона* смежных имен или при возникновении ошибки, списки отображений не создаются и возвращается ноль.</span><span class="sxs-lookup"><span data-stu-id="f54ba-123">If *range* is zero, if there is no group of *range* contiguous names available, or if any error is generated, then no display lists are generated and zero is returned.</span></span>

<span data-ttu-id="f54ba-124">Следующая функция получает сведения, связанные с **глженлистс**:</span><span class="sxs-lookup"><span data-stu-id="f54ba-124">The following function retrieves information related to **glGenLists**:</span></span>

[<span data-ttu-id="f54ba-125">**глислист**</span><span class="sxs-lookup"><span data-stu-id="f54ba-125">**glIsList**</span></span>](glislist.md)

## <a name="requirements"></a><span data-ttu-id="f54ba-126">Требования</span><span class="sxs-lookup"><span data-stu-id="f54ba-126">Requirements</span></span>



| <span data-ttu-id="f54ba-127">Требование</span><span class="sxs-lookup"><span data-stu-id="f54ba-127">Requirement</span></span> | <span data-ttu-id="f54ba-128">Значение</span><span class="sxs-lookup"><span data-stu-id="f54ba-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f54ba-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f54ba-129">Minimum supported client</span></span><br/> | <span data-ttu-id="f54ba-130">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f54ba-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="f54ba-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f54ba-131">Minimum supported server</span></span><br/> | <span data-ttu-id="f54ba-132">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f54ba-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f54ba-133">Заголовок</span><span class="sxs-lookup"><span data-stu-id="f54ba-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="f54ba-134"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="f54ba-134"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="f54ba-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f54ba-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="f54ba-136"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f54ba-136"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="f54ba-137">DLL</span><span class="sxs-lookup"><span data-stu-id="f54ba-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f54ba-138"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f54ba-138"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f54ba-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f54ba-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f54ba-140">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="f54ba-140">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="f54ba-141">**глкалллист**</span><span class="sxs-lookup"><span data-stu-id="f54ba-141">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="f54ba-142">**глкалллистс**</span><span class="sxs-lookup"><span data-stu-id="f54ba-142">**glCallLists**</span></span>](glcalllists.md)
</dt> <dt>

[<span data-ttu-id="f54ba-143">**глделетелистс**</span><span class="sxs-lookup"><span data-stu-id="f54ba-143">**glDeleteLists**</span></span>](gldeletelists.md)
</dt> <dt>

[<span data-ttu-id="f54ba-144">**гленд**</span><span class="sxs-lookup"><span data-stu-id="f54ba-144">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="f54ba-145">**глислист**</span><span class="sxs-lookup"><span data-stu-id="f54ba-145">**glIsList**</span></span>](glislist.md)
</dt> <dt>

[<span data-ttu-id="f54ba-146">**глневлист**</span><span class="sxs-lookup"><span data-stu-id="f54ba-146">**glNewList**</span></span>](glnewlist.md)
</dt> </dl>

 

 





