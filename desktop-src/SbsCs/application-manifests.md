---
description: Манифест приложения — это файл XML, который описывает и определяет общие и закрытые сборки одновременного выполнения, которые приложению следует подключить во время выполнения.
ms.assetid: c5016251-db7a-4edc-9be9-3acb03d495f8
title: Манифесты приложений
ms.topic: article
ms.date: 10/08/2020
ms.custom: 19H1
ms.openlocfilehash: 2fb7297310102134dfcacf0e5f0d907fbf3a3e0b
ms.sourcegitcommit: 7eadd92b1da5eb4eab7d516a5a768e7f7fc02d4c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/16/2021
ms.locfileid: "112230249"
---
# <a name="application-manifests"></a><span data-ttu-id="2e8c0-103">Манифесты приложений</span><span class="sxs-lookup"><span data-stu-id="2e8c0-103">Application Manifests</span></span>

<span data-ttu-id="2e8c0-104">Манифест приложения — это файл XML, который описывает и определяет общие и закрытые сборки одновременного выполнения, которые приложению следует подключить во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-104">An application manifest is an XML file that describes and identifies the shared and private side-by-side assemblies that an application should bind to at run time.</span></span> <span data-ttu-id="2e8c0-105">Это должны быть те же версии сборок, что и использованные для проверки приложения.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-105">These should be the same assembly versions that were used to test the application.</span></span> <span data-ttu-id="2e8c0-106">Манифесты приложения также могут описывать метаданные закрытых для приложения файлов.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-106">Application manifests may also describe metadata for files that are private to the application.</span></span>

<span data-ttu-id="2e8c0-107">Полный список схем XML см. в разделе [Схема файла манифеста](manifest-file-schema.md).</span><span class="sxs-lookup"><span data-stu-id="2e8c0-107">For a complete listing of the XML schema, see [Manifest File Schema](manifest-file-schema.md).</span></span>

<span data-ttu-id="2e8c0-108">Манифесты приложений имеют следующие элементы и атрибуты.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-108">Application manifests have the following elements and attributes.</span></span>

| <span data-ttu-id="2e8c0-109">Элемент</span><span class="sxs-lookup"><span data-stu-id="2e8c0-109">Element</span></span>                               | <span data-ttu-id="2e8c0-110">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="2e8c0-110">Attributes</span></span>                | <span data-ttu-id="2e8c0-111">Обязательно</span><span class="sxs-lookup"><span data-stu-id="2e8c0-111">Required</span></span> |
|---------------------------------------|---------------------------|----------|
| <span data-ttu-id="2e8c0-112">**сборок**</span><span class="sxs-lookup"><span data-stu-id="2e8c0-112">**assembly**</span></span>                          |                           | <span data-ttu-id="2e8c0-113">Да</span><span class="sxs-lookup"><span data-stu-id="2e8c0-113">Yes</span></span>      |
|                                       | <span data-ttu-id="2e8c0-114">**манифестверсион**</span><span class="sxs-lookup"><span data-stu-id="2e8c0-114">**manifestVersion**</span></span>       | <span data-ttu-id="2e8c0-115">Да</span><span class="sxs-lookup"><span data-stu-id="2e8c0-115">Yes</span></span>      |
| <span data-ttu-id="2e8c0-116">**не наследовать**</span><span class="sxs-lookup"><span data-stu-id="2e8c0-116">**noInherit**</span></span>                         |                           | <span data-ttu-id="2e8c0-117">Нет</span><span class="sxs-lookup"><span data-stu-id="2e8c0-117">No</span></span>       |
| <span data-ttu-id="2e8c0-118">**Неправильн**</span><span class="sxs-lookup"><span data-stu-id="2e8c0-118">**assemblyIdentity**</span></span>                  |                           | <span data-ttu-id="2e8c0-119">Да</span><span class="sxs-lookup"><span data-stu-id="2e8c0-119">Yes</span></span>      |
|                                       | <span data-ttu-id="2e8c0-120">**type**</span><span class="sxs-lookup"><span data-stu-id="2e8c0-120">**type**</span></span>                  | <span data-ttu-id="2e8c0-121">Да</span><span class="sxs-lookup"><span data-stu-id="2e8c0-121">Yes</span></span>      |
|                                       | <span data-ttu-id="2e8c0-122">**name**</span><span class="sxs-lookup"><span data-stu-id="2e8c0-122">**name**</span></span>                  | <span data-ttu-id="2e8c0-123">Да</span><span class="sxs-lookup"><span data-stu-id="2e8c0-123">Yes</span></span>      |
|                                       | <span data-ttu-id="2e8c0-124">**language**</span><span class="sxs-lookup"><span data-stu-id="2e8c0-124">**language**</span></span>              | <span data-ttu-id="2e8c0-125">Нет</span><span class="sxs-lookup"><span data-stu-id="2e8c0-125">No</span></span>       |
|                                       | <span data-ttu-id="2e8c0-126">**processorArchitecture**</span><span class="sxs-lookup"><span data-stu-id="2e8c0-126">**processorArchitecture**</span></span> | <span data-ttu-id="2e8c0-127">Нет</span><span class="sxs-lookup"><span data-stu-id="2e8c0-127">No</span></span>       |
|                                       | <span data-ttu-id="2e8c0-128">**version**</span><span class="sxs-lookup"><span data-stu-id="2e8c0-128">**version**</span></span>               | <span data-ttu-id="2e8c0-129">Да</span><span class="sxs-lookup"><span data-stu-id="2e8c0-129">Yes</span></span>      |
|                                       | <span data-ttu-id="2e8c0-130">**publicKeyToken**</span><span class="sxs-lookup"><span data-stu-id="2e8c0-130">**publicKeyToken**</span></span>        | <span data-ttu-id="2e8c0-131">Нет</span><span class="sxs-lookup"><span data-stu-id="2e8c0-131">No</span></span>       |
| <span data-ttu-id="2e8c0-132">**см**</span><span class="sxs-lookup"><span data-stu-id="2e8c0-132">**compatibility**</span></span>                     |                           | <span data-ttu-id="2e8c0-133">Нет</span><span class="sxs-lookup"><span data-stu-id="2e8c0-133">No</span></span>       |
| <span data-ttu-id="2e8c0-134">**приложение**</span><span class="sxs-lookup"><span data-stu-id="2e8c0-134">**application**</span></span>                       |                           | <span data-ttu-id="2e8c0-135">Нет</span><span class="sxs-lookup"><span data-stu-id="2e8c0-135">No</span></span>       |
| <span data-ttu-id="2e8c0-136">**суппортедос**</span><span class="sxs-lookup"><span data-stu-id="2e8c0-136">**supportedOS**</span></span>                       | <span data-ttu-id="2e8c0-137">**Id**</span><span class="sxs-lookup"><span data-stu-id="2e8c0-137">**Id**</span></span>                    | <span data-ttu-id="2e8c0-138">Нет</span><span class="sxs-lookup"><span data-stu-id="2e8c0-138">No</span></span>       |
| <span data-ttu-id="2e8c0-139">**maxversiontested укажите установленную**</span><span class="sxs-lookup"><span data-stu-id="2e8c0-139">**maxversiontested**</span></span>                  | <span data-ttu-id="2e8c0-140">**Id**</span><span class="sxs-lookup"><span data-stu-id="2e8c0-140">**Id**</span></span>                    | <span data-ttu-id="2e8c0-141">Нет</span><span class="sxs-lookup"><span data-stu-id="2e8c0-141">No</span></span>       |
| <span data-ttu-id="2e8c0-142">**зависимостей**</span><span class="sxs-lookup"><span data-stu-id="2e8c0-142">**dependency**</span></span>                        |                           | <span data-ttu-id="2e8c0-143">Нет</span><span class="sxs-lookup"><span data-stu-id="2e8c0-143">No</span></span>       |
| <span data-ttu-id="2e8c0-144">**dependentAssembly**</span><span class="sxs-lookup"><span data-stu-id="2e8c0-144">**dependentAssembly**</span></span>                 |                           | <span data-ttu-id="2e8c0-145">Нет</span><span class="sxs-lookup"><span data-stu-id="2e8c0-145">No</span></span>       |
| <span data-ttu-id="2e8c0-146">**file**</span><span class="sxs-lookup"><span data-stu-id="2e8c0-146">**file**</span></span>                              |                           | <span data-ttu-id="2e8c0-147">Нет</span><span class="sxs-lookup"><span data-stu-id="2e8c0-147">No</span></span>       |
|                                       | <span data-ttu-id="2e8c0-148">**name**</span><span class="sxs-lookup"><span data-stu-id="2e8c0-148">**name**</span></span>                  | <span data-ttu-id="2e8c0-149">Нет</span><span class="sxs-lookup"><span data-stu-id="2e8c0-149">No</span></span>       |
|                                       | <span data-ttu-id="2e8c0-150">**hashAlg**</span><span class="sxs-lookup"><span data-stu-id="2e8c0-150">**hashalg**</span></span>               | <span data-ttu-id="2e8c0-151">Нет</span><span class="sxs-lookup"><span data-stu-id="2e8c0-151">No</span></span>       |
|                                       | <span data-ttu-id="2e8c0-152">**hash**</span><span class="sxs-lookup"><span data-stu-id="2e8c0-152">**hash**</span></span>                  | <span data-ttu-id="2e8c0-153">Нет</span><span class="sxs-lookup"><span data-stu-id="2e8c0-153">No</span></span>       |
| <span data-ttu-id="2e8c0-154">**активекодепаже**</span><span class="sxs-lookup"><span data-stu-id="2e8c0-154">**activeCodePage**</span></span>                    |                           | <span data-ttu-id="2e8c0-155">Нет</span><span class="sxs-lookup"><span data-stu-id="2e8c0-155">No</span></span>       |
| <span data-ttu-id="2e8c0-156">**автоповышение**</span><span class="sxs-lookup"><span data-stu-id="2e8c0-156">**autoElevate**</span></span>                       |                           | <span data-ttu-id="2e8c0-157">Нет</span><span class="sxs-lookup"><span data-stu-id="2e8c0-157">No</span></span>       |
| <span data-ttu-id="2e8c0-158">**дисаблесеминг**</span><span class="sxs-lookup"><span data-stu-id="2e8c0-158">**disableTheming**</span></span>                    |                           | <span data-ttu-id="2e8c0-159">Нет</span><span class="sxs-lookup"><span data-stu-id="2e8c0-159">No</span></span>       |
| <span data-ttu-id="2e8c0-160">**дисаблевиндовфилтеринг**</span><span class="sxs-lookup"><span data-stu-id="2e8c0-160">**disableWindowFiltering**</span></span>            |                           | <span data-ttu-id="2e8c0-161">Нет</span><span class="sxs-lookup"><span data-stu-id="2e8c0-161">No</span></span>       |
| <span data-ttu-id="2e8c0-162">**дпиаваре**</span><span class="sxs-lookup"><span data-stu-id="2e8c0-162">**dpiAware**</span></span>                          |                           | <span data-ttu-id="2e8c0-163">Нет</span><span class="sxs-lookup"><span data-stu-id="2e8c0-163">No</span></span>       |
| <span data-ttu-id="2e8c0-164">**дпиаваренесс**</span><span class="sxs-lookup"><span data-stu-id="2e8c0-164">**dpiAwareness**</span></span>                      |                           | <span data-ttu-id="2e8c0-165">Нет</span><span class="sxs-lookup"><span data-stu-id="2e8c0-165">No</span></span>       |
| <span data-ttu-id="2e8c0-166">**гдискалинг**</span><span class="sxs-lookup"><span data-stu-id="2e8c0-166">**gdiScaling**</span></span>                        |                           | <span data-ttu-id="2e8c0-167">Нет</span><span class="sxs-lookup"><span data-stu-id="2e8c0-167">No</span></span>       |
| <span data-ttu-id="2e8c0-168">**хигхресолутионскроллингаваре**</span><span class="sxs-lookup"><span data-stu-id="2e8c0-168">**highResolutionScrollingAware**</span></span>      |                           | <span data-ttu-id="2e8c0-169">Нет</span><span class="sxs-lookup"><span data-stu-id="2e8c0-169">No</span></span>       |
| <span data-ttu-id="2e8c0-170">**лонгпасаваре**</span><span class="sxs-lookup"><span data-stu-id="2e8c0-170">**longPathAware**</span></span>                     |                           | <span data-ttu-id="2e8c0-171">Нет</span><span class="sxs-lookup"><span data-stu-id="2e8c0-171">No</span></span>       |
| <span data-ttu-id="2e8c0-172">**принтердриверисолатион**</span><span class="sxs-lookup"><span data-stu-id="2e8c0-172">**printerDriverIsolation**</span></span>            |                           | <span data-ttu-id="2e8c0-173">Нет</span><span class="sxs-lookup"><span data-stu-id="2e8c0-173">No</span></span>       |
| <span data-ttu-id="2e8c0-174">**ултрахигхресолутионскроллингаваре**</span><span class="sxs-lookup"><span data-stu-id="2e8c0-174">**ultraHighResolutionScrollingAware**</span></span> |                           | <span data-ttu-id="2e8c0-175">Нет</span><span class="sxs-lookup"><span data-stu-id="2e8c0-175">No</span></span>       |
| <span data-ttu-id="2e8c0-176">**msix**</span><span class="sxs-lookup"><span data-stu-id="2e8c0-176">**msix**</span></span>                              |                           | <span data-ttu-id="2e8c0-177">Нет</span><span class="sxs-lookup"><span data-stu-id="2e8c0-177">No</span></span>       |
| <span data-ttu-id="2e8c0-178">**хеаптипе**</span><span class="sxs-lookup"><span data-stu-id="2e8c0-178">**heapType**</span></span>                          |                           | <span data-ttu-id="2e8c0-179">Нет</span><span class="sxs-lookup"><span data-stu-id="2e8c0-179">No</span></span>       |

