---
title: Включение стилей оформления
description: В этом разделе объясняется, как настроить приложение, чтобы обеспечить отображение стандартных элементов управления в предпочитаемом визуальном стиле пользователя.
ms.assetid: eb6c2469-25b9-43c4-a6ca-391a7b2859b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39339c0535767011a59730534486604389f62468
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "103987949"
---
# <a name="enabling-visual-styles"></a><span data-ttu-id="ded75-103">Включение стилей оформления</span><span class="sxs-lookup"><span data-stu-id="ded75-103">Enabling Visual Styles</span></span>

<span data-ttu-id="ded75-104">В этом разделе объясняется, как настроить приложение, чтобы обеспечить отображение стандартных элементов управления в предпочитаемом визуальном стиле пользователя.</span><span class="sxs-lookup"><span data-stu-id="ded75-104">This topic explains how to configure your application to ensure that common controls are displayed in the user's preferred visual style.</span></span>

<span data-ttu-id="ded75-105">Этот раздел включает следующие подразделы:</span><span class="sxs-lookup"><span data-stu-id="ded75-105">This topic includes the following sections.</span></span>

-   [<span data-ttu-id="ded75-106">Использование манифестов или директив для обеспечения возможности применения стилей оформления к приложениям</span><span class="sxs-lookup"><span data-stu-id="ded75-106">Using Manifests or Directives to Ensure That Visual Styles Can Be Applied to Applications</span></span>](#using-manifests-or-directives-to-ensure-that-visual-styles-can-be-applied-to-applications)
-   [<span data-ttu-id="ded75-107">Использование ComCtl32.dll версии 6 в приложении, использующем только стандартные расширения</span><span class="sxs-lookup"><span data-stu-id="ded75-107">Using ComCtl32.dll Version 6 in an Application That Uses Only Standard Extensions</span></span>](#using-comctl32dll-version-6-in-an-application-that-uses-only-standard-extensions)
-   [<span data-ttu-id="ded75-108">С помощью ComCtl32 версии 6 на панели управления или библиотеки DLL, которая запускается с RunDll32.exe</span><span class="sxs-lookup"><span data-stu-id="ded75-108">Using ComCtl32 Version 6 in Control Panel or a DLL That Is Run by RunDll32.exe</span></span>](#using-comctl32-version-6-in-control-panel-or-a-dll-that-is-run-by-rundll32exe)
-   [<span data-ttu-id="ded75-109">Добавление поддержки визуального стиля для расширения, подключаемого модуля, оснастки MMC или библиотеки DLL, которая переносится в процесс</span><span class="sxs-lookup"><span data-stu-id="ded75-109">Adding Visual Style Support to an Extension, Plug-in, MMC Snap-in or a DLL That Is Brought into a Process</span></span>](#adding-visual-style-support-to-an-extension-plug-in-mmc-snap-in-or-a-dll-that-is-brought-into-a-process)
-   [<span data-ttu-id="ded75-110">Выключение визуальных стилей</span><span class="sxs-lookup"><span data-stu-id="ded75-110">Turning Off Visual Styles</span></span>](#turning-off-visual-styles)
-   [<span data-ttu-id="ded75-111">Использование стилей оформления с содержимым HTML</span><span class="sxs-lookup"><span data-stu-id="ded75-111">Using Visual Styles with HTML Content</span></span>](#using-visual-styles-with-html-content)
-   [<span data-ttu-id="ded75-112">Когда визуальные стили не применяются</span><span class="sxs-lookup"><span data-stu-id="ded75-112">When Visual Styles are not Applied</span></span>](#when-visual-styles-are-not-applied)
-   [<span data-ttu-id="ded75-113">Обеспечение совместимости приложения с более ранними версиями Windows</span><span class="sxs-lookup"><span data-stu-id="ded75-113">Making Your Application Compatible with Earlier Versions of Windows</span></span>](#making-your-application-compatible-with-earlier-versions-of-windows)
-   [<span data-ttu-id="ded75-114">См. также</span><span class="sxs-lookup"><span data-stu-id="ded75-114">Related topics</span></span>](#related-topics)

## <a name="using-manifests-or-directives-to-ensure-that-visual-styles-can-be-applied-to-applications"></a><span data-ttu-id="ded75-115">Использование манифестов или директив для обеспечения возможности применения стилей оформления к приложениям</span><span class="sxs-lookup"><span data-stu-id="ded75-115">Using Manifests or Directives to Ensure That Visual Styles Can Be Applied to Applications</span></span>

<span data-ttu-id="ded75-116">Чтобы разрешить приложению использовать стили оформления, необходимо использовать ComCtl32.dll версии 6 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="ded75-116">To enable your application to use visual styles, you must use ComCtl32.dll version 6 or later.</span></span> <span data-ttu-id="ded75-117">Поскольку версия 6 не распространяется на распространяемый пакет, она доступна только в том случае, если приложение работает в той версии Windows, которая содержит его.</span><span class="sxs-lookup"><span data-stu-id="ded75-117">Because version 6 is not redistributable, it is available only when your application is running on a version of Windows that contains it.</span></span> <span data-ttu-id="ded75-118">Windows поставляется как с версией 5, так и с версией 6.</span><span class="sxs-lookup"><span data-stu-id="ded75-118">Windows ships with both version 5 and version 6.</span></span> <span data-ttu-id="ded75-119">ComCtl32.dll версии 6 содержит как пользовательские элементы управления, так и общие элементы управления.</span><span class="sxs-lookup"><span data-stu-id="ded75-119">ComCtl32.dll version 6 contains both the user controls and the common controls.</span></span> <span data-ttu-id="ded75-120">По умолчанию приложения используют пользовательские элементы управления, определенные в User32.dll, и общие элементы управления, определенные в ComCtl32.dll версии 5.</span><span class="sxs-lookup"><span data-stu-id="ded75-120">By default, applications use the user controls defined in User32.dll and the common controls defined in ComCtl32.dll version 5.</span></span> <span data-ttu-id="ded75-121">Список версий DLL и их платформ распространения см. в разделе [общие версии элементов управления](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="ded75-121">For a list of DLL versions and their distribution platforms, see [Common Control Versions](common-control-versions.md).</span></span>

<span data-ttu-id="ded75-122">Если вы хотите, чтобы приложение использовало стили оформления, необходимо добавить манифест приложения или директиву компилятора, которая указывает, что следует использовать ComCtl32.dll версии 6, если она доступна.</span><span class="sxs-lookup"><span data-stu-id="ded75-122">If you want your application to use visual styles, you must add an application manifest or compiler directive that indicates that ComCtl32.dll version 6 should be used if it is available.</span></span>

<span data-ttu-id="ded75-123">Манифест приложения позволяет приложению указывать, какие версии сборки требуются.</span><span class="sxs-lookup"><span data-stu-id="ded75-123">An application manifest enables an application to specify which versions of an assembly it requires.</span></span> <span data-ttu-id="ded75-124">В Microsoft Win32 сборка представляет собой набор библиотек DLL и список объектов с версиями, содержащихся в этих библиотеках DLL.</span><span class="sxs-lookup"><span data-stu-id="ded75-124">In Microsoft Win32, an assembly is a set of DLLs and a list of versionable objects that are contained within those DLLs.</span></span>

<span data-ttu-id="ded75-125">Манифесты записываются в формате XML.</span><span class="sxs-lookup"><span data-stu-id="ded75-125">Manifests are written in XML.</span></span> <span data-ttu-id="ded75-126">Имя файла манифеста приложения — это имя исполняемого объекта, за которым следует расширение MANIFEST; Например, MyApp.exe. manifest.</span><span class="sxs-lookup"><span data-stu-id="ded75-126">The name of the application manifest file is the name of your executable followed by the file name extension .manifest; for example, MyApp.exe.manifest.</span></span> <span data-ttu-id="ded75-127">В следующем примере манифеста показано, что в первом разделе описывается сам манифест.</span><span class="sxs-lookup"><span data-stu-id="ded75-127">The following sample manifest shows that the first section describes the manifest itself.</span></span> <span data-ttu-id="ded75-128">В следующей таблице показаны атрибуты, заданные элементом **assemblyIdentity** в разделе описания манифеста.</span><span class="sxs-lookup"><span data-stu-id="ded75-128">The following table shows the attributes set by the **assemblyIdentity** element in the manifest description section.</span></span>



| <span data-ttu-id="ded75-129">attribute</span><span class="sxs-lookup"><span data-stu-id="ded75-129">Attribute</span></span>             | <span data-ttu-id="ded75-130">Описание</span><span class="sxs-lookup"><span data-stu-id="ded75-130">Description</span></span>                                                                                                                 |
|-----------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ded75-131">version</span><span class="sxs-lookup"><span data-stu-id="ded75-131">version</span></span>               | <span data-ttu-id="ded75-132">Версия манифеста.</span><span class="sxs-lookup"><span data-stu-id="ded75-132">Version of the manifest.</span></span> <span data-ttu-id="ded75-133">Версия должна быть указана в формате основная. Дополнительная. Редакция. сборка (т. е. n. n. n. n, где n <= 65535).</span><span class="sxs-lookup"><span data-stu-id="ded75-133">The version must be in the form major.minor.revision.build (that is, n.n.n.n, where n <=65535).</span></span> |
| <span data-ttu-id="ded75-134">processorArchitecture</span><span class="sxs-lookup"><span data-stu-id="ded75-134">processorArchitecture</span></span> | <span data-ttu-id="ded75-135">Процессор, для которого разрабатывается приложение.</span><span class="sxs-lookup"><span data-stu-id="ded75-135">Processor for which your application is developed.</span></span>                                                                          |
| <span data-ttu-id="ded75-136">name</span><span class="sxs-lookup"><span data-stu-id="ded75-136">name</span></span>                  | <span data-ttu-id="ded75-137">Включает название организации, название продукта и имя приложения.</span><span class="sxs-lookup"><span data-stu-id="ded75-137">Includes company name, product name and application name.</span></span>                                                                   |
| <span data-ttu-id="ded75-138">тип</span><span class="sxs-lookup"><span data-stu-id="ded75-138">type</span></span>                  | <span data-ttu-id="ded75-139">Тип приложения, например Win32.</span><span class="sxs-lookup"><span data-stu-id="ded75-139">Type of your application, such as Win32.</span></span>                                                                                    |



 

<span data-ttu-id="ded75-140">Пример манифеста также предоставляет описание приложения и определяет зависимости приложений.</span><span class="sxs-lookup"><span data-stu-id="ded75-140">The sample manifest also provides a description of your application and specifies application dependencies.</span></span> <span data-ttu-id="ded75-141">В следующей таблице показаны атрибуты, заданные элементом **assemblyIdentity** в разделе зависимостей.</span><span class="sxs-lookup"><span data-stu-id="ded75-141">The following table shows the attributes set by the **assemblyIdentity** element in the dependency section.</span></span>



| <span data-ttu-id="ded75-142">attribute</span><span class="sxs-lookup"><span data-stu-id="ded75-142">Attribute</span></span>             | <span data-ttu-id="ded75-143">Описание</span><span class="sxs-lookup"><span data-stu-id="ded75-143">Description</span></span>                                      |
|-----------------------|--------------------------------------------------|
| <span data-ttu-id="ded75-144">type</span><span class="sxs-lookup"><span data-stu-id="ded75-144">type</span></span>                  | <span data-ttu-id="ded75-145">Тип компонента зависимости, например Win32.</span><span class="sxs-lookup"><span data-stu-id="ded75-145">Type of the dependency component, such as Win32.</span></span> |
| <span data-ttu-id="ded75-146">name</span><span class="sxs-lookup"><span data-stu-id="ded75-146">name</span></span>                  | <span data-ttu-id="ded75-147">Имя компонента.</span><span class="sxs-lookup"><span data-stu-id="ded75-147">Name of the component.</span></span>                           |
| <span data-ttu-id="ded75-148">version</span><span class="sxs-lookup"><span data-stu-id="ded75-148">version</span></span>               | <span data-ttu-id="ded75-149">Версия компонента.</span><span class="sxs-lookup"><span data-stu-id="ded75-149">Version of the component.</span></span>                        |
| <span data-ttu-id="ded75-150">processorArchitecture</span><span class="sxs-lookup"><span data-stu-id="ded75-150">processorArchitecture</span></span> | <span data-ttu-id="ded75-151">Процессор, для которого предназначен компонент.</span><span class="sxs-lookup"><span data-stu-id="ded75-151">Processor that the component is designed for.</span></span>    |
| <span data-ttu-id="ded75-152">publicKeyToken</span><span class="sxs-lookup"><span data-stu-id="ded75-152">publicKeyToken</span></span>        | <span data-ttu-id="ded75-153">Токен ключа, используемый с этим компонентом.</span><span class="sxs-lookup"><span data-stu-id="ded75-153">Key token used with this component.</span></span>              |
| <span data-ttu-id="ded75-154">Язык</span><span class="sxs-lookup"><span data-stu-id="ded75-154">language</span></span>              | <span data-ttu-id="ded75-155">Язык компонента.</span><span class="sxs-lookup"><span data-stu-id="ded75-155">Language of the component.</span></span>                       |



 

<span data-ttu-id="ded75-156">Ниже приведен пример файла манифеста.</span><span class="sxs-lookup"><span data-stu-id="ded75-156">Following is an example of a manifest file.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ded75-157">Установите для записи **processorArchitecture** значение **"x86"** , если приложение предназначено для 32 разрядной платформы Windows, или **"amd64"** , если приложение предназначено для платформы 64 на платформе Windows.</span><span class="sxs-lookup"><span data-stu-id="ded75-157">Set the **processorArchitecture** entry to **"X86"** if your application targets the 32 bit Windows platform, or to **"amd64"** if your application targets the 64 bit Windows platform.</span></span> <span data-ttu-id="ded75-158">Можно также указать **" \* "**, чтобы обеспечить целевую платформу для всех платформ, как показано в следующих примерах.</span><span class="sxs-lookup"><span data-stu-id="ded75-158">You can also specify **"\*"**, which ensures that all platforms are targeted, as shown in the following examples.</span></span>

 


```C++
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
<assemblyIdentity
    version="1.0.0.0"
    processorArchitecture="*"
    name="CompanyName.ProductName.YourApplication"
    type="win32"
/>
<description>Your application description here.</description>
<dependency>
    <dependentAssembly>
        <assemblyIdentity
            type="win32"
            name="Microsoft.Windows.Common-Controls"
            version="6.0.0.0"
            processorArchitecture="*"
            publicKeyToken="6595b64144ccf1df"
            language="*"
        />
    </dependentAssembly>
</dependency>
</assembly>
```



<span data-ttu-id="ded75-159">При использовании Microsoft Visual C++ 2005 или более поздней версии можно добавить следующую директиву компилятора в исходный код вместо создания манифеста вручную.</span><span class="sxs-lookup"><span data-stu-id="ded75-159">If you are using Microsoft Visual C++ 2005 or later, you can add the following compiler directive to your source code instead of manually creating a manifest.</span></span> <span data-ttu-id="ded75-160">Для удобочитаемости директива разбивается на несколько строк.</span><span class="sxs-lookup"><span data-stu-id="ded75-160">For readability, the directive is broken into several lines here.</span></span>


```C++
#pragma comment(linker,"\"/manifestdependency:type='win32' \
name='Microsoft.Windows.Common-Controls' version='6.0.0.0' \
processorArchitecture='*' publicKeyToken='6595b64144ccf1df' language='*'\"")
```



<span data-ttu-id="ded75-161">В следующих разделах описаны действия по применению стилей оформления к различным типам приложений.</span><span class="sxs-lookup"><span data-stu-id="ded75-161">The following topics describe the steps for applying visual styles to different types of applications.</span></span> <span data-ttu-id="ded75-162">Обратите внимание, что в каждом случае используется один и тот же формат манифеста.</span><span class="sxs-lookup"><span data-stu-id="ded75-162">Notice that the manifest format is the same in each case.</span></span>

## <a name="using-comctl32dll-version-6-in-an-application-that-uses-only-standard-extensions"></a><span data-ttu-id="ded75-163">Использование ComCtl32.dll версии 6 в приложении, использующем только стандартные расширения</span><span class="sxs-lookup"><span data-stu-id="ded75-163">Using ComCtl32.dll Version 6 in an Application That Uses Only Standard Extensions</span></span>

<span data-ttu-id="ded75-164">Ниже приведены примеры приложений, которые не используют сторонние расширения.</span><span class="sxs-lookup"><span data-stu-id="ded75-164">The following are examples of applications that do not use third-party extensions.</span></span>

-   <span data-ttu-id="ded75-165">Calculator</span><span class="sxs-lookup"><span data-stu-id="ded75-165">Calculator</span></span>
-   <span data-ttu-id="ded75-166">Солитер</span><span class="sxs-lookup"><span data-stu-id="ded75-166">FreeCell</span></span>
-   <span data-ttu-id="ded75-167">Сапер</span><span class="sxs-lookup"><span data-stu-id="ded75-167">Minesweeper</span></span>
-   <span data-ttu-id="ded75-168">Блокнот</span><span class="sxs-lookup"><span data-stu-id="ded75-168">Notepad</span></span>
-   <span data-ttu-id="ded75-169">Косынка</span><span class="sxs-lookup"><span data-stu-id="ded75-169">Solitaire</span></span>

<span data-ttu-id="ded75-170">**Чтобы создать манифест и позволить приложению использовать стили оформления.**</span><span class="sxs-lookup"><span data-stu-id="ded75-170">**To create a manifest and enable your application to use visual styles.**</span></span>

1.  <span data-ttu-id="ded75-171">Свяжите с ComCtl32. lib и вызовите [**иниткоммонконтролс**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols).</span><span class="sxs-lookup"><span data-stu-id="ded75-171">Link to ComCtl32.lib and call [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols).</span></span>
2.  <span data-ttu-id="ded75-172">Добавьте файл с именем YourApp.exe. manifest в дерево исходного кода, имеющее формат XML-манифеста.</span><span class="sxs-lookup"><span data-stu-id="ded75-172">Add a file called YourApp.exe.manifest to your source tree that has the XML manifest format.</span></span>
    ```C++
    <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity
        version="1.0.0.0"
        processorArchitecture="*"
        name="CompanyName.ProductName.YourApplication"
        type="win32"
    />
    <description>Your application description here.</description>
    <dependency>
        <dependentAssembly>
            <assemblyIdentity
                type="win32"
                name="Microsoft.Windows.Common-Controls"
                version="6.0.0.0"
                processorArchitecture="*"
                publicKeyToken="6595b64144ccf1df"
                language="*"
            />
        </dependentAssembly>
    </dependency>
    </assembly>
    ```

    

3.  <span data-ttu-id="ded75-173">Добавьте манифест в файл ресурсов приложения следующим образом:</span><span class="sxs-lookup"><span data-stu-id="ded75-173">Add the manifest to your application's resource file as follows:</span></span>
    ```C++
    CREATEPROCESS_MANIFEST_RESOURCE_ID RT_MANIFEST "YourApp.exe.manifest"
    ```

    

    > [!Note]  
    > <span data-ttu-id="ded75-174">При добавлении предыдущей записи в ресурс ее необходимо отформатировать в одной строке.</span><span class="sxs-lookup"><span data-stu-id="ded75-174">When you add the previous entry to the resource you must format it on one line.</span></span> <span data-ttu-id="ded75-175">Кроме того, файл манифеста XML можно поместить в тот же каталог, что и исполняемый файл приложения.</span><span class="sxs-lookup"><span data-stu-id="ded75-175">Alternatively, you can place the XML manifest file in the same directory as your application's executable file.</span></span> <span data-ttu-id="ded75-176">Операционная система сначала загрузит манифест из файловой системы, а затем проверьте раздел ресурсов исполняемого файла.</span><span class="sxs-lookup"><span data-stu-id="ded75-176">The operating system will load the manifest from the file system first, then check the resource section of the executable.</span></span> <span data-ttu-id="ded75-177">Версия файловой системы имеет приоритет.</span><span class="sxs-lookup"><span data-stu-id="ded75-177">The file system version takes precedence.</span></span>

     

<span data-ttu-id="ded75-178">При сборке приложения манифест будет добавлен как двоичный ресурс.</span><span class="sxs-lookup"><span data-stu-id="ded75-178">When you build your application, the manifest will be added as a binary resource.</span></span>

## <a name="using-comctl32-version-6-in-control-panel-or-a-dll-that-is-run-by-rundll32exe"></a><span data-ttu-id="ded75-179">С помощью ComCtl32 версии 6 на панели управления или библиотеки DLL, которая запускается с RunDll32.exe</span><span class="sxs-lookup"><span data-stu-id="ded75-179">Using ComCtl32 Version 6 in Control Panel or a DLL That Is Run by RunDll32.exe</span></span>

<span data-ttu-id="ded75-180">**Чтобы создать манифест и позволить приложению использовать стили оформления.**</span><span class="sxs-lookup"><span data-stu-id="ded75-180">**To create a manifest and enable your application to use visual styles.**</span></span>

1.  <span data-ttu-id="ded75-181">Свяжите с ComCtl32. lib и вызовите [**иниткоммонконтролс**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols).</span><span class="sxs-lookup"><span data-stu-id="ded75-181">Link to ComCtl32.lib and call [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols).</span></span>
2.  <span data-ttu-id="ded75-182">Добавьте файл с именем YourApp.cpl. manifest в дерево исходного кода, имеющее формат XML-манифеста.</span><span class="sxs-lookup"><span data-stu-id="ded75-182">Add a file called YourApp.cpl.manifest to your source tree that has the XML manifest format.</span></span>
    ```C++
    <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity
        version="1.0.0.0"
        processorArchitecture="*"
        name="CompanyName.ProductName.YourApplication"
        type="win32"
    />
    <description>Your application description here.</description>
    <dependency>
        <dependentAssembly>
            <assemblyIdentity
                type="win32"
                name="Microsoft.Windows.Common-Controls"
                version="6.0.0.0"
                processorArchitecture="*"
                publicKeyToken="6595b64144ccf1df"
                language="*"
            />
        </dependentAssembly>
    </dependency>
    </assembly>
    ```

    

3.  <span data-ttu-id="ded75-183">Добавьте манифест в файл ресурсов приложения в качестве идентификатора ресурса 123.</span><span class="sxs-lookup"><span data-stu-id="ded75-183">Add the manifest to your application's resource file as resource ID 123.</span></span>

> [!Note]  
> <span data-ttu-id="ded75-184">При создании приложения панели управления поместите его в соответствующую категорию.</span><span class="sxs-lookup"><span data-stu-id="ded75-184">When you author a Control Panel application, place it in the appropriate category.</span></span> <span data-ttu-id="ded75-185">Панель управления теперь поддерживает категоризацию приложений панели управления.</span><span class="sxs-lookup"><span data-stu-id="ded75-185">Control Panel now supports categorization of Control Panel applications.</span></span> <span data-ttu-id="ded75-186">Это означает, что приложениям панели управления можно назначать идентификаторы и разделять их на области задач, такие как установка и удаление программ, оформление и темы, а также параметры даты, времени, языка и региональных параметров.</span><span class="sxs-lookup"><span data-stu-id="ded75-186">This means that Control Panel applications can be assigned identifiers and separated into task areas such as Add or Remove Programs, Appearance and Themes, or Date, Time, Language, and Regional Options.</span></span>

 

## <a name="adding-visual-style-support-to-an-extension-plug-in-mmc-snap-in-or-a-dll-that-is-brought-into-a-process"></a><span data-ttu-id="ded75-187">Добавление поддержки визуального стиля для расширения, подключаемого модуля, оснастки MMC или библиотеки DLL, которая переносится в процесс</span><span class="sxs-lookup"><span data-stu-id="ded75-187">Adding Visual Style Support to an Extension, Plug-in, MMC Snap-in or a DLL That Is Brought into a Process</span></span>

<span data-ttu-id="ded75-188">Поддержку визуальных стилей можно добавить в расширение, подключаемый модуль, оснастку MMC или библиотеку DLL, которая выполняется в процессе.</span><span class="sxs-lookup"><span data-stu-id="ded75-188">Support for visual styles can be added to an extension, plug-in, MMC snap-in, or a DLL that is brought into a process.</span></span> <span data-ttu-id="ded75-189">Например, чтобы добавить поддержку визуальных стилей для оснастки консоли управления (MMC), выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="ded75-189">For example, use the following steps to add visual styles support for an Microsoft Management Console (MMC) snap-in.</span></span>

1.  <span data-ttu-id="ded75-190">Скомпилируйте оснастку с флагом-ДИСОЛАТИОН, поддерживающим \_ \_ поддержку, или вставьте следующую инструкцию перед \# оператором include "Windows. h".</span><span class="sxs-lookup"><span data-stu-id="ded75-190">Compile your snap-in with the -DISOLATION\_AWARE\_ENABLED flag or insert the following statement before the \#include "windows.h" statement.</span></span>

    ```C++
    #define ISOLATION_AWARE_ENABLED 1
    ```

    

    <span data-ttu-id="ded75-191">Дополнительные сведения о \_ \_ включении режима изоляции см. в разделе [изоляция компонентов](/windows/desktop/SbsCs/isolating-components).</span><span class="sxs-lookup"><span data-stu-id="ded75-191">For more information about ISOLATION\_AWARE\_ENABLED, see [Isolating Components](/windows/desktop/SbsCs/isolating-components).</span></span>

2.  <span data-ttu-id="ded75-192">Включите файл заголовка Common Control в источник оснастки.</span><span class="sxs-lookup"><span data-stu-id="ded75-192">Include the common control header file in your snap-in source.</span></span>
    ```C++
    #include <commctrl.h>
    ```

    

3.  <span data-ttu-id="ded75-193">Добавьте файл с именем Йоурапп. manifest в дерево источника, использующее формат XML-манифеста.</span><span class="sxs-lookup"><span data-stu-id="ded75-193">Add a file called YourApp.manifest to your source tree that uses the XML manifest format.</span></span>
    ```C++
    <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity
        version="1.0.0.0"
        processorArchitecture="*"
        name="CompanyName.ProductName.YourApplication"
        type="win32"
    />
    <description>Your application description here.</description>
    <dependency>
        <dependentAssembly>
            <assemblyIdentity
                type="win32"
                name="Microsoft.Windows.Common-Controls"
                version="6.0.0.0"
                processorArchitecture="*"
                publicKeyToken="6595b64144ccf1df"
                language="*"
            />
        </dependentAssembly>
    </dependency>
    </assembly>
    ```

    

4.  <span data-ttu-id="ded75-194">Добавьте манифест в файл ресурсов оснастки.</span><span class="sxs-lookup"><span data-stu-id="ded75-194">Add the manifest to your snap-in's resource file.</span></span> <span data-ttu-id="ded75-195">Дополнительные сведения о добавлении манифеста в файл ресурсов см. [в разделе Использование Comctl32 версии 6 в приложении, использующем расширения, подключаемые модули или библиотеку DLL, которая содержится в процессе](/previous-versions//ms649781(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="ded75-195">See [Using ComCtl32 Version 6 in an Application That Uses Extensions, Plug-ins, or a DLL That Is Brought into a Process](/previous-versions//ms649781(v=vs.85)) for details on adding a manifest to a resource file.</span></span>

## <a name="turning-off-visual-styles"></a><span data-ttu-id="ded75-196">Выключение визуальных стилей</span><span class="sxs-lookup"><span data-stu-id="ded75-196">Turning Off Visual Styles</span></span>

<span data-ttu-id="ded75-197">Вы можете отключить визуальные стили для элемента управления или для всех элементов управления в окне, вызвав функцию [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme) следующим образом:</span><span class="sxs-lookup"><span data-stu-id="ded75-197">You can turn off visual styles for a control or for all controls in a window by calling the [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme) function as follows:</span></span>


```C++
SetWindowTheme(hwnd, L" ", L" ");
```



<span data-ttu-id="ded75-198">В предыдущем примере *HWND* — это дескриптор окна, в котором отключаются визуальные стили.</span><span class="sxs-lookup"><span data-stu-id="ded75-198">In the previous example, *hwnd* is the handle of the window in which to disable visual styles.</span></span> <span data-ttu-id="ded75-199">После вызова элемент управления визуализируется без визуальных стилей.</span><span class="sxs-lookup"><span data-stu-id="ded75-199">After the call, the control renders without visual styles.</span></span>

## <a name="using-visual-styles-with-html-content"></a><span data-ttu-id="ded75-200">Использование стилей оформления с содержимым HTML</span><span class="sxs-lookup"><span data-stu-id="ded75-200">Using Visual Styles with HTML Content</span></span>

<span data-ttu-id="ded75-201">HTML-страницы, которые изменяют свойства каскадные таблицы стилей (CSS), такие как Background или Border, не имеют примененных к ним стилей оформления.</span><span class="sxs-lookup"><span data-stu-id="ded75-201">HTML pages that modify the Cascading Style Sheets (CSS) properties such as background or border do not have visual styles applied to them.</span></span> <span data-ttu-id="ded75-202">Они отображают указанный атрибут CSS.</span><span class="sxs-lookup"><span data-stu-id="ded75-202">They display the specified CSS attribute.</span></span> <span data-ttu-id="ded75-203">При указании в составе содержимого большинство свойств CSS применяются к элементам, к которым применены визуальные стили.</span><span class="sxs-lookup"><span data-stu-id="ded75-203">When specified as part of the content, most CSS properties do apply to elements that have visual styles applied.</span></span>

<span data-ttu-id="ded75-204">По умолчанию визуальные стили применяются к встроенным элементам управления HTML на страницах, отображаемых в Microsoft Internet Explorer 6 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="ded75-204">By default, visual styles are applied to intrinsic HTML controls on pages displayed in Microsoft Internet Explorer 6 and later versions.</span></span> <span data-ttu-id="ded75-205">Чтобы отключить стили оформления для HTML-страницы, добавьте тег META в элемент</span><span class="sxs-lookup"><span data-stu-id="ded75-205">To turn off visual styles for an HTML page, add a META tag to the</span></span> <head> <span data-ttu-id="ded75-206">.</span><span class="sxs-lookup"><span data-stu-id="ded75-206">section.</span></span> <span data-ttu-id="ded75-207">Этот метод также применяется к содержимому, упакованному как HTML-приложения (HTA).</span><span class="sxs-lookup"><span data-stu-id="ded75-207">This technique also applies to content packaged as HTML Applications (HTAs).</span></span> <span data-ttu-id="ded75-208">Чтобы отключить стили оформления, тег META должен иметь следующий вид:</span><span class="sxs-lookup"><span data-stu-id="ded75-208">To turn off visual styles, the META tag must be as follows:</span></span>


```
<META HTTP-EQUIV="MSThemeCompatible" CONTENT="no">
```



> [!Note]  
> <span data-ttu-id="ded75-209">Если параметр браузера и параметр tag не согласуются, страница не будет применять стили оформления.</span><span class="sxs-lookup"><span data-stu-id="ded75-209">If the browser setting and the tag setting do not agree, the page will not apply visual styles.</span></span> <span data-ttu-id="ded75-210">Например, если для тега META задано значение «нет» и браузер настроен на включение визуальных стилей, визуальные стили не будут применены к странице.</span><span class="sxs-lookup"><span data-stu-id="ded75-210">For example, if the META tag is set to "no" and the browser is set to enable visual styles, visual styles will not be applied to the page.</span></span> <span data-ttu-id="ded75-211">Однако если в качестве тега браузера или мета задано значение "Да", а другой элемент не указан, будут применены визуальные стили.</span><span class="sxs-lookup"><span data-stu-id="ded75-211">However, if either the browser or META tag is set to "yes" and the other item is not specified, visual styles will be applied.</span></span>

 

<span data-ttu-id="ded75-212">Визуальные стили могут изменить макет содержимого.</span><span class="sxs-lookup"><span data-stu-id="ded75-212">Visual styles might change the layout of your content.</span></span> <span data-ttu-id="ded75-213">Кроме того, при задании определенных атрибутов для встроенных элементов управления HTML, таких как ширина кнопки, может оказаться, что метка кнопки нечитаема при определенных визуальных стилях.</span><span class="sxs-lookup"><span data-stu-id="ded75-213">Also, if you set certain attributes on intrinsic HTML controls, such as the width of a button, you might find that the label on the button is unreadable under certain visual styles.</span></span>

<span data-ttu-id="ded75-214">Необходимо тщательно протестировать содержимое с помощью визуальных стилей, чтобы определить, оказывает ли применение визуальных стилей негативное воздействие на содержимое и макет.</span><span class="sxs-lookup"><span data-stu-id="ded75-214">You must thoroughly test your content using visual styles to determine whether applying visual styles has an adverse effect on your content and layout.</span></span>

## <a name="when-visual-styles-are-not-applied"></a><span data-ttu-id="ded75-215">Когда визуальные стили не применяются</span><span class="sxs-lookup"><span data-stu-id="ded75-215">When Visual Styles are not Applied</span></span>

<span data-ttu-id="ded75-216">Чтобы избежать применения визуальных стилей к окну верхнего уровня, присвойте окну область, отличную от NULL (**сетвиндовргн**).</span><span class="sxs-lookup"><span data-stu-id="ded75-216">To avoid applying visual styles to a top level window, give the window a non-null region (**SetWindowRgn**).</span></span> <span data-ttu-id="ded75-217">Система предполагает, что окно с регионом, отличным от NULL, является специализированным окном, в котором не используются стили оформления.</span><span class="sxs-lookup"><span data-stu-id="ded75-217">The system assumes that a window with a non-NULL region is a specialized window that does not use visual styles.</span></span> <span data-ttu-id="ded75-218">Дочернее окно, связанное с окном верхнего уровня, не относящимся к визуальному элементу, может по-прежнему применять стили оформления, даже если в родительском окне нет.</span><span class="sxs-lookup"><span data-stu-id="ded75-218">A child window associated with a non-visual-styles top level window may still apply visual styles even though the parent window does not.</span></span>

<span data-ttu-id="ded75-219">Если вы хотите отключить использование стилей оформления для всех окон в приложении, вызовите [**сетсемеапппропертиес**](/windows/desktop/api/Uxtheme/nf-uxtheme-setthemeappproperties) и не передавайте \_ \_ флагом СТАП Allow unclient.</span><span class="sxs-lookup"><span data-stu-id="ded75-219">If you want to disable the use of visual styles for all windows in your application, call [**SetThemeAppProperties**](/windows/desktop/api/Uxtheme/nf-uxtheme-setthemeappproperties) and do not pass the STAP\_ALLOW\_NONCLIENT flag.</span></span> <span data-ttu-id="ded75-220">Если приложение не вызывает **сетсемеапппропертиес**, предполагается, что значения флага являются СТАП, \_ разрешающими \_ неклиентские СТАП, разрешить \| \_ \_ элементам управления \| СТАП разрешить доступ к \_ \_ содержимому.</span><span class="sxs-lookup"><span data-stu-id="ded75-220">If an application does not call **SetThemeAppProperties**, the assumed flag values are STAP\_ALLOW\_NONCLIENT \| STAP\_ALLOW\_CONTROLS \| STAP\_ALLOW\_WEBCONTENT.</span></span> <span data-ttu-id="ded75-221">Предполагаемые значения приводят к применению визуального стиля к неклиентской области, элементам управления и веб-содержимому.</span><span class="sxs-lookup"><span data-stu-id="ded75-221">The assumed values cause the nonclient area, the controls, and web content to have a visual style applied.</span></span>

## <a name="making-your-application-compatible-with-earlier-versions-of-windows"></a><span data-ttu-id="ded75-222">Обеспечение совместимости приложения с более ранними версиями Windows</span><span class="sxs-lookup"><span data-stu-id="ded75-222">Making Your Application Compatible with Earlier Versions of Windows</span></span>

<span data-ttu-id="ded75-223">Большая часть архитектуры визуального стиля призвана упростить поставку продукта в более ранних версиях Windows, которые не поддерживают изменение внешнего вида элементов управления.</span><span class="sxs-lookup"><span data-stu-id="ded75-223">Much of the visual style architecture is designed to make it simple to continue to ship your product on earlier versions of Windows that do not support changing the appearance of controls.</span></span> <span data-ttu-id="ded75-224">При отправке приложения для нескольких операционных систем учитывайте следующее.</span><span class="sxs-lookup"><span data-stu-id="ded75-224">When shipping an application for more than one operating system, be aware of the following:</span></span>

-   <span data-ttu-id="ded75-225">В версиях Windows до Windows 8 стили оформления отключены, когда включена высокая контрастность.</span><span class="sxs-lookup"><span data-stu-id="ded75-225">In versions of Windows prior to Windows 8, visual styles are off when high contrast is on.</span></span> <span data-ttu-id="ded75-226">Для поддержки высокой контрастности устаревшее приложение, поддерживающее стили оформления, должно предоставить отдельный путь к коду для правильной отрисовки элементов пользовательского интерфейса в высокой контрастности.</span><span class="sxs-lookup"><span data-stu-id="ded75-226">To support high contrast, a legacy application that supports visual styles needs to provide a separate code path to properly draw UI elements in high contrast.</span></span> <span data-ttu-id="ded75-227">В Windows 8 высокая контрастность является частью стилей оформления; Однако приложение Windows 8 (которое содержит GUID в разделе совместимости в манифесте приложения) по-прежнему должно предоставлять отдельный путь к коду для правильной отрисовки в Windows 7 с высокой контрастностью.</span><span class="sxs-lookup"><span data-stu-id="ded75-227">In Windows 8, high contrast is a part of visual styles; however, a Windows 8 application (one that includes the Windows 8 GUID in compatibility section of its application manifest) still needs to provide a separate code path to render correctly in high contrast on Windows 7 an earlier.</span></span>
-   <span data-ttu-id="ded75-228">Если вы используете функции ComCtl32.dll версии 6, например мозаичного представления или элемента управления связью, необходимо решить, где эти элементы управления недоступны на компьютере пользователя.</span><span class="sxs-lookup"><span data-stu-id="ded75-228">If you use the features in ComCtl32.dll version 6, such as the tile view or link control, you must handle the case where those controls are not available on your user's computer.</span></span> <span data-ttu-id="ded75-229">Версия ComCtl32.dll 6 не является распространяемой.</span><span class="sxs-lookup"><span data-stu-id="ded75-229">ComCtl32.dll version 6 is not redistributable.</span></span>
-   <span data-ttu-id="ded75-230">Протестируйте приложение, чтобы убедиться, что вы не полагаетесь на компоненты ComCtl32.dll версии 6 без предварительной проверки текущей версии.</span><span class="sxs-lookup"><span data-stu-id="ded75-230">Test your application to make sure you are not relying on features of ComCtl32.dll version 6 without first checking for the current version.</span></span>
-   <span data-ttu-id="ded75-231">Не следует связываться с Укссеме. lib.</span><span class="sxs-lookup"><span data-stu-id="ded75-231">Do not link to UxTheme.lib.</span></span>
-   <span data-ttu-id="ded75-232">Напишите код обработки ошибок для экземпляров, если визуальные стили не работают должным образом.</span><span class="sxs-lookup"><span data-stu-id="ded75-232">Write error-handling code for instances when visual styles do not work as expected.</span></span>
-   <span data-ttu-id="ded75-233">Установка манифеста приложения в более ранних версиях не повлияет на отрисовку элементов управления.</span><span class="sxs-lookup"><span data-stu-id="ded75-233">Installing your application's manifest in earlier versions will not affect the rendering of controls.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ded75-234">См. также</span><span class="sxs-lookup"><span data-stu-id="ded75-234">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ded75-235">Стили оформления</span><span class="sxs-lookup"><span data-stu-id="ded75-235">Visual Styles</span></span>](themes-overview.md)
</dt> </dl>

 

 