---
title: Рекомендации по использованию безнадежных массивов
description: Многие методы интерфейса службы автоматизации пользовательского интерфейса Майкрософт \ 32; API принимает аргументы, называемые безнадежными массивами, типа данных SAFEARRAY. В этом разделе описаны рекомендации по использованию безнадежных массивов в приложениях автоматизации пользовательского интерфейса.
ms.assetid: 07e87cfd-d565-41b5-a68d-b99dd191fa95
keywords:
- Модель автоматизации пользовательского интерфейса, надежные массивы
- Автоматизация пользовательского интерфейса, поставщики
- Модель автоматизации пользовательского интерфейса, клиенты
- Модель автоматизации пользовательского интерфейса, преобразование типов данных
- Клиенты, надежные массивы
- поставщики, модель автоматизации пользовательского интерфейса
- надежные массивы
- типы данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b12ade30398f8fbeb43336707f66a0709dfab83d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105700899"
---
# <a name="best-practices-for-using-safe-arrays"></a><span data-ttu-id="1adc1-112">Рекомендации по использованию безнадежных массивов</span><span class="sxs-lookup"><span data-stu-id="1adc1-112">Best Practices for Using Safe Arrays</span></span>

<span data-ttu-id="1adc1-113">Многие методы интерфейса API Microsoft UI Automation принимают аргументы, называемые безнадежными массивами, типа данных [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) .</span><span class="sxs-lookup"><span data-stu-id="1adc1-113">Many interface methods of the Microsoft UI Automation API take arguments called safe arrays, of the [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) data type.</span></span> <span data-ttu-id="1adc1-114">В этом разделе описаны рекомендации по использованию безнадежных массивов в приложениях автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="1adc1-114">This topic describes the best practices for using safe arrays in a UI Automation applications.</span></span>

## <a name="clients"></a><span data-ttu-id="1adc1-115">Клиенты</span><span class="sxs-lookup"><span data-stu-id="1adc1-115">Clients</span></span>

<span data-ttu-id="1adc1-116">Все надежные массивы, используемые с методами API клиента автоматизации пользовательского интерфейса, — это одномерные массивы, начинающиеся с нуля.</span><span class="sxs-lookup"><span data-stu-id="1adc1-116">All safe arrays that are used with the UI Automation client API methods are zero-based, one-dimensional arrays.</span></span> <span data-ttu-id="1adc1-117">Чтобы создать защищенный массив для клиентского метода автоматизации пользовательского интерфейса, используйте функцию [**сафеаррайкреатевектор**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearraycreatevector) , а для чтения из безопасного массива и записи в него используйте функции [**сафеаррайжетелемент**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearraygetelement) и [**сафеаррайпутелемент**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearrayputelement) .</span><span class="sxs-lookup"><span data-stu-id="1adc1-117">To create a safe array for a UI Automation client method, use the [**SafeArrayCreateVector**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearraycreatevector) function, and to read from and write to a safe array, use the [**SafeArrayGetElement**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearraygetelement) and [**SafeArrayPutElement**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearrayputelement) functions.</span></span> <span data-ttu-id="1adc1-118">По завершении использования безопасного массива всегда уничтожайте его с помощью функции [**сафеаррайдестрой**](/windows/desktop/api/oleauto/nf-oleauto-safearraydestroy) , независимо от того, был ли вы создали сейфовый массив или получили его из клиентского метода автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="1adc1-118">When you finish using a safe array, always destroy it by using the [**SafeArrayDestroy**](/windows/desktop/api/oleauto/nf-oleauto-safearraydestroy) function, whether you created the safe array or received it from a UI Automation client method.</span></span>