## <a name="file-location"></a><span data-ttu-id="2e8c0-180">Расположение файла</span><span class="sxs-lookup"><span data-stu-id="2e8c0-180">File Location</span></span>

<span data-ttu-id="2e8c0-181">Манифесты приложений должны быть добавлены в качестве ресурсов в EXE-файл или библиотеку DLL приложения.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-181">Application manifests should be included as a resource in the application's EXE file or DLL.</span></span>

<span data-ttu-id="2e8c0-182">Дополнительные сведения см. в разделе [Установка параллельных сборок](installing-side-by-side-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="2e8c0-182">For more information, see [Installing Side-by-side Assemblies](installing-side-by-side-assemblies.md).</span></span>

## <a name="file-name-syntax"></a><span data-ttu-id="2e8c0-183">Синтаксис имени файла</span><span class="sxs-lookup"><span data-stu-id="2e8c0-183">File Name Syntax</span></span>

<span data-ttu-id="2e8c0-184">Имя файла манифеста приложения — это имя исполняемого объекта приложения, за которым следует manifest.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-184">The name of an application manifest file is the name of the application's executable followed by .manifest.</span></span>

<span data-ttu-id="2e8c0-185">Например, манифест приложения, который ссылается на example.exe или example.dll, будет использовать следующий синтаксис имени файла.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-185">For example, an application manifest that refers to example.exe or example.dll would use the following file name syntax.</span></span> <span data-ttu-id="2e8c0-186">Если идентификатор ресурса равен 1, можно опустить поле <*идентификатор ресурса*>.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-186">You can omit the <*resource ID*> field if resource ID is 1.</span></span>

<span data-ttu-id="2e8c0-187">**example.exe. <*идентификатор ресурса*>. manifest**</span><span class="sxs-lookup"><span data-stu-id="2e8c0-187">**example.exe.<*resource ID*>.manifest**</span></span>

<span data-ttu-id="2e8c0-188">**example.dll. <*идентификатор ресурса*>. manifest**</span><span class="sxs-lookup"><span data-stu-id="2e8c0-188">**example.dll.<*resource ID*>.manifest**</span></span>

## <a name="elements"></a><span data-ttu-id="2e8c0-189">Элементы</span><span class="sxs-lookup"><span data-stu-id="2e8c0-189">Elements</span></span>

<span data-ttu-id="2e8c0-190">В именах элементов и атрибутов учитывается регистр.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-190">Names of elements and attributes are case-sensitive.</span></span> <span data-ttu-id="2e8c0-191">Значения элементов и атрибутов не учитывают регистр, за исключением значения атрибута Type.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-191">The values of elements and attributes are case-insensitive, except for the value of the type attribute.</span></span>

<span id="assembly"></span><span id="ASSEMBLY"></span>

### <a name="assembly"></a><span data-ttu-id="2e8c0-192">сборка</span><span class="sxs-lookup"><span data-stu-id="2e8c0-192">assembly</span></span>

<span data-ttu-id="2e8c0-193">Элемент контейнера.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-193">A container element.</span></span> <span data-ttu-id="2e8c0-194">Его первым подэлементом должен быть элемент **NoInherit** или **assemblyIdentity** .</span><span class="sxs-lookup"><span data-stu-id="2e8c0-194">Its first subelement must be a **noInherit** or **assemblyIdentity** element.</span></span> <span data-ttu-id="2e8c0-195">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-195">Required.</span></span>

<span data-ttu-id="2e8c0-196">Элемент **Assembly** должен находиться в пространстве имен urn: schemas-microsoft-com: ASM. v1.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-196">The **assembly** element must be in the namespace "urn:schemas-microsoft-com:asm.v1".</span></span> <span data-ttu-id="2e8c0-197">Дочерние элементы сборки также должны находиться в этом пространстве имен путем наследования или добавления тегов.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-197">Child elements of the assembly must also be in this namespace, by inheritance or by tagging.</span></span>

<span data-ttu-id="2e8c0-198">Элемент **Assembly** имеет следующие атрибуты.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-198">The **assembly** element has the following attributes.</span></span>



| <span data-ttu-id="2e8c0-199">attribute</span><span class="sxs-lookup"><span data-stu-id="2e8c0-199">Attribute</span></span>           | <span data-ttu-id="2e8c0-200">Описание</span><span class="sxs-lookup"><span data-stu-id="2e8c0-200">Description</span></span>                                           |
|---------------------|-------------------------------------------------------|
| <span data-ttu-id="2e8c0-201">**манифестверсион**</span><span class="sxs-lookup"><span data-stu-id="2e8c0-201">**manifestVersion**</span></span> | <span data-ttu-id="2e8c0-202">Атрибут **манифестверсион** должен иметь значение 1,0.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-202">The **manifestVersion** attribute must be set to 1.0.</span></span> |


<span id="noInherit"></span><span id="noinherit"></span><span id="NOINHERIT"></span>

### <a name="noinherit"></a><span data-ttu-id="2e8c0-203">не наследовать</span><span class="sxs-lookup"><span data-stu-id="2e8c0-203">noInherit</span></span>

<span data-ttu-id="2e8c0-204">Включите этот элемент в манифест приложения, чтобы задать [контексты активации](activation-contexts.md) , созданные из манифеста, с флагом "без наследования".</span><span class="sxs-lookup"><span data-stu-id="2e8c0-204">Include this element in an application manifest to set the [activation contexts](activation-contexts.md) generated from the manifest with the "no inherit" flag.</span></span> <span data-ttu-id="2e8c0-205">Если этот флаг не установлен в контексте активации, а контекст активации активен, он наследуется новыми потоками в том же процессе, в окнах, в процедурах Windows и [асинхронных вызовах процедур](/windows/desktop/Sync/asynchronous-procedure-calls).</span><span class="sxs-lookup"><span data-stu-id="2e8c0-205">When this flag is not set in an activation context, and the activation context is active, it is inherited by new threads in the same process, windows, window procedures, and [Asynchronous Procedure Calls](/windows/desktop/Sync/asynchronous-procedure-calls).</span></span> <span data-ttu-id="2e8c0-206">Установка этого флага предотвращает наследование активного контекста новым объектом.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-206">Setting this flag prevents the new object from inheriting the active context.</span></span>

<span data-ttu-id="2e8c0-207">Элемент **NoInherit** является необязательным и обычно опускается.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-207">The **noInherit** element is optional and typically omitted.</span></span> <span data-ttu-id="2e8c0-208">Большинство сборок работает неправильно с помощью контекста активации без наследования, так как сборка должна быть специально разработана для управления распространением собственного контекста активации.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-208">Most assemblies do not work correctly using a no-inherit activation context because the assembly must be explicitly designed to manage the propagation of their own activation context.</span></span> <span data-ttu-id="2e8c0-209">Использование элемента **NoInherit** требует, чтобы все зависимые сборки, на которые ссылается манифест приложения, имели элемент **NoInherit** в [манифесте сборки](assembly-manifests.md).</span><span class="sxs-lookup"><span data-stu-id="2e8c0-209">The use of the **noInherit** element requires that any dependent assemblies referenced by the application manifest have a **noInherit** element in their [assembly manifest](assembly-manifests.md).</span></span>

<span data-ttu-id="2e8c0-210">Если в манифесте используется параметр **NoInherit** , он должен быть первым подэлементом элемента **Assembly** .</span><span class="sxs-lookup"><span data-stu-id="2e8c0-210">If **noInherit** is used in a manifest, it must be the first subelement of the **assembly** element.</span></span> <span data-ttu-id="2e8c0-211">Элемент **assemblyIdentity** должен идти сразу после элемента **NoInherit** .</span><span class="sxs-lookup"><span data-stu-id="2e8c0-211">The **assemblyIdentity** element should come immediately after the **noInherit** element.</span></span> <span data-ttu-id="2e8c0-212">Если параметр **NoInherit** не используется, то **assemblyIdentity** должен быть первым подэлементом элемента **Assembly** .</span><span class="sxs-lookup"><span data-stu-id="2e8c0-212">If **noInherit** is not used, **assemblyIdentity** must be the first subelement of the **assembly** element.</span></span> <span data-ttu-id="2e8c0-213">У элемента **NoInherit** нет дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-213">The **noInherit** element has no child elements.</span></span> <span data-ttu-id="2e8c0-214">Он не является допустимым элементом в [манифестах сборки](assembly-manifests.md).</span><span class="sxs-lookup"><span data-stu-id="2e8c0-214">It is not a valid element in [assembly manifests](assembly-manifests.md).</span></span>

<span id="assemblyIdentity"></span><span id="assemblyidentity"></span><span id="ASSEMBLYIDENTITY"></span>

### <a name="assemblyidentity"></a><span data-ttu-id="2e8c0-215">assemblyIdentity</span><span class="sxs-lookup"><span data-stu-id="2e8c0-215">assemblyIdentity</span></span>

<span data-ttu-id="2e8c0-216">Как первый подэлемент элемента **Assembly** , **assemblyIdentity** описывает и уникально идентифицирует приложение, владеющее этим манифестом приложения.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-216">As the first subelement of an **assembly** element, **assemblyIdentity** describes and uniquely identifies the application owning this application manifest.</span></span> <span data-ttu-id="2e8c0-217">Как первый подэлемент элемента **dependentAssembly** , **assemblyIdentity** описывает параллельную сборку, необходимую для приложения.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-217">As the first subelement of a **dependentAssembly** element, **assemblyIdentity** describes a side-by-side assembly required by the application.</span></span> <span data-ttu-id="2e8c0-218">Обратите внимание, что каждая сборка, указанная в манифесте приложения, требует наличия **assemblyIdentity** , точно совпадающего с **assemblyIdentity** в манифесте сборки, на которую указывает ссылка.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-218">Note that every assembly referenced in the application manifest requires an **assemblyIdentity** that exactly matches the **assemblyIdentity** in the referenced assembly's own assembly manifest.</span></span>

<span data-ttu-id="2e8c0-219">Элемент **assemblyIdentity** имеет следующие атрибуты.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-219">The **assemblyIdentity** element has the following attributes.</span></span> <span data-ttu-id="2e8c0-220">У него нет вложенных элементов.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-220">It has no subelements.</span></span>

| <span data-ttu-id="2e8c0-221">attribute</span><span class="sxs-lookup"><span data-stu-id="2e8c0-221">Attribute</span></span>                 | <span data-ttu-id="2e8c0-222">Описание</span><span class="sxs-lookup"><span data-stu-id="2e8c0-222">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e8c0-223">**type**</span><span class="sxs-lookup"><span data-stu-id="2e8c0-223">**type**</span></span>                  | <span data-ttu-id="2e8c0-224">Указывает тип приложения или сборки.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-224">Specifies the application or assembly type.</span></span> <span data-ttu-id="2e8c0-225">Значение должно быть в виде Win32, а все — в нижнем регистре.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-225">The value must be Win32 and all in lower case.</span></span> <span data-ttu-id="2e8c0-226">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-226">Required.</span></span>                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="2e8c0-227">**name**</span><span class="sxs-lookup"><span data-stu-id="2e8c0-227">**name**</span></span>                  | <span data-ttu-id="2e8c0-228">Уникально именует приложение или сборку.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-228">Uniquely names the application or assembly.</span></span> <span data-ttu-id="2e8c0-229">Используйте следующий формат для имени: Organization.Division.Name.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-229">Use the following format for the name: Organization.Division.Name.</span></span> <span data-ttu-id="2e8c0-230">Например, Microsoft. Windows. Мисамплеапп.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-230">For example Microsoft.Windows.mysampleApp.</span></span> <span data-ttu-id="2e8c0-231">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-231">Required.</span></span>                                                                                                                                                                                                                                                               |
| <span data-ttu-id="2e8c0-232">**language**</span><span class="sxs-lookup"><span data-stu-id="2e8c0-232">**language**</span></span>              | <span data-ttu-id="2e8c0-233">Определяет язык приложения или сборки.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-233">Identifies the language of the application or assembly.</span></span> <span data-ttu-id="2e8c0-234">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-234">Optional.</span></span> <span data-ttu-id="2e8c0-235">Если приложение или сборка зависит от языка, укажите код языка DHTML.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-235">If the application or assembly is language-specific, specify the DHTML language code.</span></span> <span data-ttu-id="2e8c0-236">На **теге assemblyIdentity** приложения, предназначенного для международных использования (не зависит от языка), не указывайте атрибут Language.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-236">In the **assemblyIdentity** of an application intended for worldwide use (language neutral) omit the language attribute.</span></span><br/> <span data-ttu-id="2e8c0-237">В **теге assemblyIdentity** сборки, предназначенной для международных использования (нейтральный к языку), задайте для параметра Language значение " \* ".</span><span class="sxs-lookup"><span data-stu-id="2e8c0-237">In an **assemblyIdentity** of an assembly intended for worldwide use (language neutral) set the value of language to "\*".</span></span><br/> |
| <span data-ttu-id="2e8c0-238">**processorArchitecture**</span><span class="sxs-lookup"><span data-stu-id="2e8c0-238">**processorArchitecture**</span></span> | <span data-ttu-id="2e8c0-239">Указывает процессор.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-239">Specifies the processor.</span></span> <span data-ttu-id="2e8c0-240">Допустимые значения: `x86`, `amd64`, `arm` и `arm64`.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-240">Valid values include `x86`, `amd64`, `arm` and `arm64`.</span></span> <span data-ttu-id="2e8c0-241">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-241">Optional.</span></span>                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="2e8c0-242">**version**</span><span class="sxs-lookup"><span data-stu-id="2e8c0-242">**version**</span></span>               | <span data-ttu-id="2e8c0-243">Указывает версию приложения или сборки.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-243">Specifies the application or assembly version.</span></span> <span data-ttu-id="2e8c0-244">Используйте формат версии из четырех частей: оближешь. nnnnn. ууо. ппппп.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-244">Use the four-part version format: mmmmm.nnnnn.ooooo.ppppp.</span></span> <span data-ttu-id="2e8c0-245">Каждая из частей, разделенных точками, может быть 0-65535 включительно.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-245">Each of the parts separated by periods can be 0-65535 inclusive.</span></span> <span data-ttu-id="2e8c0-246">Дополнительные сведения см. в разделе [версии сборки](assembly-versions.md).</span><span class="sxs-lookup"><span data-stu-id="2e8c0-246">For more information, see [Assembly Versions](assembly-versions.md).</span></span> <span data-ttu-id="2e8c0-247">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-247">Required.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="2e8c0-248">**publicKeyToken**</span><span class="sxs-lookup"><span data-stu-id="2e8c0-248">**publicKeyToken**</span></span>        | <span data-ttu-id="2e8c0-249">16-символьная шестнадцатеричная строка, представляющая последние 8 байт хэша SHA-1 открытого ключа, для которого подписано приложение или сборка.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-249">A 16-character hexadecimal string representing the last 8 bytes of the SHA-1 hash of the public key under which the application or assembly is signed.</span></span> <span data-ttu-id="2e8c0-250">Открытый ключ, используемый для подписи каталога, должен иметь длину 2048 бит или более.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-250">The public key used to sign the catalog must be 2048 bits or greater.</span></span> <span data-ttu-id="2e8c0-251">Требуется для всех общих параллельных сборок.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-251">Required for all shared side-by-side assemblies.</span></span>                                                                                                                                                     |

<span id="compatibility"></span><span id="COMPATIBILITY"></span>

### <a name="compatibility"></a><span data-ttu-id="2e8c0-252">совместимость</span><span class="sxs-lookup"><span data-stu-id="2e8c0-252">compatibility</span></span>

<span data-ttu-id="2e8c0-253">Содержит по крайней мере одно **приложение**.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-253">Contains at least one **application**.</span></span> <span data-ttu-id="2e8c0-254">У него нет атрибутов.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-254">It has no attributes.</span></span> <span data-ttu-id="2e8c0-255">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-255">Optional.</span></span> <span data-ttu-id="2e8c0-256">Манифесты приложений без элемента Compatibility по умолчанию имеют совместимость с Windows Vista в Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-256">Application manifests without a compatibility element default to Windows Vista compatibility on Windows 7.</span></span>

<span id="application"></span><span id="APPLICATION"></span>

### <a name="application"></a><span data-ttu-id="2e8c0-257">application</span><span class="sxs-lookup"><span data-stu-id="2e8c0-257">application</span></span>

<span data-ttu-id="2e8c0-258">Содержит по крайней мере один элемент **суппортедос** .</span><span class="sxs-lookup"><span data-stu-id="2e8c0-258">Contains at least one **supportedOS** element.</span></span> <span data-ttu-id="2e8c0-259">Начиная с Windows 10 версии 1903, она также может содержать один необязательный элемент **maxversiontested укажите установленную** .</span><span class="sxs-lookup"><span data-stu-id="2e8c0-259">Starting in Windows 10, version 1903, it can also contain one optional **maxversiontested** element.</span></span> <span data-ttu-id="2e8c0-260">У него нет атрибутов.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-260">It has no attributes.</span></span> <span data-ttu-id="2e8c0-261">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-261">Optional.</span></span>

<span id="supportedOS"></span><span id="supportedos"></span><span id="SUPPORTEDOS"></span>

### <a name="supportedos"></a><span data-ttu-id="2e8c0-262">суппортедос</span><span class="sxs-lookup"><span data-stu-id="2e8c0-262">supportedOS</span></span>

<span data-ttu-id="2e8c0-263">Элемент **суппортедос** имеет следующий атрибут.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-263">The **supportedOS** element has the following attribute.</span></span> <span data-ttu-id="2e8c0-264">У него нет вложенных элементов.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-264">It has no subelements.</span></span>

| <span data-ttu-id="2e8c0-265">attribute</span><span class="sxs-lookup"><span data-stu-id="2e8c0-265">Attribute</span></span> | <span data-ttu-id="2e8c0-266">Описание</span><span class="sxs-lookup"><span data-stu-id="2e8c0-266">Description</span></span>   |
|-----------|-----------------------|
| <span data-ttu-id="2e8c0-267">**Id**</span><span class="sxs-lookup"><span data-stu-id="2e8c0-267">**Id**</span></span>    | <span data-ttu-id="2e8c0-268">Задайте для атрибута ID значение **{e2011457-1546-43c5-a5fe-008deee3d3f0}** , чтобы запустить приложение с помощью функции Vista.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-268">Set the Id attribute to **{e2011457-1546-43c5-a5fe-008deee3d3f0}** to run the application using Vista functionality.</span></span> <span data-ttu-id="2e8c0-269">Это может позволить приложению, разработанному для Windows Vista, работать в более поздней версии операционной системы.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-269">This can enable an application designed for Windows Vista to run on a later operating system.</span></span> <br/> <span data-ttu-id="2e8c0-270">Задайте для атрибута ID значение **{35138b9a-5d96-4fbd-8e2d-a2440225f93a}** , чтобы запустить приложение с помощью функции Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-270">Set the Id attribute to **{35138b9a-5d96-4fbd-8e2d-a2440225f93a}** to run the application using Windows 7 functionality.</span></span><br/> <span data-ttu-id="2e8c0-271">Для приложений, поддерживающих функции Windows Vista, Windows 7 и Windows 8, не требуются отдельные манифесты.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-271">Applications that support Windows Vista, Windows 7, and Windows 8 functionality do not require separate manifests.</span></span> <span data-ttu-id="2e8c0-272">В этом случае добавьте идентификаторы GUID для всех операционных систем Windows.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-272">In this case, add the GUIDs for all the Windows operating systems.</span></span><br/> <span data-ttu-id="2e8c0-273">Сведения о поведении атрибута **ID** в Windows см. в статье [совместимость Windows 8 и Windows Server 2012 Cookbook](https://www.microsoft.com/download/details.aspx?id=27416).</span><span class="sxs-lookup"><span data-stu-id="2e8c0-273">For info about the **Id** attribute behavior in Windows, see the [Windows 8 and Windows Server 2012 Compatibility Cookbook](https://www.microsoft.com/download/details.aspx?id=27416).</span></span><br/> <span data-ttu-id="2e8c0-274">Следующие идентификаторы GUID соответствуют указанным операционным системам:</span><span class="sxs-lookup"><span data-stu-id="2e8c0-274">The following GUIDs correspond with the indicated operating systems:</span></span><br/> <span data-ttu-id="2e8c0-275">**{8e0f7a12-bfb3-4fe8-b9a5-48fd50a15a9a}** — > Windows 10, windows Server 2016 и windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="2e8c0-275">**{8e0f7a12-bfb3-4fe8-b9a5-48fd50a15a9a}** -> Windows 10, Windows Server 2016 and Windows Server 2019</span></span><br/> <span data-ttu-id="2e8c0-276">**{1f676c76-80e1-4239-95bb-83d0f6d0da78}** — > Windows 8.1 и Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="2e8c0-276">**{1f676c76-80e1-4239-95bb-83d0f6d0da78}** -> Windows 8.1 and Windows Server 2012 R2</span></span><br/> <span data-ttu-id="2e8c0-277">**{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}** — > Windows 8 и windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2e8c0-277">**{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}** -> Windows 8 and Windows Server 2012</span></span><br/> <span data-ttu-id="2e8c0-278">**{35138b9a-5d96-4fbd-8e2d-a2440225f93a}** — > Windows 7 и windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2e8c0-278">**{35138b9a-5d96-4fbd-8e2d-a2440225f93a}** -> Windows 7 and Windows Server 2008 R2</span></span><br/> <span data-ttu-id="2e8c0-279">**{e2011457-1546-43c5-a5fe-008deee3d3f0}** — > Windows Vista и windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2e8c0-279">**{e2011457-1546-43c5-a5fe-008deee3d3f0}** -> Windows Vista and Windows Server 2008</span></span><br/> <span data-ttu-id="2e8c0-280">Вы можете протестировать это в Windows 7 или Windows 8. x, запустив монитор ресурсов (ресмон), перейдя на вкладку ЦП, щелкнув правой кнопкой мыши метки столбцов, выбрать столбец и проверить "контекст операционной системы".</span><span class="sxs-lookup"><span data-stu-id="2e8c0-280">You can test this on Windows 7 or Windows 8.x by running Resource Monitor (resmon), going to the CPU tab, right-clicking on the column labels, "Select Column...", and check "Operating System Context".</span></span> <span data-ttu-id="2e8c0-281">В Windows 8. x можно также найти этот столбец, доступный в диспетчере задач (панели Диспетчер задач).</span><span class="sxs-lookup"><span data-stu-id="2e8c0-281">On Windows 8.x, you can also find this column available in the Task Manager (taskmgr).</span></span> <span data-ttu-id="2e8c0-282">Содержимое столбца показывает наибольшее найденное значение или "Windows Vista" в качестве значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-282">The content of the column shows the highest value found or "Windows Vista" as the default.</span></span> <br/> |

<span id="maxVersionTested"></span><span id="maxversiontested"></span><span id="MAXVERSIONTESTED"></span>

### <a name="maxversiontested"></a><span data-ttu-id="2e8c0-283">maxversiontested укажите установленную</span><span class="sxs-lookup"><span data-stu-id="2e8c0-283">maxversiontested</span></span>

<span data-ttu-id="2e8c0-284">Элемент **maxversiontested укажите установленную** указывает версии Windows, с которыми проверялось приложение, начиная с минимальной версии ОС, поддерживаемой приложением до максимальной версии.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-284">The **maxversiontested** element specifies the versions of Windows that the application was tested against starting with the minimum OS version the application supports up to the maximum version.</span></span> <span data-ttu-id="2e8c0-285">Полный набор версий можно найти [здесь](https://developer.microsoft.com/windows/downloads/sdk-archive/).</span><span class="sxs-lookup"><span data-stu-id="2e8c0-285">The complete set of versions can be found [here](https://developer.microsoft.com/windows/downloads/sdk-archive/).</span></span> <span data-ttu-id="2e8c0-286">Он предназначен для использования в приложениях для настольных систем, использующих [острова XAML](/windows/apps/desktop/modernize/xaml-islands) и не развернутых в пакете MSIX.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-286">This is intended to be used by desktop applications that use [XAML Islands](/windows/apps/desktop/modernize/xaml-islands) and that are not deployed in an MSIX package.</span></span> <span data-ttu-id="2e8c0-287">Этот элемент поддерживается в Windows 10, версии 1903 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-287">This element is supported in Windows 10, version 1903, and later versions.</span></span>

<span data-ttu-id="2e8c0-288">Элемент **maxversiontested укажите установленную** имеет следующий атрибут.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-288">The **maxversiontested** element has the following attribute.</span></span> <span data-ttu-id="2e8c0-289">У него нет вложенных элементов.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-289">It has no subelements.</span></span>

| <span data-ttu-id="2e8c0-290">attribute</span><span class="sxs-lookup"><span data-stu-id="2e8c0-290">Attribute</span></span> | <span data-ttu-id="2e8c0-291">Описание</span><span class="sxs-lookup"><span data-stu-id="2e8c0-291">Description</span></span>    |
|-----------|----------------|
| <span data-ttu-id="2e8c0-292">**Id**</span><span class="sxs-lookup"><span data-stu-id="2e8c0-292">**Id**</span></span>    | <span data-ttu-id="2e8c0-293">Задайте для атрибута ID строку версии из 4 частей, которая указывает максимальную версию Windows, с которой было протестировано приложение.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-293">Set the Id attribute to a 4-part version string that specifies the maximum version of Windows that the application was tested against.</span></span> <span data-ttu-id="2e8c0-294">Например, "10.0.18226.0".</span><span class="sxs-lookup"><span data-stu-id="2e8c0-294">For example, "10.0.18226.0".</span></span> |

<span id="dependency"></span><span id="DEPENDENCY"></span>

### <a name="dependency"></a><span data-ttu-id="2e8c0-295">dependency</span><span class="sxs-lookup"><span data-stu-id="2e8c0-295">dependency</span></span>

<span data-ttu-id="2e8c0-296">Содержит по меньшей мере один **dependentAssembly**.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-296">Contains at least one **dependentAssembly**.</span></span> <span data-ttu-id="2e8c0-297">У него нет атрибутов.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-297">It has no attributes.</span></span> <span data-ttu-id="2e8c0-298">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-298">Optional.</span></span>

<span id="dependentAssembly"></span><span id="dependentassembly"></span><span id="DEPENDENTASSEMBLY"></span>

### <a name="dependentassembly"></a><span data-ttu-id="2e8c0-299">dependentAssembly</span><span class="sxs-lookup"><span data-stu-id="2e8c0-299">dependentAssembly</span></span>

<span data-ttu-id="2e8c0-300">Первый подэлемент **dependentAssembly** должен быть элементом **assemblyIdentity** , описывающим параллельную сборку, необходимую для приложения.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-300">The first subelement of **dependentAssembly** must be an **assemblyIdentity** element that describes a side-by-side assembly required by the application.</span></span> <span data-ttu-id="2e8c0-301">Каждое **dependentAssembly** должно находиться внутри только одной **зависимости**.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-301">Every **dependentAssembly** must be inside exactly one **dependency**.</span></span> <span data-ttu-id="2e8c0-302">У него нет атрибутов.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-302">It has no attributes.</span></span>

<span id="file"></span><span id="FILE"></span>

### <a name="file"></a><span data-ttu-id="2e8c0-303">файл</span><span class="sxs-lookup"><span data-stu-id="2e8c0-303">file</span></span>

<span data-ttu-id="2e8c0-304">Указывает файлы, являющиеся частными для приложения.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-304">Specifies files that are private to the application.</span></span> <span data-ttu-id="2e8c0-305">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-305">Optional.</span></span>

<span data-ttu-id="2e8c0-306">Элемент **File** содержит атрибуты, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-306">The **file** element has the attributes shown in the following table.</span></span>



| <span data-ttu-id="2e8c0-307">attribute</span><span class="sxs-lookup"><span data-stu-id="2e8c0-307">Attribute</span></span>   | <span data-ttu-id="2e8c0-308">Описание</span><span class="sxs-lookup"><span data-stu-id="2e8c0-308">Description</span></span>                                                                                             |
|-------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e8c0-309">**name**</span><span class="sxs-lookup"><span data-stu-id="2e8c0-309">**name**</span></span>    | <span data-ttu-id="2e8c0-310">Имя файла.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-310">Name of the file.</span></span> <span data-ttu-id="2e8c0-311">Например, Comctl32.dll.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-311">For example, Comctl32.dll.</span></span>                                                            |
| <span data-ttu-id="2e8c0-312">**hashAlg**</span><span class="sxs-lookup"><span data-stu-id="2e8c0-312">**hashalg**</span></span> | <span data-ttu-id="2e8c0-313">Алгоритм, используемый для создания хэша файла.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-313">Algorithm used to create a hash of the file.</span></span> <span data-ttu-id="2e8c0-314">Это значение должно быть SHA1.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-314">This value should be SHA1.</span></span>                                 |
| <span data-ttu-id="2e8c0-315">**hash**</span><span class="sxs-lookup"><span data-stu-id="2e8c0-315">**hash**</span></span>    | <span data-ttu-id="2e8c0-316">Хэш файла, на который ссылается имя.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-316">A hash of the file referred to by name.</span></span> <span data-ttu-id="2e8c0-317">Шестнадцатеричная строка длины в зависимости от хэш-алгоритма.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-317">A hexadecimal string of length depending on the hash algorithm.</span></span> |

<span id="activeCodePage"></span><span id="activecodepage"></span><span id="ACTIVECODEPAGE"></span>

### <a name="activecodepage"></a><span data-ttu-id="2e8c0-318">активекодепаже</span><span class="sxs-lookup"><span data-stu-id="2e8c0-318">activeCodePage</span></span>

<span data-ttu-id="2e8c0-319">Заставить процесс использовать UTF-8 в качестве кодовой страницы процесса.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-319">Force a process to use UTF-8 as the process code page.</span></span>

<span data-ttu-id="2e8c0-320">**активекодепаже** был добавлен в Windows версии 1903 (обновление 2019 мая).</span><span class="sxs-lookup"><span data-stu-id="2e8c0-320">**activeCodePage** was added in Windows Version 1903 (May 2019 Update).</span></span> <span data-ttu-id="2e8c0-321">Вы можете объявить это свойство и целевой объект или выполнить его в более ранних сборках Windows, но необходимо как обычно выполнять обнаружение и преобразование кодовых страниц прежних версий.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-321">You can declare this property and target/run on earlier Windows builds, but you must handle legacy code page detection and conversion as usual.</span></span> <span data-ttu-id="2e8c0-322">Дополнительные сведения см. [в разделе Использование кодовой страницы UTF-8](/windows/uwp/design/globalizing/use-utf8-code-page) .</span><span class="sxs-lookup"><span data-stu-id="2e8c0-322">See [Use the UTF-8 code page](/windows/uwp/design/globalizing/use-utf8-code-page) for details.</span></span>

<span data-ttu-id="2e8c0-323">Этот элемент не содержит атрибуты.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-323">This element has no attributes.</span></span> <span data-ttu-id="2e8c0-324">**UTF-8** является допустимым значением для элемента **активекодепаже** .</span><span class="sxs-lookup"><span data-stu-id="2e8c0-324">**UTF-8** is only valid value for **activeCodePage** element.</span></span>

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2019/WindowsSettings"> 
      <activeCodePage>UTF-8</activeCodePage> 
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="autoElevate"></span><span id="autoelevate"></span><span id="AUTOELEVATE"></span>

### <a name="autoelevate"></a><span data-ttu-id="2e8c0-325">автоповышение</span><span class="sxs-lookup"><span data-stu-id="2e8c0-325">autoElevate</span></span>

<span data-ttu-id="2e8c0-326">Указывает, включен ли автоматический повышенный уровень прав.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-326">Specifies whether auto elevate is enabled.</span></span> <span data-ttu-id="2e8c0-327">**Значение true** указывает, что он включен.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-327">**TRUE** indicates that it is enabled.</span></span> <span data-ttu-id="2e8c0-328">У него нет атрибутов.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-328">It has no attributes.</span></span>

<span id="disableTheming"></span><span id="disabletheming"></span><span id="DISABLETHEMING"></span>

### <a name="disabletheming"></a><span data-ttu-id="2e8c0-329">дисаблесеминг</span><span class="sxs-lookup"><span data-stu-id="2e8c0-329">disableTheming</span></span>

<span data-ttu-id="2e8c0-330">Указывает, отключено ли предоставление элементов пользовательского интерфейса для темы.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-330">Specifies whether giving UI elements a theme is disabled.</span></span> <span data-ttu-id="2e8c0-331">**Значение true** указывает, что отключено.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-331">**TRUE** indicates disabled.</span></span> <span data-ttu-id="2e8c0-332">У него нет атрибутов.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-332">It has no attributes.</span></span>

<span id="disableWindowFiltering"></span><span id="disablewindowfiltering"></span><span id="DISABLEWINDOWFILTERING"></span>

### <a name="disablewindowfiltering"></a><span data-ttu-id="2e8c0-333">дисаблевиндовфилтеринг</span><span class="sxs-lookup"><span data-stu-id="2e8c0-333">disableWindowFiltering</span></span>

<span data-ttu-id="2e8c0-334">Указывает, следует ли отключить фильтрацию окон.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-334">Specifies whether to disable window filtering.</span></span> <span data-ttu-id="2e8c0-335">**True** — отключить фильтрацию окон, чтобы можно было перечислить иммерсивное окно с рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-335">**TRUE** disables window filtering so you can enumerate immersive windows from the desktop.</span></span> <span data-ttu-id="2e8c0-336">**дисаблевиндовфилтеринг** был добавлен в Windows 8 и не имеет атрибутов.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-336">**disableWindowFiltering** was added in Windows 8 and has no attributes.</span></span>

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2011/WindowsSettings">
      <disableWindowFiltering>true</disableWindowFiltering>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="dpiAware"></span><span id="dpiaware"></span><span id="DPIAWARE"></span>

### <a name="dpiaware"></a><span data-ttu-id="2e8c0-337">дпиаваре</span><span class="sxs-lookup"><span data-stu-id="2e8c0-337">dpiAware</span></span>

<span data-ttu-id="2e8c0-338">Указывает, учитывается ли текущий процесс в точках на дюйм (DPI).</span><span class="sxs-lookup"><span data-stu-id="2e8c0-338">Specifies whether the current process is dots per inch (dpi) aware.</span></span>

<span data-ttu-id="2e8c0-339">**Windows 10, версия 1607:** Элемент **дпиаваре** игнорируется, если имеется элемент **дпиаваренесс** .</span><span class="sxs-lookup"><span data-stu-id="2e8c0-339">**Windows 10, version 1607:** The **dpiAware** element is ignored if the **dpiAwareness** element is present.</span></span> <span data-ttu-id="2e8c0-340">Можно включить оба элемента в манифест, если вы хотите указать другое поведение для Windows 10 версии 1607, чем для более ранней версии операционной системы.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-340">You can include both elements in a manifest if you want to specify a different behavior for Windows 10, version 1607 than for an earlier version of the operating system.</span></span>

<span data-ttu-id="2e8c0-341">В следующей таблице описывается поведение, получаемое в зависимости от наличия элемента **дпиаваре** и содержащегося в нем текста.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-341">The following table describes the behavior that results based upon the presence of the **dpiAware** element and the text that it contains.</span></span> <span data-ttu-id="2e8c0-342">В тексте элемента не учитывается регистр.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-342">The text within the element is not case-sensitive.</span></span>

| <span data-ttu-id="2e8c0-343">Состояние элемента **дпиаваре**</span><span class="sxs-lookup"><span data-stu-id="2e8c0-343">State of the **dpiAware** element</span></span> | <span data-ttu-id="2e8c0-344">Описание</span><span class="sxs-lookup"><span data-stu-id="2e8c0-344">Description</span></span>     |
|-----------------------------------|---------|
| <span data-ttu-id="2e8c0-345">Absent</span><span class="sxs-lookup"><span data-stu-id="2e8c0-345">Absent</span></span>                            | <span data-ttu-id="2e8c0-346">По умолчанию текущий процесс не знает dpi.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-346">The current process is dpi unaware by default.</span></span> <span data-ttu-id="2e8c0-347">Этот параметр можно изменить программным путем, вызвав функцию [**сетпроцессдпиаваренесс**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) или [**сетпроцессдпиаваре**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) .</span><span class="sxs-lookup"><span data-stu-id="2e8c0-347">You can programmatically change this setting by calling the [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) or [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) function.</span></span>                                                                                                                                                            |
| <span data-ttu-id="2e8c0-348">Содержит значение "true"</span><span class="sxs-lookup"><span data-stu-id="2e8c0-348">Contains "true"</span></span>                   | <span data-ttu-id="2e8c0-349">Текущий процесс учитывает dpi системы.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-349">The current process is system dpi aware.</span></span>                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="2e8c0-350">Содержит значение "false"</span><span class="sxs-lookup"><span data-stu-id="2e8c0-350">Contains "false"</span></span>                  | <span data-ttu-id="2e8c0-351">Windows **Vista, Windows 7 и Windows 8:** Поведение аналогично поведению, если **дпиаваре** отсутствует.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-351">**Windows Vista, Windows 7 and Windows 8:** The behavior is the same as when the **dpiAware** is absent.</span></span><br/> <span data-ttu-id="2e8c0-352">**Windows 8.1 и Windows 10:** Текущий процесс не знает dpi, и программное изменение этого параметра невозможно выполнить, вызвав функцию [**сетпроцессдпиаваренесс**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) или [**сетпроцессдпиаваре**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) .</span><span class="sxs-lookup"><span data-stu-id="2e8c0-352">**Windows 8.1 and Windows 10:** The current process is dpi unaware, and you cannot programmatically change this setting by calling the [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) or [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) function.</span></span><br/> |
| <span data-ttu-id="2e8c0-353">Содержит "true/PM"</span><span class="sxs-lookup"><span data-stu-id="2e8c0-353">Contains "true/pm"</span></span>                | <span data-ttu-id="2e8c0-354">Windows **Vista, Windows 7 и Windows 8:** Текущий процесс учитывает dpi системы.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-354">**Windows Vista, Windows 7 and Windows 8:** The current process is system dpi aware.</span></span><br/> <span data-ttu-id="2e8c0-355">**Windows 8.1 и Windows 10:** Текущий процесс учитывает dpi для каждого монитора.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-355">**Windows 8.1 and Windows 10:** The current process is per-monitor dpi aware.</span></span><br/>                                                                                                                                                                                                          |
| <span data-ttu-id="2e8c0-356">Содержит "на монитор"</span><span class="sxs-lookup"><span data-stu-id="2e8c0-356">Contains "per monitor"</span></span>            | <span data-ttu-id="2e8c0-357">Windows **Vista, Windows 7 и Windows 8:** Поведение аналогично поведению, если **дпиаваре** отсутствует.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-357">**Windows Vista, Windows 7 and Windows 8:** The behavior is the same as when the **dpiAware** is absent.</span></span><br/> <span data-ttu-id="2e8c0-358">**Windows 8.1 и Windows 10:** Текущий процесс учитывает dpi для каждого монитора.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-358">**Windows 8.1 and Windows 10:** The current process is per-monitor dpi aware.</span></span><br/>                                                                                                                                                                                      |
| <span data-ttu-id="2e8c0-359">Содержит любую другую строку</span><span class="sxs-lookup"><span data-stu-id="2e8c0-359">Contains any other string</span></span>         | <span data-ttu-id="2e8c0-360">Windows **Vista, Windows 7 и Windows 8:** Поведение аналогично поведению, если **дпиаваре** отсутствует.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-360">**Windows Vista, Windows 7 and Windows 8:** The behavior is the same as when the **dpiAware** is absent.</span></span><br/> <span data-ttu-id="2e8c0-361">**Windows 8.1 и Windows 10:** Текущий процесс не знает dpi, и программное изменение этого параметра невозможно выполнить, вызвав функцию [**сетпроцессдпиаваренесс**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) или [**сетпроцессдпиаваре**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) .</span><span class="sxs-lookup"><span data-stu-id="2e8c0-361">**Windows 8.1 and Windows 10:** The current process is dpi unaware, and you cannot programmatically change this setting by calling the [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) or [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) function.</span></span><br/> |

<span data-ttu-id="2e8c0-362">Дополнительные сведения о параметрах осведомленности о dpi см. в разделе [Сравнение уровней осведомленности о dpi](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot)).</span><span class="sxs-lookup"><span data-stu-id="2e8c0-362">For more information about dpi awareness settings, see [Comparison of DPI Awareness Levels](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot)).</span></span>

