---
description: Представляет область, используемую распознавателем для рисования рукописного ввода. Область называется руководством по распознаванию.
ms.assetid: c4990aa5-8c8b-4206-8376-b5c0d0c8e0a7
title: Класс Инкрекогнизергуиде (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkRecognizerGuide
- InkRecognizerGuide.IInkRecognizerGuide
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 55729513f748afc87f184b73eaba976184307bc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272842"
---
# <a name="inkrecognizerguide-class"></a><span data-ttu-id="fa050-104">Класс Инкрекогнизергуиде</span><span class="sxs-lookup"><span data-stu-id="fa050-104">InkRecognizerGuide class</span></span>

<span data-ttu-id="fa050-105">Представляет область, используемую распознавателем для рисования рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="fa050-105">Represents the area that the recognizer uses in which ink can be drawn.</span></span> <span data-ttu-id="fa050-106">Область называется руководством по распознаванию.</span><span class="sxs-lookup"><span data-stu-id="fa050-106">The area is known as the recognition guide.</span></span>

<span data-ttu-id="fa050-107">**Инкрекогнизергуиде** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="fa050-107">**InkRecognizerGuide** has these types of members:</span></span>

-   [<span data-ttu-id="fa050-108">Интерфейсы</span><span class="sxs-lookup"><span data-stu-id="fa050-108">Interfaces</span></span>](#interfaces)
-   [<span data-ttu-id="fa050-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="fa050-109">Properties</span></span>](#properties)

### <a name="interfaces"></a><span data-ttu-id="fa050-110">Интерфейсы</span><span class="sxs-lookup"><span data-stu-id="fa050-110">Interfaces</span></span>

<span data-ttu-id="fa050-111">Класс **инкрекогнизергуиде** определяет эти интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="fa050-111">The **InkRecognizerGuide** class defines these interfaces.</span></span>



| <span data-ttu-id="fa050-112">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="fa050-112">Interface</span></span>               | <span data-ttu-id="fa050-113">Описание</span><span class="sxs-lookup"><span data-stu-id="fa050-113">Description</span></span>                                                                  |
|:------------------------|:-----------------------------------------------------------------------------|
| <span data-ttu-id="fa050-114">**иинкрекогнизергуиде**</span><span class="sxs-lookup"><span data-stu-id="fa050-114">**IInkRecognizerGuide**</span></span> | <span data-ttu-id="fa050-115">Этот объект реализует COM-интерфейс **иинкрекогнизергуиде** .</span><span class="sxs-lookup"><span data-stu-id="fa050-115">This object implements the **IInkRecognizerGuide** COM interface.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="fa050-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="fa050-116">Properties</span></span>

<span data-ttu-id="fa050-117">Класс **инкрекогнизергуиде** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="fa050-117">The **InkRecognizerGuide** class has these properties.</span></span>



| <span data-ttu-id="fa050-118">Свойство</span><span class="sxs-lookup"><span data-stu-id="fa050-118">Property</span></span>                                                       | <span data-ttu-id="fa050-119">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="fa050-119">Access type</span></span>           | <span data-ttu-id="fa050-120">Описание</span><span class="sxs-lookup"><span data-stu-id="fa050-120">Description</span></span>                                                                                                                    |
|:---------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fa050-121">**Столбцы**</span><span class="sxs-lookup"><span data-stu-id="fa050-121">**Columns**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_columns)<br/>       | <span data-ttu-id="fa050-122">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="fa050-122">Read/write</span></span><br/> | <span data-ttu-id="fa050-123">Возвращает или задает количество столбцов в поле с руководством.</span><span class="sxs-lookup"><span data-stu-id="fa050-123">Gets or sets the number of columns in the guide box.</span></span><br/>                                                                |
| [<span data-ttu-id="fa050-124">**дравнбокс**</span><span class="sxs-lookup"><span data-stu-id="fa050-124">**DrawnBox**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_drawnbox)<br/>     | <span data-ttu-id="fa050-125">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="fa050-125">Read/write</span></span><br/> | <span data-ttu-id="fa050-126">Возвращает или задает поле, которое физически рисуется на экране планшета и в котором происходит запись.</span><span class="sxs-lookup"><span data-stu-id="fa050-126">Gets or sets the box that is physically drawn on the tablet's screen and in which writing takes place.</span></span><br/>              |
| [<span data-ttu-id="fa050-127">**гуидедата**</span><span class="sxs-lookup"><span data-stu-id="fa050-127">**GuideData**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_guidedata)<br/>   | <span data-ttu-id="fa050-128">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="fa050-128">Read/write</span></span><br/> | <span data-ttu-id="fa050-129">Возвращает или задает данные руководств для разработчиков на C++.</span><span class="sxs-lookup"><span data-stu-id="fa050-129">Gets or sets guide data for C++ developers.</span></span><br/>                                                                         |
| [<span data-ttu-id="fa050-130">**Заполнение нажатием клавиши**</span><span class="sxs-lookup"><span data-stu-id="fa050-130">**Midline**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_midline)<br/>       | <span data-ttu-id="fa050-131">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="fa050-131">Read/write</span></span><br/> | <span data-ttu-id="fa050-132">Возвращает или задает высоту заполнение нажатием клавиши.</span><span class="sxs-lookup"><span data-stu-id="fa050-132">Gets or sets the midline height.</span></span> <span data-ttu-id="fa050-133">Высота заполнение нажатием клавиши — это расстояние от базовой линии до заполнение нажатием клавиши нарисованного бокса.</span><span class="sxs-lookup"><span data-stu-id="fa050-133">The midline height is distance from the baseline to the midline, of the drawn box.</span></span><br/> |
| [<span data-ttu-id="fa050-134">**Сквоз**</span><span class="sxs-lookup"><span data-stu-id="fa050-134">**Rows**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_rows)<br/>             | <span data-ttu-id="fa050-135">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="fa050-135">Read/write</span></span><br/> | <span data-ttu-id="fa050-136">Возвращает или задает количество строк в поле "Guide".</span><span class="sxs-lookup"><span data-stu-id="fa050-136">Gets or sets the number of rows in the guide box.</span></span><br/>                                                                   |
| [<span data-ttu-id="fa050-137">**вритингбокс**</span><span class="sxs-lookup"><span data-stu-id="fa050-137">**WritingBox**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_writingbox)<br/> | <span data-ttu-id="fa050-138">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="fa050-138">Read/write</span></span><br/> | <span data-ttu-id="fa050-139">Возвращает или задает невидимую область для записи в окне руководства, в которой может выполняться запись.</span><span class="sxs-lookup"><span data-stu-id="fa050-139">Gets or sets the invisible writing area of the guide box in which writing can actually take place.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="fa050-140">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fa050-140">Remarks</span></span>

<span data-ttu-id="fa050-141">Для создания экземпляра этого объекта можно вызвать метод [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) .</span><span class="sxs-lookup"><span data-stu-id="fa050-141">This object can be instantiated by calling the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) method.</span></span>

<span data-ttu-id="fa050-142">По умолчанию нет руководств по распознавателю.</span><span class="sxs-lookup"><span data-stu-id="fa050-142">By default, there is no recognizer guide.</span></span> <span data-ttu-id="fa050-143">По умолчанию для всех свойств задано значение 0.</span><span class="sxs-lookup"><span data-stu-id="fa050-143">A default guide has all property values set to 0.</span></span> <span data-ttu-id="fa050-144">Для настройки программы необходимо использовать свойства этого объекта.</span><span class="sxs-lookup"><span data-stu-id="fa050-144">You must use the properties of this object to set the guide.</span></span>

<span data-ttu-id="fa050-145">Если приложение выводит рекомендации на экране, на котором пользователь ожидает записи, приложение должно задать значения свойств руководства распознавателя, чтобы информировать распознаватель.</span><span class="sxs-lookup"><span data-stu-id="fa050-145">If the application has drawn guidelines on the screen on which the user is expected to write, the application should set the values of the properties of the recognizer guide to inform the recognizer.</span></span> <span data-ttu-id="fa050-146">Эти свойства предназначены только для использования распознавателя.</span><span class="sxs-lookup"><span data-stu-id="fa050-146">These properties are for the recognizer's use only.</span></span> <span data-ttu-id="fa050-147">В противном случае Нарисуйте визуальные подсказки на экране.</span><span class="sxs-lookup"><span data-stu-id="fa050-147">Setting them does not, by itself, draw visual clues on the display.</span></span> <span data-ttu-id="fa050-148">Приложение или элемент управления рисует визуальные подсказки.</span><span class="sxs-lookup"><span data-stu-id="fa050-148">The application or the control draws the visual clues.</span></span>

<span data-ttu-id="fa050-149">Средство распознавания может состоять из строк и столбцов, и они предоставляют распознавателю Улучшенный контекст, в котором выполняется распознавание.</span><span class="sxs-lookup"><span data-stu-id="fa050-149">The recognizer guide can consist of rows and columns, and these give the recognizer a better context in which to perform recognition.</span></span> <span data-ttu-id="fa050-150">Такие буквы, как «t» и «I», легче распознаются при использовании руководств для предоставления контекста рукописному вводу.</span><span class="sxs-lookup"><span data-stu-id="fa050-150">Letters such as "t" and "I" are more easily recognized when a guide is used to give context to the ink.</span></span> <span data-ttu-id="fa050-151">Например, можно нарисовать горизонтальные линии на экране, которые показывают, где должно происходить запись (этот тип руководства будет состоять только из строк и не содержит столбцов).</span><span class="sxs-lookup"><span data-stu-id="fa050-151">For example, you can draw horizontal lines on a screen, that show where writing should occur (this type of guide would consist only of rows, and no columns).</span></span> <span data-ttu-id="fa050-152">При написании строк вместо какого-либо произвольного пространства распознавание распознавания улучшается.</span><span class="sxs-lookup"><span data-stu-id="fa050-152">By writing on the lines, instead of some arbitrary space, recognition accuracy improves.</span></span>

<span data-ttu-id="fa050-153">В данном руководством определяются границы рукописного ввода в координатах рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="fa050-153">The guide specifies the boundaries of the ink in ink space coordinates.</span></span>

<span data-ttu-id="fa050-154">Свойство [**дравнбокс**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_drawnbox) может определять поле, размер которого совпадает с размером поля, определенного свойством [**вритингбокс**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_writingbox) , или меньше него.</span><span class="sxs-lookup"><span data-stu-id="fa050-154">The [**DrawnBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_drawnbox) property can define a box which is the same size as or smaller than the box defined by the [**WritingBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_writingbox) property.</span></span>

<span data-ttu-id="fa050-155">На следующем рисунке показаны элементы в руководству распознавателя с двумя строками и без столбцов.</span><span class="sxs-lookup"><span data-stu-id="fa050-155">The following figure shows the elements of a recognizer guide with two rows and no columns.</span></span>

![Иллюстрация, демонстрирующая элементы с руководством распознавателя](images/927cc2f3-549f-4279-aab9-bd5ade070eaf.jpg)

<span data-ttu-id="fa050-157">В дополнение к рисованию линий на экране, которые показывают пользователей, на которых нужно писать, можно нарисовать ячейки на экране, где записываются символы или слова.</span><span class="sxs-lookup"><span data-stu-id="fa050-157">In addition to drawing lines on the screen that show users where to write, you can draw cells on the screen in which characters or words are written.</span></span> <span data-ttu-id="fa050-158">Это называется Boxed Input и полезно для некоторых азиатских языков.</span><span class="sxs-lookup"><span data-stu-id="fa050-158">This is called boxed input and is useful with some Asian languages.</span></span> <span data-ttu-id="fa050-159">Чтобы определить, поддерживает ли распознаватель Упакованные входные данные, вызовите свойство [**capabilities**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_capabilities) объекта [**иинкрекогнизер**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) .</span><span class="sxs-lookup"><span data-stu-id="fa050-159">To determine if the recognizer is capable of boxed input, call the [**Capabilities**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_capabilities) property of the [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) object.</span></span>

<span data-ttu-id="fa050-160">На следующем рисунке показано средство распознавания с четырьмя столбцами.</span><span class="sxs-lookup"><span data-stu-id="fa050-160">The following figure shows a recognizer guide with four columns.</span></span>

![Иллюстрация с руководством распознавателя с четырьмя столбцами](images/de44c07e-4b55-42d0-8e8b-997e2da79e52.jpg)

## <a name="requirements"></a><span data-ttu-id="fa050-162">Требования</span><span class="sxs-lookup"><span data-stu-id="fa050-162">Requirements</span></span>



| <span data-ttu-id="fa050-163">Требование</span><span class="sxs-lookup"><span data-stu-id="fa050-163">Requirement</span></span> | <span data-ttu-id="fa050-164">Значение</span><span class="sxs-lookup"><span data-stu-id="fa050-164">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa050-165">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fa050-165">Minimum supported client</span></span><br/> | <span data-ttu-id="fa050-166">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="fa050-166">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="fa050-167">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fa050-167">Minimum supported server</span></span><br/> | <span data-ttu-id="fa050-168">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="fa050-168">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="fa050-169">Header</span><span class="sxs-lookup"><span data-stu-id="fa050-169">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa050-170"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="fa050-170"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="fa050-171">Библиотека</span><span class="sxs-lookup"><span data-stu-id="fa050-171">Library</span></span><br/>                  | <dl> <span data-ttu-id="fa050-172"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa050-172"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="fa050-173">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fa050-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa050-174">**Интерфейс Иинкрекогнизер**</span><span class="sxs-lookup"><span data-stu-id="fa050-174">**IInkRecognizer Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer)
</dt> <dt>

[<span data-ttu-id="fa050-175">**Класс Инкрекогнизерконтекст**</span><span class="sxs-lookup"><span data-stu-id="fa050-175">**InkRecognizerContext Class**</span></span>](inkrecognizercontext-class.md)
</dt> </dl>

 

