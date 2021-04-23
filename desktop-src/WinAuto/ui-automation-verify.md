---
title: Проверка модели автоматизации пользовательского интерфейса (проверка UIA)
description: Проверка модели автоматизации пользовательского интерфейса (UIA Verify) — это платформа тестирования для ручного и автоматизированного тестирования реализации автоматизации пользовательского интерфейса (Майкрософт) для элемента управления или приложения.
ms.assetid: C66AF411-2746-4695-A893-1552B3ED1066
keywords:
- Средство UI Automation Verify
- Проверка UIA
- Реализация модели автоматизации пользовательского интерфейса, тестирование
- тестирование автоматизации пользовательского интерфейса
- Средства тестирования UIA
- Средства тестирования модели автоматизации пользовательского интерфейса
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b794e5d191c07a9c0db602ebac0f908bbdf960bf
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/20/2020
ms.locfileid: "104412597"
---
# <a name="accessibility-tools---ui-automation-verify-uia-verify"></a><span data-ttu-id="a0bcf-109">Средства специальных возможностей — проверка модели автоматизации пользовательского интерфейса (проверка UIA)</span><span class="sxs-lookup"><span data-stu-id="a0bcf-109">Accessibility tools - UI Automation Verify (UIA Verify)</span></span>

<span data-ttu-id="a0bcf-110">**Проверка модели автоматизации пользовательского интерфейса (UIA Verify)** — это платформа тестирования для ручного и автоматизированного тестирования реализации автоматизации пользовательского интерфейса (Майкрософт) для элемента управления или приложения.</span><span class="sxs-lookup"><span data-stu-id="a0bcf-110">**UI Automation Verify (UIA Verify)** is a testing framework for manual and automated testing of a control's or application's implementation of Microsoft UI Automation.</span></span> <span data-ttu-id="a0bcf-111">Большая часть функциональных возможностей платформы тестирования поступает из библиотеки DLL, именуемой WUIATestLibrary.dll.</span><span class="sxs-lookup"><span data-stu-id="a0bcf-111">Most of the testing framework's functionality comes from a DLL called WUIATestLibrary.dll.</span></span> <span data-ttu-id="a0bcf-112">Эта библиотека DLL содержит код для тестирования определенной функциональности автоматизации пользовательского интерфейса, а также поддерживает ведение журнала результатов теста.</span><span class="sxs-lookup"><span data-stu-id="a0bcf-112">This DLL contains the code for testing specific UI Automation functionality, and it also supports logging of the test results.</span></span> <span data-ttu-id="a0bcf-113">Вы можете интегрировать приложение в тестовый код и выполнять регулярные, автоматизированное тестирование или проведение проверок в сценариях автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="a0bcf-113">You can integrate your application into the test code and conduct regular, automated testing or spot checks of your UI Automation scenarios.</span></span>

<span data-ttu-id="a0bcf-114">Программа **UIA-проверки** устанавливается вместе с пакетом средств разработки программного обеспечения (SDK) для Windows.</span><span class="sxs-lookup"><span data-stu-id="a0bcf-114">**UIA Verify** is installed with the Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="a0bcf-115">Он находится в \\ папке bin \\ < *версии* > \\ < *Platform* > \\ уиаверифи пути установки пакета SDK (VisualUIAVerifyNative.exe).</span><span class="sxs-lookup"><span data-stu-id="a0bcf-115">It is located in the \\bin\\<*version*>\\<*platform*>\\UIAVerify folder of the SDK installation path (VisualUIAVerifyNative.exe).</span></span>

<span data-ttu-id="a0bcf-116">**Проверка UIA** состоит из API-интерфейса, который называется библиотекой тестирования модели автоматизации пользовательского интерфейса, и пользовательского интерфейса с именем "Проверка визуальной **автоматизации пользовательского интерфейса**".</span><span class="sxs-lookup"><span data-stu-id="a0bcf-116">**UIA Verify** consists of an API called the UI Automation Test Library, and a GUI interface called Visual **UI Automation Verify**.</span></span> <span data-ttu-id="a0bcf-117">Они описаны в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="a0bcf-117">These are described in the following topics.</span></span>

