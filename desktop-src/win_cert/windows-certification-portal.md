---
title: Сертификация настольного приложения
description: Выполните следующие действия, чтобы получить сертификат для настольного приложения, сертифицированного для Windows 7, Windows 8, Windows 8.1 и Windows 10. Если вы хотите преобразовать приложение для настольного компьютера, чтобы оно было совместимо с универсальная платформа Windows и магазином Windows, вы будете использовать Windows Desktop Bridge. в этом случае следует следовать указаниям по настройке моста для настольных систем. Если вы разрабатываете и сертифицироватье приложение UWP с самого начала, см. статью рекомендации по сертификации приложений Windows в UWP для получения сведений о сертификации.
ms.assetid: d77d9f1c-1738-4f44-a351-1985ffc21707
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a52eb0f1040c438cb61f4729923c8928116447e8
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/09/2020
ms.locfileid: "103797070"
---
# <a name="certify-your-desktop-application"></a><span data-ttu-id="4475a-103">Сертификация настольного приложения</span><span class="sxs-lookup"><span data-stu-id="4475a-103">Certify your desktop application</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4475a-104">Сертификация классических приложений Win32 является [устаревшей](https://techcommunity.microsoft.com/t5/windows-hardware-certification/win32-logo-certification-deprecation/ba-p/364920).</span><span class="sxs-lookup"><span data-stu-id="4475a-104">Certification for Win32 desktop apps is [deprecated](https://techcommunity.microsoft.com/t5/windows-hardware-certification/win32-logo-certification-deprecation/ba-p/364920).</span></span> <span data-ttu-id="4475a-105">Вместо этого [отправьте сюда файлы](https://www.microsoft.com/wdsi/filesubmission/).</span><span class="sxs-lookup"><span data-stu-id="4475a-105">Instead, [submit files here](https://www.microsoft.com/wdsi/filesubmission/).</span></span>

<span data-ttu-id="4475a-106">Выполните следующие действия, чтобы получить сертификат для настольного приложения для Windows 7, Windows 8, Windows 8.1 и Windows 10.</span><span class="sxs-lookup"><span data-stu-id="4475a-106">Follow these steps to get your desktop app certified for Windows 7, Windows 8, Windows 8.1, and Windows 10.</span></span>

