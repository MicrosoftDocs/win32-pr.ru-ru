---
description: Если в приложении не размещена библиотека DLL, расширение, подключаемый модуль или панель управления, можно использовать метод, описанный в этом разделе, чтобы включить сборку для приложения.
ms.assetid: d043ec1b-ac31-45fb-9232-eec42aef4ac3
title: Включение сборки в приложении без расширений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a1bbcfe510f5a3cdbce323f01cb9342ce236c7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105651146"
---
# <a name="enabling-an-assembly-in-an-application-without-extensions"></a><span data-ttu-id="2197f-103">Включение сборки в приложении без расширений</span><span class="sxs-lookup"><span data-stu-id="2197f-103">Enabling an Assembly in an Application Without Extensions</span></span>

<span data-ttu-id="2197f-104">Если в приложении не размещена библиотека DLL, расширение, подключаемый модуль или панель управления, можно использовать метод, описанный в этом разделе, чтобы включить сборку для приложения.</span><span class="sxs-lookup"><span data-stu-id="2197f-104">If your application does not host a DLL, extension, plug-in, or control panel, you can use the method described in this section to enable an assembly for your application.</span></span> <span data-ttu-id="2197f-105">Дополнительные сведения о добавлении сборки в приложения с расширениями см. [в разделе Включение сборки в приложении, где размещается библиотека DLL, расширение или панель управления](enabling-an-assembly-in-an-application-hosting-a-dll-extension-or-control-panel.md).</span><span class="sxs-lookup"><span data-stu-id="2197f-105">For more information about adding an assembly to applications with extensions, see [Enabling an Assembly in an Application Hosting a DLL, Extension, or Control Panel](enabling-an-assembly-in-an-application-hosting-a-dll-extension-or-control-panel.md).</span></span>

<span data-ttu-id="2197f-106">**Включение сборки в приложении без размещенных компонентов**</span><span class="sxs-lookup"><span data-stu-id="2197f-106">**To enable an assembly in an application without any hosted components**</span></span>

1.  <span data-ttu-id="2197f-107">Создайте манифест, описывающий зависимость приложения или расширения для сборки.</span><span class="sxs-lookup"><span data-stu-id="2197f-107">Author a manifest that describes the dependence of the application or extension on the assembly.</span></span>

    <span data-ttu-id="2197f-108">Например, манифест для "Йоураппликатион" можно создать, скопировав следующий пример манифеста и подставив правильные значения для **assemblyIdentity**, **processorArchitecture** и **Description**.</span><span class="sxs-lookup"><span data-stu-id="2197f-108">For example, the manifest for "YourApplication" can be created by copying the following sample manifest and substituting correct values for **assemblyIdentity**, **processorArchitecture**, and **description**.</span></span> <span data-ttu-id="2197f-109">Установите значение **processorArchitecture** на x86, если сборка на 32-разрядной платформе, и на ia64 при сборке на 64-разрядной платформе.</span><span class="sxs-lookup"><span data-stu-id="2197f-109">Set the value of **processorArchitecture** to x86 if building on a 32-bit platform, and to ia64 if building on a 64-bit platform.</span></span> <span data-ttu-id="2197f-110">Элемент **Description** содержит описание параметра приложения.</span><span class="sxs-lookup"><span data-stu-id="2197f-110">The **description** element contains an option description of the application.</span></span> <span data-ttu-id="2197f-111">Дополнительные сведения о формате манифеста см. в разделе [манифесты приложений](application-manifests.md).</span><span class="sxs-lookup"><span data-stu-id="2197f-111">For more information about the manifest format, see [application manifests](application-manifests.md).</span></span>

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

2.  <span data-ttu-id="2197f-112">Добавьте манифест в приложение в качестве ресурса в двоичный файл заголовка исполняемого файла приложения.</span><span class="sxs-lookup"><span data-stu-id="2197f-112">Add the manifest to the application as a resource in the application's binary executable header file.</span></span> <span data-ttu-id="2197f-113">Не рекомендуется добавлять манифест в приложение в качестве внешнего файла манифеста.</span><span class="sxs-lookup"><span data-stu-id="2197f-113">It is not recommended that you add the manifest to the application as an external manifest file.</span></span>

    <span data-ttu-id="2197f-114">Чтобы добавить манифест в качестве ресурса, создайте ресурс в приложении типа "RT \_ manifest ID 1".</span><span class="sxs-lookup"><span data-stu-id="2197f-114">To add the manifest as a resource, create a resource in the application of type RT\_MANIFEST id 1.</span></span> <span data-ttu-id="2197f-115">Например, если имя приложения — Йоурапп, файл заголовка приложения должен содержать следующее:</span><span class="sxs-lookup"><span data-stu-id="2197f-115">For example, if the application's name is YourApp, the application's header file should contain the following:</span></span>

    ``` syntax
    #define MANIFEST_RESOURCE_ID 1
    MANIFEST_RESOURCE_ID RT_MANIFEST "YourApp.manifest"
    ```

    <span data-ttu-id="2197f-116">При добавлении манифеста в качестве внешнего файла манифеста следует убедиться, что установка копирует файл манифеста в папку, содержащую исполняемый файл приложения.</span><span class="sxs-lookup"><span data-stu-id="2197f-116">If you instead add the manifest as an external manifest file, be sure that the installation copies the manifest file into the folder containing the application's executable file.</span></span>

3.  <span data-ttu-id="2197f-117">Выполните проверку, чтобы убедиться, что сборки, используемые приложением, работают в приложении правильно.</span><span class="sxs-lookup"><span data-stu-id="2197f-117">Test to ensure that assemblies used by the application work correctly in the application.</span></span>

 

 