> [!NOTE]
> <span data-ttu-id="a0bcf-118">**Проверка пользовательского интерфейса** — это устаревший инструмент.</span><span class="sxs-lookup"><span data-stu-id="a0bcf-118">**UI Automation Verify** is a legacy tool.</span></span> <span data-ttu-id="a0bcf-119">Вместо этого рекомендуется использовать [аналитические сведения о специальных возможностях](https://accessibilityinsights.io/) .</span><span class="sxs-lookup"><span data-stu-id="a0bcf-119">We recommend using [Accessibility Insights](https://accessibilityinsights.io/) instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0bcf-120">Требования</span><span class="sxs-lookup"><span data-stu-id="a0bcf-120">Requirements</span></span>

<span data-ttu-id="a0bcf-121">В системе должна присутствовать модель автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="a0bcf-121">UI Automation must be present on the system.</span></span> <span data-ttu-id="a0bcf-122">Дополнительные сведения см. в разделе "требования" [модели автоматизации пользовательского интерфейса](entry-uiauto-win32.md).</span><span class="sxs-lookup"><span data-stu-id="a0bcf-122">For more information, see the "Requirements" section of [UI Automation](entry-uiauto-win32.md).</span></span>

<span data-ttu-id="a0bcf-123">Программа **UIA-проверки** устанавливается как часть общего набора средств в Windows SDK, она не распространяется отдельно.</span><span class="sxs-lookup"><span data-stu-id="a0bcf-123">**UIA Verify** is installed as part of the overall set of tools in the Windows SDK, it is not distributed as a separate download.</span></span> <span data-ttu-id="a0bcf-124">Windows SDK включает все средства, связанные со специальными возможностями, описанные в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="a0bcf-124">The Windows SDK includes all of the accessibility-related tools documented in this section.</span></span> [<span data-ttu-id="a0bcf-125">Получите Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="a0bcf-125">Get the Windows SDK.</span></span>](https://developer.microsoft.com/) <span data-ttu-id="a0bcf-126">(Кроме того, если требуется предыдущая версия, можно загрузить архив SDK, связанный с этой страницей.)</span><span class="sxs-lookup"><span data-stu-id="a0bcf-126">(There's also an SDK download archive linked from that page, if you need a previous version.)</span></span>

<span data-ttu-id="a0bcf-127">Чтобы выполнить команду **UIA Verify** в качестве визуального средства, найдите VisualUIAVerifyNative.exe \\ в \\ < папке bin *Platform* > \\ уиаверифи и запустите ее (обычно запускать от имени администратора не требуется).</span><span class="sxs-lookup"><span data-stu-id="a0bcf-127">To run **UIA Verify** as a visual tool, find VisualUIAVerifyNative.exe in the \\bin\\<*platform*>\\UIAVerify folder and run it (you don't typically have to run as administrator).</span></span> <span data-ttu-id="a0bcf-128">Дополнительные сведения см. в разделе [Проверка визуальной автоматизации пользовательского интерфейса](visual-ui-automation-verify.md).</span><span class="sxs-lookup"><span data-stu-id="a0bcf-128">For more information, see [Visual UI Automation Verify](visual-ui-automation-verify.md).</span></span> <span data-ttu-id="a0bcf-129">Сведения об использовании библиотек см. в разделе [Библиотека тестов автоматизации пользовательского интерфейса](ui-automation-test-library.md).</span><span class="sxs-lookup"><span data-stu-id="a0bcf-129">To use the libraries, see [UI Automation Test Library](ui-automation-test-library.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a0bcf-130">См. также</span><span class="sxs-lookup"><span data-stu-id="a0bcf-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0bcf-131">Средство Accessible Event Watcher</span><span class="sxs-lookup"><span data-stu-id="a0bcf-131">Accessible Event Watcher</span></span>](accessible-event-watcher.md)
</dt> <dt>

[<span data-ttu-id="a0bcf-132">Проверить</span><span class="sxs-lookup"><span data-stu-id="a0bcf-132">Inspect</span></span>](inspect-objects.md)
</dt> <dt>

[<span data-ttu-id="a0bcf-133">Средства тестирования</span><span class="sxs-lookup"><span data-stu-id="a0bcf-133">Testing Tools</span></span>](testing-tools.md)
</dt> <dt>

[<span data-ttu-id="a0bcf-134">Средство UI Accessibility Checker</span><span class="sxs-lookup"><span data-stu-id="a0bcf-134">UI Accessibility Checker</span></span>](ui-accessibility-checker.md)
</dt> </dl>

 

 