<span data-ttu-id="4475a-107">Если вы хотите преобразовать приложение для настольного компьютера, чтобы оно было совместимо с универсальная платформа Windows и магазином Windows, вы будете использовать [классическое мост Windows](https://developer.microsoft.com/windows/bridges/desktop). в этом случае необходимо следовать указаниям по настройке [моста для настольных систем](/windows/uwp/porting/desktop-to-uwp-root) .</span><span class="sxs-lookup"><span data-stu-id="4475a-107">If you wish to convert your desktop app to be compatible with the Universal Windows Platform and Windows Store, you will use the [Windows Desktop Bridge](https://developer.microsoft.com/windows/bridges/desktop), in which case you should follow the [Desktop Bridge](/windows/uwp/porting/desktop-to-uwp-root) guidance for certification steps.</span></span>

<span data-ttu-id="4475a-108">Если вы разрабатываете и сертифицироватье приложение UWP с самого начала, см. статью [рекомендации по сертификации приложений Windows в UWP](/windows/uwp/debug-test-perf/windows-app-certification-kit) для получения сведений о сертификации.</span><span class="sxs-lookup"><span data-stu-id="4475a-108">If you are developing and certifying a UWP app from the start, see [Guidance for Windows App Certification in UWP](/windows/uwp/debug-test-perf/windows-app-certification-kit) for info on certification.</span></span>

## <a name="step-1-prepare-for-certification"></a><span data-ttu-id="4475a-109">Шаг 1. Подготовка к сертификации</span><span class="sxs-lookup"><span data-stu-id="4475a-109">Step 1: Prepare for certification</span></span>



| <span data-ttu-id="4475a-110">Раздел</span><span class="sxs-lookup"><span data-stu-id="4475a-110">Topic</span></span>                                                                                       | <span data-ttu-id="4475a-111">Описание</span><span class="sxs-lookup"><span data-stu-id="4475a-111">Description</span></span>                                                                                    |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4475a-112">Каковы преимущества?</span><span class="sxs-lookup"><span data-stu-id="4475a-112">What are the benefits?</span></span>](what-are-the-benefits-.md)<br/>                             | <span data-ttu-id="4475a-113">Сертификация классического приложения предоставляет несколько преимуществ для вас и ваших клиентов.</span><span class="sxs-lookup"><span data-stu-id="4475a-113">Certifying your desktop app provides several benefits for you and your customers.</span></span>              |
| [<span data-ttu-id="4475a-114">Чтение требований</span><span class="sxs-lookup"><span data-stu-id="4475a-114">Read the requirements</span></span>](certification-requirements-for-windows-desktop-apps.md)<br/> | <span data-ttu-id="4475a-115">Ознакомьтесь с техническими требованиями и квалификацией соответствия требованиям, которые должны соответствовать классу Desktop.</span><span class="sxs-lookup"><span data-stu-id="4475a-115">Review the technical requirements and eligibility qualifications that a desktop app must meet.</span></span> |



 

## <a name="step-2-test-your-app-with-the-windows-app-certification-kit"></a><span data-ttu-id="4475a-116">Шаг 2. Тестирование приложения с помощью набора сертификации приложений для Windows</span><span class="sxs-lookup"><span data-stu-id="4475a-116">Step 2: Test your app with the Windows App Certification Kit</span></span>



| <span data-ttu-id="4475a-117">Раздел</span><span class="sxs-lookup"><span data-stu-id="4475a-117">Topic</span></span>                                                          | <span data-ttu-id="4475a-118">Описание</span><span class="sxs-lookup"><span data-stu-id="4475a-118">Description</span></span>                                                                                                                                                                           |
|----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4475a-119">Получение комплекта</span><span class="sxs-lookup"><span data-stu-id="4475a-119">Get the Kit</span></span>](https://developer.microsoft.com/windows/downloads/app-certification-kit/) | <span data-ttu-id="4475a-120">Чтобы сертифицировать приложение, необходимо установить и запустить комплект сертификации приложений для Windows (входит в состав Windows SDK).</span><span class="sxs-lookup"><span data-stu-id="4475a-120">To certify your app, you have to install and run the Windows App Certification Kit (included in the Windows SDK).</span></span>                                                                     |
| [<span data-ttu-id="4475a-121">Использование набора</span><span class="sxs-lookup"><span data-stu-id="4475a-121">Using the Kit</span></span>](using-the-windows-app-certification-kit.md)   | <span data-ttu-id="4475a-122">Перед отправкой приложения необходимо проверить его на готовность.</span><span class="sxs-lookup"><span data-stu-id="4475a-122">Before you can submit your app, you must test it for readiness.</span></span> <span data-ttu-id="4475a-123">Вы также можете скачать копию [технического документа о сертификации приложений](https://www.microsoft.com/download/details.aspx?id=27414).</span><span class="sxs-lookup"><span data-stu-id="4475a-123">You can also download a copy of the [app certification white paper](https://www.microsoft.com/download/details.aspx?id=27414).</span></span> |
| [<span data-ttu-id="4475a-124">Проверка сведений о тесте</span><span class="sxs-lookup"><span data-stu-id="4475a-124">Review test details</span></span>](windows-app-certification-kit-tests.md) | <span data-ttu-id="4475a-125">Получите список тестов, которые необходимо передать приложению для обеспечения совместимости с последней версией операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="4475a-125">Get the list of the tests your app needs to pass to qualify for compatibility with the latest Windows operating system.</span></span>                                                               |



 

<span data-ttu-id="4475a-126">Примечание. драйверы фильтра также должны пройти [Комплект сертификации оборудования](https://download.microsoft.com/download/1/8/B/18BC088A-537D-4386-9334-687747A602E6/hlk/hlksetup.exe).</span><span class="sxs-lookup"><span data-stu-id="4475a-126">Note: Filter drivers must also pass the [Hardware Certification Kit](https://download.microsoft.com/download/1/8/B/18BC088A-537D-4386-9334-687747A602E6/hlk/hlksetup.exe).</span></span> <span data-ttu-id="4475a-127">(См. статью [требования к сертификации для классических приложений Windows, раздел 6,2](certification-requirements-for-windows-desktop-apps.md).)</span><span class="sxs-lookup"><span data-stu-id="4475a-127">(See [Certification requirements for Windows desktop apps, section 6.2](certification-requirements-for-windows-desktop-apps.md).)</span></span>

## <a name="step-3-use-the-windows-certification-dashboard"></a><span data-ttu-id="4475a-128">Шаг 3. Использование панели мониторинга сертификации Windows</span><span class="sxs-lookup"><span data-stu-id="4475a-128">Step 3: Use the Windows Certification Dashboard</span></span>

<span data-ttu-id="4475a-129">Чтобы отправить приложение для сертификации, необходимо войти в систему или зарегистрировать учетную запись компании на [панели мониторинга сертификации Windows](/previous-versions/hh833792(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="4475a-129">To submit your app for certification, you'll need to log in or register a company account on the [Windows Certification Dashboard](/previous-versions/hh833792(v=msdn.10)).</span></span> <span data-ttu-id="4475a-130">После этого вы сможете получить сертификат только для своих приложений, но вы также получите доступ к средствам для просмотра и управления приложением на всех этапах процесса.</span><span class="sxs-lookup"><span data-stu-id="4475a-130">Once you do, not only will you be able to get your app certified, but you'll also gain access to tools to review and manage your app at all stages of the process.</span></span>



| <span data-ttu-id="4475a-131">Раздел</span><span class="sxs-lookup"><span data-stu-id="4475a-131">Topic</span></span>                                                                                                                   | <span data-ttu-id="4475a-132">Описание</span><span class="sxs-lookup"><span data-stu-id="4475a-132">Description</span></span>                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4475a-133">Настройка учетной записи</span><span class="sxs-lookup"><span data-stu-id="4475a-133">Set up your account</span></span>](/windows-hardware/drivers/dashboard/)                 | <span data-ttu-id="4475a-134">Если ваша компания еще не зарегистрирована, ее необходимо зарегистрировать на панели мониторинга сертификации Windows.</span><span class="sxs-lookup"><span data-stu-id="4475a-134">If your company isn't already registered, you must register it through the Windows Certification Dashboard.</span></span>                                        |
| [<span data-ttu-id="4475a-135">Получение сертификата для подписи кода</span><span class="sxs-lookup"><span data-stu-id="4475a-135">Get a code signing certificate</span></span>](/windows-hardware/drivers/dashboard/)      | <span data-ttu-id="4475a-136">Прежде чем можно будет установить учетную запись панели сертификации Windows, необходимо получить сертификат подписи кода для защиты цифровой информации.</span><span class="sxs-lookup"><span data-stu-id="4475a-136">Before you can establish a Windows Certification Dashboard account, you need to get a code signing certificate to secure your digital information.</span></span> |
| [<span data-ttu-id="4475a-137">Локальное тестирование и отправка результатов</span><span class="sxs-lookup"><span data-stu-id="4475a-137">Test locally and upload the results</span></span>](/windows-hardware/drivers/dashboard/) | <span data-ttu-id="4475a-138">После выполнения тестов набора сертификации приложений для Windows отправьте результаты на панель мониторинга сертификации Windows.</span><span class="sxs-lookup"><span data-stu-id="4475a-138">After your run the Windows App Certification Kit tests, upload the results to the Windows Certification Dashboard.</span></span>                                 |
| [<span data-ttu-id="4475a-139">Управление отправкой</span><span class="sxs-lookup"><span data-stu-id="4475a-139">Manage your submission</span></span>](/windows-hardware/drivers/dashboard/)              | <span data-ttu-id="4475a-140">После отправки приложения для сертификации можно просмотреть его отправку на панели мониторинга сертификации Windows.</span><span class="sxs-lookup"><span data-stu-id="4475a-140">After you submit your app for certification, you can review your submission through the Windows Certification Dashboard.</span></span>                           |



 

## <a name="step-4-promote-your-desktop-app"></a><span data-ttu-id="4475a-141">Шаг 4. продвижение классического приложения</span><span class="sxs-lookup"><span data-stu-id="4475a-141">Step 4: Promote your desktop app</span></span>



| <span data-ttu-id="4475a-142">Раздел</span><span class="sxs-lookup"><span data-stu-id="4475a-142">Topic</span></span>                                                                      | <span data-ttu-id="4475a-143">Описание</span><span class="sxs-lookup"><span data-stu-id="4475a-143">Description</span></span>                                                                                                               |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4475a-144">Проверка совместимости приложений</span><span class="sxs-lookup"><span data-stu-id="4475a-144">Check app compatibility</span></span>](/windows/compatibility/windows-8-1-introduction) | <span data-ttu-id="4475a-145">Если вы создаете приложение для Windows 8.1, изучите вопросы совместимости.</span><span class="sxs-lookup"><span data-stu-id="4475a-145">If you are building an app for Windows 8.1, investigate compatibility concerns.</span></span>                                           |
| [<span data-ttu-id="4475a-146">Использование логотипа с приложением</span><span class="sxs-lookup"><span data-stu-id="4475a-146">Use the logo with your app</span></span>](https://techcommunity.microsoft.com/t5/windows-hardware-certification/bg-p/WindowsHardwareCertification)                  | <span data-ttu-id="4475a-147">Отображение логотипа на упаковке и в рекламных материалах, а также других рекламных материалов в соответствии с рекомендациями.</span><span class="sxs-lookup"><span data-stu-id="4475a-147">Display the logo on packaging and in ads and other promotional materials according to the guidelines.</span></span> <span data-ttu-id="4475a-148">Только для Windows 7.</span><span class="sxs-lookup"><span data-stu-id="4475a-148">For Windows 7 only.</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="4475a-149">См. также:</span><span class="sxs-lookup"><span data-stu-id="4475a-149">See also:</span></span>

<span data-ttu-id="4475a-150">[Форум по совместимости приложений](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowscompatibility). Получите поддержку от сообщества о совместимости и сертификации логотипов.</span><span class="sxs-lookup"><span data-stu-id="4475a-150">[App compatibility forum](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowscompatibility): Find support from the community about compatibility and logo certification.</span></span>

<span data-ttu-id="4475a-151">[Блог Windows SDK](https://blogs.msdn.com/b/winsdk/archive/tags/certification/). Найдите советы и новости, связанные с сертификацией приложений.</span><span class="sxs-lookup"><span data-stu-id="4475a-151">[Windows SDK blog](https://blogs.msdn.com/b/winsdk/archive/tags/certification/): Find tips and news related to app certification.</span></span>

<span data-ttu-id="4475a-152">[Форум по Windows Server]( https://social.technet.microsoft.com/Forums/windowsserver/home?forum=WSAppCompat). для получения ответов посетите форум по сертификации.</span><span class="sxs-lookup"><span data-stu-id="4475a-152">[Windows Server forum]( https://social.technet.microsoft.com/Forums/windowsserver/home?forum=WSAppCompat): Visit the Certification forum to get answers.</span></span>

<span data-ttu-id="4475a-153">[Совместимость Cookbook](/windows/desktop/w8cookbook/windows-8-and-windows-server-8-compatibility-cookbook-portal): получение сведений о новых возможностях и изменениях в последней версии Windows.</span><span class="sxs-lookup"><span data-stu-id="4475a-153">[Compatibility cookbook](/windows/desktop/w8cookbook/windows-8-and-windows-server-8-compatibility-cookbook-portal): Get info about what's new or changed in the latest version of Windows.</span></span>

 

