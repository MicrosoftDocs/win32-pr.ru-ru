---
description: Происходит, когда класс Инкрекогнизерконтекст создает результаты после вызова метода метода Баккграундрекогнизевисалтернатес.
ms.assetid: 5e86a4d5-c0a7-4283-81cc-ec3a26f74880
title: Событие Инкрекогнизерконтекст. Рекогнитионвисалтернатес (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4a7d35d8281305b0cb5f84114bb2f2fa0e718c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265458"
---
# <a name="inkrecognizercontextrecognitionwithalternates-event"></a><span data-ttu-id="59214-103">Инкрекогнизерконтекст. Рекогнитионвисалтернатес, событие</span><span class="sxs-lookup"><span data-stu-id="59214-103">InkRecognizerContext.RecognitionWithAlternates event</span></span>

<span data-ttu-id="59214-104">Происходит, когда [**класс инкрекогнизерконтекст**](inkrecognizercontext-class.md) создает результаты после вызова метода [**метода баккграундрекогнизевисалтернатес**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) .</span><span class="sxs-lookup"><span data-stu-id="59214-104">Occurs when the [**InkRecognizerContext Class**](inkrecognizercontext-class.md) has generated results after calling the [**BackgroundRecognizeWithAlternates Method**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="59214-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="59214-105">Syntax</span></span>


```C++
void RecognitionWithAlternates(
  [in] IInkRecognitionResult *RecognitionResult,
  [in] VARIANT               CustomData,
  [in] InkRecognitionStatus  RecognitionStatus
);
```



## <a name="parameters"></a><span data-ttu-id="59214-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="59214-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59214-107">*Рекогнитионресулт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="59214-107">*RecognitionResult* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59214-108">Результат распознавания события.</span><span class="sxs-lookup"><span data-stu-id="59214-108">The recognition result from the event.</span></span>

</dd> <dt>

<span data-ttu-id="59214-109">*CustomData* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="59214-109">*CustomData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59214-110">Пользовательские данные для результата распознавания.</span><span class="sxs-lookup"><span data-stu-id="59214-110">The custom data for the recognition result.</span></span>

<span data-ttu-id="59214-111">Дополнительные сведения о структуре вариантов см. в разделе [Использование библиотеки COM](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="59214-111">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> <dt>

<span data-ttu-id="59214-112">*Рекогнитионстатус* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="59214-112">*RecognitionStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59214-113">Состояние распознавания на самый последний результат распознавания.</span><span class="sxs-lookup"><span data-stu-id="59214-113">The recognition status as of the most recent recognition result.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59214-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="59214-114">Return value</span></span>

<span data-ttu-id="59214-115">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="59214-115">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="59214-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="59214-116">Remarks</span></span>

<span data-ttu-id="59214-117">Поведение прикладного программного интерфейса (API) непредсказуемо, если вы попытаетесь получить доступ к исходному объекту [**инкрекогнизерконтекст**](inkrecognizercontext-class.md) из обработчика событий распознавания.</span><span class="sxs-lookup"><span data-stu-id="59214-117">The behavior of the application programming interface (API) is unpredictable if you try to gain access to the original [**InkRecognizerContext**](inkrecognizercontext-class.md) object from the recognition event handler.</span></span> <span data-ttu-id="59214-118">Не пытайтесь это сделать.</span><span class="sxs-lookup"><span data-stu-id="59214-118">Do not attempt to do this.</span></span> <span data-ttu-id="59214-119">Вместо этого, если это необходимо, создайте флаг и задайте его в обработчике событий [**распознавания**](inkrecognizercontext-recognition.md) .</span><span class="sxs-lookup"><span data-stu-id="59214-119">Instead, if you need to do this, create a flag and set it in the [**Recognition**](inkrecognizercontext-recognition.md) event handler.</span></span> <span data-ttu-id="59214-120">Затем можно опросить этот флаг, чтобы определить, когда следует изменять свойства **инкрекогнизерконтекст** за пределами обработчика событий.</span><span class="sxs-lookup"><span data-stu-id="59214-120">Then you can poll that flag to determine when to change the **InkRecognizerContext** properties outside of the event handler.</span></span>

<span data-ttu-id="59214-121">Этот метод события определен в \_ интерфейсе иинкевентс.</span><span class="sxs-lookup"><span data-stu-id="59214-121">This event method is defined in the \_IInkEvents interface.</span></span> <span data-ttu-id="59214-122">\_Интерфейс иинкевентс реализует интерфейс [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) с идентификатором DISPID \_ иререкогнитионвисалтернатес.</span><span class="sxs-lookup"><span data-stu-id="59214-122">The \_IInkEvents interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IRERecognitionWithAlternates.</span></span>

## <a name="requirements"></a><span data-ttu-id="59214-123">Требования</span><span class="sxs-lookup"><span data-stu-id="59214-123">Requirements</span></span>



| <span data-ttu-id="59214-124">Требование</span><span class="sxs-lookup"><span data-stu-id="59214-124">Requirement</span></span> | <span data-ttu-id="59214-125">Значение</span><span class="sxs-lookup"><span data-stu-id="59214-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59214-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="59214-126">Minimum supported client</span></span><br/> | <span data-ttu-id="59214-127">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="59214-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="59214-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="59214-128">Minimum supported server</span></span><br/> | <span data-ttu-id="59214-129">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="59214-129">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="59214-130">Header</span><span class="sxs-lookup"><span data-stu-id="59214-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="59214-131"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="59214-131"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="59214-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="59214-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="59214-133"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="59214-133"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="59214-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="59214-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59214-135">**Класс Инкрекогнизерконтекст**</span><span class="sxs-lookup"><span data-stu-id="59214-135">**InkRecognizerContext Class**</span></span>](inkrecognizercontext-class.md)
</dt> <dt>

[<span data-ttu-id="59214-136">**Метод Баккграундрекогнизевисалтернатес**</span><span class="sxs-lookup"><span data-stu-id="59214-136">**BackgroundRecognizeWithAlternates Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates)
</dt> <dt>

[<span data-ttu-id="59214-137">**Метод распознавания**</span><span class="sxs-lookup"><span data-stu-id="59214-137">**Recognize Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize)
</dt> <dt>

[<span data-ttu-id="59214-138">**Интерфейс Иинкрекогнитионресулт**</span><span class="sxs-lookup"><span data-stu-id="59214-138">**IInkRecognitionResult Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult)
</dt> </dl>

 

