---
title: Функция Глпопклиентаттриб (GL. h)
description: Функции Глпушклиентаттриб и Глпопклиентаттриб сохраняют и восстанавливают группы клиентских переменных состояния в стеке Client-Attribute. | Функция Глпопклиентаттриб (GL. h)
ms.assetid: 030a3955-35bf-4862-9691-54b0c24514e8
keywords:
- Функция Глпопклиентаттриб OpenGL
topic_type:
- apiref
api_name:
- glPopClientAttrib
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e9f09e9c7292754a736594a9bf3d57a70063744
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353352"
---
# <a name="glpopclientattrib-function"></a><span data-ttu-id="cf1b2-105">Функция Глпопклиентаттриб</span><span class="sxs-lookup"><span data-stu-id="cf1b2-105">glPopClientAttrib function</span></span>

<span data-ttu-id="cf1b2-106">Функции [**глпушклиентаттриб**](glpushclientattrib.md) и **глпопклиентаттриб** сохраняют и восстанавливают группы клиентских переменных состояния в стеке Client-Attribute.</span><span class="sxs-lookup"><span data-stu-id="cf1b2-106">The [**glPushClientAttrib**](glpushclientattrib.md) and **glPopClientAttrib** functions save and restore groups of client-state variables on the client-attribute stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf1b2-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cf1b2-107">Syntax</span></span>


```C++
void WINAPI glPopClientAttrib(void);
```



## <a name="parameters"></a><span data-ttu-id="cf1b2-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="cf1b2-108">Parameters</span></span>

<span data-ttu-id="cf1b2-109">У этой функции нет параметров.</span><span class="sxs-lookup"><span data-stu-id="cf1b2-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cf1b2-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cf1b2-110">Return value</span></span>

<span data-ttu-id="cf1b2-111">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="cf1b2-111">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="cf1b2-112">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="cf1b2-112">Error codes</span></span>

<span data-ttu-id="cf1b2-113">С помощью функции [**глжетеррор**](glgeterror.md) можно получить следующий код ошибки.</span><span class="sxs-lookup"><span data-stu-id="cf1b2-113">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="cf1b2-114">Имя</span><span class="sxs-lookup"><span data-stu-id="cf1b2-114">Name</span></span>                                                                                               | <span data-ttu-id="cf1b2-115">Значение</span><span class="sxs-lookup"><span data-stu-id="cf1b2-115">Meaning</span></span>                                                                       |
|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="cf1b2-116"><dt>**\_переполнение стека GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cf1b2-116"><dt>**GL\_STACK\_OVERFLOW**</dt></span></span> </dl> | <span data-ttu-id="cf1b2-117">Функция была вызвана во время заполнения стека клиентского атрибута.</span><span class="sxs-lookup"><span data-stu-id="cf1b2-117">The function was called while the client-attribute stack was full.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="cf1b2-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cf1b2-118">Remarks</span></span>

<span data-ttu-id="cf1b2-119">Функция **глпушклиентаттриб** использует параметр маски, чтобы определить, какие группы переменных клиентского состояния сохраняются в стеке Client-Attribute.</span><span class="sxs-lookup"><span data-stu-id="cf1b2-119">The **glPushClientAttrib** function uses its mask parameter to determine which groups of client-state variables are saved on the client-attribute stack.</span></span> <span data-ttu-id="cf1b2-120">Можно использовать оператор побитового или для объединения принятых символьных констант, чтобы задать биты и создать маску.</span><span class="sxs-lookup"><span data-stu-id="cf1b2-120">You can use the bitwise OR operator to join together accepted symbolic constants to set bits and construct a mask.</span></span>

