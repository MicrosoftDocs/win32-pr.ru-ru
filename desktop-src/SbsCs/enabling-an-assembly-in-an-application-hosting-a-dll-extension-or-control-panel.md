---
description: Если в приложении размещается библиотека DLL, расширение, подключаемый модуль или панель управления стороннего разработчика, может потребоваться включить сборку в приложении&\# 8212; без включения этой сборки для размещенных компонентов.
ms.assetid: 832957ca-82fc-4600-b469-512621dde921
title: Включение сборки в приложении, где размещается библиотека DLL, расширение или панель управления
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b04dd19b18c2cdce4783be47333b9afe53dd1ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647407"
---
# <a name="enabling-an-assembly-in-an-application-hosting-a-dll-extension-or-control-panel"></a><span data-ttu-id="1e3b2-103">Включение сборки в приложении, где размещается библиотека DLL, расширение или панель управления</span><span class="sxs-lookup"><span data-stu-id="1e3b2-103">Enabling an Assembly in an Application Hosting a DLL, Extension, or Control Panel</span></span>

<span data-ttu-id="1e3b2-104">Если в приложении размещается библиотека DLL, расширение, подключаемый модуль или панель управления стороннего разработчика, может потребоваться включить сборку в приложении, не включая эту сборку для размещенных компонентов.</span><span class="sxs-lookup"><span data-stu-id="1e3b2-104">If your application hosts a third-party DLL, extension, plug-in, or control panel, you may want to enable an assembly in your application—without also enabling this assembly for the hosted components.</span></span> <span data-ttu-id="1e3b2-105">Это может быть так, когда размещенному компоненту требуется изменение кода для использования сборки.</span><span class="sxs-lookup"><span data-stu-id="1e3b2-105">This can be the case when a hosted component requires code changes to use the assembly.</span></span> <span data-ttu-id="1e3b2-106">Как разработчик приложения, возможно, вам не удастся внести изменения в эти компоненты сторонних разработчиков.</span><span class="sxs-lookup"><span data-stu-id="1e3b2-106">As the application developer, you may be unable to make changes to these third-party components.</span></span> <span data-ttu-id="1e3b2-107">В этом случае следует выполнить процедуру, описанную в этом разделе, чтобы приложение может использовать сборку без влияния на размещенные компоненты.</span><span class="sxs-lookup"><span data-stu-id="1e3b2-107">In this case, you should follow the procedure described in this section so that your application can use the assembly without affecting the hosted components.</span></span>

-   <span data-ttu-id="1e3b2-108">Чтобы включить сборку в приложении, не затрагивая размещенные библиотеки DLL, расширения, подключаемые модули или панели управления, манифест, описывающий зависимость приложения от сборки, должен быть включен в приложение в качестве ресурса.</span><span class="sxs-lookup"><span data-stu-id="1e3b2-108">To enable an assembly in an application without affecting any hosted DLLs, extensions, plug-ins, or control panels, a manifest that describes the application's dependence on the assembly should be included in the application as a resource.</span></span> <span data-ttu-id="1e3b2-109">Размещенные компоненты, которые не включены в сборку, не должны включать манифесты, описывающие эту зависимость.</span><span class="sxs-lookup"><span data-stu-id="1e3b2-109">The hosted components that are not being enabled with the assembly should not include manifests describing this dependency.</span></span>
-   <span data-ttu-id="1e3b2-110">Чтобы включить сборку в приложении и ее размещенных библиотеках DLL, расширениях, подключаемых модулях или панелях управления, включите манифесты как ресурсы как в приложение, так и на его размещенные компоненты.</span><span class="sxs-lookup"><span data-stu-id="1e3b2-110">To enable an assembly in an application and its hosted DLLs, extensions, plug-ins, or control panels, include manifests as resources in both the application and its hosted components.</span></span> <span data-ttu-id="1e3b2-111">Манифесты, включенные в приложение и в размещенные компоненты, должны описывать зависимость от сборки.</span><span class="sxs-lookup"><span data-stu-id="1e3b2-111">The manifests included in the application and in the hosted components should each describe a dependence on the assembly.</span></span> <span data-ttu-id="1e3b2-112">Как правило, разработчик приложения добавляет в приложение манифест, а разработчик размещенных компонентов добавляет манифест в библиотеку DLL, расширение, подключаемый модуль или панель управления.</span><span class="sxs-lookup"><span data-stu-id="1e3b2-112">Typically, the application developer adds a manifest to the application and the hosted component developer adds a manifest to the DLL, extension, plug-in, or control panel.</span></span>

<span data-ttu-id="1e3b2-113">Следующий метод можно использовать для добавления манифеста в приложение или размещенного компонента, который является библиотекой DLL, расширением, подключаемым модулем или панелью управления.</span><span class="sxs-lookup"><span data-stu-id="1e3b2-113">The following method can be used to add a manifest to an application or a hosted component that is a DLL, extension, plug-in, or control panel.</span></span>