<span data-ttu-id="2e8c0-363">**дпиаваре** не имеет атрибутов.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-363">**dpiAware** has no attributes.</span></span>

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2005/WindowsSettings">
      <dpiAware>true</dpiAware>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="dpiAwareness"></span><span id="dpiawareness"></span><span id="DPIAWARENESS"></span>

### <a name="dpiawareness"></a><span data-ttu-id="2e8c0-364">дпиаваренесс</span><span class="sxs-lookup"><span data-stu-id="2e8c0-364">dpiAwareness</span></span>

<span data-ttu-id="2e8c0-365">Указывает, учитывается ли текущий процесс в точках на дюйм (DPI).</span><span class="sxs-lookup"><span data-stu-id="2e8c0-365">Specifies whether the current process is dots per inch (dpi) aware.</span></span>

<span data-ttu-id="2e8c0-366">Минимальная версия операционной системы, поддерживающая элемент **дпиаваренесс** , — Windows 10, версия 1607.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-366">The minimum version of the operating system that supports the **dpiAwareness** element is Windows 10, version 1607.</span></span> <span data-ttu-id="2e8c0-367">Для версий, которые поддерживают элемент **дпиаваренесс** , **дпиаваренесс** переопределяет элемент **дпиаваре** .</span><span class="sxs-lookup"><span data-stu-id="2e8c0-367">For versions that support the **dpiAwareness** element, the **dpiAwareness** overrides the **dpiAware** element.</span></span> <span data-ttu-id="2e8c0-368">Можно включить оба элемента в манифест, если вы хотите указать другое поведение для Windows 10 версии 1607, чем для более ранней версии операционной системы.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-368">You can include both elements in a manifest if you want to specify a different behavior for Windows 10, version 1607 than for an earlier version of the operating system.</span></span>