<span data-ttu-id="cf1b2-121">Функция **глпопклиентаттриб** восстанавливает значения переменных клиентского состояния, сохраненных в прошлом с помощью **глпушклиентаттриб**.</span><span class="sxs-lookup"><span data-stu-id="cf1b2-121">The **glPopClientAttrib** function restores the values of the client-state variables last saved with **glPushclientAttrib**.</span></span> <span data-ttu-id="cf1b2-122">Переменные состояния клиента, которые не были сохранены ранее, остались без изменений.</span><span class="sxs-lookup"><span data-stu-id="cf1b2-122">Client-state variables not previously saved are left unchanged.</span></span> <span data-ttu-id="cf1b2-123">При принудительной отправке атрибутов в полный стек атрибутов клиента или при извлечении атрибутов из пустого стека устанавливается флаг ошибки, а в состояние OpenGL другие изменения не вносятся.</span><span class="sxs-lookup"><span data-stu-id="cf1b2-123">Pushing attributes onto a full client-attribute stack or popping attributes off an empty stack sets an error flag and no other change is made to the OpenGL state.</span></span> <span data-ttu-id="cf1b2-124">По умолчанию стек атрибутов клиента пуст.</span><span class="sxs-lookup"><span data-stu-id="cf1b2-124">By default the client attribute stack is empty.</span></span>

<span data-ttu-id="cf1b2-125">Некоторые значения состояния клиента OpenGL не могут быть сохранены в стеке Client-Attribute.</span><span class="sxs-lookup"><span data-stu-id="cf1b2-125">Some OpenGL client-state values cannot be saved on the client-attribute stack.</span></span> <span data-ttu-id="cf1b2-126">Например, нельзя сохранить состояние SELECT или Feedback в стеке Client-Attribute.</span><span class="sxs-lookup"><span data-stu-id="cf1b2-126">For example, you cannot save the select or feedback states on the client-attribute stack.</span></span> <span data-ttu-id="cf1b2-127">Глубина стека клиентского атрибута составляет не менее 16.</span><span class="sxs-lookup"><span data-stu-id="cf1b2-127">The depth of the client-attribute stack is at least 16.</span></span>

<span data-ttu-id="cf1b2-128">Функции **глпушклиентаттриб** и **глпопклиентаттриб** не компилируются в списки вывода, но выполняются немедленно.</span><span class="sxs-lookup"><span data-stu-id="cf1b2-128">The **glPushclientAttrib** and **glPopClientAttrib** functions are not compiled into display lists, but are executed immediately.</span></span>

<span data-ttu-id="cf1b2-129">Функции **глпушклиентаттриб** и **глпопклиентаттриб** могут отправлять только режимы хранения пикселов и точки подключения точек и клиентов массива вершин.</span><span class="sxs-lookup"><span data-stu-id="cf1b2-129">The **glPushClientAttrib** and **glPopClientAttrib** functions can only push and pop pixel storage modes and vertex array client states.</span></span> <span data-ttu-id="cf1b2-130">Для отправки и POP-состояний, которые хранятся на сервере, необходимо использовать [**глпушаттриб**](glpushattrib.md) и [**глпопаттриб**](glpopattrib.md) .</span><span class="sxs-lookup"><span data-stu-id="cf1b2-130">You must use [**glPushAttrib**](glpushattrib.md) and [**glPopAttrib**](glpopattrib.md) to push and pop states that are kept on the server.</span></span>

> [!Note]  
> <span data-ttu-id="cf1b2-131">Функции **глпушклиентаттриб** и **глпопклиентаттриб** доступны только в OpenGL версии 1,1 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="cf1b2-131">The **glPushClientAttrib** and **glPopClientAttrib** functions are only available in OpenGL version 1.1 or later.</span></span>

 

<span data-ttu-id="cf1b2-132">Следующие функции извлекают сведения, относящиеся к **глпушклиентаттриб** и **глпопклиентаттриб**:</span><span class="sxs-lookup"><span data-stu-id="cf1b2-132">The following functions retrieve information related to **glPushClientAttrib** and **glPopClientAttrib**:</span></span>

