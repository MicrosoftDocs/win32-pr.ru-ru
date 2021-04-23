---
title: Функция Глпушклиентаттриб (GL. h)
description: Функции Глпушклиентаттриб и Глпопклиентаттриб сохраняют и восстанавливают группы клиентских переменных состояния в стеке Client-Attribute. | Функция Глпушклиентаттриб (GL. h)
ms.assetid: 69f28af6-1023-4546-95ff-169525c23b07
keywords:
- Функция Глпушклиентаттриб OpenGL
topic_type:
- apiref
api_name:
- glPushClientAttrib
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 944e2e4229f0d36f0009ce337fd3806020322dbf
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353782"
---
# <a name="glpushclientattrib-function"></a><span data-ttu-id="9c09f-105">Функция Глпушклиентаттриб</span><span class="sxs-lookup"><span data-stu-id="9c09f-105">glPushClientAttrib function</span></span>

<span data-ttu-id="9c09f-106">Функции **глпушклиентаттриб** и [**глпопклиентаттриб**](glpopclientattrib.md) сохраняют и восстанавливают группы клиентских переменных состояния в стеке Client-Attribute.</span><span class="sxs-lookup"><span data-stu-id="9c09f-106">The **glPushClientAttrib** and [**glPopClientAttrib**](glpopclientattrib.md) functions save and restore groups of client-state variables on the client-attribute stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c09f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9c09f-107">Syntax</span></span>


```C++
void WINAPI glPushClientAttrib(
   GLbitfield mask
);
```



## <a name="parameters"></a><span data-ttu-id="9c09f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9c09f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c09f-109">*виде*</span><span class="sxs-lookup"><span data-stu-id="9c09f-109">*mask*</span></span> 
</dt> <dd>

<span data-ttu-id="9c09f-110">Маска, указывающая, какие атрибуты следует сохранить.</span><span class="sxs-lookup"><span data-stu-id="9c09f-110">A mask that indicates which attributes to save.</span></span> <span data-ttu-id="9c09f-111">Ниже приведены константы символьной маски и связанные с ними состояния клиента OpenGL.</span><span class="sxs-lookup"><span data-stu-id="9c09f-111">The following are the symbolic mask constants and their associated OpenGL client states.</span></span>



| <span data-ttu-id="9c09f-112">Значение</span><span class="sxs-lookup"><span data-stu-id="9c09f-112">Value</span></span>                                                                                                                                                                                                                                            | <span data-ttu-id="9c09f-113">Значение</span><span class="sxs-lookup"><span data-stu-id="9c09f-113">Meaning</span></span>                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <span id="GL_CLIENT_PIXEL_STORE_BIT"></span><span id="gl_client_pixel_store_bit"></span><dl> <span data-ttu-id="9c09f-114"><dt>**\_ \_ \_ бит хранилища пикселей клиента \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="9c09f-114"><dt>**GL\_CLIENT\_PIXEL\_STORE\_BIT**</dt></span></span> </dl>                                             | <span data-ttu-id="9c09f-115">Атрибуты режима хранения пикселей.</span><span class="sxs-lookup"><span data-stu-id="9c09f-115">Pixel storage mode attributes.</span></span><br/>         |
| <span id="GL_CLIENT_VERTEX_ARRAY_BIT"></span><span id="gl_client_vertex_array_bit"></span><dl> <span data-ttu-id="9c09f-116"><dt>**\_ \_ \_ бит массива вершин клиента \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="9c09f-116"><dt>**GL\_CLIENT\_VERTEX\_ARRAY\_BIT**</dt></span></span> </dl>                                          | <span data-ttu-id="9c09f-117">Атрибуты массива вершин.</span><span class="sxs-lookup"><span data-stu-id="9c09f-117">Vertex array attributes.</span></span><br/>               |
| <span id="GL_CLIENT_ALL_ATTRIB_BITs"></span><span id="gl_client_all_attrib_bits"></span><span id="GL_CLIENT_ALL_ATTRIB_BITS"></span><dl> <span data-ttu-id="9c09f-118"><dt>**\_ \_ Все атрибуты " \_ клиент GL" \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9c09f-118"><dt>**GL\_CLIENT\_ALL\_ATTRIB\_BITs**</dt></span></span> </dl> | <span data-ttu-id="9c09f-119">все зависящие от стека атрибуты состояния клиента.</span><span class="sxs-lookup"><span data-stu-id="9c09f-119">all stackable client-state attributes.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c09f-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9c09f-120">Return value</span></span>

<span data-ttu-id="9c09f-121">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="9c09f-121">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="9c09f-122">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="9c09f-122">Error codes</span></span>