<span data-ttu-id="2e8c0-369">Элемент **дпиаваренесс** может содержать один элемент или список элементов с разделителями-запятыми.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-369">The **dpiAwareness** element can contain a single item or a list of comma-separated items.</span></span> <span data-ttu-id="2e8c0-370">В последнем случае используется первый (крайний левый) элемент в списке, распознанном операционной системой.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-370">In the latter case, the first (leftmost) item in the list recognized by the operating system is used.</span></span> <span data-ttu-id="2e8c0-371">Таким образом можно указать различные варианты поведения, поддерживаемые в будущих версиях операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-371">In this way, you can specify different behaviors supported in future Windows operating system versions.</span></span>

<span data-ttu-id="2e8c0-372">В следующей таблице описывается поведение, получаемое в зависимости от наличия элемента **дпиаваренесс** и содержащегося в нем текста в его левом распознанном элементе.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-372">The following table describes the behavior that results based upon the presence of the **dpiAwareness** element and the text that it contains in its leftmost recognized item.</span></span> <span data-ttu-id="2e8c0-373">В тексте элемента не учитывается регистр.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-373">The text within the element is not case-sensitive.</span></span>

| <span data-ttu-id="2e8c0-374">состояние элемента **дпиаваренесс** :</span><span class="sxs-lookup"><span data-stu-id="2e8c0-374">**dpiAwareness** element status:</span></span>        | <span data-ttu-id="2e8c0-375">Описание</span><span class="sxs-lookup"><span data-stu-id="2e8c0-375">Description</span></span>                          |
|-----------------------------------------|-------------------------------------------|
| <span data-ttu-id="2e8c0-376">Отсутствует элемент</span><span class="sxs-lookup"><span data-stu-id="2e8c0-376">Element is absent</span></span>                       | <span data-ttu-id="2e8c0-377">Элемент **дпиаваре** указывает, учитывается ли в процессе разрешение dpi.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-377">The **dpiAware** element specifies whether the process is dpi aware.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="2e8c0-378">Не содержит распознанные элементы</span><span class="sxs-lookup"><span data-stu-id="2e8c0-378">Contains no recognized items</span></span>            | <span data-ttu-id="2e8c0-379">По умолчанию текущий процесс не знает dpi.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-379">The current process is dpi unaware by default.</span></span> <span data-ttu-id="2e8c0-380">Этот параметр можно изменить программным путем, вызвав функцию [**сетпроцессдпиаваренесс**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) или [**сетпроцессдпиаваре**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) .</span><span class="sxs-lookup"><span data-stu-id="2e8c0-380">You can programmatically change this setting by calling the [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) or [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) function.</span></span> |
| <span data-ttu-id="2e8c0-381">Первый распознанный элемент — "System"</span><span class="sxs-lookup"><span data-stu-id="2e8c0-381">First recognized item is "system"</span></span>       | <span data-ttu-id="2e8c0-382">Текущий процесс учитывает dpi системы.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-382">The current process is system dpi aware.</span></span>                                                                                                                                                                                               |
| <span data-ttu-id="2e8c0-383">Первый распознанный элемент — "пермонитор"</span><span class="sxs-lookup"><span data-stu-id="2e8c0-383">First recognized item is "permonitor"</span></span>   | <span data-ttu-id="2e8c0-384">Текущий процесс учитывает dpi для каждого монитора.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-384">The current process is per-monitor dpi aware.</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="2e8c0-385">Первый распознанный элемент — "permonitorv2"</span><span class="sxs-lookup"><span data-stu-id="2e8c0-385">First recognized item is "permonitorv2"</span></span> | <span data-ttu-id="2e8c0-386">В текущем процессе используется контекст осведомленности по dpi для каждого монитора.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-386">The current process uses the per-monitor-v2 dpi awareness context.</span></span> <span data-ttu-id="2e8c0-387">Этот элемент будет распознан только в Windows 10 версии 1703 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-387">This item will only be recognized on Windows 10 version 1703 or later.</span></span>                                                                                              |
| <span data-ttu-id="2e8c0-388">Первый распознанный элемент «не осведомлен»</span><span class="sxs-lookup"><span data-stu-id="2e8c0-388">First recognized item is "unaware"</span></span>      | <span data-ttu-id="2e8c0-389">Текущий процесс является неосведомленным от dpi.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-389">The current process is dpi unaware.</span></span> <span data-ttu-id="2e8c0-390">Вы **не можете** программно изменить этот параметр, вызвав функцию [**сетпроцессдпиаваренесс**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) или [**сетпроцессдпиаваре**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) .</span><span class="sxs-lookup"><span data-stu-id="2e8c0-390">You **cannot** programmatically change this setting by calling the [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) or [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) function.</span></span>      |