<span data-ttu-id="cf1b2-133">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом \_ " \_ \_ глубина СТЕКа \_ " для клиента GL</span><span class="sxs-lookup"><span data-stu-id="cf1b2-133">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CLIENT\_ATTRIB\_STACK\_DEPTH</span></span>

<span data-ttu-id="cf1b2-134">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом \_ " \_ Максимальная \_ \_ глубина стека для клиента \_ "</span><span class="sxs-lookup"><span data-stu-id="cf1b2-134">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAX\_CLIENT\_ATTRIB\_STACK\_DEPTH</span></span>

## <a name="requirements"></a><span data-ttu-id="cf1b2-135">Требования</span><span class="sxs-lookup"><span data-stu-id="cf1b2-135">Requirements</span></span>



| <span data-ttu-id="cf1b2-136">Требование</span><span class="sxs-lookup"><span data-stu-id="cf1b2-136">Requirement</span></span> | <span data-ttu-id="cf1b2-137">Значение</span><span class="sxs-lookup"><span data-stu-id="cf1b2-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cf1b2-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cf1b2-138">Minimum supported client</span></span><br/> | <span data-ttu-id="cf1b2-139">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="cf1b2-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="cf1b2-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cf1b2-140">Minimum supported server</span></span><br/> | <span data-ttu-id="cf1b2-141">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="cf1b2-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="cf1b2-142">Заголовок</span><span class="sxs-lookup"><span data-stu-id="cf1b2-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf1b2-143"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf1b2-143"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="cf1b2-144">Библиотека</span><span class="sxs-lookup"><span data-stu-id="cf1b2-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="cf1b2-145"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cf1b2-145"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="cf1b2-146">DLL</span><span class="sxs-lookup"><span data-stu-id="cf1b2-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cf1b2-147"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf1b2-147"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf1b2-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cf1b2-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf1b2-149">**глколорпоинтер**</span><span class="sxs-lookup"><span data-stu-id="cf1b2-149">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="cf1b2-150">**глдисаблеклиентстате**</span><span class="sxs-lookup"><span data-stu-id="cf1b2-150">**glDisableClientState**</span></span>](gldisableclientstate.md)
</dt> <dt>

[<span data-ttu-id="cf1b2-151">**гледжефлагпоинтер**</span><span class="sxs-lookup"><span data-stu-id="cf1b2-151">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="cf1b2-152">**гленаблеклиентстате**</span><span class="sxs-lookup"><span data-stu-id="cf1b2-152">**glEnableClientState**</span></span>](glenableclientstate.md)
</dt> <dt>

[<span data-ttu-id="cf1b2-153">**глжет**</span><span class="sxs-lookup"><span data-stu-id="cf1b2-153">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="cf1b2-154">**глжетеррор**</span><span class="sxs-lookup"><span data-stu-id="cf1b2-154">**glGetError**</span></span>](glgeterror.md)
</dt> <dt>

[<span data-ttu-id="cf1b2-155">**глиндекспоинтер**</span><span class="sxs-lookup"><span data-stu-id="cf1b2-155">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="cf1b2-156">**глнормалпоинтер**</span><span class="sxs-lookup"><span data-stu-id="cf1b2-156">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="cf1b2-157">**глневлист**</span><span class="sxs-lookup"><span data-stu-id="cf1b2-157">**glNewList**</span></span>](glnewlist.md)
</dt> <dt>

[<span data-ttu-id="cf1b2-158">**глпикселсторе**</span><span class="sxs-lookup"><span data-stu-id="cf1b2-158">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="cf1b2-159">**глпушаттриб**</span><span class="sxs-lookup"><span data-stu-id="cf1b2-159">**glPushAttrib**</span></span>](glpushattrib.md)
</dt> <dt>

[<span data-ttu-id="cf1b2-160">**глтекскурдпоинтер**</span><span class="sxs-lookup"><span data-stu-id="cf1b2-160">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="cf1b2-161">**глвертекспоинтер**</span><span class="sxs-lookup"><span data-stu-id="cf1b2-161">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 





