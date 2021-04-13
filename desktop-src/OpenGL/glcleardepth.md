---
title: Функция Глклеардепс (GL. h)
description: Функция Глклеардепс указывает значение Clear для буфера глубины.
ms.assetid: 8e26ae78-edc1-4201-a0db-d5bc8ae6dc82
keywords:
- Функция Глклеардепс OpenGL
topic_type:
- apiref
api_name:
- glClearDepth
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9cf968c7ae172bf4ce354c84b2071d62304327ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340780"
---
# <a name="glcleardepth-function"></a><span data-ttu-id="5a3e6-104">Функция Глклеардепс</span><span class="sxs-lookup"><span data-stu-id="5a3e6-104">glClearDepth function</span></span>

<span data-ttu-id="5a3e6-105">Функция **глклеардепс** указывает значение Clear для буфера глубины.</span><span class="sxs-lookup"><span data-stu-id="5a3e6-105">The **glClearDepth** function specifies the clear value for the depth buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a3e6-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5a3e6-106">Syntax</span></span>


```C++
void WINAPI glClearDepth(
   GLclampd depth
);
```



## <a name="parameters"></a><span data-ttu-id="5a3e6-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="5a3e6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a3e6-108">*Длина*</span><span class="sxs-lookup"><span data-stu-id="5a3e6-108">*depth*</span></span> 
</dt> <dd>

<span data-ttu-id="5a3e6-109">Значение глубины, используемое при очистке буфера глубины.</span><span class="sxs-lookup"><span data-stu-id="5a3e6-109">The depth value used when the depth buffer is cleared.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a3e6-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5a3e6-110">Return value</span></span>

<span data-ttu-id="5a3e6-111">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="5a3e6-111">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="5a3e6-112">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="5a3e6-112">Error codes</span></span>

<span data-ttu-id="5a3e6-113">С помощью функции [**глжетеррор**](glgeterror.md) можно получить следующий код ошибки.</span><span class="sxs-lookup"><span data-stu-id="5a3e6-113">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="5a3e6-114">Имя</span><span class="sxs-lookup"><span data-stu-id="5a3e6-114">Name</span></span>                                                                                                  | <span data-ttu-id="5a3e6-115">Значение</span><span class="sxs-lookup"><span data-stu-id="5a3e6-115">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5a3e6-116"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="5a3e6-116"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="5a3e6-117">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="5a3e6-117">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="5a3e6-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5a3e6-118">Remarks</span></span>

<span data-ttu-id="5a3e6-119">Функция **глклеардепс** указывает значение глубины, используемое [**глклеар**](glclear.md) для очистки буфера глубины.</span><span class="sxs-lookup"><span data-stu-id="5a3e6-119">The **glClearDepth** function specifies the depth value used by [**glClear**](glclear.md) to clear the depth buffer.</span></span> <span data-ttu-id="5a3e6-120">Значения, заданные параметром **глклеардепс** , записываются в диапазон \[ 0, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="5a3e6-120">Values specified by **glClearDepth** are clamped to the range \[0,1\].</span></span>

<span data-ttu-id="5a3e6-121">Следующая функция получает сведения, связанные с функцией **глклеардепс** :</span><span class="sxs-lookup"><span data-stu-id="5a3e6-121">The following function retrieves information related to the **glClearDepth** function:</span></span>

<span data-ttu-id="5a3e6-122">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом \_ " \_ Очистка \_ значения глубины GL"</span><span class="sxs-lookup"><span data-stu-id="5a3e6-122">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_DEPTH\_CLEAR\_VALUE</span></span>

## <a name="requirements"></a><span data-ttu-id="5a3e6-123">Требования</span><span class="sxs-lookup"><span data-stu-id="5a3e6-123">Requirements</span></span>



| <span data-ttu-id="5a3e6-124">Требование</span><span class="sxs-lookup"><span data-stu-id="5a3e6-124">Requirement</span></span> | <span data-ttu-id="5a3e6-125">Значение</span><span class="sxs-lookup"><span data-stu-id="5a3e6-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5a3e6-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5a3e6-126">Minimum supported client</span></span><br/> | <span data-ttu-id="5a3e6-127">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5a3e6-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="5a3e6-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5a3e6-128">Minimum supported server</span></span><br/> | <span data-ttu-id="5a3e6-129">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5a3e6-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5a3e6-130">Заголовок</span><span class="sxs-lookup"><span data-stu-id="5a3e6-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a3e6-131"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a3e6-131"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="5a3e6-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5a3e6-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="5a3e6-133"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5a3e6-133"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="5a3e6-134">DLL</span><span class="sxs-lookup"><span data-stu-id="5a3e6-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5a3e6-135"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a3e6-135"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a3e6-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5a3e6-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a3e6-137">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="5a3e6-137">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="5a3e6-138">**глклеар**</span><span class="sxs-lookup"><span data-stu-id="5a3e6-138">**glClear**</span></span>](glclear.md)
</dt> <dt>

[<span data-ttu-id="5a3e6-139">**гленд**</span><span class="sxs-lookup"><span data-stu-id="5a3e6-139">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="5a3e6-140">**глжет**</span><span class="sxs-lookup"><span data-stu-id="5a3e6-140">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> </dl>

 

 