<span data-ttu-id="9c09f-123">С помощью функции [**глжетеррор**](glgeterror.md) можно получить следующий код ошибки.</span><span class="sxs-lookup"><span data-stu-id="9c09f-123">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="9c09f-124">Имя</span><span class="sxs-lookup"><span data-stu-id="9c09f-124">Name</span></span>                                                                                               | <span data-ttu-id="9c09f-125">Значение</span><span class="sxs-lookup"><span data-stu-id="9c09f-125">Meaning</span></span>                                                                       |
|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9c09f-126"><dt>**\_переполнение стека GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9c09f-126"><dt>**GL\_STACK\_OVERFLOW**</dt></span></span> </dl> | <span data-ttu-id="9c09f-127">Функция была вызвана во время заполнения стека клиентского атрибута.</span><span class="sxs-lookup"><span data-stu-id="9c09f-127">The function was called while the client-attribute stack was full.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="9c09f-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9c09f-128">Remarks</span></span>

<span data-ttu-id="9c09f-129">Функция **глпушклиентаттриб** использует параметр маски, чтобы определить, какие группы переменных клиентского состояния сохраняются в стеке Client-Attribute.</span><span class="sxs-lookup"><span data-stu-id="9c09f-129">The **glPushClientAttrib** function uses its mask parameter to determine which groups of client-state variables are saved on the client-attribute stack.</span></span> <span data-ttu-id="9c09f-130">Можно использовать оператор побитового или для объединения принятых символьных констант, чтобы задать биты и создать маску.</span><span class="sxs-lookup"><span data-stu-id="9c09f-130">You can use the bitwise OR operator to join together accepted symbolic constants to set bits and construct a mask.</span></span>

<span data-ttu-id="9c09f-131">Функция [**глпопклиентаттриб**](glpopclientattrib.md) восстанавливает значения переменных клиентского состояния, сохраненных в прошлом с помощью **глпушклиентаттриб**.</span><span class="sxs-lookup"><span data-stu-id="9c09f-131">The [**glPopClientAttrib**](glpopclientattrib.md) function restores the values of the client-state variables last saved with **glPushclientAttrib**.</span></span> <span data-ttu-id="9c09f-132">Переменные состояния клиента, которые не были сохранены ранее, остались без изменений.</span><span class="sxs-lookup"><span data-stu-id="9c09f-132">Client-state variables not previously saved are left unchanged.</span></span> <span data-ttu-id="9c09f-133">При принудительной отправке атрибутов в полный стек атрибутов клиента или при извлечении атрибутов из пустого стека устанавливается флаг ошибки, а в состояние OpenGL другие изменения не вносятся.</span><span class="sxs-lookup"><span data-stu-id="9c09f-133">Pushing attributes onto a full client-attribute stack or popping attributes off an empty stack sets an error flag and no other change is made to the OpenGL state.</span></span> <span data-ttu-id="9c09f-134">По умолчанию стек атрибутов клиента пуст.</span><span class="sxs-lookup"><span data-stu-id="9c09f-134">By default the client attribute stack is empty.</span></span>

<span data-ttu-id="9c09f-135">Некоторые значения состояния клиента OpenGL не могут быть сохранены в стеке Client-Attribute.</span><span class="sxs-lookup"><span data-stu-id="9c09f-135">Some OpenGL client-state values cannot be saved on the client-attribute stack.</span></span> <span data-ttu-id="9c09f-136">Например, нельзя сохранить состояние SELECT или Feedback в стеке Client-Attribute.</span><span class="sxs-lookup"><span data-stu-id="9c09f-136">For example, you cannot save the select or feedback states on the client-attribute stack.</span></span> <span data-ttu-id="9c09f-137">Глубина стека клиентского атрибута составляет не менее 16.</span><span class="sxs-lookup"><span data-stu-id="9c09f-137">The depth of the client-attribute stack is at least 16.</span></span>

<span data-ttu-id="9c09f-138">Функции **глпушклиентаттриб** и **глпопклиентаттриб** не компилируются в списки вывода, но выполняются немедленно.</span><span class="sxs-lookup"><span data-stu-id="9c09f-138">The **glPushclientAttrib** and **glPopClientAttrib** functions are not compiled into display lists, but are executed immediately.</span></span>

<span data-ttu-id="9c09f-139">Функции **глпушклиентаттриб** и **глпопклиентаттриб** могут отправлять только режимы хранения пикселов и точки подключения точек и клиентов массива вершин.</span><span class="sxs-lookup"><span data-stu-id="9c09f-139">The **glPushClientAttrib** and **glPopClientAttrib** functions can only push and pop pixel storage modes and vertex array client states.</span></span> <span data-ttu-id="9c09f-140">Для отправки и POP-состояний, которые хранятся на сервере, необходимо использовать [**глпушаттриб**](glpushattrib.md) и [**глпопаттриб**](glpopattrib.md) .</span><span class="sxs-lookup"><span data-stu-id="9c09f-140">You must use [**glPushAttrib**](glpushattrib.md) and [**glPopAttrib**](glpopattrib.md) to push and pop states that are kept on the server.</span></span>

