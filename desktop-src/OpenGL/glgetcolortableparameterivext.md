---
title: Функция Глжетколортаблепараметеривекст (GL. h)
description: Функции Глжетколортаблепараметерфвекст и Глжетколортаблепараметеривекст получают параметры палитры из цветовых таблиц. | Функция Глжетколортаблепараметеривекст (GL. h)
ms.assetid: 39a0b346-d103-4426-8536-95e7e1548f7a
keywords:
- Функция Глжетколортаблепараметеривекст OpenGL
topic_type:
- apiref
api_name:
- glGetColorTableParameterivEXT
api_location:
- Gl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 897dd11781968838bb8c26a716e3857acc119e9c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105684935"
---
# <a name="glgetcolortableparameterivext-function"></a><span data-ttu-id="c96f7-105">Функция Глжетколортаблепараметеривекст</span><span class="sxs-lookup"><span data-stu-id="c96f7-105">glGetColorTableParameterivEXT function</span></span>

<span data-ttu-id="c96f7-106">Функции [**глжетколортаблепараметерфвекст**](glgetcolortableparameterfvext.md) и **глжетколортаблепараметеривекст** получают параметры палитры из цветовых таблиц.</span><span class="sxs-lookup"><span data-stu-id="c96f7-106">The [**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md) and **glGetColorTableParameterivEXT** functions get palette parameters from color tables.</span></span>

## <a name="syntax"></a><span data-ttu-id="c96f7-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c96f7-107">Syntax</span></span>


```C++
void WINAPI glGetColorTableParameterivEXT(
   GLenum target,
   GLenum pname,
   GLint  *params
);
```



## <a name="parameters"></a><span data-ttu-id="c96f7-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c96f7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c96f7-109">*target*</span><span class="sxs-lookup"><span data-stu-id="c96f7-109">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="c96f7-110">Целевая текстура палитры, для которой требуется получить данные параметров.</span><span class="sxs-lookup"><span data-stu-id="c96f7-110">The target texture of the palette for which you want parameter data.</span></span> <span data-ttu-id="c96f7-111">Должен быть ТЕКСТУРой \_ 1d, \_ 2D текстуры, \_ одномерной текстуры-посредника \_ или \_ 2D-текстурной текстуры \_ .</span><span class="sxs-lookup"><span data-stu-id="c96f7-111">Must be TEXTURE\_1D, TEXTURE\_2D, PROXY\_TEXTURE\_1D, or PROXY\_TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="c96f7-112">*pname*</span><span class="sxs-lookup"><span data-stu-id="c96f7-112">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="c96f7-113">Символьная константа для типа данных параметров палитры, на которую указывает *params*.</span><span class="sxs-lookup"><span data-stu-id="c96f7-113">A symbolic constant for the type of palette parameter data pointed to by *params*.</span></span>

<span data-ttu-id="c96f7-114">Ниже приведены допустимые символьные константы и их значения.</span><span class="sxs-lookup"><span data-stu-id="c96f7-114">The following are the accepted symbolic constants and their meanings.</span></span>



