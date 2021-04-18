---
title: Функция Глреадбуффер (GL. h)
description: Функция Глреадбуффер выбирает источник цветового буфера для пикселей.
ms.assetid: 734153fa-e809-4b70-867e-55e46ab95712
keywords:
- Функция Глреадбуффер OpenGL
topic_type:
- apiref
api_name:
- glReadBuffer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59f0e88cdcb2b1b3257b23606f8160e0986584db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682022"
---
# <a name="glreadbuffer-function"></a><span data-ttu-id="21fac-104">Функция Глреадбуффер</span><span class="sxs-lookup"><span data-stu-id="21fac-104">glReadBuffer function</span></span>

<span data-ttu-id="21fac-105">Функция **глреадбуффер** выбирает источник цветового буфера для пикселей.</span><span class="sxs-lookup"><span data-stu-id="21fac-105">The **glReadBuffer** function selects a color buffer source for pixels.</span></span>

## <a name="syntax"></a><span data-ttu-id="21fac-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="21fac-106">Syntax</span></span>


```C++
void WINAPI glReadBuffer(
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="21fac-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="21fac-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21fac-108">*mode*</span><span class="sxs-lookup"><span data-stu-id="21fac-108">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="21fac-109">Буфер цвета.</span><span class="sxs-lookup"><span data-stu-id="21fac-109">A color buffer.</span></span> <span data-ttu-id="21fac-110">Допустимые значения: GL \_ спереди \_ слева, GL \_ спереди справа, GL \_ назад, \_ \_ GL \_ назад, GL \_ \_ спереди, GL \_ назад, ГК \_ Left, GL \_ справа и GL \_ AUX *i*,  где находится между 0 и вспомогательными \_ \_ буферами ГК 1.</span><span class="sxs-lookup"><span data-stu-id="21fac-110">Accepted values are GL\_FRONT\_LEFT, GL\_FRONT\_RIGHT, GL\_BACK\_LEFT, GL\_BACK\_RIGHT, GL\_FRONT, GL\_BACK, GL\_LEFT, GL\_RIGHT, and GL\_AUX *i*, where *i* is between 0 and GL\_AUX\_BUFFERS 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21fac-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="21fac-111">Return value</span></span>

<span data-ttu-id="21fac-112">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="21fac-112">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="21fac-113">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="21fac-113">Error codes</span></span>

<span data-ttu-id="21fac-114">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="21fac-114">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="21fac-115">Имя</span><span class="sxs-lookup"><span data-stu-id="21fac-115">Name</span></span>                                                                                                  | <span data-ttu-id="21fac-116">Значение</span><span class="sxs-lookup"><span data-stu-id="21fac-116">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="21fac-117"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="21fac-117"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="21fac-118">*режим* не был одним из двенадцати (или более) допустимых значений.</span><span class="sxs-lookup"><span data-stu-id="21fac-118">*mode* was not an one of the twelve (or more) accepted values.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="21fac-119"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="21fac-119"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="21fac-120">в *режиме* указан несуществующий буфер.</span><span class="sxs-lookup"><span data-stu-id="21fac-120">*mode* specified a buffer that does not exist.</span></span><br/>                                                                             |
| <dl> <span data-ttu-id="21fac-121"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="21fac-121"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="21fac-122">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="21fac-122">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="21fac-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="21fac-123">Remarks</span></span>

<span data-ttu-id="21fac-124">Функция **глреадбуффер** задает буфер цвета в качестве источника для последующих команд [**глреадпикселс**](glreadpixels.md) и [**глкопипикселс**](glcopypixels.md) .</span><span class="sxs-lookup"><span data-stu-id="21fac-124">The **glReadBuffer** function specifies a color buffer as the source for subsequent [**glReadPixels**](glreadpixels.md) and [**glCopyPixels**](glcopypixels.md) commands.</span></span> <span data-ttu-id="21fac-125">Параметр *mode* принимает одно из двенадцати или более предопределенных значений.</span><span class="sxs-lookup"><span data-stu-id="21fac-125">The *mode* parameter accepts one of twelve or more predefined values.</span></span> <span data-ttu-id="21fac-126">(GL \_ AUX0 через GL \_ AUX3 определяются всегда.) В полностью настроенной системе, на главной странице GL, \_ \_ левой и главной части GL \_ все имя передний \_ левый буфер, GL \_ переднего плана \_ и \_ правое название в ГК, а также \_ \_ \_ имя заднего левого буфера.</span><span class="sxs-lookup"><span data-stu-id="21fac-126">(GL\_AUX0 through GL\_AUX3 are always defined.) In a fully configured system, GL\_FRONT, GL\_LEFT, and GL\_FRONT\_LEFT all name the front-left buffer, GL\_FRONT\_RIGHT and GL\_RIGHT name the front-right buffer, and GL\_BACK\_LEFT and GL\_BACK name the back-left buffer.</span></span>

<span data-ttu-id="21fac-127">Нестерео конфигурации с двойной буферизацией имеют только внешний левый и задний левый буфер.</span><span class="sxs-lookup"><span data-stu-id="21fac-127">Nonstereo double-buffered configurations have only a front-left and a back-left buffer.</span></span> <span data-ttu-id="21fac-128">Однобуферные конфигурации имеют передний левый и передний правый буфер, если стерео, и только передний левый буфер, если не стерео.</span><span class="sxs-lookup"><span data-stu-id="21fac-128">Single-buffered configurations have a front-left and a front-right buffer if stereo, and only a front-left buffer if nonstereo.</span></span> <span data-ttu-id="21fac-129">Указание несуществующего буфера для **глреадбуффер** является ошибкой.</span><span class="sxs-lookup"><span data-stu-id="21fac-129">It is an error to specify a nonexistent buffer to **glReadBuffer**.</span></span>

<span data-ttu-id="21fac-130">По умолчанию *режим* — GL \_ спереди в однобуферных конфигурациях, а GL — \_ в двойных буферизованных конфигурациях.</span><span class="sxs-lookup"><span data-stu-id="21fac-130">By default, *mode* is GL\_FRONT in single-buffered configurations, and GL\_BACK in double-buffered configurations.</span></span>

<span data-ttu-id="21fac-131">Следующая функция получает сведения, связанные с **глреадбуффер**:</span><span class="sxs-lookup"><span data-stu-id="21fac-131">The following function retrieves information related to **glReadBuffer**:</span></span>

<span data-ttu-id="21fac-132">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом \_ буфера чтения GL \_</span><span class="sxs-lookup"><span data-stu-id="21fac-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_READ\_BUFFER</span></span>

## <a name="requirements"></a><span data-ttu-id="21fac-133">Требования</span><span class="sxs-lookup"><span data-stu-id="21fac-133">Requirements</span></span>



| <span data-ttu-id="21fac-134">Требование</span><span class="sxs-lookup"><span data-stu-id="21fac-134">Requirement</span></span> | <span data-ttu-id="21fac-135">Значение</span><span class="sxs-lookup"><span data-stu-id="21fac-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="21fac-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="21fac-136">Minimum supported client</span></span><br/> | <span data-ttu-id="21fac-137">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="21fac-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="21fac-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="21fac-138">Minimum supported server</span></span><br/> | <span data-ttu-id="21fac-139">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="21fac-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="21fac-140">Заголовок</span><span class="sxs-lookup"><span data-stu-id="21fac-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="21fac-141"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="21fac-141"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="21fac-142">Библиотека</span><span class="sxs-lookup"><span data-stu-id="21fac-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="21fac-143"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="21fac-143"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="21fac-144">DLL</span><span class="sxs-lookup"><span data-stu-id="21fac-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="21fac-145"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21fac-145"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21fac-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="21fac-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21fac-147">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="21fac-147">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="21fac-148">**глкопипикселс**</span><span class="sxs-lookup"><span data-stu-id="21fac-148">**glCopyPixels**</span></span>](glcopypixels.md)
</dt> <dt>

[<span data-ttu-id="21fac-149">**глдравбуффер**</span><span class="sxs-lookup"><span data-stu-id="21fac-149">**glDrawBuffer**</span></span>](gldrawbuffer.md)
</dt> <dt>

[<span data-ttu-id="21fac-150">**гленд**</span><span class="sxs-lookup"><span data-stu-id="21fac-150">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="21fac-151">**глреадпикселс**</span><span class="sxs-lookup"><span data-stu-id="21fac-151">**glReadPixels**</span></span>](glreadpixels.md)
</dt> </dl>

 

 





