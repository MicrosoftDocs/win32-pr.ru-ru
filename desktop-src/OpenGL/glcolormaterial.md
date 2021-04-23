---
title: Функция Глколорматериал (GL. h)
description: Функция Глколорматериал заставляет цвет материала контролировать текущий цвет.
ms.assetid: 6dbef2c2-f902-4f25-8a87-9e3d710dd807
keywords:
- Функция Глколорматериал OpenGL
topic_type:
- apiref
api_name:
- glColorMaterial
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d32823eaa82e6a260790dd6fa23747f2b4228649
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415697"
---
# <a name="glcolormaterial-function"></a><span data-ttu-id="e56ae-104">Функция Глколорматериал</span><span class="sxs-lookup"><span data-stu-id="e56ae-104">glColorMaterial function</span></span>

<span data-ttu-id="e56ae-105">Функция **глколорматериал** заставляет цвет материала контролировать текущий цвет.</span><span class="sxs-lookup"><span data-stu-id="e56ae-105">The **glColorMaterial** function causes a material color to track the current color.</span></span>

## <a name="syntax"></a><span data-ttu-id="e56ae-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e56ae-106">Syntax</span></span>


```C++
void WINAPI glColorMaterial(
   GLenum face,
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="e56ae-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="e56ae-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e56ae-108">*личным*</span><span class="sxs-lookup"><span data-stu-id="e56ae-108">*face*</span></span> 
</dt> <dd>

<span data-ttu-id="e56ae-109">Указывает, следует ли отслеживанию текущего цвета на внешнем, обратном или обоих параметрах переднего и заднего плана.</span><span class="sxs-lookup"><span data-stu-id="e56ae-109">Specifies whether front, back, or both front and back material parameters should track the current color.</span></span> <span data-ttu-id="e56ae-110">Допустимые значения: GL \_ Front, GL \_ назад и GL \_ Front \_ и \_ Back.</span><span class="sxs-lookup"><span data-stu-id="e56ae-110">Accepted values are GL\_FRONT, GL\_BACK, and GL\_FRONT\_AND\_BACK.</span></span> <span data-ttu-id="e56ae-111">Значение по умолчанию — GL \_ Front \_ и \_ Back.</span><span class="sxs-lookup"><span data-stu-id="e56ae-111">The default value is GL\_FRONT\_AND\_BACK.</span></span>

</dd> <dt>

<span data-ttu-id="e56ae-112">*mode*</span><span class="sxs-lookup"><span data-stu-id="e56ae-112">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="e56ae-113">Указывает, какой из нескольких параметров материала позволяет контролировать текущий цвет.</span><span class="sxs-lookup"><span data-stu-id="e56ae-113">Specifies which of several material parameters track the current color.</span></span> <span data-ttu-id="e56ae-114">Допустимые значения: «Эмиссия GL», «наружная высветка», «Диффузия GL», « \_ \_ \_ \_ освещение» и « \_ \_ \_ диффузия».</span><span class="sxs-lookup"><span data-stu-id="e56ae-114">Accepted values are GL\_EMISSION, GL\_AMBIENT, GL\_DIFFUSE, GL\_SPECULAR, and GL\_AMBIENT\_AND\_DIFFUSE.</span></span> <span data-ttu-id="e56ae-115">Значение по умолчанию — « \_ внешняя \_ » и « \_ диффузная».</span><span class="sxs-lookup"><span data-stu-id="e56ae-115">The default value is GL\_AMBIENT\_AND\_DIFFUSE.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e56ae-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e56ae-116">Return value</span></span>

<span data-ttu-id="e56ae-117">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="e56ae-117">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e56ae-118">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="e56ae-118">Error codes</span></span>

<span data-ttu-id="e56ae-119">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="e56ae-119">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="e56ae-120">Имя</span><span class="sxs-lookup"><span data-stu-id="e56ae-120">Name</span></span>                                                                                                  | <span data-ttu-id="e56ae-121">Значение</span><span class="sxs-lookup"><span data-stu-id="e56ae-121">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e56ae-122"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="e56ae-122"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="e56ae-123">*лицо* или *режим* не являются допустимыми значениями.</span><span class="sxs-lookup"><span data-stu-id="e56ae-123">*face* or *mode* was not an accepted value.</span></span><br/>                                                                                |
| <dl> <span data-ttu-id="e56ae-124"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="e56ae-124"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="e56ae-125">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="e56ae-125">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="e56ae-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e56ae-126">Remarks</span></span>

<span data-ttu-id="e56ae-127">Функция **глколорматериал** указывает, какие параметры материала отписывают текущий цвет.</span><span class="sxs-lookup"><span data-stu-id="e56ae-127">The **glColorMaterial** function specifies which material parameters track the current color.</span></span> <span data-ttu-id="e56ae-128">При включении \_ цветового \_ материала GL для каждого материала или материалов, заданных *лицом*, параметр материала или параметры, заданные *режимом* , записывают текущий цвет в любое время.</span><span class="sxs-lookup"><span data-stu-id="e56ae-128">When you enable GL\_COLOR\_MATERIAL, for each of the material or materials specified by *face*, the material parameter or parameters specified by *mode* track the current color at all times.</span></span> <span data-ttu-id="e56ae-129">Включать и отключать \_ цветовые \_ материалы GL можно с помощью функций [**гленабле**](glenable.md) и [**глдисабле**](gldisable.md), которые вызываются с использованием \_ цветового материала GL в \_ качестве аргумента.</span><span class="sxs-lookup"><span data-stu-id="e56ae-129">Enable and disable GL\_COLOR\_MATERIAL with the functions [**glEnable**](glenable.md) and [**glDisable**](gldisable.md), which you call with GL\_COLOR\_MATERIAL as their argument.</span></span> <span data-ttu-id="e56ae-130">По умолчанию \_ цветовой \_ материал GL отключен.</span><span class="sxs-lookup"><span data-stu-id="e56ae-130">By default, GL\_COLOR\_MATERIAL is disabled.</span></span>

<span data-ttu-id="e56ae-131">С помощью **глколорматериал** можно изменить подмножество параметров материала для каждой вершины, используя только функцию [**глколор**](glcolor-functions.md) , не вызывая [**глматериал**](glmaterial-functions.md).</span><span class="sxs-lookup"><span data-stu-id="e56ae-131">With **glColorMaterial**, you can change a subset of material parameters for each vertex using only the [**glColor**](glcolor-functions.md) function, without calling [**glMaterial**](glmaterial-functions.md).</span></span> <span data-ttu-id="e56ae-132">Если вы собираетесь указать только такое подмножество параметров для каждой вершины, лучше сделать это с помощью **глколорматериал** , чем с помощью **глматериал**.</span><span class="sxs-lookup"><span data-stu-id="e56ae-132">If you are going to specify only such a subset of parameters for each vertex, it is better to do so with **glColorMaterial** than with **glMaterial**.</span></span>

<span data-ttu-id="e56ae-133">Следующие функции извлекают сведения, относящиеся к **глколорматериал**:</span><span class="sxs-lookup"><span data-stu-id="e56ae-133">The following functions retrieve information related to **glColorMaterial**:</span></span>

<span data-ttu-id="e56ae-134">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом \_ " \_ параметр цветового материала GL" \_</span><span class="sxs-lookup"><span data-stu-id="e56ae-134">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_COLOR\_MATERIAL\_PARAMETER</span></span>

<span data-ttu-id="e56ae-135">**глжет** с аргументом « \_ ЦВЕТовой \_ материал GL» \_</span><span class="sxs-lookup"><span data-stu-id="e56ae-135">**glGet** with argument GL\_COLOR\_MATERIAL\_FACE</span></span>

<span data-ttu-id="e56ae-136">[**глисенаблед**](glisenabled.md) с аргументом " \_ ЦВЕТовой материал GL" \_</span><span class="sxs-lookup"><span data-stu-id="e56ae-136">[**glIsEnabled**](glisenabled.md) with argument GL\_COLOR\_MATERIAL</span></span>

## <a name="requirements"></a><span data-ttu-id="e56ae-137">Требования</span><span class="sxs-lookup"><span data-stu-id="e56ae-137">Requirements</span></span>



| <span data-ttu-id="e56ae-138">Требование</span><span class="sxs-lookup"><span data-stu-id="e56ae-138">Requirement</span></span> | <span data-ttu-id="e56ae-139">Значение</span><span class="sxs-lookup"><span data-stu-id="e56ae-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e56ae-140">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e56ae-140">Minimum supported client</span></span><br/> | <span data-ttu-id="e56ae-141">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e56ae-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="e56ae-142">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e56ae-142">Minimum supported server</span></span><br/> | <span data-ttu-id="e56ae-143">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e56ae-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e56ae-144">Заголовок</span><span class="sxs-lookup"><span data-stu-id="e56ae-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="e56ae-145"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="e56ae-145"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="e56ae-146">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e56ae-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="e56ae-147"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e56ae-147"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="e56ae-148">DLL</span><span class="sxs-lookup"><span data-stu-id="e56ae-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e56ae-149"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e56ae-149"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e56ae-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e56ae-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e56ae-151">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="e56ae-151">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="e56ae-152">**глколор**</span><span class="sxs-lookup"><span data-stu-id="e56ae-152">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="e56ae-153">**глдисабле**</span><span class="sxs-lookup"><span data-stu-id="e56ae-153">**glDisable**</span></span>](gldisable.md)
</dt> <dt>

[<span data-ttu-id="e56ae-154">**гленабле**</span><span class="sxs-lookup"><span data-stu-id="e56ae-154">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="e56ae-155">**гленд**</span><span class="sxs-lookup"><span data-stu-id="e56ae-155">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="e56ae-156">**глжет**</span><span class="sxs-lookup"><span data-stu-id="e56ae-156">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="e56ae-157">**глисенаблед**</span><span class="sxs-lookup"><span data-stu-id="e56ae-157">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="e56ae-158">**гллигхт**</span><span class="sxs-lookup"><span data-stu-id="e56ae-158">**glLight**</span></span>](gllight-functions.md)
</dt> <dt>

[<span data-ttu-id="e56ae-159">**гллигхтмодел**</span><span class="sxs-lookup"><span data-stu-id="e56ae-159">**glLightModel**</span></span>](gllightmodel-functions.md)
</dt> <dt>

[<span data-ttu-id="e56ae-160">**глматериал**</span><span class="sxs-lookup"><span data-stu-id="e56ae-160">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> </dl>

 

 