> [!Note]  
> <span data-ttu-id="9c09f-141">Функции **глпушклиентаттриб** и **глпопклиентаттриб** доступны только в OpenGL версии 1,1 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="9c09f-141">The **glPushClientAttrib** and **glPopClientAttrib** functions are only available in OpenGL version 1.1 or later.</span></span>

 

<span data-ttu-id="9c09f-142">Следующие функции извлекают сведения, относящиеся к **глпушклиентаттриб** и **глпопклиентаттриб**:</span><span class="sxs-lookup"><span data-stu-id="9c09f-142">The following functions retrieve information related to **glPushClientAttrib** and **glPopClientAttrib**:</span></span>

<span data-ttu-id="9c09f-143">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом \_ " \_ \_ глубина СТЕКа \_ " для клиента GL</span><span class="sxs-lookup"><span data-stu-id="9c09f-143">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CLIENT\_ATTRIB\_STACK\_DEPTH</span></span>

<span data-ttu-id="9c09f-144">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом \_ " \_ Максимальная \_ \_ глубина стека для клиента \_ "</span><span class="sxs-lookup"><span data-stu-id="9c09f-144">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAX\_CLIENT\_ATTRIB\_STACK\_DEPTH</span></span>

## <a name="requirements"></a><span data-ttu-id="9c09f-145">Требования</span><span class="sxs-lookup"><span data-stu-id="9c09f-145">Requirements</span></span>



| <span data-ttu-id="9c09f-146">Требование</span><span class="sxs-lookup"><span data-stu-id="9c09f-146">Requirement</span></span> | <span data-ttu-id="9c09f-147">Значение</span><span class="sxs-lookup"><span data-stu-id="9c09f-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9c09f-148">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9c09f-148">Minimum supported client</span></span><br/> | <span data-ttu-id="9c09f-149">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9c09f-149">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="9c09f-150">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9c09f-150">Minimum supported server</span></span><br/> | <span data-ttu-id="9c09f-151">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9c09f-151">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9c09f-152">Заголовок</span><span class="sxs-lookup"><span data-stu-id="9c09f-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c09f-153"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c09f-153"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="9c09f-154">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9c09f-154">Library</span></span><br/>                  | <dl> <span data-ttu-id="9c09f-155"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9c09f-155"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="9c09f-156">DLL</span><span class="sxs-lookup"><span data-stu-id="9c09f-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9c09f-157"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9c09f-157"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c09f-158">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9c09f-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c09f-159">**глколорпоинтер**</span><span class="sxs-lookup"><span data-stu-id="9c09f-159">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="9c09f-160">**глдисаблеклиентстате**</span><span class="sxs-lookup"><span data-stu-id="9c09f-160">**glDisableClientState**</span></span>](gldisableclientstate.md)
</dt> <dt>

[<span data-ttu-id="9c09f-161">**гледжефлагпоинтер**</span><span class="sxs-lookup"><span data-stu-id="9c09f-161">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="9c09f-162">**гленаблеклиентстате**</span><span class="sxs-lookup"><span data-stu-id="9c09f-162">**glEnableClientState**</span></span>](glenableclientstate.md)
</dt> <dt>

[<span data-ttu-id="9c09f-163">**глжет**</span><span class="sxs-lookup"><span data-stu-id="9c09f-163">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="9c09f-164">**глжетеррор**</span><span class="sxs-lookup"><span data-stu-id="9c09f-164">**glGetError**</span></span>](glgeterror.md)
</dt> <dt>

[<span data-ttu-id="9c09f-165">**глиндекспоинтер**</span><span class="sxs-lookup"><span data-stu-id="9c09f-165">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="9c09f-166">**глнормалпоинтер**</span><span class="sxs-lookup"><span data-stu-id="9c09f-166">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="9c09f-167">**глневлист**</span><span class="sxs-lookup"><span data-stu-id="9c09f-167">**glNewList**</span></span>](glnewlist.md)
</dt> <dt>

[<span data-ttu-id="9c09f-168">**глпикселсторе**</span><span class="sxs-lookup"><span data-stu-id="9c09f-168">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="9c09f-169">**глпушаттриб**</span><span class="sxs-lookup"><span data-stu-id="9c09f-169">**glPushAttrib**</span></span>](glpushattrib.md)
</dt> <dt>

[<span data-ttu-id="9c09f-170">**глтекскурдпоинтер**</span><span class="sxs-lookup"><span data-stu-id="9c09f-170">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="9c09f-171">**глвертекспоинтер**</span><span class="sxs-lookup"><span data-stu-id="9c09f-171">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 