<span data-ttu-id="2e8c0-391">Дополнительные сведения о параметрах осведомленности о разрешении, поддерживаемых этим элементом, см. в разделе [ \_ Поддержка dpi](/windows/desktop/api/windef/ne-windef-dpi_awareness) и [ \_ \_ контекст осведомленности](/windows/desktop/hidpi/dpi-awareness-context)о dpi.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-391">For more information about dpi awareness settings supported by this element, see [DPI\_AWARENESS](/windows/desktop/api/windef/ne-windef-dpi_awareness) and [DPI\_AWARENESS\_CONTEXT](/windows/desktop/hidpi/dpi-awareness-context).</span></span>

<span data-ttu-id="2e8c0-392">**дпиаваренесс** не имеет атрибутов.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-392">**dpiAwareness** has no attributes.</span></span>

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2016/WindowsSettings">
      <dpiAwareness>PerMonitorV2, unaware</dpiAwareness>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="gdiScaling"></span><span id="gdiscaling"></span><span id="GDISCALING"></span>

### <a name="gdiscaling"></a><span data-ttu-id="2e8c0-393">гдискалинг</span><span class="sxs-lookup"><span data-stu-id="2e8c0-393">gdiScaling</span></span>

<span data-ttu-id="2e8c0-394">Указывает, включено ли масштабирование GDI.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-394">Specifies whether GDI scaling is enabled.</span></span> <span data-ttu-id="2e8c0-395">Минимальная версия операционной системы, поддерживающая элемент **гдискалинг** , — Windows 10 версии 1703.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-395">The minimum version of the operating system that supports the **gdiScaling** element is Windows 10 version 1703.</span></span>