| <span data-ttu-id="c96f7-115">Значение</span><span class="sxs-lookup"><span data-stu-id="c96f7-115">Value</span></span>                                                                                                                                                                                                             | <span data-ttu-id="c96f7-116">Значение</span><span class="sxs-lookup"><span data-stu-id="c96f7-116">Meaning</span></span>                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_TABLE_FORMAT_EXT"></span><span id="gl_color_table_format_ext"></span><dl> <span data-ttu-id="c96f7-117"><dt>**\_Формат таблицы цветов GL ( \_ \_ \_ Расш.)**</dt></span><span class="sxs-lookup"><span data-stu-id="c96f7-117"><dt>**GL\_COLOR\_TABLE\_FORMAT\_EXT**</dt></span></span> </dl>              | <span data-ttu-id="c96f7-118">Возвращает внутренний формат, заданный последним вызовом [**глколортабликст**](glcolortableext.md) или значением по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c96f7-118">Return the internal format specified by the most recent call to [**glColorTableEXT**](glcolortableext.md) or the default value.</span></span><br/> |
| <span id="GL_COLOR_TABLE_WIDTH_EXT"></span><span id="gl_color_table_width_ext"></span><dl> <span data-ttu-id="c96f7-119"><dt>**\_Ширина таблицы цветов GL ( \_ \_ \_ Расш.)**</dt></span><span class="sxs-lookup"><span data-stu-id="c96f7-119"><dt>**GL\_COLOR\_TABLE\_WIDTH\_EXT**</dt></span></span> </dl>                 | <span data-ttu-id="c96f7-120">Возврат ширины текущей палитры.</span><span class="sxs-lookup"><span data-stu-id="c96f7-120">Return the width of the current palette.</span></span><br/>                                                                                         |
| <span id="GL_COLOR_TABLE_RED_SIZE_EXT"></span><span id="gl_color_table_red_size_ext"></span><dl> <span data-ttu-id="c96f7-121"><dt>**\_ \_ \_ \_ внешний размер таблицы цветовых таблиц GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c96f7-121"><dt>**GL\_COLOR\_TABLE\_RED\_SIZE\_EXT**</dt></span></span> </dl>       | <span data-ttu-id="c96f7-122">Возвращает фактический размер, используемый внутренне для хранения красного компонента данных палитры.</span><span class="sxs-lookup"><span data-stu-id="c96f7-122">Return the actual size used internally to store the red component of the palette data.</span></span><br/>                                           |
| <span id="GL_COLOR_TABLE_GREEN_SIZE_EXT"></span><span id="gl_color_table_green_size_ext"></span><dl> <span data-ttu-id="c96f7-123"><dt>**\_ \_ \_ \_ внешний размер таблицы цвета \_ GL в главной таблице**</dt></span><span class="sxs-lookup"><span data-stu-id="c96f7-123"><dt>**GL\_COLOR\_TABLE\_GREEN\_SIZE\_EXT**</dt></span></span> </dl> | <span data-ttu-id="c96f7-124">Возвращает фактический размер, используемый внутренне для хранения зеленого компонента данных палитры.</span><span class="sxs-lookup"><span data-stu-id="c96f7-124">Return the actual size used internally to store the green component of the palette data.</span></span><br/>                                         |
| <span id="GL_COLOR_TABLE_BLUE_SIZE_EXT"></span><span id="gl_color_table_blue_size_ext"></span><dl> <span data-ttu-id="c96f7-125"><dt>**\_ \_ \_ \_ внешний размер таблицы цветовых таблиц GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c96f7-125"><dt>**GL\_COLOR\_TABLE\_BLUE\_SIZE\_EXT**</dt></span></span> </dl>    | <span data-ttu-id="c96f7-126">Возвращает фактический размер, используемый внутренне для хранения синего компонента данных палитры.</span><span class="sxs-lookup"><span data-stu-id="c96f7-126">Return the actual size used internally to store the blue component of the palette data.</span></span><br/>                                          |
| <span id="GL_COLOR_TABLE_ALPHA_SIZE_EXT"></span><span id="gl_color_table_alpha_size_ext"></span><dl> <span data-ttu-id="c96f7-127"><dt>**\_Таблица цветовой таблицы GL — \_ \_ \_ внешний размер (латиница \_ )**</dt></span><span class="sxs-lookup"><span data-stu-id="c96f7-127"><dt>**GL\_COLOR\_TABLE\_ALPHA\_SIZE\_EXT**</dt></span></span> </dl> | <span data-ttu-id="c96f7-128">Возвращает фактический размер, используемый внутренне для хранения альфа-компонента данных палитры.</span><span class="sxs-lookup"><span data-stu-id="c96f7-128">Return the actual size used internally to store the alpha component of the palette data.</span></span><br/>                                         |



 

</dd> <dt>

