---
description: Представляет матрицу 3x3, которая, в свою очередь, представляет аффинное преобразование.
ms.assetid: 79abff2e-d1d3-4a32-9ac2-f46c1b21f742
title: Класс Инктрансформ (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkTransform
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 61641f0fed8ec98321e155f82ff9a35150e7fdcd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105713065"
---
# <a name="inktransform-class"></a><span data-ttu-id="6d228-103">Класс Инктрансформ</span><span class="sxs-lookup"><span data-stu-id="6d228-103">InkTransform class</span></span>

<span data-ttu-id="6d228-104">Представляет матрицу 3x3, которая, в свою очередь, представляет аффинное преобразование.</span><span class="sxs-lookup"><span data-stu-id="6d228-104">Represents a 3x3 matrix that, in turn, represents an affine transformation.</span></span>

<span data-ttu-id="6d228-105">**Инктрансформ** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="6d228-105">**InkTransform** has these types of members:</span></span>

-   [<span data-ttu-id="6d228-106">Методы</span><span class="sxs-lookup"><span data-stu-id="6d228-106">Methods</span></span>](#methods)
-   [<span data-ttu-id="6d228-107">Свойства</span><span class="sxs-lookup"><span data-stu-id="6d228-107">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="6d228-108">Методы</span><span class="sxs-lookup"><span data-stu-id="6d228-108">Methods</span></span>

<span data-ttu-id="6d228-109">Класс **инктрансформ** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="6d228-109">The **InkTransform** class has these methods.</span></span>



| <span data-ttu-id="6d228-110">Метод</span><span class="sxs-lookup"><span data-stu-id="6d228-110">Method</span></span>                                                  | <span data-ttu-id="6d228-111">Описание</span><span class="sxs-lookup"><span data-stu-id="6d228-111">Description</span></span>                                                                                                                 |
|:--------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6d228-112">**Преобразование**</span><span class="sxs-lookup"><span data-stu-id="6d228-112">**GetTransform**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-gettransform)       | <span data-ttu-id="6d228-113">Извлекает **инктрансформ** как 6 с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="6d228-113">Retrieves the **InkTransform** as 6 floats.</span></span><br/>                                                                      |
| [<span data-ttu-id="6d228-114">**Характеризу**</span><span class="sxs-lookup"><span data-stu-id="6d228-114">**Reflect**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-reflect)                 | <span data-ttu-id="6d228-115">Отражает преобразование в горизонтальном или вертикальном направлении.</span><span class="sxs-lookup"><span data-stu-id="6d228-115">Reflects the transform in either the horizontal or vertical directions.</span></span><br/>                                          |
| [<span data-ttu-id="6d228-116">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="6d228-116">**Reset**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-reset)                     | <span data-ttu-id="6d228-117">Сбрасывает преобразование в исходное состояние.</span><span class="sxs-lookup"><span data-stu-id="6d228-117">Resets the transform to its original state.</span></span><br/>                                                                      |
| [<span data-ttu-id="6d228-118">**Поворот**</span><span class="sxs-lookup"><span data-stu-id="6d228-118">**Rotate**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-rotate)                   | <span data-ttu-id="6d228-119">Поворачивает преобразование на угол, измеренный в градусах, и при необходимости задает центральную точку для поворота.</span><span class="sxs-lookup"><span data-stu-id="6d228-119">Rotates the transform by an angle measured in degrees, and optionally specifies a center point for the rotation.</span></span><br/> |
| [<span data-ttu-id="6d228-120">**ScaleTransform**</span><span class="sxs-lookup"><span data-stu-id="6d228-120">**ScaleTransform**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-scaletransform) | <span data-ttu-id="6d228-121">Масштабирует преобразование по коэффициентам X и Y.</span><span class="sxs-lookup"><span data-stu-id="6d228-121">Scales the transform by X and Y factors.</span></span><br/>                                                                         |
| [<span data-ttu-id="6d228-122">**сеттрансформ**</span><span class="sxs-lookup"><span data-stu-id="6d228-122">**SetTransform**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-settransform)       | <span data-ttu-id="6d228-123">Изменяет **инктрансформ** , используя 6 с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="6d228-123">Modifies the **InkTransform** using 6 floats.</span></span><br/>                                                                    |
| [<span data-ttu-id="6d228-124">**Сдвиг**</span><span class="sxs-lookup"><span data-stu-id="6d228-124">**Shear**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-shear)                     | <span data-ttu-id="6d228-125">Применяет наклон с заданными коэффициентами горизонтального и вертикального.</span><span class="sxs-lookup"><span data-stu-id="6d228-125">Applies a shear with the specified horizontal and vertical factors.</span></span><br/>                                              |
| [<span data-ttu-id="6d228-126">**Перевести**</span><span class="sxs-lookup"><span data-stu-id="6d228-126">**Translate**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-translate)             | <span data-ttu-id="6d228-127">Перемещает преобразование на указанные горизонтальные и вертикальные компоненты.</span><span class="sxs-lookup"><span data-stu-id="6d228-127">Moves the transform by the specified horizontal and vertical components.</span></span><br/>                                         |



 

### <a name="properties"></a><span data-ttu-id="6d228-128">Свойства</span><span class="sxs-lookup"><span data-stu-id="6d228-128">Properties</span></span>

<span data-ttu-id="6d228-129">Класс **инктрансформ** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="6d228-129">The **InkTransform** class has these properties.</span></span>



| <span data-ttu-id="6d228-130">Свойство</span><span class="sxs-lookup"><span data-stu-id="6d228-130">Property</span></span>                                     | <span data-ttu-id="6d228-131">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="6d228-131">Access type</span></span>           | <span data-ttu-id="6d228-132">Описание</span><span class="sxs-lookup"><span data-stu-id="6d228-132">Description</span></span>                                                                                          |
|:---------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6d228-133">**Данные**</span><span class="sxs-lookup"><span data-stu-id="6d228-133">**Data**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_data)<br/> | <span data-ttu-id="6d228-134">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="6d228-134">Read/write</span></span><br/> | <span data-ttu-id="6d228-135">Возвращает или задает версию автоматизации структуры XFORM WIN32.</span><span class="sxs-lookup"><span data-stu-id="6d228-135">Gets or sets the Automation version of the WIN32 XFORM struct.</span></span><br/>                            |
| [<span data-ttu-id="6d228-136">**eDx**</span><span class="sxs-lookup"><span data-stu-id="6d228-136">**eDx**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_edx)<br/>   | <span data-ttu-id="6d228-137">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="6d228-137">Read/write</span></span><br/> | <span data-ttu-id="6d228-138">Возвращает или задает вещественное число, указывающее элемент в третьей строке, первый столбец.</span><span class="sxs-lookup"><span data-stu-id="6d228-138">Gets or sets the real number that specifies the element in the third row, first column.</span></span><br/>   |
| [<span data-ttu-id="6d228-139">**еди**</span><span class="sxs-lookup"><span data-stu-id="6d228-139">**eDy**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_edy)<br/>   | <span data-ttu-id="6d228-140">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="6d228-140">Read/write</span></span><br/> | <span data-ttu-id="6d228-141">Возвращает или задает вещественное число, указывающее элемент в третьей строке второго столбца.</span><span class="sxs-lookup"><span data-stu-id="6d228-141">Gets or sets the real number that specifies the element in the third row, second column.</span></span><br/>  |
| [<span data-ttu-id="6d228-142">**eM11**</span><span class="sxs-lookup"><span data-stu-id="6d228-142">**eM11**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_em11)<br/> | <span data-ttu-id="6d228-143">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="6d228-143">Read/write</span></span><br/> | <span data-ttu-id="6d228-144">Возвращает или задает вещественное число, указывающее элемент в первой строке, первый столбец.</span><span class="sxs-lookup"><span data-stu-id="6d228-144">Gets or sets the real number that specifies the element in the first row, first column.</span></span><br/>   |
| [<span data-ttu-id="6d228-145">**eM12**</span><span class="sxs-lookup"><span data-stu-id="6d228-145">**eM12**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_em12)<br/> | <span data-ttu-id="6d228-146">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="6d228-146">Read/write</span></span><br/> | <span data-ttu-id="6d228-147">Возвращает или задает вещественное число, указывающее элемент в первой строке второго столбца.</span><span class="sxs-lookup"><span data-stu-id="6d228-147">Gets or sets the real number that specifies the element in the first row, second column.</span></span><br/>  |
| [<span data-ttu-id="6d228-148">**eM21**</span><span class="sxs-lookup"><span data-stu-id="6d228-148">**eM21**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_em21)<br/> | <span data-ttu-id="6d228-149">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="6d228-149">Read/write</span></span><br/> | <span data-ttu-id="6d228-150">Возвращает или задает вещественное число, указывающее элемент во второй строке, первый столбец.</span><span class="sxs-lookup"><span data-stu-id="6d228-150">Gets or sets the real number that specifies the element in the second row, first column.</span></span><br/>  |
| [<span data-ttu-id="6d228-151">**eM22**</span><span class="sxs-lookup"><span data-stu-id="6d228-151">**eM22**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_em22)<br/> | <span data-ttu-id="6d228-152">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="6d228-152">Read/write</span></span><br/> | <span data-ttu-id="6d228-153">Возвращает или задает вещественное число, указывающее элемент во второй строке второго столбца.</span><span class="sxs-lookup"><span data-stu-id="6d228-153">Gets or sets the real number that specifies the element in the second row, second column.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6d228-154">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6d228-154">Remarks</span></span>

<span data-ttu-id="6d228-155">Для создания экземпляра этого объекта можно вызвать метод [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) в C++.</span><span class="sxs-lookup"><span data-stu-id="6d228-155">This object can be instantiated by calling the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) method in C++.</span></span>

<span data-ttu-id="6d228-156">Объект хранит только шесть из девяти чисел в матрице 3x3, так как все матрицы 3x3, представляющие аффинных преобразований, имеют тот же третий столбец (0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="6d228-156">The object stores only six of the nine numbers in a 3x3 matrix because all 3x3 matrices that represent affine transformations have the same third column (0, 0, 1).</span></span> <span data-ttu-id="6d228-157">Этот объект в свою очередь используется для описания операций преобразования, таких как перемещение, наклон, масштабирование или вращение в объекте [**инкрендерер**](inkrenderer-class.md) , [**Иинкстрокедисп**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) Object или [инкстрокес](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) Collection.</span><span class="sxs-lookup"><span data-stu-id="6d228-157">This object in turn is used to describe transformation operations such as moving, shearing, scaling, or rotating in an [**InkRenderer**](inkrenderer-class.md) object, [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object, or [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection.</span></span>

> [!Note]  
> <span data-ttu-id="6d228-158">Объект **инктрансформ** соотносится с структурой [**XForm**](/windows/win32/api/wingdi/ns-wingdi-xform) .</span><span class="sxs-lookup"><span data-stu-id="6d228-158">The **InkTransform** object correlates to the [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) structure.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6d228-159">Требования</span><span class="sxs-lookup"><span data-stu-id="6d228-159">Requirements</span></span>



| <span data-ttu-id="6d228-160">Требование</span><span class="sxs-lookup"><span data-stu-id="6d228-160">Requirement</span></span> | <span data-ttu-id="6d228-161">Значение</span><span class="sxs-lookup"><span data-stu-id="6d228-161">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d228-162">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6d228-162">Minimum supported client</span></span><br/> | <span data-ttu-id="6d228-163">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="6d228-163">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="6d228-164">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6d228-164">Minimum supported server</span></span><br/> | <span data-ttu-id="6d228-165">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="6d228-165">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="6d228-166">Header</span><span class="sxs-lookup"><span data-stu-id="6d228-166">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d228-167"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="6d228-167"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="6d228-168">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6d228-168">Library</span></span><br/>                  | <dl> <span data-ttu-id="6d228-169"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d228-169"><dt>InkObj.dll</dt></span></span> </dl>                               |



 