<span data-ttu-id="2e8c0-396">Платформа GDI (интерфейс графических устройств) может применять масштабирование DPI к примитивам и тексту на уровне отдельных мониторов без обновления самого приложения.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-396">The GDI (graphics device interface) framework can apply DPI scaling to primitives and text on a per-monitor basis without updates to the application itself.</span></span> <span data-ttu-id="2e8c0-397">Это может быть полезно для приложений GDI, которые больше не обновляются.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-397">This can be useful for GDI applications no longer being actively updated.</span></span>

<span data-ttu-id="2e8c0-398">Невекторная графика (например, точечные рисунки, значки или панели инструментов) не может масштабироваться этим элементом.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-398">Non-vector graphics (such as bitmaps, icons, or toolbars) cannot be scaled by this element.</span></span> <span data-ttu-id="2e8c0-399">Кроме того, графика и текст, отображаемые в растровых изображениях, динамически создаваемые приложениями, также не могут масштабироваться этим элементом.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-399">In addition, graphics and text appearing within bitmaps dynamically constructed by applications also cannot be scaled by this element.</span></span>

<span data-ttu-id="2e8c0-400">**Значение true** указывает, что этот элемент включен.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-400">**TRUE** indicates that this element is enabled.</span></span> <span data-ttu-id="2e8c0-401">У него нет атрибутов.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-401">It has no attributes.</span></span>