<span data-ttu-id="1e3b2-114">**Для включения сборки в приложении или размещенном компоненте.**</span><span class="sxs-lookup"><span data-stu-id="1e3b2-114">**To enable an assembly in an application or hosted component.**</span></span>

1.  <span data-ttu-id="1e3b2-115">Создайте манифест, описывающий зависимость приложения или расширения для сборки.</span><span class="sxs-lookup"><span data-stu-id="1e3b2-115">Author a manifest that describes the dependence of the application or extension on the assembly.</span></span>

    <span data-ttu-id="1e3b2-116">Например, манифест для "Йоураппликатион" можно создать, скопировав следующий пример манифеста и подставив правильные значения для **assemblyIdentity**, **processorArchitecture** и **Description**.</span><span class="sxs-lookup"><span data-stu-id="1e3b2-116">For example, the manifest for "YourApplication" can be created by copying the following sample manifest and substituting correct values for **assemblyIdentity**, **processorArchitecture**, and **description**.</span></span> <span data-ttu-id="1e3b2-117">Установите значение **processorArchitecture** равным x86, если сборка на базе 32-разрядной платформы и архитектура ia64 при сборке на 64-разрядной платформе.</span><span class="sxs-lookup"><span data-stu-id="1e3b2-117">Set the value of **processorArchitecture** to x86 if building on a 32-bit platform and to ia64 if building on a 64-bit platform.</span></span> <span data-ttu-id="1e3b2-118">Элемент **Description** содержит описание параметра приложения.</span><span class="sxs-lookup"><span data-stu-id="1e3b2-118">The **description** element contains an option description of the application.</span></span> <span data-ttu-id="1e3b2-119">Дополнительные сведения о формате манифеста см. в разделе [манифесты приложений](application-manifests.md).</span><span class="sxs-lookup"><span data-stu-id="1e3b2-119">For more information about the manifest format, see [application manifests](application-manifests.md).</span></span>

    ``` syntax
    <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity
        version="1.0.0.0"
        processorArchitecture="x86"
        name="YourCompanyName.YourDivision.YourApp"
        type="win32"
    />
    <description>Your app description here</description>
    <dependency>
        <dependentAssembly>
            <assemblyIdentity
                type="win32"
                name="Proseware.Research.SampleAssembly"
                version="6.0.0.0"
                processorArchitecture="X86"
                publicKeyToken="0000000000000000"
                language="*"
            />
        </dependentAssembly>
    </dependency>
    </assembly>
    ```

2.  <span data-ttu-id="1e3b2-120">Создайте ресурс в приложении или расширение типа "RT" с \_ идентификатором 2.</span><span class="sxs-lookup"><span data-stu-id="1e3b2-120">Create a resource in the application or extension of type RT\_MANIFEST id 2.</span></span>

    <span data-ttu-id="1e3b2-121">Например, если имя приложения — Йоурапп, приложение должно содержать следующее:</span><span class="sxs-lookup"><span data-stu-id="1e3b2-121">For example, if the application's name is YourApp, the application should contain the following:</span></span>

    ``` syntax
    #define MANIFEST_RESOURCE_ID 2
    MANIFEST_RESOURCE_ID RT_MANIFEST "YourApp.manifest"
    ```

3.  <span data-ttu-id="1e3b2-122">Скомпилируйте приложение с флагом-ДИСОЛАТИОН \_ , поддерживающим \_ поддержку, или вставьте эту инструкцию перед \# оператором include "Windows. h".</span><span class="sxs-lookup"><span data-stu-id="1e3b2-122">Compile the application with the -DISOLATION\_AWARE\_ENABLED flag, or insert this statement before the \#include "Windows.h" statement.</span></span> <span data-ttu-id="1e3b2-123">В случае приложения с несколькими модулями \_ \_ на всех модулях должен быть включен флаг-дисолатион с поддержкой включения.</span><span class="sxs-lookup"><span data-stu-id="1e3b2-123">In the case of an application with multiple modules, the -DISOLATION\_AWARE\_ENABLED flag is required on all modules.</span></span>

    ``` syntax
    #define ISOLATION_AWARE_ENABLED 1
    ```

4.  <span data-ttu-id="1e3b2-124">Проверьте, правильно ли работают сборки, используемые приложением, в приложении и размещенном компоненте.</span><span class="sxs-lookup"><span data-stu-id="1e3b2-124">Test to ensure that assemblies that are used by the application work correctly in the application and hosted component.</span></span>

<span data-ttu-id="1e3b2-125">Дополнительные сведения о добавлении сборки в приложения без расширений см. в разделе [Включение сборки в приложении без расширений](enabling-an-assembly-in-an-application-without-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="1e3b2-125">For more information about adding an assembly to applications without extensions, see [Enabling an Assembly in an Application Without Extensions](enabling-an-assembly-in-an-application-without-extensions.md).</span></span>

 

 



