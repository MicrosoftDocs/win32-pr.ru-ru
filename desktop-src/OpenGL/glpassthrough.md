---
title: Функция Глпасссраугх (GL. h)
description: Функция Глпасссраугх помещает маркер в буфер обратной связи.
ms.assetid: 14664ac6-eb25-46ae-86d8-7ece31df103f
keywords:
- Функция Глпасссраугх OpenGL
topic_type:
- apiref
api_name:
- glPassThrough
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd1174dd933d46813a89c35b781d0408c3ac5476
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802002"
---
# <a name="glpassthrough-function"></a><span data-ttu-id="5c183-104">Функция Глпасссраугх</span><span class="sxs-lookup"><span data-stu-id="5c183-104">glPassThrough function</span></span>

<span data-ttu-id="5c183-105">Функция **глпасссраугх** помещает маркер в буфер обратной связи.</span><span class="sxs-lookup"><span data-stu-id="5c183-105">The **glPassThrough** function places a marker in the feedback buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c183-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5c183-106">Syntax</span></span>


```C++
void WINAPI glPassThrough(
   GLfloat token
);
```



## <a name="parameters"></a><span data-ttu-id="5c183-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="5c183-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c183-108">*token*</span><span class="sxs-lookup"><span data-stu-id="5c183-108">*token*</span></span> 
</dt> <dd>

<span data-ttu-id="5c183-109">Значение маркера, помещаемое в буфер обратной связи.</span><span class="sxs-lookup"><span data-stu-id="5c183-109">A marker value to be placed in the feedback buffer.</span></span> <span data-ttu-id="5c183-110">Он указывается со следующим уникальным идентификационным значением.</span><span class="sxs-lookup"><span data-stu-id="5c183-110">It is indicated with the following unique identifying value.</span></span>



| <span data-ttu-id="5c183-111">Значение</span><span class="sxs-lookup"><span data-stu-id="5c183-111">Value</span></span>                                                                                                                                                                                   | <span data-ttu-id="5c183-112">Значение</span><span class="sxs-lookup"><span data-stu-id="5c183-112">Meaning</span></span>                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_PASS_THROUGH_TOKEN"></span><span id="gl_pass_through_token"></span><dl> <span data-ttu-id="5c183-113"><dt>**\_токен передачи GL \_ по \_ ГК**</dt></span><span class="sxs-lookup"><span data-stu-id="5c183-113"><dt>**GL\_PASS\_THROUGH\_TOKEN**</dt></span></span> </dl> | <span data-ttu-id="5c183-114">Порядок команд **глпасссраугх** по отношению к спецификации графических примитивов сохраняется.</span><span class="sxs-lookup"><span data-stu-id="5c183-114">The order of **glPassThrough** commands with respect to the specification of graphics primitives is maintained.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c183-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5c183-115">Return value</span></span>

<span data-ttu-id="5c183-116">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="5c183-116">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="5c183-117">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="5c183-117">Error codes</span></span>

<span data-ttu-id="5c183-118">С помощью функции [**глжетеррор**](glgeterror.md) можно получить следующий код ошибки.</span><span class="sxs-lookup"><span data-stu-id="5c183-118">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="5c183-119">Имя</span><span class="sxs-lookup"><span data-stu-id="5c183-119">Name</span></span>                                                                                                  | <span data-ttu-id="5c183-120">Значение</span><span class="sxs-lookup"><span data-stu-id="5c183-120">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5c183-121"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="5c183-121"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="5c183-122">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="5c183-122">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="5c183-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5c183-123">Remarks</span></span>