```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2017/WindowsSettings">
      <gdiScaling>true</gdiScaling>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="highResolutionScrollingAware"></span><span id="highresolutionscrollingaware"></span><span id="HIGHRESOLUTIONSCROLLINGAWARE"></span>

### <a name="highresolutionscrollingaware"></a><span data-ttu-id="2e8c0-402">хигхресолутионскроллингаваре</span><span class="sxs-lookup"><span data-stu-id="2e8c0-402">highResolutionScrollingAware</span></span>

<span data-ttu-id="2e8c0-403">Указывает, включено ли разрешение на прокрутку с высоким разрешением.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-403">Specifies whether high-resolution-scrolling aware is enabled.</span></span> <span data-ttu-id="2e8c0-404">**Значение true** указывает, что он включен.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-404">**TRUE** indicates that it is enabled.</span></span> <span data-ttu-id="2e8c0-405">У него нет атрибутов.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-405">It has no attributes.</span></span>

<span id="longPathAware"></span><span id="longpathaware"></span><span id="LONGPATHAWARE"></span>

### <a name="longpathaware"></a><span data-ttu-id="2e8c0-406">лонгпасаваре</span><span class="sxs-lookup"><span data-stu-id="2e8c0-406">longPathAware</span></span>

<span data-ttu-id="2e8c0-407">Включает длинные пути, длина которых превышает **MAX_PATH** .</span><span class="sxs-lookup"><span data-stu-id="2e8c0-407">Enables long paths that exceed **MAX_PATH** in length.</span></span> <span data-ttu-id="2e8c0-408">Этот элемент поддерживается в Windows 10, версии 1607 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-408">This element is supported in Windows 10, version 1607, and later.</span></span> <span data-ttu-id="2e8c0-409">Дополнительные сведения см. в [этой статье](../fileio/maximum-file-path-limitation.md).</span><span class="sxs-lookup"><span data-stu-id="2e8c0-409">For more information, see [this article](../fileio/maximum-file-path-limitation.md).</span></span>

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns:ws2="http://schemas.microsoft.com/SMI/2016/WindowsSettings">
      <ws2:longPathAware>true</ws2:longPathAware>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="printerDriverIsolation"></span><span id="printerdriverisolation"></span><span id="PRINTERDRIVERISOLATION"></span>

### <a name="printerdriverisolation"></a><span data-ttu-id="2e8c0-410">принтердриверисолатион</span><span class="sxs-lookup"><span data-stu-id="2e8c0-410">printerDriverIsolation</span></span>

<span data-ttu-id="2e8c0-411">Указывает, включена ли изоляция драйвера принтера.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-411">Specifies whether printer driver isolation is enabled.</span></span> <span data-ttu-id="2e8c0-412">**Значение true** указывает, что он включен.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-412">**TRUE** indicates that it is enabled.</span></span> <span data-ttu-id="2e8c0-413">У него нет атрибутов.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-413">It has no attributes.</span></span> <span data-ttu-id="2e8c0-414">Изоляция драйвера принтера повышает надежность службы печати Windows, позволяя драйверам принтера выполняться в процессах, отдельных от процесса, в котором работает диспетчер очереди печати.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-414">Printer driver isolation improves the reliability of the Windows print service by enabling printer drivers to run in processes that are separate from the process in which the print spooler runs.</span></span> <span data-ttu-id="2e8c0-415">Поддержка изоляции драйвера принтера начата в Windows 7 и Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-415">Support for printer driver isolation started in Windows 7 and Windows Server 2008 R2.</span></span> <span data-ttu-id="2e8c0-416">Приложение может объявить изоляцию драйвера принтера в своем манифесте приложения, чтобы изолировать себя от драйвера принтера и повысить его надежность.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-416">An app can declare printer driver isolation in its app manifest to isolate itself from the printer driver and improve its reliability.</span></span> <span data-ttu-id="2e8c0-417">Это значит, что приложение не будет завершаться сбоем, если в драйвере принтера произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-417">That is, the app won't crash if the printer driver has an error.</span></span>


```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2011/WindowsSettings">
      <printerDriverIsolation>true</printerDriverIsolation>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="ultraHighResolutionScrollingAware"></span><span id="ultrahighresolutionscrollingaware"></span><span id="ULTRAHIGHRESOLUTIONSCROLLINGAWARE"></span>

