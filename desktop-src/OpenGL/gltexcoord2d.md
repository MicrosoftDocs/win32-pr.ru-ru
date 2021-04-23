---
title: Функция glTexCoord2d (GL. h)
description: Задает текущие координаты текстуры. | Функция glTexCoord2d (GL. h)
ms.assetid: 624d566f-72ae-4a7d-adad-5fcfee5b5aca
keywords:
- Функция glTexCoord2d OpenGL
topic_type:
- apiref
api_name:
- glTexCoord2d
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 825df8eb8adbfca08b11620d74928284a613780b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105684896"
---
# <a name="gltexcoord2d-function"></a><span data-ttu-id="9804b-105">Функция glTexCoord2d</span><span class="sxs-lookup"><span data-stu-id="9804b-105">glTexCoord2d function</span></span>

<span data-ttu-id="9804b-106">Задает текущие координаты текстуры.</span><span class="sxs-lookup"><span data-stu-id="9804b-106">Sets the current texture coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="9804b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9804b-107">Syntax</span></span>


```C++
void WINAPI glTexCoord2d(
   GLdouble s,
   GLdouble t
);
```



## <a name="parameters"></a><span data-ttu-id="9804b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9804b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9804b-109">*s*</span><span class="sxs-lookup"><span data-stu-id="9804b-109">*s*</span></span> 
</dt> <dd>

<span data-ttu-id="9804b-110">Координата текстуры "s".</span><span class="sxs-lookup"><span data-stu-id="9804b-110">The s texture coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="9804b-111">*t*</span><span class="sxs-lookup"><span data-stu-id="9804b-111">*t*</span></span> 
</dt> <dd>

<span data-ttu-id="9804b-112">Координата текстуры t.</span><span class="sxs-lookup"><span data-stu-id="9804b-112">The t texture coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9804b-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9804b-113">Return value</span></span>

<span data-ttu-id="9804b-114">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="9804b-114">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9804b-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9804b-115">Remarks</span></span>

<span data-ttu-id="9804b-116">Функция [**глтекскурд**](gltexcoord-functions.md) задает текущие координаты текстуры, которые являются частью данных, связанных с вершинами многоугольников.</span><span class="sxs-lookup"><span data-stu-id="9804b-116">The [**glTexCoord**](gltexcoord-functions.md) function sets the current texture coordinates that are part of the data associated with polygon vertices.</span></span> <span data-ttu-id="9804b-117">Функция **глтекскурд** задает координаты текстуры в одном, двух, трех или четырех измерениях.</span><span class="sxs-lookup"><span data-stu-id="9804b-117">The **glTexCoord** function specifies texture coordinates in one, two, three, or four dimensions.</span></span> <span data-ttu-id="9804b-118">Функция glTexCoord1 устанавливает для текущих координат текстуры значение (s, 0, 0, 1); вызов glTexCoord2 задает для них значение (s, t, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="9804b-118">The glTexCoord1 function sets the current texture coordinates to (s, 0, 0, 1); a call to glTexCoord2 sets them to (s, t, 0, 1).</span></span> <span data-ttu-id="9804b-119">Аналогичным образом glTexCoord3 определяет координаты текстуры как (s, t, r, 1), а glTexCoord4 определяет все четыре компонента явным образом (s, t, r, q).</span><span class="sxs-lookup"><span data-stu-id="9804b-119">Similarly, glTexCoord3 specifies the texture coordinates as (s, t, r, 1), and glTexCoord4 defines all four components explicitly as (s, t, r, q).</span></span> <span data-ttu-id="9804b-120">Текущие координаты текстуры можно обновить в любое время.</span><span class="sxs-lookup"><span data-stu-id="9804b-120">You can update the current texture coordinates at any time.</span></span> <span data-ttu-id="9804b-121">В частности, можно вызвать Глтекскурд между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="9804b-121">In particular, you can call glTexCoord between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="9804b-122">Следующая функция получает сведения, связанные с **глтекскурд**:</span><span class="sxs-lookup"><span data-stu-id="9804b-122">The following function retrieves information related to **glTexCoord**:</span></span>

<span data-ttu-id="9804b-123">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом в качестве \_ \_ координат текущей текстуры главной книги \_</span><span class="sxs-lookup"><span data-stu-id="9804b-123">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_TEXTURE\_COORDS</span></span>

## <a name="requirements"></a><span data-ttu-id="9804b-124">Требования</span><span class="sxs-lookup"><span data-stu-id="9804b-124">Requirements</span></span>



| <span data-ttu-id="9804b-125">Требование</span><span class="sxs-lookup"><span data-stu-id="9804b-125">Requirement</span></span> | <span data-ttu-id="9804b-126">Значение</span><span class="sxs-lookup"><span data-stu-id="9804b-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9804b-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9804b-127">Minimum supported client</span></span><br/> | <span data-ttu-id="9804b-128">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9804b-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="9804b-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9804b-129">Minimum supported server</span></span><br/> | <span data-ttu-id="9804b-130">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9804b-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9804b-131">Заголовок</span><span class="sxs-lookup"><span data-stu-id="9804b-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="9804b-132"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="9804b-132"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="9804b-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9804b-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="9804b-134"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9804b-134"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="9804b-135">DLL</span><span class="sxs-lookup"><span data-stu-id="9804b-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9804b-136"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9804b-136"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9804b-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9804b-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9804b-138">глвертекс</span><span class="sxs-lookup"><span data-stu-id="9804b-138">glVertex</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