<span data-ttu-id="5c183-124">Обратная связь — это режим рендеринга OpenGL, выбранный путем вызова [**глрендермоде**](glrendermode.md) с помощью \_ предложения GL.</span><span class="sxs-lookup"><span data-stu-id="5c183-124">Feedback is an OpenGL render mode selected by calling [**glRenderMode**](glrendermode.md) with GL\_FEEDBACK.</span></span> <span data-ttu-id="5c183-125">Когда OpenGL находится в режиме обратной связи, никакие Пиксели не создаются путем растрирования.</span><span class="sxs-lookup"><span data-stu-id="5c183-125">When OpenGL is in feedback mode, no pixels are produced by rasterization.</span></span> <span data-ttu-id="5c183-126">Вместо этого сведения о примитивах, которые были бы растровыми, отправляются обратно в приложение OpenGL.</span><span class="sxs-lookup"><span data-stu-id="5c183-126">Instead, information about primitives that would have been rasterized is fed back to the application by OpenGL.</span></span> <span data-ttu-id="5c183-127">Описание буфера обратной связи и его значений см. в разделе [**глфидбаккбуффер**](glfeedbackbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="5c183-127">See [**glFeedbackBuffer**](glfeedbackbuffer.md) for a description of the feedback buffer and the values in it.</span></span>

<span data-ttu-id="5c183-128">Функция **глпасссраугх** вставляет определяемый пользователем маркер в буфер обратной связи при его выполнении в режиме обратной связи.</span><span class="sxs-lookup"><span data-stu-id="5c183-128">The **glPassThrough** function inserts a user-defined marker in the feedback buffer when it is executed in feedback mode.</span></span> <span data-ttu-id="5c183-129">Параметр *Token* возвращается так, как если бы он был примитивом.</span><span class="sxs-lookup"><span data-stu-id="5c183-129">The *token* parameter is returned as if it were a primitive.</span></span>

<span data-ttu-id="5c183-130">Функция **глпасссраугх** игнорируется, если OpenGL не находится в режиме обратной связи.</span><span class="sxs-lookup"><span data-stu-id="5c183-130">The **glPassThrough** function is ignored if OpenGL is not in feedback mode.</span></span>

<span data-ttu-id="5c183-131">Следующая функция получает сведения, связанные с **глпасссраугх**:</span><span class="sxs-lookup"><span data-stu-id="5c183-131">The following function retrieves information related to **glPassThrough**:</span></span>

<span data-ttu-id="5c183-132">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом \_ режим рендеринга GL \_</span><span class="sxs-lookup"><span data-stu-id="5c183-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_RENDER\_MODE</span></span>

## <a name="requirements"></a><span data-ttu-id="5c183-133">Требования</span><span class="sxs-lookup"><span data-stu-id="5c183-133">Requirements</span></span>



| <span data-ttu-id="5c183-134">Требование</span><span class="sxs-lookup"><span data-stu-id="5c183-134">Requirement</span></span> | <span data-ttu-id="5c183-135">Значение</span><span class="sxs-lookup"><span data-stu-id="5c183-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5c183-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5c183-136">Minimum supported client</span></span><br/> | <span data-ttu-id="5c183-137">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5c183-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="5c183-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5c183-138">Minimum supported server</span></span><br/> | <span data-ttu-id="5c183-139">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5c183-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5c183-140">Заголовок</span><span class="sxs-lookup"><span data-stu-id="5c183-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c183-141"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c183-141"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="5c183-142">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5c183-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="5c183-143"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5c183-143"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="5c183-144">DLL</span><span class="sxs-lookup"><span data-stu-id="5c183-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5c183-145"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5c183-145"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c183-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5c183-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c183-147">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="5c183-147">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="5c183-148">**гленд**</span><span class="sxs-lookup"><span data-stu-id="5c183-148">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="5c183-149">**глфидбаккбуффер**</span><span class="sxs-lookup"><span data-stu-id="5c183-149">**glFeedbackBuffer**</span></span>](glfeedbackbuffer.md)
</dt> <dt>

[<span data-ttu-id="5c183-150">**глрендермоде**</span><span class="sxs-lookup"><span data-stu-id="5c183-150">**glRenderMode**</span></span>](glrendermode.md)
</dt> </dl>

 

 