### <a name="ultrahighresolutionscrollingaware"></a><span data-ttu-id="2e8c0-418">ултрахигхресолутионскроллингаваре</span><span class="sxs-lookup"><span data-stu-id="2e8c0-418">ultraHighResolutionScrollingAware</span></span>

<span data-ttu-id="2e8c0-419">Указывает, включено ли разрешение на прокрутку Ultra-High-resolution.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-419">Specifies whether ultra-high-resolution-scrolling aware is enabled.</span></span> <span data-ttu-id="2e8c0-420">**Значение true** указывает, что он включен.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-420">**TRUE** indicates that it is enabled.</span></span> <span data-ttu-id="2e8c0-421">У него нет атрибутов.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-421">It has no attributes.</span></span>

<span id="msix"></span><span id="MSIX"></span>

### <a name="msix"></a><span data-ttu-id="2e8c0-422">msix</span><span class="sxs-lookup"><span data-stu-id="2e8c0-422">msix</span></span>

<span data-ttu-id="2e8c0-423">Указывает сведения об удостоверении [разреженного пакета MSIX](/windows/apps/desktop/modernize/grant-identity-to-nonpackaged-apps) для текущего приложения.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-423">Specifies the identity info of a [sparse MSIX package](/windows/apps/desktop/modernize/grant-identity-to-nonpackaged-apps) for the current application.</span></span> <span data-ttu-id="2e8c0-424">Этот элемент поддерживается в Windows 10, версии 2004 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-424">This element is supported in Windows 10, version 2004, and later versions.</span></span>

<span data-ttu-id="2e8c0-425">Элемент **msix** должен находиться в пространстве имен `urn:schemas-microsoft-com:msix.v1` .</span><span class="sxs-lookup"><span data-stu-id="2e8c0-425">The **msix** element must be in the namespace `urn:schemas-microsoft-com:msix.v1`.</span></span> <span data-ttu-id="2e8c0-426">Он содержит атрибуты, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-426">It has the attributes shown in the following table.</span></span>

| <span data-ttu-id="2e8c0-427">attribute</span><span class="sxs-lookup"><span data-stu-id="2e8c0-427">Attribute</span></span>   | <span data-ttu-id="2e8c0-428">Описание</span><span class="sxs-lookup"><span data-stu-id="2e8c0-428">Description</span></span>                                                                                             |
|-------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e8c0-429">**publisher**</span><span class="sxs-lookup"><span data-stu-id="2e8c0-429">**publisher**</span></span>    | <span data-ttu-id="2e8c0-430">Описание сведений об издателе.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-430">Describes the publisher information.</span></span> <span data-ttu-id="2e8c0-431">Это значение должно соответствовать атрибуту **издателя** в элементе [Identity](/uwp/schemas/appxpackage/uapmanifestschema/element-identity) манифеста разреженного пакета.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-431">This value must match the **Publisher** attribute in the [Identity](/uwp/schemas/appxpackage/uapmanifestschema/element-identity) element in your sparse package manifest.</span></span> |
| <span data-ttu-id="2e8c0-432">**packageName**</span><span class="sxs-lookup"><span data-stu-id="2e8c0-432">**packageName**</span></span> | <span data-ttu-id="2e8c0-433">Описывает содержимое пакета.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-433">Describes the contents of the package.</span></span> <span data-ttu-id="2e8c0-434">Это значение должно соответствовать атрибуту **Name** в элементе [Identity](/uwp/schemas/appxpackage/uapmanifestschema/element-identity) манифеста разреженного пакета.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-434">This value must match the **Name** attribute in the [Identity](/uwp/schemas/appxpackage/uapmanifestschema/element-identity) element in your sparse package manifest.</span></span>    |
| <span data-ttu-id="2e8c0-435">**applicationId**</span><span class="sxs-lookup"><span data-stu-id="2e8c0-435">**applicationId**</span></span>    | <span data-ttu-id="2e8c0-436">Уникальный идентификатор приложения.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-436">The unique identifier of the application.</span></span> <span data-ttu-id="2e8c0-437">Это значение должно соответствовать атрибуту **ID** в элементе [Application](/uwp/schemas/appxpackage/uapmanifestschema/element-application) в манифесте разреженного пакета.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-437">This value must match the **Id** attribute in the [Application](/uwp/schemas/appxpackage/uapmanifestschema/element-application) element in your sparse package manifest.</span></span>  |

```xml
<?xml version="1.0" encoding="utf-8"?>
<assembly manifestVersion="1.0" xmlns="urn:schemas-microsoft-com:asm.v1">
  <assemblyIdentity version="1.0.0.0" name="Contoso.PhotoStoreApp"/>
  <msix xmlns="urn:schemas-microsoft-com:msix.v1"
          publisher="CN=Contoso"
          packageName="ContosoPhotoStore"
          applicationId="ContosoPhotoStore"
        />
</assembly>
```

### <a name="heaptype"></a><span data-ttu-id="2e8c0-438">хеаптипе</span><span class="sxs-lookup"><span data-stu-id="2e8c0-438">heapType</span></span>

<span data-ttu-id="2e8c0-439">Переопределяет реализацию кучи по умолчанию для использования [API кучи Win32](../Memory/heap-functions.md) .</span><span class="sxs-lookup"><span data-stu-id="2e8c0-439">Overrides the default heap implementation for the [Win32 heap APIs](../Memory/heap-functions.md) to use.</span></span>

* <span data-ttu-id="2e8c0-440">Значение **сегменсеап** указывает, что будет использоваться куча сегмента.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-440">The value **SegmentHeap** indicates that segment heap will be used.</span></span> <span data-ttu-id="2e8c0-441">Куча сегментов — это современная реализация кучи, которая обычно сокращает общее использование памяти.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-441">Segment heap is a modern heap implementation that will generally reduce your overall memory usage.</span></span> <span data-ttu-id="2e8c0-442">Этот элемент поддерживается в Windows 10, версия 2004 (сборка 19041) и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-442">This element is supported in Windows 10, version 2004 (build 19041) and later.</span></span>
* <span data-ttu-id="2e8c0-443">Все остальные значения игнорируются.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-443">All other values are ignored.</span></span>

<span data-ttu-id="2e8c0-444">Этот элемент не содержит атрибуты.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-444">This element has no attributes.</span></span>

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2020/WindowsSettings">
      <heapType>SegmentHeap</heapType>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

## <a name="example"></a><span data-ttu-id="2e8c0-445">Пример</span><span class="sxs-lookup"><span data-stu-id="2e8c0-445">Example</span></span>

<span data-ttu-id="2e8c0-446">Ниже приведен пример манифеста приложения для приложения с именем MySampleApp.exe.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-446">The following is an example of an application manifest for an application named MySampleApp.exe.</span></span> <span data-ttu-id="2e8c0-447">Приложение использует Самплеассембли параллельную сборку.</span><span class="sxs-lookup"><span data-stu-id="2e8c0-447">The application consumes the SampleAssembly side-by-side assembly.</span></span>

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">

  <compatibility xmlns="urn:schemas-microsoft-com:compatibility.v1"> 
      <application> 
        <!--This Id value indicates the application supports Windows Vista functionality -->
          <supportedOS Id="{e2011457-1546-43c5-a5fe-008deee3d3f0}"/> 
        <!--This Id value indicates the application supports Windows 7 functionality-->
          <supportedOS Id="{35138b9a-5d96-4fbd-8e2d-a2440225f93a}"/>
        <!--This Id value indicates the application supports Windows 8 functionality-->
          <supportedOS Id="{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}"/>
        <!--This Id value indicates the application supports Windows 8.1 functionality-->
          <supportedOS Id="{1f676c76-80e1-4239-95bb-83d0f6d0da78}"/>
      </application> 
  </compatibility>

  <assemblyIdentity type="win32" 
                    name="myOrganization.myDivision.mySampleApp" 
                    version="6.0.0.0" 
                    processorArchitecture="x86" 
                    publicKeyToken="0000000000000000"
  />
  <dependency>
    <dependentAssembly>
      <assemblyIdentity type="win32" 
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