<span data-ttu-id="1adc1-119">Несколько методов автоматизации пользовательского интерфейса, включая методы получения свойств, такие как [**GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue), получают [**варианты**](/windows/win32/api/oaidl/ns-oaidl-variant), которые могут содержать структуры [**Point**](/previous-versions//dd162805(v=vs.85)) или [**уиарект**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiarect) .</span><span class="sxs-lookup"><span data-stu-id="1adc1-119">Several UI Automation methods, including property-retrieval methods such as [**GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue), retrieve [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant)s that can contain [**POINT**](/previous-versions//dd162805(v=vs.85)) or [**UiaRect**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiarect) structures.</span></span> <span data-ttu-id="1adc1-120">**Точка** упаковывается в **Variant** как надежный массив значений типа Double (VT \_ R8) с элементом **x** с индексом 0, а элемент **y** — с индексом 1.</span><span class="sxs-lookup"><span data-stu-id="1adc1-120">A **POINT** is packed into a **VARIANT** as a safe array of doubles (VT\_R8) with the **x** member at index 0, and the **y** member at index 1.</span></span> <span data-ttu-id="1adc1-121">Аналогичным образом **уиарект** упаковывается в **вариант** в виде безопасного массива значений типа Double с **левым**, **верхним**, **шириной** и **высотой** в индексах от 0 до 3 соответственно.</span><span class="sxs-lookup"><span data-stu-id="1adc1-121">Similarly, a **UiaRect** is packed into a **VARIANT** as a safe array of doubles with the **left**, **top**, **width**, and **height** members at indexes 0 through 3, respectively.</span></span> <span data-ttu-id="1adc1-122">Для массива структур **уиарект** надежный массив содержит последовательный массив из четырех значений Double для каждого **уиарект**.</span><span class="sxs-lookup"><span data-stu-id="1adc1-122">For an array of **UiaRect** structures, the safe array contains a sequential array of four doubles for each **UiaRect**.</span></span> <span data-ttu-id="1adc1-123">Элементы **левого**, **верхнего**, **ширины** и **высоты** первого **уиарект** занимают индекс от 0 до 3, элементы второго прямоугольника занимают индекс 4 – 7 и т. д.</span><span class="sxs-lookup"><span data-stu-id="1adc1-123">The **left**, **top**, **width**, and **height** members of the first **UiaRect** occupy index 0 through 3, the members of the second rectangle occupy index 4 through 7, and so on.</span></span>

<span data-ttu-id="1adc1-124">Интерфейс [**иуиаутоматион**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) включает следующие методы для преобразования между [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) и различными типами данных.</span><span class="sxs-lookup"><span data-stu-id="1adc1-124">The [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) interface includes the following methods for converting between [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) and various other data types.</span></span>



| <span data-ttu-id="1adc1-125">Метод</span><span class="sxs-lookup"><span data-stu-id="1adc1-125">Method</span></span>                                                                                               | <span data-ttu-id="1adc1-126">Описание</span><span class="sxs-lookup"><span data-stu-id="1adc1-126">Description</span></span>                                                                                                     |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1adc1-127">**Иуиаутоматион:: Интнативеаррайтосафеаррай**</span><span class="sxs-lookup"><span data-stu-id="1adc1-127">**IUIAutomation::IntNativeArrayToSafeArray**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-intnativearraytosafearray)   | <span data-ttu-id="1adc1-128">Преобразует массив целых чисел в тип [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray).</span><span class="sxs-lookup"><span data-stu-id="1adc1-128">Converts an array of integers to a [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray).</span></span>                                          |
| [<span data-ttu-id="1adc1-129">**Иуиаутоматион:: Интсафеаррайтонативеаррай**</span><span class="sxs-lookup"><span data-stu-id="1adc1-129">**IUIAutomation::IntSafeArrayToNativeArray**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-intsafearraytonativearray)   | <span data-ttu-id="1adc1-130">Преобразует массив [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) целых чисел в массив.</span><span class="sxs-lookup"><span data-stu-id="1adc1-130">Converts a [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) of integers to an array.</span></span>                                          |
| [<span data-ttu-id="1adc1-131">**Иуиаутоматион:: Сафеаррайторектнативеаррай**</span><span class="sxs-lookup"><span data-stu-id="1adc1-131">**IUIAutomation::SafeArrayToRectNativeArray**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-safearraytorectnativearray) | <span data-ttu-id="1adc1-132">Преобразует массив [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) , содержащий координаты прямоугольника, в массив типа **Rect**.</span><span class="sxs-lookup"><span data-stu-id="1adc1-132">Converts a [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) that contains rectangle coordinates to an array of type **RECT**.</span></span> |



 

## <a name="providers"></a><span data-ttu-id="1adc1-133">Поставщики</span><span class="sxs-lookup"><span data-stu-id="1adc1-133">Providers</span></span>

<span data-ttu-id="1adc1-134">Поставщик должен реализовать ряд методов интерфейса, которые вызываются автоматизацией пользовательского интерфейса для получения сведений от поставщика.</span><span class="sxs-lookup"><span data-stu-id="1adc1-134">A provider must implement a number of interface methods that UI Automation calls to retrieve information from the provider.</span></span> <span data-ttu-id="1adc1-135">Множество раз эта информация состоит из массива значений.</span><span class="sxs-lookup"><span data-stu-id="1adc1-135">Many times, this information consists of an array of values.</span></span> <span data-ttu-id="1adc1-136">Чтобы вернуть массив в модель автоматизации пользовательского интерфейса, поставщик должен упаковать массив в структуру [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) .</span><span class="sxs-lookup"><span data-stu-id="1adc1-136">To return an array to UI Automation, the provider must pack the array into a [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) structure.</span></span> <span data-ttu-id="1adc1-137">Элементы массива должны иметь ожидаемый тип данных и должны находиться в ожидаемом порядке.</span><span class="sxs-lookup"><span data-stu-id="1adc1-137">The array elements must be of the expected data type, and must appear in the expected order.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1adc1-138">См. также</span><span class="sxs-lookup"><span data-stu-id="1adc1-138">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="1adc1-139">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="1adc1-139">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="1adc1-140">Общие сведения о свойствах автоматизированного пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="1adc1-140">UI Automation Properties Overview</span></span>](uiauto-propertiesoverview.md)
</dt> <dt>

[<span data-ttu-id="1adc1-141">Основы модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="1adc1-141">UI Automation Fundamentals</span></span>](entry-uiautocore-overview.md)
</dt> </dl>

 

 