---
title: Вспомогательные темы высокая контрастность
description: В этом разделе сравнивается поддержка тем с высокой контрастностью в Windows 8 и более ранних версий Windows, а также объясняется, как поддерживать темы с высокой контрастностью в приложениях Windows 8.
ms.assetid: 6E4F1198-E69C-4C60-B3B0-2702AECAA203
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2068d64b585f302f578296c9e156895c23b9bce9
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "103891113"
---
# <a name="supporting-high-contrast-themes"></a><span data-ttu-id="52d23-103">Вспомогательные темы высокая контрастность</span><span class="sxs-lookup"><span data-stu-id="52d23-103">Supporting High Contrast Themes</span></span>

<span data-ttu-id="52d23-104">В этом разделе сравнивается поддержка тем с высокой контрастностью в Windows 8 и более ранних версий Windows, а также объясняется, как поддерживать темы с высокой контрастностью в приложениях Windows 8.</span><span class="sxs-lookup"><span data-stu-id="52d23-104">This topic compares the support for high contrast themes in Windows 8 to that of previous versions of Windows, and explains how to support high contrast themes in a Windows 8 application.</span></span>

<span data-ttu-id="52d23-105">Он включает в себя следующие разделы.</span><span class="sxs-lookup"><span data-stu-id="52d23-105">It includes the following sections.</span></span>

