---
title: Функция Глжетпоинтерв (GL. h)
description: Функция Глжетпоинтерв возвращает адрес массива данных вершины.
ms.assetid: 6f85c508-9335-4474-8cc5-e67c7421a8e4
keywords:
- Функция Глжетпоинтерв OpenGL
topic_type:
- apiref
api_name:
- glGetPointerv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 569861922514af88835fbb4e313dab3286b7c47d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682023"
---
# <a name="glgetpointerv-function"></a><span data-ttu-id="65b17-104">Функция Глжетпоинтерв</span><span class="sxs-lookup"><span data-stu-id="65b17-104">glGetPointerv function</span></span>

<span data-ttu-id="65b17-105">Функция **глжетпоинтерв** возвращает адрес массива данных вершины.</span><span class="sxs-lookup"><span data-stu-id="65b17-105">The **glGetPointerv** function returns the address of a vertex data array.</span></span>

## <a name="syntax"></a><span data-ttu-id="65b17-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="65b17-106">Syntax</span></span>


```C++
void WINAPI glGetPointerv(
   GLenum pname,
   GLvoid **params
);
```



## <a name="parameters"></a><span data-ttu-id="65b17-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="65b17-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65b17-108">*pname*</span><span class="sxs-lookup"><span data-stu-id="65b17-108">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="65b17-109">Тип указателя на массив, возвращаемый из следующих символьных констант: \_ указатель на \_ массив цветов GL \_ , \_ указатель на \_ массив флагов GL, указатель на \_ \_ \_ буфер обратной связи GL, указатель \_ \_ \_ массива индексов GL \_ \_ , стандартный указатель на массив, GL \_ \_ \_ , \_ текстура \_ курд, указатель на \_ \_ \_ буфер выбора, а также указатель на \_ \_ \_ массив вершин \_ \_ в ГК.</span><span class="sxs-lookup"><span data-stu-id="65b17-109">The type of array pointer to return from the following symbolic constants: GL\_COLOR\_ARRAY\_POINTER, GL\_EDGE\_FLAG\_ARRAY\_POINTER, GL\_FEEDBACK\_BUFFER\_POINTER, GL\_INDEX\_ARRAY\_POINTER, GL\_NORMAL\_ARRAY\_POINTER, GL\_TEXTURE\_COORD\_ARRAY\_POINTER, GL\_SELECTION\_BUFFER\_POINTER, and GL\_VERTEX\_ARRAY\_POINTER.</span></span>

</dd> <dt>

<span data-ttu-id="65b17-110">*params*</span><span class="sxs-lookup"><span data-stu-id="65b17-110">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="65b17-111">Возвращает значение указателя массива, заданного параметром *pname*.</span><span class="sxs-lookup"><span data-stu-id="65b17-111">Returns the value of the array pointer specified by *pname*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65b17-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="65b17-112">Return value</span></span>

<span data-ttu-id="65b17-113">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="65b17-113">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="65b17-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="65b17-114">Error codes</span></span>

<span data-ttu-id="65b17-115">С помощью функции [**глжетеррор**](glgeterror.md) можно получить следующий код ошибки.</span><span class="sxs-lookup"><span data-stu-id="65b17-115">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="65b17-116">Имя</span><span class="sxs-lookup"><span data-stu-id="65b17-116">Name</span></span>                                                                                             | <span data-ttu-id="65b17-117">Значение</span><span class="sxs-lookup"><span data-stu-id="65b17-117">Meaning</span></span>                                       |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="65b17-118"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="65b17-118"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl> | <span data-ttu-id="65b17-119">*pname* не является допустимым значением.</span><span class="sxs-lookup"><span data-stu-id="65b17-119">*pname* was not an accepted value.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="65b17-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="65b17-120">Remarks</span></span>

<span data-ttu-id="65b17-121">Функция **глжетпоинтерв** возвращает сведения о указателе на массив.</span><span class="sxs-lookup"><span data-stu-id="65b17-121">The **glGetPointerv** function returns array pointer information.</span></span> <span data-ttu-id="65b17-122">Параметр *pname* — это символьная константа, указывающая вид возвращаемого указателя массива, а *params* — это указатель на расположение для размещения возвращаемых данных.</span><span class="sxs-lookup"><span data-stu-id="65b17-122">The *pname* parameter is a symbolic constant specifying the kind of array pointer to return, and *params* is a pointer to a location to place the returned data.</span></span>

## <a name="requirements"></a><span data-ttu-id="65b17-123">Требования</span><span class="sxs-lookup"><span data-stu-id="65b17-123">Requirements</span></span>



| <span data-ttu-id="65b17-124">Требование</span><span class="sxs-lookup"><span data-stu-id="65b17-124">Requirement</span></span> | <span data-ttu-id="65b17-125">Значение</span><span class="sxs-lookup"><span data-stu-id="65b17-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="65b17-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="65b17-126">Minimum supported client</span></span><br/> | <span data-ttu-id="65b17-127">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="65b17-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="65b17-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="65b17-128">Minimum supported server</span></span><br/> | <span data-ttu-id="65b17-129">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="65b17-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="65b17-130">Заголовок</span><span class="sxs-lookup"><span data-stu-id="65b17-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="65b17-131"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="65b17-131"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="65b17-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="65b17-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="65b17-133"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="65b17-133"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="65b17-134">DLL</span><span class="sxs-lookup"><span data-stu-id="65b17-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65b17-135"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65b17-135"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65b17-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="65b17-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65b17-137">**гларрайелемент**</span><span class="sxs-lookup"><span data-stu-id="65b17-137">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="65b17-138">**глколорпоинтер**</span><span class="sxs-lookup"><span data-stu-id="65b17-138">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="65b17-139">**глдраваррайс**</span><span class="sxs-lookup"><span data-stu-id="65b17-139">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="65b17-140">**гледжефлагпоинтер**</span><span class="sxs-lookup"><span data-stu-id="65b17-140">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="65b17-141">**глжетстринг**</span><span class="sxs-lookup"><span data-stu-id="65b17-141">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="65b17-142">**глиндекспоинтер**</span><span class="sxs-lookup"><span data-stu-id="65b17-142">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="65b17-143">**глнормалпоинтер**</span><span class="sxs-lookup"><span data-stu-id="65b17-143">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="65b17-144">**глтекскурдпоинтер**</span><span class="sxs-lookup"><span data-stu-id="65b17-144">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="65b17-145">**глвертекспоинтер**</span><span class="sxs-lookup"><span data-stu-id="65b17-145">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 