<span data-ttu-id="c96f7-129">*params*</span><span class="sxs-lookup"><span data-stu-id="c96f7-129">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="c96f7-130">Указывает на данные параметра таблицы цветов, указанные параметром *pname* .</span><span class="sxs-lookup"><span data-stu-id="c96f7-130">Points to the color table parameter data specified by the *pname* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c96f7-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c96f7-131">Return value</span></span>

<span data-ttu-id="c96f7-132">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="c96f7-132">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c96f7-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c96f7-133">Remarks</span></span>

<span data-ttu-id="c96f7-134">Функции **глжетколортаблепараметеривекст** и [**глжетколортаблепараметерфвекст**](glgetcolortableparameterfvext.md) используются для получения определенных данных параметров из таблиц цветов, установленных с помощью [**глколортабликст**](glcolortableext.md) для целевых палитр текстуры.</span><span class="sxs-lookup"><span data-stu-id="c96f7-134">You use the **glGetColorTableParameterivEXT** and [**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md) functions to retrieve specific parameter data from color tables set with [**glColorTableEXT**](glcolortableext.md) for targeted texture palettes.</span></span> <span data-ttu-id="c96f7-135">Кроме того, эти функции можно использовать для определения количества записей в таблице цветов, возвращаемых **глжетколортабликст** .</span><span class="sxs-lookup"><span data-stu-id="c96f7-135">Also you can use these functions to determine the number of color table entries that **glGetColorTableEXT** returns.</span></span>

<span data-ttu-id="c96f7-136">Если параметр *Target* имеет значение \_ текстуры прокси-сервера \_ 1d или 2D-текстура \_ ГК \_ \_ \_ , а реализация не поддерживает значения, указанные для *формата* или *ширины*, **глколортабликст** может не создать запрошенную таблицу цветов.</span><span class="sxs-lookup"><span data-stu-id="c96f7-136">When the *target* parameter is GL\_PROXY\_TEXTURE\_1D or GL\_PROXY\_TEXTURE\_2D, and the implementation does not support the values specified for either *format* or *width*, **glColorTableEXT** can fail to create the requested color table.</span></span> <span data-ttu-id="c96f7-137">В этом случае таблица цветов пуста, и все полученные параметры будут равны нулю.</span><span class="sxs-lookup"><span data-stu-id="c96f7-137">In this case, the color table is empty and all parameters retrieved will be zero.</span></span> <span data-ttu-id="c96f7-138">Можно определить, поддерживает ли OpenGL определенный формат и размер цветовой таблицы, вызвав **глколортабликст** с целевым объектом-посредником, а затем вызвав **глжетколортаблепараметеривекст** или [**глжетколортаблепараметерфвекст**](glgetcolortableparameterfvext.md) , чтобы определить, совпадает ли параметр Width, заданный **глколортабликст**.</span><span class="sxs-lookup"><span data-stu-id="c96f7-138">You can determine whether OpenGL supports a particular color table format and size by calling **glColorTableEXT** with a proxy target, and then calling **glGetColorTableParameterivEXT** or [**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md) to determine whether the width parameter matches that set by **glColorTableEXT**.</span></span> <span data-ttu-id="c96f7-139">Если полученная ширина равна нулю, запрос на таблицу цветов с помощью **глколортабле** не выполнен.</span><span class="sxs-lookup"><span data-stu-id="c96f7-139">If the retrieved width is zero, the color table request by **glColorTable** failed.</span></span> <span data-ttu-id="c96f7-140">Если полученная ширина не равна нулю, можно вызвать **глколортабле** с реальной целью с текстурой \_ 1d или 2D-текстурой, \_ чтобы задать таблицу цветов.</span><span class="sxs-lookup"><span data-stu-id="c96f7-140">If the retrieved width is not zero, you can call **glColorTable** with the real target with TEXTURE\_1D or TEXTURE\_2D to set the color table.</span></span>