-   [<span data-ttu-id="52d23-106">Общие сведения о поддержке для высокая контрастностьных тем</span><span class="sxs-lookup"><span data-stu-id="52d23-106">Overview of Support for High Contrast Themes</span></span>](#overview-of-support-for-high-contrast-themes)
-   [<span data-ttu-id="52d23-107">Поддержка тем высокая контрастность в Windows 8 и более поздних версиях</span><span class="sxs-lookup"><span data-stu-id="52d23-107">Supporting High Contrast Themes in Windows 8 and later</span></span>](#supporting-high-contrast-themes-in-windows-8-and-later)
-   [<span data-ttu-id="52d23-108">Добавление раздела "совместимость" в манифест приложения</span><span class="sxs-lookup"><span data-stu-id="52d23-108">Adding a Compatibility Section to Your Application Manifest</span></span>](#adding-a-compatibility-section-to-your-application-manifest)
-   [<span data-ttu-id="52d23-109">Обнаружение высокая контрастность в предыдущих версиях Windows</span><span class="sxs-lookup"><span data-stu-id="52d23-109">Detecting High Contrast in Previous Versions of Windows</span></span>](#detecting-high-contrast-in-previous-versions-of-windows)
-   [<span data-ttu-id="52d23-110">См. также</span><span class="sxs-lookup"><span data-stu-id="52d23-110">Related topics</span></span>](#related-topics)

## <a name="overview-of-support-for-high-contrast-themes"></a><span data-ttu-id="52d23-111">Общие сведения о поддержке для высокая контрастностьных тем</span><span class="sxs-lookup"><span data-stu-id="52d23-111">Overview of Support for High Contrast Themes</span></span>

<span data-ttu-id="52d23-112">Windows 7 и более ранние версии поддерживают две модели, включая классическую модель Windows и текущие стили оформления.</span><span class="sxs-lookup"><span data-stu-id="52d23-112">Windows 7 and earlier support two theming models, including the legacy Windows classic model, and the current visual styles.</span></span> <span data-ttu-id="52d23-113">Классическая модель Windows была сохранена в Windows 7 главным образом для поддержки различных тем высокой контрастности.</span><span class="sxs-lookup"><span data-stu-id="52d23-113">The Windows classic model has been retained through Windows 7 mainly to support the various high contrast themes.</span></span> <span data-ttu-id="52d23-114">Однако классическая модель Windows имеет ряд недостатков:</span><span class="sxs-lookup"><span data-stu-id="52d23-114">However, the Windows classic model has a number of drawbacks:</span></span>

-   <span data-ttu-id="52d23-115">Нет поддержки тем, которые используют стили оформления, например Windows Aero.</span><span class="sxs-lookup"><span data-stu-id="52d23-115">No support for themes that use visual styles, such as Windows Aero.</span></span> <span data-ttu-id="52d23-116">Пользователи с темами с высокой контрастностью должны использовать классический пользовательский интерфейс Windows.</span><span class="sxs-lookup"><span data-stu-id="52d23-116">Users of high contrast themes must use the Windows classic UI.</span></span>
-   <span data-ttu-id="52d23-117">Не поддерживаются функции пользовательского интерфейса, которые используют диспетчер окон рабочего стола (DWM) для выполнения, такие как предварительный просмотр эскизов и полноэкранная экранная лупа, появившаяся в Windows 7.</span><span class="sxs-lookup"><span data-stu-id="52d23-117">No support for UI features that rely on Desktop Window Manager (DWM) to run, such as thumbnail previews and the full screen magnifier that was introduced in Windows 7.</span></span>
-   <span data-ttu-id="52d23-118">Разработчики должны поддерживать два отдельных пути кода для поддержки двух разных моделей.</span><span class="sxs-lookup"><span data-stu-id="52d23-118">Developers must maintain two separate code paths to support the two different theming models.</span></span>

<span data-ttu-id="52d23-119">В ОС Windows 8 и более поздних версиях следующие изменения в модели позволяют устранить предыдущие недостатки:</span><span class="sxs-lookup"><span data-stu-id="52d23-119">In Windows 8 and later, the following changes to the theming model address the previous drawbacks:</span></span>

-   <span data-ttu-id="52d23-120">Модель классической модели Windows больше не поддерживается, что позволяет разработчикам поддерживать только один путь кода для приложений, предназначенных только для Windows 8.</span><span class="sxs-lookup"><span data-stu-id="52d23-120">The Windows classic theming model is no longer supported, enabling developers to maintain just one code path for applications that target only Windows 8.</span></span>
-   <span data-ttu-id="52d23-121">Поскольку стили оформления и DWM включены в Windows 8, пользователи с высокой контрастностью имеют доступ к таким функциям, как предварительный просмотр эскизов и полноэкранная экранная лупа.</span><span class="sxs-lookup"><span data-stu-id="52d23-121">Because visual styles and DWM are on in Windows 8, high contrast users have access to features such as thumbnail previews and the full-screen magnifier.</span></span>
-   <span data-ttu-id="52d23-122">Визуальные стили поддерживают настройку цветов различных элементов пользовательского интерфейса, позволяя пользователям с высокой контрастностью настраивать пользовательский интерфейс в соответствии с индивидуальными потребностями и предпочтениями.</span><span class="sxs-lookup"><span data-stu-id="52d23-122">Visual styles support setting the colors of various UI elements, enabling high contrast users to customize the UI to accommodate individual needs and preferences.</span></span>
-   <span data-ttu-id="52d23-123">В Windows 8 реализована поддержка совместимости для существующих приложений, предназначенных для использования высококонтрастных тем, основанных на классической модели Windows.</span><span class="sxs-lookup"><span data-stu-id="52d23-123">Windows 8 includes compatibility support for existing applications that are designed to use high contrast themes based on the Windows classic theming model.</span></span>

## <a name="supporting-high-contrast-themes-in-windows-8-and-later"></a><span data-ttu-id="52d23-124">Поддержка тем высокая контрастность в Windows 8 и более поздних версиях</span><span class="sxs-lookup"><span data-stu-id="52d23-124">Supporting High Contrast Themes in Windows 8 and later</span></span>

<span data-ttu-id="52d23-125">В Windows 8, поскольку стили оформления включены в режиме высокой контрастности, поддержка тем с высокой контрастностью очень проста, если вы хотите следовать приведенным ниже рекомендациям.</span><span class="sxs-lookup"><span data-stu-id="52d23-125">In Windows 8, because visual styles are on in high contrast mode, supporting high contrast themes is straightforward as long as you heed the following guidelines.</span></span>

-   <span data-ttu-id="52d23-126">Размеры шрифта и элементов управления.</span><span class="sxs-lookup"><span data-stu-id="52d23-126">Font and control sizes.</span></span> <span data-ttu-id="52d23-127">Чтобы обеспечить доступность пользовательского интерфейса для пользователей с ограниченными возможностями, установите размеры шрифтов в соответствии с текущими параметрами темы.</span><span class="sxs-lookup"><span data-stu-id="52d23-127">To ensure that your UI is accessible to users with disabilities, set font sizes according to the current theme settings.</span></span> <span data-ttu-id="52d23-128">Установите размер элементов управления как минимум по размеру по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="52d23-128">Set the size of controls to be at least the default size.</span></span>
-   <span data-ttu-id="52d23-129">"Цвета".</span><span class="sxs-lookup"><span data-stu-id="52d23-129">Colors.</span></span> <span data-ttu-id="52d23-130">Старайтесь не использовать жестко запрограммированные цвета.</span><span class="sxs-lookup"><span data-stu-id="52d23-130">Avoid using hard-coded colors.</span></span> <span data-ttu-id="52d23-131">Вместо этого используйте системные цвета, так как они основаны на текущей теме.</span><span class="sxs-lookup"><span data-stu-id="52d23-131">Instead, use the system colors because they are based on the current theme.</span></span> <span data-ttu-id="52d23-132">Использование пользовательских цветов может помешать и переопределить цвета в темах с высокой контрастностью.</span><span class="sxs-lookup"><span data-stu-id="52d23-132">Using custom colors can interfere with and override the colors in the high contrast themes.</span></span>
-   <span data-ttu-id="52d23-133">Манифест приложения.</span><span class="sxs-lookup"><span data-stu-id="52d23-133">Application manifest.</span></span> <span data-ttu-id="52d23-134">Для приложений, предназначенных для работы с новыми темами с высокой контрастностью, в манифесте должен быть определен раздел совместимости приложений, содержащий идентификаторы GUID совместимости с Windows 8.</span><span class="sxs-lookup"><span data-stu-id="52d23-134">Applications designed to work with the new high contrast themes should have an application compatibility section defined in their manifest that contains the Windows 8 compatibility GUIDs.</span></span> <span data-ttu-id="52d23-135">В противном случае Windows предполагает, что приложение предназначено для более старой версии Windows и отображает пользовательский интерфейс приложения, имитируя модель классической модели Windows.</span><span class="sxs-lookup"><span data-stu-id="52d23-135">Otherwise, Windows assumes that the application is designed for an older version of Windows and renders the application UI by simulating the Windows classic theming model.</span></span>

## <a name="adding-a-compatibility-section-to-your-application-manifest"></a><span data-ttu-id="52d23-136">Добавление раздела "совместимость" в манифест приложения</span><span class="sxs-lookup"><span data-stu-id="52d23-136">Adding a Compatibility Section to Your Application Manifest</span></span>

<span data-ttu-id="52d23-137">Манифест приложения — это XML-файл, описывающий требования к приложению.</span><span class="sxs-lookup"><span data-stu-id="52d23-137">An application manifest is an XML file that describes the requirements for an application.</span></span> <span data-ttu-id="52d23-138">Раздел Compatibility (совместимость) манифеста определяет версии Windows, поддерживаемые приложением.</span><span class="sxs-lookup"><span data-stu-id="52d23-138">The compatibility section of the manifest identifies the versions of Windows supported by the application.</span></span> <span data-ttu-id="52d23-139">Следующие идентификаторы GUID используются в разделе "совместимость" для обнаружения различных версий Windows.</span><span class="sxs-lookup"><span data-stu-id="52d23-139">The following GUIDs are used in the compatibility section to identify the various versions of Windows.</span></span>

| <span data-ttu-id="52d23-140">Версия</span><span class="sxs-lookup"><span data-stu-id="52d23-140">Version</span></span>       | <span data-ttu-id="52d23-141">Код GUID</span><span class="sxs-lookup"><span data-stu-id="52d23-141">GUID</span></span>                                   |
|---------------|----------------------------------------|
| <span data-ttu-id="52d23-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="52d23-142">Windows Vista</span></span> | <span data-ttu-id="52d23-143">{e2011457-1546-43c5-a5fe-008deee3d3f0}</span><span class="sxs-lookup"><span data-stu-id="52d23-143">{e2011457-1546-43c5-a5fe-008deee3d3f0}</span></span> |
| <span data-ttu-id="52d23-144">Windows 7</span><span class="sxs-lookup"><span data-stu-id="52d23-144">Windows 7</span></span>     | <span data-ttu-id="52d23-145">{35138b9a-5d96-4fbd-8e2d-a2440225f93a}</span><span class="sxs-lookup"><span data-stu-id="52d23-145">{35138b9a-5d96-4fbd-8e2d-a2440225f93a}</span></span> |
| <span data-ttu-id="52d23-146">Windows 8</span><span class="sxs-lookup"><span data-stu-id="52d23-146">Windows 8</span></span>     | <span data-ttu-id="52d23-147">{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}</span><span class="sxs-lookup"><span data-stu-id="52d23-147">{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}</span></span> |



 

<span data-ttu-id="52d23-148">В разделе "совместимость" можно указать несколько версий Windows, но каждая из них должна содержаться в своем собственном `<supportedOS/>` теге.</span><span class="sxs-lookup"><span data-stu-id="52d23-148">The compatibility section can specify multiple versions of Windows, but each must be contained within its own `<supportedOS/>` tag.</span></span> <span data-ttu-id="52d23-149">В следующем примере показан манифест приложения, задающий Windows 7 и Windows 8 в разделе Compatibility:</span><span class="sxs-lookup"><span data-stu-id="52d23-149">The following example shows an application manifest that specifies Windows 7 and Windows 8 in the compatibility section:</span></span>


```C++
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <compatibility xmlns="urn:schemas-microsoft-com:compatibility.v1">
        <application>
            <!--The ID below indicates application support for Windows 8 -->
            <supportedOS Id="{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}"/>

            <!--The ID below indicates application support for Windows 7 -->
            <supportedOS Id="{35138b9a-5d96-4fbd-8e2d-a2440225f93a}"/>
        </application>
    </compatibility>
</assembly>
```



<span data-ttu-id="52d23-150">Если приложение не имеет манифеста совместимости, предполагается, что оно является приложением Windows Vista и не использует элементы управления темами в клиентской области при активной теме с высокой контрастностью.</span><span class="sxs-lookup"><span data-stu-id="52d23-150">If an application does not have a compatibility manifest, it is assumed to be a Windows Vista application and does not use themed controls in the client area when a high contrast theme is active.</span></span> <span data-ttu-id="52d23-151">Кроме того, влияет поведение некоторых функций визуальных стилей.</span><span class="sxs-lookup"><span data-stu-id="52d23-151">Also, the behavior of some visual styles functions are affected.</span></span> <span data-ttu-id="52d23-152">Например, [**иссемеактиве**](/windows/desktop/api/Uxtheme/nf-uxtheme-isthemeactive), [**искомпоситионактиве**](/windows/desktop/api/Uxtheme/nf-uxtheme-iscompositionactive)и [**исаппсемед**](/windows/desktop/api/Uxtheme/nf-uxtheme-isappthemed) возвращают значение false, а [**опенсемедата**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) и [**опенсемедатаекс**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedataex) возвращают нулевой маркер.</span><span class="sxs-lookup"><span data-stu-id="52d23-152">For example, [**IsThemeActive**](/windows/desktop/api/Uxtheme/nf-uxtheme-isthemeactive), [**IsCompositionActive**](/windows/desktop/api/Uxtheme/nf-uxtheme-iscompositionactive), and [**IsAppThemed**](/windows/desktop/api/Uxtheme/nf-uxtheme-isappthemed) return FALSE, while [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) and [**OpenThemeDataEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedataex) return a NULL handle.</span></span> <span data-ttu-id="52d23-153">Это обеспечивает поддержку совместимости, поэтому приложения, созданные до Windows 8, могут по-прежнему отображать пользовательский интерфейс в том же виде, что и режим высокой контрастности в предыдущих версиях Windows, где стили оформления недоступны.</span><span class="sxs-lookup"><span data-stu-id="52d23-153">This is for compatibility support, so that applications built before Windows 8 can still render their UI in the same look as the high contrast mode of previous versions of Windows where visual styles are not available.</span></span>

<span data-ttu-id="52d23-154">В Windows 8 приложение по-прежнему получает преимущества композиции рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="52d23-154">On Windows 8, the application still receives the benefits of desktop composition.</span></span> <span data-ttu-id="52d23-155">Это означает, например, что приложения для удобства использования, такие как полноэкранная экранная лупа, не зависят от состояния манифеста отдельного приложения.</span><span class="sxs-lookup"><span data-stu-id="52d23-155">This means, for example, that usability applications such as the full screen magnifier don't depend on the status of an individual application's manifest.</span></span> <span data-ttu-id="52d23-156">Приложение для удобства использования продолжит работать в режиме высокой контрастности с приложением, которое не определяет себя как совместимое с Windows 8 в манифесте.</span><span class="sxs-lookup"><span data-stu-id="52d23-156">The usability application continues to work in high contrast mode with an application that does not identify itself as Windows 8 compatible in its manifest.</span></span>

<span data-ttu-id="52d23-157">На следующих изображениях показано простое диалоговое окно с высокой контрастностью в Windows 7.</span><span class="sxs-lookup"><span data-stu-id="52d23-157">The following images show a simple dialog box in high contrast on Windows 7.</span></span>

![диалоговое окно «контрастность целях»](images/win7-high-contrast.png)

<span data-ttu-id="52d23-159">На этом рисунке показано то же диалоговое окно с высокой контрастностью в Windows 8, но с совместимостью Windows 7, указанным в манифесте приложения:</span><span class="sxs-lookup"><span data-stu-id="52d23-159">This image shows the same dialog box in high contrast on Windows 8, but with Windows 7 compatibility specified in the application manifest:</span></span>

![диалоговое окно «высокая контрастность» W8](images/win7-compat.png)

<span data-ttu-id="52d23-161">На этом рисунке показано то же диалоговое окно с высокой контрастностью в Windows 8, в котором Windows 8 указана в манифесте приложения:</span><span class="sxs-lookup"><span data-stu-id="52d23-161">This image shows the same dialog box in high contrast on Windows 8, with Windows 8 specified in the application manifest:</span></span>

![диалоговое окно высокой контрастности W8 с манифестом](images/win8-manifest.png)

## <a name="detecting-high-contrast-in-previous-versions-of-windows"></a><span data-ttu-id="52d23-163">Обнаружение высокая контрастность в предыдущих версиях Windows</span><span class="sxs-lookup"><span data-stu-id="52d23-163">Detecting High Contrast in Previous Versions of Windows</span></span>

<span data-ttu-id="52d23-164">Приложения, работающие в предыдущих версиях Windows, не имеют доступа к новым темам с высокой контрастностью.</span><span class="sxs-lookup"><span data-stu-id="52d23-164">Applications running on previous versions of Windows do not have access to the new high contrast themes.</span></span> <span data-ttu-id="52d23-165">Если приложение должно работать в предыдущих версиях, следует включить поддержку визуализации пользовательского интерфейса в высоком Контравиндовсст в классической модели Windows.</span><span class="sxs-lookup"><span data-stu-id="52d23-165">If your application needs to run on previous versions of , you should include support for rendering your UI in high contraWindowsst in the Windows classic theming model.</span></span> <span data-ttu-id="52d23-166">Приложение может определить, активна ли тема с высокой контрастностью, вызвав функцию [**системпараметерсинфо**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) с флагом **SPI \_ жесигхконтраст** .</span><span class="sxs-lookup"><span data-stu-id="52d23-166">Your application can determine whether a high contrast theme is active by calling the [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) function with the **SPI\_GETHIGHCONTRAST** flag.</span></span>

## <a name="related-topics"></a><span data-ttu-id="52d23-167">См. также</span><span class="sxs-lookup"><span data-stu-id="52d23-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52d23-168">Включение стилей оформления</span><span class="sxs-lookup"><span data-stu-id="52d23-168">Enabling Visual Styles</span></span>](cookbook-overview.md)
</dt> <dt>

[<span data-ttu-id="52d23-169">Стили оформления</span><span class="sxs-lookup"><span data-stu-id="52d23-169">Visual Styles</span></span>](themes-overview.md)
</dt> </dl>

 

 