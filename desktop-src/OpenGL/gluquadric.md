---
title: Функция Глукуадриккаллбакк (GLU. h)
description: Функция Глукуадриккаллбакк определяет обратный вызов для объекта куадрик.
ms.assetid: 1f1e9fe9-7239-419c-92b6-af2534850ac5
keywords:
- Функция Глукуадриккаллбакк OpenGL
topic_type:
- apiref
api_name:
- gluQuadricCallback
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c0c92e3cd4e723b59ee9060c5e2f33b710e7f69
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534799"
---
# <a name="gluquadriccallback-function"></a><span data-ttu-id="50622-104">Функция Глукуадриккаллбакк</span><span class="sxs-lookup"><span data-stu-id="50622-104">gluQuadricCallback function</span></span>

<span data-ttu-id="50622-105">Функция **глукуадриккаллбакк** определяет обратный вызов для объекта куадрик.</span><span class="sxs-lookup"><span data-stu-id="50622-105">The **gluQuadricCallback** function defines a callback for a quadric object.</span></span>

## <a name="syntax"></a><span data-ttu-id="50622-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="50622-106">Syntax</span></span>


```C++
void WINAPI gluQuadricCallback(
   GLUquadric *qobj,
   GLenum     which,
   void (CALLBACK *fn)()
);
```



## <a name="parameters"></a><span data-ttu-id="50622-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="50622-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50622-108">*кобж*</span><span class="sxs-lookup"><span data-stu-id="50622-108">*qobj*</span></span> 
</dt> <dd>

<span data-ttu-id="50622-109">Объект куадрик (созданный с помощью [**глуневкуадрик**](glunewquadric.md)).</span><span class="sxs-lookup"><span data-stu-id="50622-109">The quadric object (created with [**gluNewQuadric**](glunewquadric.md)).</span></span>

</dd> <dt>

<span data-ttu-id="50622-110">*какую*</span><span class="sxs-lookup"><span data-stu-id="50622-110">*which*</span></span> 
</dt> <dd>

<span data-ttu-id="50622-111">Определяемый обратный вызов.</span><span class="sxs-lookup"><span data-stu-id="50622-111">The callback being defined.</span></span> <span data-ttu-id="50622-112">Единственное допустимое значение — GLU \_ Error.</span><span class="sxs-lookup"><span data-stu-id="50622-112">The only valid value is GLU\_ERROR.</span></span>



| <span data-ttu-id="50622-113">Значение</span><span class="sxs-lookup"><span data-stu-id="50622-113">Value</span></span>                                                                                                                                             | <span data-ttu-id="50622-114">Значение</span><span class="sxs-lookup"><span data-stu-id="50622-114">Meaning</span></span>                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GLU_ERROR"></span><span id="glu_error"></span><dl> <span data-ttu-id="50622-115"><dt>**GLU, \_ Ошибка**</dt></span><span class="sxs-lookup"><span data-stu-id="50622-115"><dt>**GLU\_ERROR**</dt></span></span> </dl> | <span data-ttu-id="50622-116">Функция **глукуадриккаллбакк** вызывается при возникновении ошибки.</span><span class="sxs-lookup"><span data-stu-id="50622-116">The **gluQuadricCallback** function is called when an error is encountered.</span></span> <span data-ttu-id="50622-117">Его единственный аргумент имеет тип **гленум** и указывает конкретную ошибку, которая возникла.</span><span class="sxs-lookup"><span data-stu-id="50622-117">Its single argument is of type **GLenum**, and it indicates the specific error that occurred.</span></span> <span data-ttu-id="50622-118">Символьные строки, описывающие эти ошибки, можно получить с помощью вызова [**глуеррорстринг**](gluerrorstring.md) .</span><span class="sxs-lookup"><span data-stu-id="50622-118">Character strings describing these errors can be retrieved with the [**gluErrorString**](gluerrorstring.md) call.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="50622-119">*FN*</span><span class="sxs-lookup"><span data-stu-id="50622-119">*fn*</span></span> 
</dt> <dd>

<span data-ttu-id="50622-120">Вызываемая функция.</span><span class="sxs-lookup"><span data-stu-id="50622-120">The function to be called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50622-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="50622-121">Return value</span></span>

<span data-ttu-id="50622-122">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="50622-122">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="50622-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="50622-123">Remarks</span></span>

<span data-ttu-id="50622-124">Используйте **глукуадриккаллбакк** для определения нового обратного вызова, который будет использоваться объектом куадрик.</span><span class="sxs-lookup"><span data-stu-id="50622-124">Use **gluQuadricCallback** to define a new callback to be used by a quadric object.</span></span> <span data-ttu-id="50622-125">Если указанный обратный вызов уже определен, он заменяется.</span><span class="sxs-lookup"><span data-stu-id="50622-125">If the specified callback is already defined, it is replaced.</span></span> <span data-ttu-id="50622-126">Если *fn* имеет **значение NULL**, любой существующий обратный вызов удаляется.</span><span class="sxs-lookup"><span data-stu-id="50622-126">If *fn* is **NULL**, any existing callback is erased.</span></span>

## <a name="requirements"></a><span data-ttu-id="50622-127">Требования</span><span class="sxs-lookup"><span data-stu-id="50622-127">Requirements</span></span>



| <span data-ttu-id="50622-128">Требование</span><span class="sxs-lookup"><span data-stu-id="50622-128">Requirement</span></span> | <span data-ttu-id="50622-129">Значение</span><span class="sxs-lookup"><span data-stu-id="50622-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="50622-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="50622-130">Minimum supported client</span></span><br/> | <span data-ttu-id="50622-131">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="50622-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="50622-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="50622-132">Minimum supported server</span></span><br/> | <span data-ttu-id="50622-133">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="50622-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="50622-134">Заголовок</span><span class="sxs-lookup"><span data-stu-id="50622-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="50622-135"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="50622-135"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="50622-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="50622-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="50622-137"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="50622-137"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="50622-138">DLL</span><span class="sxs-lookup"><span data-stu-id="50622-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="50622-139"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50622-139"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50622-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="50622-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50622-141">**глуеррорстринг**</span><span class="sxs-lookup"><span data-stu-id="50622-141">**gluErrorString**</span></span>](gluerrorstring.md)
</dt> <dt>

[<span data-ttu-id="50622-142">**глуневкуадрик**</span><span class="sxs-lookup"><span data-stu-id="50622-142">**gluNewQuadric**</span></span>](glunewquadric.md)
</dt> </dl>

 

 





