---
title: Функция glTexCoord3sv (GL. h)
description: Задает текущие координаты текстуры. | Функция glTexCoord3sv (GL. h)
ms.assetid: bd7970df-82b3-4ccd-960d-9c04a6726bab
keywords:
- Функция glTexCoord3sv OpenGL
topic_type:
- apiref
api_name:
- glTexCoord3sv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f193d0a918dea09e5ca8fa65f20c1bd4a49084d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "103914548"
---
# <a name="gltexcoord3sv-function"></a><span data-ttu-id="53cd8-105">Функция glTexCoord3sv</span><span class="sxs-lookup"><span data-stu-id="53cd8-105">glTexCoord3sv function</span></span>

<span data-ttu-id="53cd8-106">Задает текущие координаты текстуры.</span><span class="sxs-lookup"><span data-stu-id="53cd8-106">Sets the current texture coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="53cd8-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="53cd8-107">Syntax</span></span>


```C++
void WINAPI glTexCoord3sv(
   const GLshort *v
);
```



## <a name="parameters"></a><span data-ttu-id="53cd8-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="53cd8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53cd8-109">*3,3*</span><span class="sxs-lookup"><span data-stu-id="53cd8-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="53cd8-110">Указатель на массив из трех элементов, который, в свою очередь, указывает координаты s, t и r текстуры.</span><span class="sxs-lookup"><span data-stu-id="53cd8-110">A pointer to an array of three elements, which in turn specifies the s, t, and r texture coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53cd8-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="53cd8-111">Return value</span></span>

<span data-ttu-id="53cd8-112">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="53cd8-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="53cd8-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="53cd8-113">Remarks</span></span>

<span data-ttu-id="53cd8-114">Функция [**глтекскурд**](gltexcoord-functions.md) задает текущие координаты текстуры, которые являются частью данных, связанных с вершинами многоугольников.</span><span class="sxs-lookup"><span data-stu-id="53cd8-114">The [**glTexCoord**](gltexcoord-functions.md) function sets the current texture coordinates that are part of the data associated with polygon vertices.</span></span> <span data-ttu-id="53cd8-115">Функция **глтекскурд** задает координаты текстуры в одном, двух, трех или четырех измерениях.</span><span class="sxs-lookup"><span data-stu-id="53cd8-115">The **glTexCoord** function specifies texture coordinates in one, two, three, or four dimensions.</span></span> <span data-ttu-id="53cd8-116">Функция glTexCoord1 устанавливает для текущих координат текстуры значение (s, 0, 0, 1); вызов glTexCoord2 задает для них значение (s, t, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="53cd8-116">The glTexCoord1 function sets the current texture coordinates to (s, 0, 0, 1); a call to glTexCoord2 sets them to (s, t, 0, 1).</span></span> <span data-ttu-id="53cd8-117">Аналогичным образом glTexCoord3 определяет координаты текстуры как (s, t, r, 1), а glTexCoord4 определяет все четыре компонента явным образом (s, t, r, q).</span><span class="sxs-lookup"><span data-stu-id="53cd8-117">Similarly, glTexCoord3 specifies the texture coordinates as (s, t, r, 1), and glTexCoord4 defines all four components explicitly as (s, t, r, q).</span></span> <span data-ttu-id="53cd8-118">Текущие координаты текстуры можно обновить в любое время.</span><span class="sxs-lookup"><span data-stu-id="53cd8-118">You can update the current texture coordinates at any time.</span></span> <span data-ttu-id="53cd8-119">В частности, можно вызвать Глтекскурд между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="53cd8-119">In particular, you can call glTexCoord between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="53cd8-120">Следующая функция получает сведения, связанные с **глтекскурд**:</span><span class="sxs-lookup"><span data-stu-id="53cd8-120">The following function retrieves information related to **glTexCoord**:</span></span>

<span data-ttu-id="53cd8-121">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом в качестве \_ \_ координат текущей текстуры главной книги \_</span><span class="sxs-lookup"><span data-stu-id="53cd8-121">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_TEXTURE\_COORDS</span></span>

## <a name="requirements"></a><span data-ttu-id="53cd8-122">Требования</span><span class="sxs-lookup"><span data-stu-id="53cd8-122">Requirements</span></span>



| <span data-ttu-id="53cd8-123">Требование</span><span class="sxs-lookup"><span data-stu-id="53cd8-123">Requirement</span></span> | <span data-ttu-id="53cd8-124">Значение</span><span class="sxs-lookup"><span data-stu-id="53cd8-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="53cd8-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="53cd8-125">Minimum supported client</span></span><br/> | <span data-ttu-id="53cd8-126">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="53cd8-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="53cd8-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="53cd8-127">Minimum supported server</span></span><br/> | <span data-ttu-id="53cd8-128">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="53cd8-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="53cd8-129">Заголовок</span><span class="sxs-lookup"><span data-stu-id="53cd8-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="53cd8-130"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="53cd8-130"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="53cd8-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="53cd8-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="53cd8-132"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="53cd8-132"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="53cd8-133">DLL</span><span class="sxs-lookup"><span data-stu-id="53cd8-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="53cd8-134"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53cd8-134"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53cd8-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="53cd8-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53cd8-136">глвертекс</span><span class="sxs-lookup"><span data-stu-id="53cd8-136">glVertex</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





