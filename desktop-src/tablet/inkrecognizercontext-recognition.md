---
description: Происходит, когда Инкрекогнизерконтекст создает результаты из метода Баккграундрекогнизе.
ms.assetid: 0cc319af-cd0b-4089-928b-cae6c86f6f61
title: Событие Инкрекогнизерконтекст. Recognition (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86da1a7470169f9f978e92a87f3e32f7e63acb42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105719658"
---
# <a name="inkrecognizercontextrecognition-event"></a><span data-ttu-id="01957-103">Событие Инкрекогнизерконтекст. Recognition</span><span class="sxs-lookup"><span data-stu-id="01957-103">InkRecognizerContext.Recognition event</span></span>

<span data-ttu-id="01957-104">Происходит, когда [**инкрекогнизерконтекст**](inkrecognizercontext-class.md) создает результаты из метода [**баккграундрекогнизе**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize) .</span><span class="sxs-lookup"><span data-stu-id="01957-104">Occurs when the [**InkRecognizerContext**](inkrecognizercontext-class.md) has generated results from the [**BackgroundRecognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="01957-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="01957-105">Syntax</span></span>


```C++
void Recognition(
  [in] BSTR                 RecognizedString,
  [in] VARIANT              CustomData,
  [in] InkRecognitionStatus RecognitionStatus
);
```



## <a name="parameters"></a><span data-ttu-id="01957-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="01957-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01957-107">*Рекогнизедстринг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="01957-107">*RecognizedString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01957-108">Текст результата распознавания с наибольшей достоверностью.</span><span class="sxs-lookup"><span data-stu-id="01957-108">The recognition result text with the highest confidence.</span></span>

<span data-ttu-id="01957-109">Дополнительные сведения о типе данных BSTR см. в разделе [Использование библиотеки COM](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="01957-109">For more information about the BSTR data type, see the [Using the COM Library](using-the-com-library.md).</span></span>

</dd> <dt>

<span data-ttu-id="01957-110">*CustomData* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="01957-110">*CustomData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01957-111">Объект, содержащий пользовательские данные для результата распознавания.</span><span class="sxs-lookup"><span data-stu-id="01957-111">The object that contains the custom data for the recognition result.</span></span>

<span data-ttu-id="01957-112">Дополнительные сведения о структуре вариантов см. в разделе [Использование библиотеки COM](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="01957-112">For more information about the VARIANT structure, see the [Using the COM Library](using-the-com-library.md).</span></span>

</dd> <dt>

<span data-ttu-id="01957-113">*Рекогнитионстатус* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="01957-113">*RecognitionStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01957-114">Состояние распознавания на самый последний результат распознавания.</span><span class="sxs-lookup"><span data-stu-id="01957-114">The recognition status as of the most recent recognition result.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01957-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="01957-115">Return value</span></span>

<span data-ttu-id="01957-116">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="01957-116">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="01957-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="01957-117">Remarks</span></span>

<span data-ttu-id="01957-118">Поведение прикладного программного интерфейса (API) непредсказуемо, если вы попытаетесь получить доступ к исходному объекту [**инкрекогнизерконтекст**](inkrecognizercontext-class.md) из обработчика событий распознавания.</span><span class="sxs-lookup"><span data-stu-id="01957-118">The behavior of the application programming interface (API) is unpredictable if you try to gain access to the original [**InkRecognizerContext**](inkrecognizercontext-class.md) object from the recognition event handler.</span></span> <span data-ttu-id="01957-119">Не пытайтесь это сделать.</span><span class="sxs-lookup"><span data-stu-id="01957-119">Do not attempt to do this.</span></span> <span data-ttu-id="01957-120">Вместо этого, если это необходимо, создайте флаг и задайте его в обработчике событий [распознавания](ink-recognition.md) .</span><span class="sxs-lookup"><span data-stu-id="01957-120">Instead, if you need to do this, create a flag and set it in the [Recognition](ink-recognition.md) event handler.</span></span> <span data-ttu-id="01957-121">Затем можно опросить этот флаг, чтобы определить, когда следует изменять свойства **инкрекогнизерконтекст** за пределами обработчика событий.</span><span class="sxs-lookup"><span data-stu-id="01957-121">Then you can poll that flag to determine when to change the **InkRecognizerContext** properties outside of the event handler.</span></span>

<span data-ttu-id="01957-122">Этот метод события определен в \_ интерфейсе иинкевентс.</span><span class="sxs-lookup"><span data-stu-id="01957-122">This event method is defined in the \_IInkEvents interface.</span></span> <span data-ttu-id="01957-123">\_Интерфейс иинкевентс реализует интерфейс [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) с идентификатором DISPID \_ иререкогнитион.</span><span class="sxs-lookup"><span data-stu-id="01957-123">The \_IInkEvents interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IRERecognition.</span></span>

## <a name="requirements"></a><span data-ttu-id="01957-124">Требования</span><span class="sxs-lookup"><span data-stu-id="01957-124">Requirements</span></span>



| <span data-ttu-id="01957-125">Требование</span><span class="sxs-lookup"><span data-stu-id="01957-125">Requirement</span></span> | <span data-ttu-id="01957-126">Значение</span><span class="sxs-lookup"><span data-stu-id="01957-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01957-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="01957-127">Minimum supported client</span></span><br/> | <span data-ttu-id="01957-128">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="01957-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="01957-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="01957-129">Minimum supported server</span></span><br/> | <span data-ttu-id="01957-130">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="01957-130">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="01957-131">Header</span><span class="sxs-lookup"><span data-stu-id="01957-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="01957-132"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="01957-132"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="01957-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="01957-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="01957-134"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01957-134"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="01957-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="01957-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01957-136">**Класс Инкрекогнизерконтекст**</span><span class="sxs-lookup"><span data-stu-id="01957-136">**InkRecognizerContext Class**</span></span>](inkrecognizercontext-class.md)
</dt> <dt>

[<span data-ttu-id="01957-137">**Метод Баккграундрекогнизе**</span><span class="sxs-lookup"><span data-stu-id="01957-137">**BackgroundRecognize Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize)
</dt> <dt>

[<span data-ttu-id="01957-138">**Перечисление Инкрекогнитионстатус**</span><span class="sxs-lookup"><span data-stu-id="01957-138">**InkRecognitionStatus Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognitionstatus)
</dt> <dt>

[<span data-ttu-id="01957-139">**Метод распознавания**</span><span class="sxs-lookup"><span data-stu-id="01957-139">**Recognize Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize)
</dt> <dt>

[<span data-ttu-id="01957-140">**Интерфейс Иинкрекогнитионресулт**</span><span class="sxs-lookup"><span data-stu-id="01957-140">**IInkRecognitionResult Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult)
</dt> </dl>

 