<span data-ttu-id="c96f7-141">Функции **глжетколортаблепараметеривекст** и [**глжетколортаблепараметерфвекст**](glgetcolortableparameterfvext.md) — это функции расширения, которые не являются частью стандартной библиотеки OpenGL, но являются частью \_ расширения текстуры с помощью \_ палитры типа "Расш \_ .</span><span class="sxs-lookup"><span data-stu-id="c96f7-141">The **glGetColorTableParameterivEXT** and [**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md) functions are extension functions that are not part of the standard OpenGL library but are part of the GL\_EXT\_paletted\_texture extension.</span></span> <span data-ttu-id="c96f7-142">Чтобы проверить, поддерживает ли ваша реализация OpenGL **глжетколортаблепараметеривекст** и **глжетколортаблепараметерфвекст**, вызовите [**глжетстринг**](glgetstring.md)**(GL-** \_ расширения **)**.</span><span class="sxs-lookup"><span data-stu-id="c96f7-142">To check whether your implementation of OpenGL supports **glGetColorTableParameterivEXT** and **glGetColorTableParameterfvEXT**, call [**glGetString**](glgetstring.md)**(** GL\_EXTENSIONS **)**.</span></span> <span data-ttu-id="c96f7-143">Если он возвращает \_ \_ текстуру с расширенной палитрой GL \_ , поддерживаются **глжетколортаблепараметеривекст** и **глжетколортаблепараметерфвекст** .</span><span class="sxs-lookup"><span data-stu-id="c96f7-143">If it returns GL\_EXT\_paletted\_texture, **glGetColorTableParameterivEXT** and **glGetColorTableParameterfvEXT** are supported.</span></span> <span data-ttu-id="c96f7-144">Чтобы получить адрес функции расширения, вызовите [**вглжетпрокаддресс**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress).</span><span class="sxs-lookup"><span data-stu-id="c96f7-144">To obtain the function address of an extension function, call [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress).</span></span>

## <a name="requirements"></a><span data-ttu-id="c96f7-145">Требования</span><span class="sxs-lookup"><span data-stu-id="c96f7-145">Requirements</span></span>



| <span data-ttu-id="c96f7-146">Требование</span><span class="sxs-lookup"><span data-stu-id="c96f7-146">Requirement</span></span> | <span data-ttu-id="c96f7-147">Значение</span><span class="sxs-lookup"><span data-stu-id="c96f7-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="c96f7-148">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c96f7-148">Minimum supported client</span></span><br/> | <span data-ttu-id="c96f7-149">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c96f7-149">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                      |
| <span data-ttu-id="c96f7-150">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c96f7-150">Minimum supported server</span></span><br/> | <span data-ttu-id="c96f7-151">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c96f7-151">Windows 2000 Server \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="c96f7-152">Заголовок</span><span class="sxs-lookup"><span data-stu-id="c96f7-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="c96f7-153"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="c96f7-153"><dt>Gl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c96f7-154">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c96f7-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c96f7-155">**глколорсубтабликст**</span><span class="sxs-lookup"><span data-stu-id="c96f7-155">**glColorSubTableEXT**</span></span>](glcolorsubtableext.md)
</dt> <dt>

[<span data-ttu-id="c96f7-156">**глколортабликст**</span><span class="sxs-lookup"><span data-stu-id="c96f7-156">**glColorTableEXT**</span></span>](glcolortableext.md)
</dt> <dt>

[<span data-ttu-id="c96f7-157">**глжетколортабликст**</span><span class="sxs-lookup"><span data-stu-id="c96f7-157">**glGetColorTableEXT**</span></span>](glgetcolortableext.md)
</dt> <dt>

[<span data-ttu-id="c96f7-158">**глжетколортаблепараметерфвекст**</span><span class="sxs-lookup"><span data-stu-id="c96f7-158">**glGetColorTableParameterfvEXT**</span></span>](glgetcolortableparameterfvext.md)
</dt> <dt>

[<span data-ttu-id="c96f7-159">**вглжетпрокаддресс**</span><span class="sxs-lookup"><span data-stu-id="c96f7-159">**wglGetProcAddress**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)
</dt> </dl>

 

 





