---
title: Функция ГлклеарстенЦил (GL. h)
description: Функция ГлклеарстенЦил указывает значение Clear для буфера шаблона.
ms.assetid: bbde8fa8-78f3-45bd-bac3-5d03839acc52
keywords:
- Функция ГлклеарстенЦил OpenGL
topic_type:
- apiref
api_name:
- glClearStencil
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78d831540b4c7833368bbac075835faaec359695
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988791"
---
# <a name="glclearstencil-function"></a><span data-ttu-id="62027-104">Функция ГлклеарстенЦил</span><span class="sxs-lookup"><span data-stu-id="62027-104">glClearStencil function</span></span>

<span data-ttu-id="62027-105">Функция **глклеарстенЦил** указывает значение Clear для буфера шаблона.</span><span class="sxs-lookup"><span data-stu-id="62027-105">The **glClearStencil** function specifies the clear value for the stencil buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="62027-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="62027-106">Syntax</span></span>


```C++
void WINAPI glClearStencil(
   GLint s
);
```



## <a name="parameters"></a><span data-ttu-id="62027-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="62027-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62027-108">*s*</span><span class="sxs-lookup"><span data-stu-id="62027-108">*s*</span></span> 
</dt> <dd>

<span data-ttu-id="62027-109">Индекс, используемый при очистке буфера шаблона.</span><span class="sxs-lookup"><span data-stu-id="62027-109">The index used when the stencil buffer is cleared.</span></span> <span data-ttu-id="62027-110">Значение по умолчанию равно нулю.</span><span class="sxs-lookup"><span data-stu-id="62027-110">The default value is zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62027-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="62027-111">Return value</span></span>

<span data-ttu-id="62027-112">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="62027-112">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="62027-113">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="62027-113">Error codes</span></span>

<span data-ttu-id="62027-114">С помощью функции [**глжетеррор**](glgeterror.md) можно получить следующий код ошибки.</span><span class="sxs-lookup"><span data-stu-id="62027-114">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="62027-115">Имя</span><span class="sxs-lookup"><span data-stu-id="62027-115">Name</span></span>                                                                                                  | <span data-ttu-id="62027-116">Значение</span><span class="sxs-lookup"><span data-stu-id="62027-116">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="62027-117"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="62027-117"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="62027-118">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="62027-118">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="62027-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="62027-119">Remarks</span></span>

<span data-ttu-id="62027-120">Функция **глклеарстенЦил** указывает индекс, используемый [**глклеар**](glclear.md) для очистки буфера шаблона.</span><span class="sxs-lookup"><span data-stu-id="62027-120">The **glClearStencil** function specifies the index used by [**glClear**](glclear.md) to clear the stencil buffer.</span></span> <span data-ttu-id="62027-121">Параметр *s* замаскирован с 2 <sup>м</sup>  -1, где *m* — число битов в буфере шаблона.</span><span class="sxs-lookup"><span data-stu-id="62027-121">The *s* parameter is masked with 2 <sup>m</sup>  - 1, where *m* is the number of bits in the stencil buffer.</span></span>

<span data-ttu-id="62027-122">Следующие функции извлекают сведения, относящиеся к функции **глклеарстенЦил** :</span><span class="sxs-lookup"><span data-stu-id="62027-122">The following functions retrieve information related to the **glClearStencil** function:</span></span>

<span data-ttu-id="62027-123">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом \_ " \_ очистить значение трафарета GL" \_</span><span class="sxs-lookup"><span data-stu-id="62027-123">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_STENCIL\_CLEAR\_VALUE</span></span>

<span data-ttu-id="62027-124">**глжет** с аргументом \_ биты шаблона GL \_</span><span class="sxs-lookup"><span data-stu-id="62027-124">**glGet** with argument GL\_STENCIL\_BITS</span></span>

## <a name="requirements"></a><span data-ttu-id="62027-125">Требования</span><span class="sxs-lookup"><span data-stu-id="62027-125">Requirements</span></span>



| <span data-ttu-id="62027-126">Требование</span><span class="sxs-lookup"><span data-stu-id="62027-126">Requirement</span></span> | <span data-ttu-id="62027-127">Значение</span><span class="sxs-lookup"><span data-stu-id="62027-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="62027-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="62027-128">Minimum supported client</span></span><br/> | <span data-ttu-id="62027-129">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="62027-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="62027-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="62027-130">Minimum supported server</span></span><br/> | <span data-ttu-id="62027-131">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="62027-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="62027-132">Заголовок</span><span class="sxs-lookup"><span data-stu-id="62027-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="62027-133"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="62027-133"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="62027-134">Библиотека</span><span class="sxs-lookup"><span data-stu-id="62027-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="62027-135"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="62027-135"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="62027-136">DLL</span><span class="sxs-lookup"><span data-stu-id="62027-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62027-137"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62027-137"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62027-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="62027-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62027-139">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="62027-139">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="62027-140">**глклеар**</span><span class="sxs-lookup"><span data-stu-id="62027-140">**glClear**</span></span>](glclear.md)
</dt> <dt>

[<span data-ttu-id="62027-141">**гленд**</span><span class="sxs-lookup"><span data-stu-id="62027-141">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="62027-142">**глжет**</span><span class="sxs-lookup"><span data-stu-id="62027-142">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> </dl>

 

 





