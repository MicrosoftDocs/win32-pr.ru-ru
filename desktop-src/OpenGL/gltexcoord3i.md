---
title: Функция glTexCoord3i (GL. h)
description: Задает текущие координаты текстуры. | Функция glTexCoord3i (GL. h)
ms.assetid: a153bbce-9f8c-48e1-a33a-a4474efe3ffd
keywords:
- Функция glTexCoord3i OpenGL
topic_type:
- apiref
api_name:
- glTexCoord3i
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 757921bc1a3298b31be9cbcd76263dc6aa98593d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104000139"
---
# <a name="gltexcoord3i-function"></a><span data-ttu-id="dc277-105">Функция glTexCoord3i</span><span class="sxs-lookup"><span data-stu-id="dc277-105">glTexCoord3i function</span></span>

<span data-ttu-id="dc277-106">Задает текущие координаты текстуры.</span><span class="sxs-lookup"><span data-stu-id="dc277-106">Sets the current texture coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc277-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dc277-107">Syntax</span></span>


```C++
void WINAPI glTexCoord3i(
   GLint s,
   GLint t,
   GLint r
);
```



## <a name="parameters"></a><span data-ttu-id="dc277-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="dc277-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc277-109">*s*</span><span class="sxs-lookup"><span data-stu-id="dc277-109">*s*</span></span> 
</dt> <dd>

<span data-ttu-id="dc277-110">Координата текстуры "s".</span><span class="sxs-lookup"><span data-stu-id="dc277-110">The s texture coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="dc277-111">*t*</span><span class="sxs-lookup"><span data-stu-id="dc277-111">*t*</span></span> 
</dt> <dd>

<span data-ttu-id="dc277-112">Координата текстуры t.</span><span class="sxs-lookup"><span data-stu-id="dc277-112">The t texture coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="dc277-113">*r*</span><span class="sxs-lookup"><span data-stu-id="dc277-113">*r*</span></span> 
</dt> <dd>

<span data-ttu-id="dc277-114">Координата текстуры r.</span><span class="sxs-lookup"><span data-stu-id="dc277-114">The r texture coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc277-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dc277-115">Return value</span></span>

<span data-ttu-id="dc277-116">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="dc277-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc277-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dc277-117">Remarks</span></span>

<span data-ttu-id="dc277-118">Функция [**глтекскурд**](gltexcoord-functions.md) задает текущие координаты текстуры, которые являются частью данных, связанных с вершинами многоугольников.</span><span class="sxs-lookup"><span data-stu-id="dc277-118">The [**glTexCoord**](gltexcoord-functions.md) function sets the current texture coordinates that are part of the data associated with polygon vertices.</span></span> <span data-ttu-id="dc277-119">Функция **глтекскурд** задает координаты текстуры в одном, двух, трех или четырех измерениях.</span><span class="sxs-lookup"><span data-stu-id="dc277-119">The **glTexCoord** function specifies texture coordinates in one, two, three, or four dimensions.</span></span> <span data-ttu-id="dc277-120">Функция glTexCoord1 устанавливает для текущих координат текстуры значение (s, 0, 0, 1); вызов glTexCoord2 задает для них значение (s, t, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="dc277-120">The glTexCoord1 function sets the current texture coordinates to (s, 0, 0, 1); a call to glTexCoord2 sets them to (s, t, 0, 1).</span></span> <span data-ttu-id="dc277-121">Аналогичным образом glTexCoord3 определяет координаты текстуры как (s, t, r, 1), а glTexCoord4 определяет все четыре компонента явным образом (s, t, r, q).</span><span class="sxs-lookup"><span data-stu-id="dc277-121">Similarly, glTexCoord3 specifies the texture coordinates as (s, t, r, 1), and glTexCoord4 defines all four components explicitly as (s, t, r, q).</span></span> <span data-ttu-id="dc277-122">Текущие координаты текстуры можно обновить в любое время.</span><span class="sxs-lookup"><span data-stu-id="dc277-122">You can update the current texture coordinates at any time.</span></span> <span data-ttu-id="dc277-123">В частности, можно вызвать Глтекскурд между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="dc277-123">In particular, you can call glTexCoord between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="dc277-124">Следующая функция получает сведения, связанные с **глтекскурд**:</span><span class="sxs-lookup"><span data-stu-id="dc277-124">The following function retrieves information related to **glTexCoord**:</span></span>

<span data-ttu-id="dc277-125">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом в качестве \_ \_ координат текущей текстуры главной книги \_</span><span class="sxs-lookup"><span data-stu-id="dc277-125">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_TEXTURE\_COORDS</span></span>

## <a name="requirements"></a><span data-ttu-id="dc277-126">Требования</span><span class="sxs-lookup"><span data-stu-id="dc277-126">Requirements</span></span>



| <span data-ttu-id="dc277-127">Требование</span><span class="sxs-lookup"><span data-stu-id="dc277-127">Requirement</span></span> | <span data-ttu-id="dc277-128">Значение</span><span class="sxs-lookup"><span data-stu-id="dc277-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dc277-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dc277-129">Minimum supported client</span></span><br/> | <span data-ttu-id="dc277-130">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="dc277-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="dc277-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dc277-131">Minimum supported server</span></span><br/> | <span data-ttu-id="dc277-132">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="dc277-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="dc277-133">Заголовок</span><span class="sxs-lookup"><span data-stu-id="dc277-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc277-134"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc277-134"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="dc277-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="dc277-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="dc277-136"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dc277-136"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="dc277-137">DLL</span><span class="sxs-lookup"><span data-stu-id="dc277-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dc277-138"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dc277-138"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc277-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dc277-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc277-140">глвертекс</span><span class="sxs-lookup"><span data-stu-id="dc277-140">glVertex</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





