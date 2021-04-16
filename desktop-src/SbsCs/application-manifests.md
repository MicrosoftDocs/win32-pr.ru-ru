---
description: Манифест приложения — это файл XML, который описывает и определяет общие и закрытые сборки одновременного выполнения, которые приложению следует подключить во время выполнения.
ms.assetid: c5016251-db7a-4edc-9be9-3acb03d495f8
title: Манифесты приложений
ms.topic: article
ms.date: 10/08/2020
ms.custom: 19H1
ms.openlocfilehash: cb065bc4d6d29f4142c23cdd91c83769e2fb9b87
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/05/2021
ms.locfileid: "105651234"
---
# <a name="application-manifests"></a><span data-ttu-id="fb9dc-103">Манифесты приложений</span><span class="sxs-lookup"><span data-stu-id="fb9dc-103">Application Manifests</span></span>

<span data-ttu-id="fb9dc-104">Манифест приложения — это файл XML, который описывает и определяет общие и закрытые сборки одновременного выполнения, которые приложению следует подключить во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-104">An application manifest is an XML file that describes and identifies the shared and private side-by-side assemblies that an application should bind to at run time.</span></span> <span data-ttu-id="fb9dc-105">Это должны быть те же версии сборок, что и использованные для проверки приложения.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-105">These should be the same assembly versions that were used to test the application.</span></span> <span data-ttu-id="fb9dc-106">Манифесты приложения также могут описывать метаданные закрытых для приложения файлов.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-106">Application manifests may also describe metadata for files that are private to the application.</span></span>

<span data-ttu-id="fb9dc-107">Полный список схем XML см. в разделе [Схема файла манифеста](manifest-file-schema.md).</span><span class="sxs-lookup"><span data-stu-id="fb9dc-107">For a complete listing of the XML schema, see [Manifest File Schema](manifest-file-schema.md).</span></span>

<span data-ttu-id="fb9dc-108">Манифесты приложений имеют следующие элементы и атрибуты.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-108">Application manifests have the following elements and attributes.</span></span>

| <span data-ttu-id="fb9dc-109">Элемент</span><span class="sxs-lookup"><span data-stu-id="fb9dc-109">Element</span></span>                               | <span data-ttu-id="fb9dc-110">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="fb9dc-110">Attributes</span></span>                | <span data-ttu-id="fb9dc-111">Обязательно</span><span class="sxs-lookup"><span data-stu-id="fb9dc-111">Required</span></span> |
|---------------------------------------|---------------------------|----------|
| <span data-ttu-id="fb9dc-112">**сборок**</span><span class="sxs-lookup"><span data-stu-id="fb9dc-112">**assembly**</span></span>                          |                           | <span data-ttu-id="fb9dc-113">Да</span><span class="sxs-lookup"><span data-stu-id="fb9dc-113">Yes</span></span>      |
|                                       | <span data-ttu-id="fb9dc-114">**манифестверсион**</span><span class="sxs-lookup"><span data-stu-id="fb9dc-114">**manifestVersion**</span></span>       | <span data-ttu-id="fb9dc-115">Да</span><span class="sxs-lookup"><span data-stu-id="fb9dc-115">Yes</span></span>      |
| <span data-ttu-id="fb9dc-116">**не наследовать**</span><span class="sxs-lookup"><span data-stu-id="fb9dc-116">**noInherit**</span></span>                         |                           | <span data-ttu-id="fb9dc-117">Нет</span><span class="sxs-lookup"><span data-stu-id="fb9dc-117">No</span></span>       |
| <span data-ttu-id="fb9dc-118">**Неправильн**</span><span class="sxs-lookup"><span data-stu-id="fb9dc-118">**assemblyIdentity**</span></span>                  |                           | <span data-ttu-id="fb9dc-119">Да</span><span class="sxs-lookup"><span data-stu-id="fb9dc-119">Yes</span></span>      |
|                                       | <span data-ttu-id="fb9dc-120">**type**</span><span class="sxs-lookup"><span data-stu-id="fb9dc-120">**type**</span></span>                  | <span data-ttu-id="fb9dc-121">Да</span><span class="sxs-lookup"><span data-stu-id="fb9dc-121">Yes</span></span>      |
|                                       | <span data-ttu-id="fb9dc-122">**name**</span><span class="sxs-lookup"><span data-stu-id="fb9dc-122">**name**</span></span>                  | <span data-ttu-id="fb9dc-123">Да</span><span class="sxs-lookup"><span data-stu-id="fb9dc-123">Yes</span></span>      |
|                                       | <span data-ttu-id="fb9dc-124">**language**</span><span class="sxs-lookup"><span data-stu-id="fb9dc-124">**language**</span></span>              | <span data-ttu-id="fb9dc-125">Нет</span><span class="sxs-lookup"><span data-stu-id="fb9dc-125">No</span></span>       |
|                                       | <span data-ttu-id="fb9dc-126">**processorArchitecture**</span><span class="sxs-lookup"><span data-stu-id="fb9dc-126">**processorArchitecture**</span></span> | <span data-ttu-id="fb9dc-127">Нет</span><span class="sxs-lookup"><span data-stu-id="fb9dc-127">No</span></span>       |
|                                       | <span data-ttu-id="fb9dc-128">**version**</span><span class="sxs-lookup"><span data-stu-id="fb9dc-128">**version**</span></span>               | <span data-ttu-id="fb9dc-129">Да</span><span class="sxs-lookup"><span data-stu-id="fb9dc-129">Yes</span></span>      |
|                                       | <span data-ttu-id="fb9dc-130">**publicKeyToken**</span><span class="sxs-lookup"><span data-stu-id="fb9dc-130">**publicKeyToken**</span></span>        | <span data-ttu-id="fb9dc-131">Нет</span><span class="sxs-lookup"><span data-stu-id="fb9dc-131">No</span></span>       |
| <span data-ttu-id="fb9dc-132">**совместимость**</span><span class="sxs-lookup"><span data-stu-id="fb9dc-132">**compatibility**</span></span>                     |                           | <span data-ttu-id="fb9dc-133">Нет</span><span class="sxs-lookup"><span data-stu-id="fb9dc-133">No</span></span>       |
| <span data-ttu-id="fb9dc-134">**приложение**</span><span class="sxs-lookup"><span data-stu-id="fb9dc-134">**application**</span></span>                       |                           | <span data-ttu-id="fb9dc-135">Нет</span><span class="sxs-lookup"><span data-stu-id="fb9dc-135">No</span></span>       |
| <span data-ttu-id="fb9dc-136">**суппортедос**</span><span class="sxs-lookup"><span data-stu-id="fb9dc-136">**supportedOS**</span></span>                       | <span data-ttu-id="fb9dc-137">**Id**</span><span class="sxs-lookup"><span data-stu-id="fb9dc-137">**Id**</span></span>                    | <span data-ttu-id="fb9dc-138">Нет</span><span class="sxs-lookup"><span data-stu-id="fb9dc-138">No</span></span>       |
| <span data-ttu-id="fb9dc-139">**maxversiontested укажите установленную**</span><span class="sxs-lookup"><span data-stu-id="fb9dc-139">**maxversiontested**</span></span>                  | <span data-ttu-id="fb9dc-140">**Id**</span><span class="sxs-lookup"><span data-stu-id="fb9dc-140">**Id**</span></span>                    | <span data-ttu-id="fb9dc-141">Нет</span><span class="sxs-lookup"><span data-stu-id="fb9dc-141">No</span></span>       |
| <span data-ttu-id="fb9dc-142">**зависимостей**</span><span class="sxs-lookup"><span data-stu-id="fb9dc-142">**dependency**</span></span>                        |                           | <span data-ttu-id="fb9dc-143">Нет</span><span class="sxs-lookup"><span data-stu-id="fb9dc-143">No</span></span>       |
| <span data-ttu-id="fb9dc-144">**dependentAssembly**</span><span class="sxs-lookup"><span data-stu-id="fb9dc-144">**dependentAssembly**</span></span>                 |                           | <span data-ttu-id="fb9dc-145">Нет</span><span class="sxs-lookup"><span data-stu-id="fb9dc-145">No</span></span>       |
| <span data-ttu-id="fb9dc-146">**file**</span><span class="sxs-lookup"><span data-stu-id="fb9dc-146">**file**</span></span>                              |                           | <span data-ttu-id="fb9dc-147">Нет</span><span class="sxs-lookup"><span data-stu-id="fb9dc-147">No</span></span>       |
|                                       | <span data-ttu-id="fb9dc-148">**name**</span><span class="sxs-lookup"><span data-stu-id="fb9dc-148">**name**</span></span>                  | <span data-ttu-id="fb9dc-149">Нет</span><span class="sxs-lookup"><span data-stu-id="fb9dc-149">No</span></span>       |
|                                       | <span data-ttu-id="fb9dc-150">**hashAlg**</span><span class="sxs-lookup"><span data-stu-id="fb9dc-150">**hashalg**</span></span>               | <span data-ttu-id="fb9dc-151">Нет</span><span class="sxs-lookup"><span data-stu-id="fb9dc-151">No</span></span>       |
|                                       | <span data-ttu-id="fb9dc-152">**hash**</span><span class="sxs-lookup"><span data-stu-id="fb9dc-152">**hash**</span></span>                  | <span data-ttu-id="fb9dc-153">Нет</span><span class="sxs-lookup"><span data-stu-id="fb9dc-153">No</span></span>       |
| <span data-ttu-id="fb9dc-154">**активекодепаже**</span><span class="sxs-lookup"><span data-stu-id="fb9dc-154">**activeCodePage**</span></span>                    |                           | <span data-ttu-id="fb9dc-155">Нет</span><span class="sxs-lookup"><span data-stu-id="fb9dc-155">No</span></span>       |
| <span data-ttu-id="fb9dc-156">**автоповышение**</span><span class="sxs-lookup"><span data-stu-id="fb9dc-156">**autoElevate**</span></span>                       |                           | <span data-ttu-id="fb9dc-157">Нет</span><span class="sxs-lookup"><span data-stu-id="fb9dc-157">No</span></span>       |
| <span data-ttu-id="fb9dc-158">**дисаблесеминг**</span><span class="sxs-lookup"><span data-stu-id="fb9dc-158">**disableTheming**</span></span>                    |                           | <span data-ttu-id="fb9dc-159">Нет</span><span class="sxs-lookup"><span data-stu-id="fb9dc-159">No</span></span>       |
| <span data-ttu-id="fb9dc-160">**дисаблевиндовфилтеринг**</span><span class="sxs-lookup"><span data-stu-id="fb9dc-160">**disableWindowFiltering**</span></span>            |                           | <span data-ttu-id="fb9dc-161">Нет</span><span class="sxs-lookup"><span data-stu-id="fb9dc-161">No</span></span>       |
| <span data-ttu-id="fb9dc-162">**дпиаваре**</span><span class="sxs-lookup"><span data-stu-id="fb9dc-162">**dpiAware**</span></span>                          |                           | <span data-ttu-id="fb9dc-163">Нет</span><span class="sxs-lookup"><span data-stu-id="fb9dc-163">No</span></span>       |
| <span data-ttu-id="fb9dc-164">**дпиаваренесс**</span><span class="sxs-lookup"><span data-stu-id="fb9dc-164">**dpiAwareness**</span></span>                      |                           | <span data-ttu-id="fb9dc-165">Нет</span><span class="sxs-lookup"><span data-stu-id="fb9dc-165">No</span></span>       |
| <span data-ttu-id="fb9dc-166">**гдискалинг**</span><span class="sxs-lookup"><span data-stu-id="fb9dc-166">**gdiScaling**</span></span>                        |                           | <span data-ttu-id="fb9dc-167">Нет</span><span class="sxs-lookup"><span data-stu-id="fb9dc-167">No</span></span>       |
| <span data-ttu-id="fb9dc-168">**хигхресолутионскроллингаваре**</span><span class="sxs-lookup"><span data-stu-id="fb9dc-168">**highResolutionScrollingAware**</span></span>      |                           | <span data-ttu-id="fb9dc-169">Нет</span><span class="sxs-lookup"><span data-stu-id="fb9dc-169">No</span></span>       |
| <span data-ttu-id="fb9dc-170">**лонгпасаваре**</span><span class="sxs-lookup"><span data-stu-id="fb9dc-170">**longPathAware**</span></span>                     |                           | <span data-ttu-id="fb9dc-171">Нет</span><span class="sxs-lookup"><span data-stu-id="fb9dc-171">No</span></span>       |
| <span data-ttu-id="fb9dc-172">**принтердриверисолатион**</span><span class="sxs-lookup"><span data-stu-id="fb9dc-172">**printerDriverIsolation**</span></span>            |                           | <span data-ttu-id="fb9dc-173">Нет</span><span class="sxs-lookup"><span data-stu-id="fb9dc-173">No</span></span>       |
| <span data-ttu-id="fb9dc-174">**ултрахигхресолутионскроллингаваре**</span><span class="sxs-lookup"><span data-stu-id="fb9dc-174">**ultraHighResolutionScrollingAware**</span></span> |                           | <span data-ttu-id="fb9dc-175">Нет</span><span class="sxs-lookup"><span data-stu-id="fb9dc-175">No</span></span>       |
| <span data-ttu-id="fb9dc-176">**msix**</span><span class="sxs-lookup"><span data-stu-id="fb9dc-176">**msix**</span></span>                              |                           | <span data-ttu-id="fb9dc-177">Нет</span><span class="sxs-lookup"><span data-stu-id="fb9dc-177">No</span></span>       |
| <span data-ttu-id="fb9dc-178">**хеаптипе**</span><span class="sxs-lookup"><span data-stu-id="fb9dc-178">**heapType**</span></span>                          |                           | <span data-ttu-id="fb9dc-179">Нет</span><span class="sxs-lookup"><span data-stu-id="fb9dc-179">No</span></span>       |

## <a name="file-location"></a><span data-ttu-id="fb9dc-180">Расположение файла</span><span class="sxs-lookup"><span data-stu-id="fb9dc-180">File Location</span></span>

<span data-ttu-id="fb9dc-181">Манифесты приложений должны быть добавлены в качестве ресурсов в EXE-файл или библиотеку DLL приложения.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-181">Application manifests should be included as a resource in the application's EXE file or DLL.</span></span>

<span data-ttu-id="fb9dc-182">Дополнительные сведения см. в разделе [Установка параллельных сборок](installing-side-by-side-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="fb9dc-182">For more information, see [Installing Side-by-side Assemblies](installing-side-by-side-assemblies.md).</span></span>

## <a name="file-name-syntax"></a><span data-ttu-id="fb9dc-183">Синтаксис имени файла</span><span class="sxs-lookup"><span data-stu-id="fb9dc-183">File Name Syntax</span></span>

<span data-ttu-id="fb9dc-184">Имя файла манифеста приложения — это имя исполняемого объекта приложения, за которым следует manifest.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-184">The name of an application manifest file is the name of the application's executable followed by .manifest.</span></span>

<span data-ttu-id="fb9dc-185">Например, манифест приложения, который ссылается на example.exe или example.dll, будет использовать следующий синтаксис имени файла.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-185">For example, an application manifest that refers to example.exe or example.dll would use the following file name syntax.</span></span> <span data-ttu-id="fb9dc-186">Если идентификатор ресурса равен 1, можно опустить поле <*идентификатор ресурса*>.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-186">You can omit the <*resource ID*> field if resource ID is 1.</span></span>

<span data-ttu-id="fb9dc-187">**example.exe. <*идентификатор ресурса*>. manifest**</span><span class="sxs-lookup"><span data-stu-id="fb9dc-187">**example.exe.<*resource ID*>.manifest**</span></span>

<span data-ttu-id="fb9dc-188">**example.dll. <*идентификатор ресурса*>. manifest**</span><span class="sxs-lookup"><span data-stu-id="fb9dc-188">**example.dll.<*resource ID*>.manifest**</span></span>

## <a name="elements"></a><span data-ttu-id="fb9dc-189">Элементы</span><span class="sxs-lookup"><span data-stu-id="fb9dc-189">Elements</span></span>

<span data-ttu-id="fb9dc-190">В именах элементов и атрибутов учитывается регистр.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-190">Names of elements and attributes are case-sensitive.</span></span> <span data-ttu-id="fb9dc-191">Значения элементов и атрибутов не учитывают регистр, за исключением значения атрибута Type.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-191">The values of elements and attributes are case-insensitive, except for the value of the type attribute.</span></span>

<span id="assembly"></span><span id="ASSEMBLY"></span>

### <a name="assembly"></a><span data-ttu-id="fb9dc-192">сборка</span><span class="sxs-lookup"><span data-stu-id="fb9dc-192">assembly</span></span>

<span data-ttu-id="fb9dc-193">Элемент контейнера.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-193">A container element.</span></span> <span data-ttu-id="fb9dc-194">Его первым подэлементом должен быть элемент **NoInherit** или **assemblyIdentity** .</span><span class="sxs-lookup"><span data-stu-id="fb9dc-194">Its first subelement must be a **noInherit** or **assemblyIdentity** element.</span></span> <span data-ttu-id="fb9dc-195">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-195">Required.</span></span>

<span data-ttu-id="fb9dc-196">Элемент **Assembly** должен находиться в пространстве имен urn: schemas-microsoft-com: ASM. v1.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-196">The **assembly** element must be in the namespace "urn:schemas-microsoft-com:asm.v1".</span></span> <span data-ttu-id="fb9dc-197">Дочерние элементы сборки также должны находиться в этом пространстве имен путем наследования или добавления тегов.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-197">Child elements of the assembly must also be in this namespace, by inheritance or by tagging.</span></span>

<span data-ttu-id="fb9dc-198">Элемент **Assembly** имеет следующие атрибуты.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-198">The **assembly** element has the following attributes.</span></span>



| <span data-ttu-id="fb9dc-199">attribute</span><span class="sxs-lookup"><span data-stu-id="fb9dc-199">Attribute</span></span>           | <span data-ttu-id="fb9dc-200">Описание</span><span class="sxs-lookup"><span data-stu-id="fb9dc-200">Description</span></span>                                           |
|---------------------|-------------------------------------------------------|
| <span data-ttu-id="fb9dc-201">**манифестверсион**</span><span class="sxs-lookup"><span data-stu-id="fb9dc-201">**manifestVersion**</span></span> | <span data-ttu-id="fb9dc-202">Атрибут **манифестверсион** должен иметь значение 1,0.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-202">The **manifestVersion** attribute must be set to 1.0.</span></span> |


<span id="noInherit"></span><span id="noinherit"></span><span id="NOINHERIT"></span>

### <a name="noinherit"></a><span data-ttu-id="fb9dc-203">не наследовать</span><span class="sxs-lookup"><span data-stu-id="fb9dc-203">noInherit</span></span>

<span data-ttu-id="fb9dc-204">Включите этот элемент в манифест приложения, чтобы задать [контексты активации](activation-contexts.md) , созданные из манифеста, с флагом "без наследования".</span><span class="sxs-lookup"><span data-stu-id="fb9dc-204">Include this element in an application manifest to set the [activation contexts](activation-contexts.md) generated from the manifest with the "no inherit" flag.</span></span> <span data-ttu-id="fb9dc-205">Если этот флаг не установлен в контексте активации, а контекст активации активен, он наследуется новыми потоками в том же процессе, в окнах, в процедурах Windows и [асинхронных вызовах процедур](/windows/desktop/Sync/asynchronous-procedure-calls).</span><span class="sxs-lookup"><span data-stu-id="fb9dc-205">When this flag is not set in an activation context, and the activation context is active, it is inherited by new threads in the same process, windows, window procedures, and [Asynchronous Procedure Calls](/windows/desktop/Sync/asynchronous-procedure-calls).</span></span> <span data-ttu-id="fb9dc-206">Установка этого флага предотвращает наследование активного контекста новым объектом.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-206">Setting this flag prevents the new object from inheriting the active context.</span></span>

<span data-ttu-id="fb9dc-207">Элемент **NoInherit** является необязательным и обычно опускается.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-207">The **noInherit** element is optional and typically omitted.</span></span> <span data-ttu-id="fb9dc-208">Большинство сборок работает неправильно с помощью контекста активации без наследования, так как сборка должна быть специально разработана для управления распространением собственного контекста активации.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-208">Most assemblies do not work correctly using a no-inherit activation context because the assembly must be explicitly designed to manage the propagation of their own activation context.</span></span> <span data-ttu-id="fb9dc-209">Использование элемента **NoInherit** требует, чтобы все зависимые сборки, на которые ссылается манифест приложения, имели элемент **NoInherit** в [манифесте сборки](assembly-manifests.md).</span><span class="sxs-lookup"><span data-stu-id="fb9dc-209">The use of the **noInherit** element requires that any dependent assemblies referenced by the application manifest have a **noInherit** element in their [assembly manifest](assembly-manifests.md).</span></span>

<span data-ttu-id="fb9dc-210">Если в манифесте используется параметр **NoInherit** , он должен быть первым подэлементом элемента **Assembly** .</span><span class="sxs-lookup"><span data-stu-id="fb9dc-210">If **noInherit** is used in a manifest, it must be the first subelement of the **assembly** element.</span></span> <span data-ttu-id="fb9dc-211">Элемент **assemblyIdentity** должен идти сразу после элемента **NoInherit** .</span><span class="sxs-lookup"><span data-stu-id="fb9dc-211">The **assemblyIdentity** element should come immediately after the **noInherit** element.</span></span> <span data-ttu-id="fb9dc-212">Если параметр **NoInherit** не используется, то **assemblyIdentity** должен быть первым подэлементом элемента **Assembly** .</span><span class="sxs-lookup"><span data-stu-id="fb9dc-212">If **noInherit** is not used, **assemblyIdentity** must be the first subelement of the **assembly** element.</span></span> <span data-ttu-id="fb9dc-213">У элемента **NoInherit** нет дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-213">The **noInherit** element has no child elements.</span></span> <span data-ttu-id="fb9dc-214">Он не является допустимым элементом в [манифестах сборки](assembly-manifests.md).</span><span class="sxs-lookup"><span data-stu-id="fb9dc-214">It is not a valid element in [assembly manifests](assembly-manifests.md).</span></span>

<span id="assemblyIdentity"></span><span id="assemblyidentity"></span><span id="ASSEMBLYIDENTITY"></span>

### <a name="assemblyidentity"></a><span data-ttu-id="fb9dc-215">assemblyIdentity</span><span class="sxs-lookup"><span data-stu-id="fb9dc-215">assemblyIdentity</span></span>

<span data-ttu-id="fb9dc-216">Как первый подэлемент элемента **Assembly** , **assemblyIdentity** описывает и уникально идентифицирует приложение, владеющее этим манифестом приложения.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-216">As the first subelement of an **assembly** element, **assemblyIdentity** describes and uniquely identifies the application owning this application manifest.</span></span> <span data-ttu-id="fb9dc-217">Как первый подэлемент элемента **dependentAssembly** , **assemblyIdentity** описывает параллельную сборку, необходимую для приложения.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-217">As the first subelement of a **dependentAssembly** element, **assemblyIdentity** describes a side-by-side assembly required by the application.</span></span> <span data-ttu-id="fb9dc-218">Обратите внимание, что каждая сборка, указанная в манифесте приложения, требует наличия **assemblyIdentity** , точно совпадающего с **assemblyIdentity** в манифесте сборки, на которую указывает ссылка.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-218">Note that every assembly referenced in the application manifest requires an **assemblyIdentity** that exactly matches the **assemblyIdentity** in the referenced assembly's own assembly manifest.</span></span>

<span data-ttu-id="fb9dc-219">Элемент **assemblyIdentity** имеет следующие атрибуты.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-219">The **assemblyIdentity** element has the following attributes.</span></span> <span data-ttu-id="fb9dc-220">У него нет вложенных элементов.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-220">It has no subelements.</span></span>

| <span data-ttu-id="fb9dc-221">attribute</span><span class="sxs-lookup"><span data-stu-id="fb9dc-221">Attribute</span></span>                 | <span data-ttu-id="fb9dc-222">Описание</span><span class="sxs-lookup"><span data-stu-id="fb9dc-222">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb9dc-223">**type**</span><span class="sxs-lookup"><span data-stu-id="fb9dc-223">**type**</span></span>                  | <span data-ttu-id="fb9dc-224">Указывает тип приложения или сборки.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-224">Specifies the application or assembly type.</span></span> <span data-ttu-id="fb9dc-225">Значение должно быть в виде Win32, а все — в нижнем регистре.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-225">The value must be Win32 and all in lower case.</span></span> <span data-ttu-id="fb9dc-226">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-226">Required.</span></span>                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="fb9dc-227">**name**</span><span class="sxs-lookup"><span data-stu-id="fb9dc-227">**name**</span></span>                  | <span data-ttu-id="fb9dc-228">Уникально именует приложение или сборку.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-228">Uniquely names the application or assembly.</span></span> <span data-ttu-id="fb9dc-229">Используйте следующий формат для имени: Organization.Division.Name.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-229">Use the following format for the name: Organization.Division.Name.</span></span> <span data-ttu-id="fb9dc-230">Например, Microsoft. Windows. Мисамплеапп.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-230">For example Microsoft.Windows.mysampleApp.</span></span> <span data-ttu-id="fb9dc-231">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-231">Required.</span></span>                                                                                                                                                                                                                                                               |
| <span data-ttu-id="fb9dc-232">**language**</span><span class="sxs-lookup"><span data-stu-id="fb9dc-232">**language**</span></span>              | <span data-ttu-id="fb9dc-233">Определяет язык приложения или сборки.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-233">Identifies the language of the application or assembly.</span></span> <span data-ttu-id="fb9dc-234">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-234">Optional.</span></span> <span data-ttu-id="fb9dc-235">Если приложение или сборка зависит от языка, укажите код языка DHTML.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-235">If the application or assembly is language-specific, specify the DHTML language code.</span></span> <span data-ttu-id="fb9dc-236">На **теге assemblyIdentity** приложения, предназначенного для международных использования (не зависит от языка), не указывайте атрибут Language.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-236">In the **assemblyIdentity** of an application intended for worldwide use (language neutral) omit the language attribute.</span></span><br/> <span data-ttu-id="fb9dc-237">В **теге assemblyIdentity** сборки, предназначенной для международных использования (нейтральный к языку), задайте для параметра Language значение " \* ".</span><span class="sxs-lookup"><span data-stu-id="fb9dc-237">In an **assemblyIdentity** of an assembly intended for worldwide use (language neutral) set the value of language to "\*".</span></span><br/> |
| <span data-ttu-id="fb9dc-238">**processorArchitecture**</span><span class="sxs-lookup"><span data-stu-id="fb9dc-238">**processorArchitecture**</span></span> | <span data-ttu-id="fb9dc-239">Указывает процессор.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-239">Specifies the processor.</span></span> <span data-ttu-id="fb9dc-240">Допустимые значения: `x86`, `amd64`, `arm` и `arm64`.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-240">Valid values include `x86`, `amd64`, `arm` and `arm64`.</span></span> <span data-ttu-id="fb9dc-241">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-241">Optional.</span></span>                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="fb9dc-242">**version**</span><span class="sxs-lookup"><span data-stu-id="fb9dc-242">**version**</span></span>               | <span data-ttu-id="fb9dc-243">Указывает версию приложения или сборки.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-243">Specifies the application or assembly version.</span></span> <span data-ttu-id="fb9dc-244">Используйте формат версии из четырех частей: оближешь. nnnnn. ууо. ппппп.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-244">Use the four-part version format: mmmmm.nnnnn.ooooo.ppppp.</span></span> <span data-ttu-id="fb9dc-245">Каждая из частей, разделенных точками, может быть 0-65535 включительно.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-245">Each of the parts separated by periods can be 0-65535 inclusive.</span></span> <span data-ttu-id="fb9dc-246">Дополнительные сведения см. в разделе [версии сборки](assembly-versions.md).</span><span class="sxs-lookup"><span data-stu-id="fb9dc-246">For more information, see [Assembly Versions](assembly-versions.md).</span></span> <span data-ttu-id="fb9dc-247">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-247">Required.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="fb9dc-248">**publicKeyToken**</span><span class="sxs-lookup"><span data-stu-id="fb9dc-248">**publicKeyToken**</span></span>        | <span data-ttu-id="fb9dc-249">16-символьная шестнадцатеричная строка, представляющая последние 8 байт хэша SHA-1 открытого ключа, для которого подписано приложение или сборка.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-249">A 16-character hexadecimal string representing the last 8 bytes of the SHA-1 hash of the public key under which the application or assembly is signed.</span></span> <span data-ttu-id="fb9dc-250">Открытый ключ, используемый для подписи каталога, должен иметь длину 2048 бит или более.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-250">The public key used to sign the catalog must be 2048 bits or greater.</span></span> <span data-ttu-id="fb9dc-251">Требуется для всех общих параллельных сборок.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-251">Required for all shared side-by-side assemblies.</span></span>                                                                                                                                                     |

<span id="compatibility"></span><span id="COMPATIBILITY"></span>

### <a name="compatibility"></a><span data-ttu-id="fb9dc-252">совместимость</span><span class="sxs-lookup"><span data-stu-id="fb9dc-252">compatibility</span></span>

<span data-ttu-id="fb9dc-253">Содержит по крайней мере одно **приложение**.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-253">Contains at least one **application**.</span></span> <span data-ttu-id="fb9dc-254">У него нет атрибутов.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-254">It has no attributes.</span></span> <span data-ttu-id="fb9dc-255">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-255">Optional.</span></span> <span data-ttu-id="fb9dc-256">Манифесты приложений без элемента Compatibility по умолчанию имеют совместимость с Windows Vista в Windows 7.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-256">Application manifests without a compatibility element default to Windows Vista compatibility on Windows 7.</span></span>

<span id="application"></span><span id="APPLICATION"></span>

### <a name="application"></a><span data-ttu-id="fb9dc-257">application</span><span class="sxs-lookup"><span data-stu-id="fb9dc-257">application</span></span>

<span data-ttu-id="fb9dc-258">Содержит по крайней мере один элемент **суппортедос** .</span><span class="sxs-lookup"><span data-stu-id="fb9dc-258">Contains at least one **supportedOS** element.</span></span> <span data-ttu-id="fb9dc-259">Начиная с Windows 10 версии 1903, она также может содержать один необязательный элемент **maxversiontested укажите установленную** .</span><span class="sxs-lookup"><span data-stu-id="fb9dc-259">Starting in Windows 10, version 1903, it can also contain one optional **maxversiontested** element.</span></span> <span data-ttu-id="fb9dc-260">У него нет атрибутов.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-260">It has no attributes.</span></span> <span data-ttu-id="fb9dc-261">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-261">Optional.</span></span>

<span id="supportedOS"></span><span id="supportedos"></span><span id="SUPPORTEDOS"></span>

### <a name="supportedos"></a><span data-ttu-id="fb9dc-262">суппортедос</span><span class="sxs-lookup"><span data-stu-id="fb9dc-262">supportedOS</span></span>

<span data-ttu-id="fb9dc-263">Элемент **суппортедос** имеет следующий атрибут.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-263">The **supportedOS** element has the following attribute.</span></span> <span data-ttu-id="fb9dc-264">У него нет вложенных элементов.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-264">It has no subelements.</span></span>

| <span data-ttu-id="fb9dc-265">attribute</span><span class="sxs-lookup"><span data-stu-id="fb9dc-265">Attribute</span></span> | <span data-ttu-id="fb9dc-266">Описание</span><span class="sxs-lookup"><span data-stu-id="fb9dc-266">Description</span></span>   |
|-----------|-----------------------|
| <span data-ttu-id="fb9dc-267">**Id**</span><span class="sxs-lookup"><span data-stu-id="fb9dc-267">**Id**</span></span>    | <span data-ttu-id="fb9dc-268">Задайте для атрибута ID значение **{e2011457-1546-43c5-a5fe-008deee3d3f0}** , чтобы запустить приложение с помощью функции Vista.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-268">Set the Id attribute to **{e2011457-1546-43c5-a5fe-008deee3d3f0}** to run the application using Vista functionality.</span></span> <span data-ttu-id="fb9dc-269">Это может позволить приложению, разработанному для Windows Vista, работать в более поздней версии операционной системы.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-269">This can enable an application designed for Windows Vista to run on a later operating system.</span></span> <br/> <span data-ttu-id="fb9dc-270">Задайте для атрибута ID значение **{35138b9a-5d96-4fbd-8e2d-a2440225f93a}** , чтобы запустить приложение с помощью функции Windows 7.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-270">Set the Id attribute to **{35138b9a-5d96-4fbd-8e2d-a2440225f93a}** to run the application using Windows 7 functionality.</span></span><br/> <span data-ttu-id="fb9dc-271">Для приложений, поддерживающих функции Windows Vista, Windows 7 и Windows 8, не требуются отдельные манифесты.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-271">Applications that support Windows Vista, Windows 7, and Windows 8 functionality do not require separate manifests.</span></span> <span data-ttu-id="fb9dc-272">В этом случае добавьте идентификаторы GUID для всех операционных систем Windows.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-272">In this case, add the GUIDs for all the Windows operating systems.</span></span><br/> <span data-ttu-id="fb9dc-273">Сведения о поведении атрибута **ID** в Windows см. в статье [совместимость Windows 8 и Windows Server 2012 Cookbook](https://www.microsoft.com/download/details.aspx?id=27416).</span><span class="sxs-lookup"><span data-stu-id="fb9dc-273">For info about the **Id** attribute behavior in Windows, see the [Windows 8 and Windows Server 2012 Compatibility Cookbook](https://www.microsoft.com/download/details.aspx?id=27416).</span></span><br/> <span data-ttu-id="fb9dc-274">Следующие идентификаторы GUID соответствуют указанным операционным системам:</span><span class="sxs-lookup"><span data-stu-id="fb9dc-274">The following GUIDs correspond with the indicated operating systems:</span></span><br/> <span data-ttu-id="fb9dc-275">**{8e0f7a12-bfb3-4fe8-b9a5-48fd50a15a9a}** — > Windows 10, windows Server 2016 и windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="fb9dc-275">**{8e0f7a12-bfb3-4fe8-b9a5-48fd50a15a9a}** -> Windows 10, Windows Server 2016 and Windows Server 2019</span></span><br/> <span data-ttu-id="fb9dc-276">**{1f676c76-80e1-4239-95bb-83d0f6d0da78}** — > Windows 8.1 и Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="fb9dc-276">**{1f676c76-80e1-4239-95bb-83d0f6d0da78}** -> Windows 8.1 and Windows Server 2012 R2</span></span><br/> <span data-ttu-id="fb9dc-277">**{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}** — > Windows 8 и windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fb9dc-277">**{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}** -> Windows 8 and Windows Server 2012</span></span><br/> <span data-ttu-id="fb9dc-278">**{35138b9a-5d96-4fbd-8e2d-a2440225f93a}** — > Windows 7 и windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="fb9dc-278">**{35138b9a-5d96-4fbd-8e2d-a2440225f93a}** -> Windows 7 and Windows Server 2008 R2</span></span><br/> <span data-ttu-id="fb9dc-279">**{e2011457-1546-43c5-a5fe-008deee3d3f0}** — > Windows Vista и windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fb9dc-279">**{e2011457-1546-43c5-a5fe-008deee3d3f0}** -> Windows Vista and Windows Server 2008</span></span><br/> <span data-ttu-id="fb9dc-280">Вы можете протестировать это в Windows 7 или Windows 8. x, запустив монитор ресурсов (ресмон), перейдя на вкладку ЦП, щелкнув правой кнопкой мыши метки столбцов, выбрать столбец и проверить "контекст операционной системы".</span><span class="sxs-lookup"><span data-stu-id="fb9dc-280">You can test this on Windows 7 or Windows 8.x by running Resource Monitor (resmon), going to the CPU tab, right-clicking on the column labels, "Select Column...", and check "Operating System Context".</span></span> <span data-ttu-id="fb9dc-281">В Windows 8. x можно также найти этот столбец, доступный в диспетчере задач (панели Диспетчер задач).</span><span class="sxs-lookup"><span data-stu-id="fb9dc-281">On Windows 8.x, you can also find this column available in the Task Manager (taskmgr).</span></span> <span data-ttu-id="fb9dc-282">Содержимое столбца показывает наибольшее найденное значение или "Windows Vista" в качестве значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-282">The content of the column shows the highest value found or "Windows Vista" as the default.</span></span> <br/> |

<span id="maxVersionTested"></span><span id="maxversiontested"></span><span id="MAXVERSIONTESTED"></span>

### <a name="maxversiontested"></a><span data-ttu-id="fb9dc-283">maxversiontested укажите установленную</span><span class="sxs-lookup"><span data-stu-id="fb9dc-283">maxversiontested</span></span>

<span data-ttu-id="fb9dc-284">Элемент **maxversiontested укажите установленную** указывает максимальную версию Windows, для которой было протестировано приложение.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-284">The **maxversiontested** element specifies the maximum version of Windows that the application was tested against.</span></span> <span data-ttu-id="fb9dc-285">Он предназначен для использования в приложениях для настольных систем, использующих [острова XAML](/windows/apps/desktop/modernize/xaml-islands) и не развернутых в пакете MSIX.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-285">This is intended to be used by desktop applications that use [XAML Islands](/windows/apps/desktop/modernize/xaml-islands) and that are not deployed in an MSIX package.</span></span> <span data-ttu-id="fb9dc-286">Этот элемент поддерживается в Windows 10, версии 1903 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-286">This element is supported in Windows 10, version 1903, and later versions.</span></span>

<span data-ttu-id="fb9dc-287">Элемент **maxversiontested укажите установленную** имеет следующий атрибут.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-287">The **maxversiontested** element has the following attribute.</span></span> <span data-ttu-id="fb9dc-288">У него нет вложенных элементов.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-288">It has no subelements.</span></span>

| <span data-ttu-id="fb9dc-289">attribute</span><span class="sxs-lookup"><span data-stu-id="fb9dc-289">Attribute</span></span> | <span data-ttu-id="fb9dc-290">Описание</span><span class="sxs-lookup"><span data-stu-id="fb9dc-290">Description</span></span>    |
|-----------|----------------|
| <span data-ttu-id="fb9dc-291">**Id**</span><span class="sxs-lookup"><span data-stu-id="fb9dc-291">**Id**</span></span>    | <span data-ttu-id="fb9dc-292">Задайте для атрибута ID строку версии из 4 частей, которая указывает максимальную версию Windows, с которой было протестировано приложение.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-292">Set the Id attribute to a 4-part version string that specifies the maximum version of Windows that the application was tested against.</span></span> <span data-ttu-id="fb9dc-293">Например, "10.0.18226.0".</span><span class="sxs-lookup"><span data-stu-id="fb9dc-293">For example, "10.0.18226.0".</span></span> |

<span id="dependency"></span><span id="DEPENDENCY"></span>

### <a name="dependency"></a><span data-ttu-id="fb9dc-294">dependency</span><span class="sxs-lookup"><span data-stu-id="fb9dc-294">dependency</span></span>

<span data-ttu-id="fb9dc-295">Содержит по меньшей мере один **dependentAssembly**.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-295">Contains at least one **dependentAssembly**.</span></span> <span data-ttu-id="fb9dc-296">У него нет атрибутов.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-296">It has no attributes.</span></span> <span data-ttu-id="fb9dc-297">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-297">Optional.</span></span>

<span id="dependentAssembly"></span><span id="dependentassembly"></span><span id="DEPENDENTASSEMBLY"></span>

### <a name="dependentassembly"></a><span data-ttu-id="fb9dc-298">dependentAssembly</span><span class="sxs-lookup"><span data-stu-id="fb9dc-298">dependentAssembly</span></span>

<span data-ttu-id="fb9dc-299">Первый подэлемент **dependentAssembly** должен быть элементом **assemblyIdentity** , описывающим параллельную сборку, необходимую для приложения.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-299">The first subelement of **dependentAssembly** must be an **assemblyIdentity** element that describes a side-by-side assembly required by the application.</span></span> <span data-ttu-id="fb9dc-300">Каждое **dependentAssembly** должно находиться внутри только одной **зависимости**.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-300">Every **dependentAssembly** must be inside exactly one **dependency**.</span></span> <span data-ttu-id="fb9dc-301">У него нет атрибутов.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-301">It has no attributes.</span></span>

<span id="file"></span><span id="FILE"></span>

### <a name="file"></a><span data-ttu-id="fb9dc-302">файл</span><span class="sxs-lookup"><span data-stu-id="fb9dc-302">file</span></span>

<span data-ttu-id="fb9dc-303">Указывает файлы, являющиеся частными для приложения.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-303">Specifies files that are private to the application.</span></span> <span data-ttu-id="fb9dc-304">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-304">Optional.</span></span>

<span data-ttu-id="fb9dc-305">Элемент **File** содержит атрибуты, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-305">The **file** element has the attributes shown in the following table.</span></span>



| <span data-ttu-id="fb9dc-306">attribute</span><span class="sxs-lookup"><span data-stu-id="fb9dc-306">Attribute</span></span>   | <span data-ttu-id="fb9dc-307">Описание</span><span class="sxs-lookup"><span data-stu-id="fb9dc-307">Description</span></span>                                                                                             |
|-------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb9dc-308">**name**</span><span class="sxs-lookup"><span data-stu-id="fb9dc-308">**name**</span></span>    | <span data-ttu-id="fb9dc-309">Имя файла.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-309">Name of the file.</span></span> <span data-ttu-id="fb9dc-310">Например, Comctl32.dll.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-310">For example, Comctl32.dll.</span></span>                                                            |
| <span data-ttu-id="fb9dc-311">**hashAlg**</span><span class="sxs-lookup"><span data-stu-id="fb9dc-311">**hashalg**</span></span> | <span data-ttu-id="fb9dc-312">Алгоритм, используемый для создания хэша файла.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-312">Algorithm used to create a hash of the file.</span></span> <span data-ttu-id="fb9dc-313">Это значение должно быть SHA1.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-313">This value should be SHA1.</span></span>                                 |
| <span data-ttu-id="fb9dc-314">**hash**</span><span class="sxs-lookup"><span data-stu-id="fb9dc-314">**hash**</span></span>    | <span data-ttu-id="fb9dc-315">Хэш файла, на который ссылается имя.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-315">A hash of the file referred to by name.</span></span> <span data-ttu-id="fb9dc-316">Шестнадцатеричная строка длины в зависимости от хэш-алгоритма.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-316">A hexadecimal string of length depending on the hash algorithm.</span></span> |

<span id="activeCodePage"></span><span id="activecodepage"></span><span id="ACTIVECODEPAGE"></span>

### <a name="activecodepage"></a><span data-ttu-id="fb9dc-317">активекодепаже</span><span class="sxs-lookup"><span data-stu-id="fb9dc-317">activeCodePage</span></span>

<span data-ttu-id="fb9dc-318">Заставить процесс использовать UTF-8 в качестве кодовой страницы процесса.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-318">Force a process to use UTF-8 as the process code page.</span></span>

<span data-ttu-id="fb9dc-319">**активекодепаже** был добавлен в Windows версии 1903 (обновление 2019 мая).</span><span class="sxs-lookup"><span data-stu-id="fb9dc-319">**activeCodePage** was added in Windows Version 1903 (May 2019 Update).</span></span> <span data-ttu-id="fb9dc-320">Вы можете объявить это свойство и целевой объект или выполнить его в более ранних сборках Windows, но необходимо как обычно выполнять обнаружение и преобразование кодовых страниц прежних версий.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-320">You can declare this property and target/run on earlier Windows builds, but you must handle legacy code page detection and conversion as usual.</span></span> <span data-ttu-id="fb9dc-321">Дополнительные сведения см. [в разделе Использование кодовой страницы UTF-8](/windows/uwp/design/globalizing/use-utf8-code-page) .</span><span class="sxs-lookup"><span data-stu-id="fb9dc-321">See [Use the UTF-8 code page](/windows/uwp/design/globalizing/use-utf8-code-page) for details.</span></span>

<span data-ttu-id="fb9dc-322">Этот элемент не содержит атрибуты.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-322">This element has no attributes.</span></span> <span data-ttu-id="fb9dc-323">**UTF-8** является допустимым значением для элемента **активекодепаже** .</span><span class="sxs-lookup"><span data-stu-id="fb9dc-323">**UTF-8** is only valid value for **activeCodePage** element.</span></span>

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

### <a name="autoelevate"></a><span data-ttu-id="fb9dc-324">автоповышение</span><span class="sxs-lookup"><span data-stu-id="fb9dc-324">autoElevate</span></span>

<span data-ttu-id="fb9dc-325">Указывает, включен ли автоматический повышенный уровень прав.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-325">Specifies whether auto elevate is enabled.</span></span> <span data-ttu-id="fb9dc-326">**Значение true** указывает, что он включен.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-326">**TRUE** indicates that it is enabled.</span></span> <span data-ttu-id="fb9dc-327">У него нет атрибутов.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-327">It has no attributes.</span></span>

<span id="disableTheming"></span><span id="disabletheming"></span><span id="DISABLETHEMING"></span>

### <a name="disabletheming"></a><span data-ttu-id="fb9dc-328">дисаблесеминг</span><span class="sxs-lookup"><span data-stu-id="fb9dc-328">disableTheming</span></span>

<span data-ttu-id="fb9dc-329">Указывает, отключено ли предоставление элементов пользовательского интерфейса для темы.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-329">Specifies whether giving UI elements a theme is disabled.</span></span> <span data-ttu-id="fb9dc-330">**Значение true** указывает, что отключено.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-330">**TRUE** indicates disabled.</span></span> <span data-ttu-id="fb9dc-331">У него нет атрибутов.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-331">It has no attributes.</span></span>

<span id="disableWindowFiltering"></span><span id="disablewindowfiltering"></span><span id="DISABLEWINDOWFILTERING"></span>

### <a name="disablewindowfiltering"></a><span data-ttu-id="fb9dc-332">дисаблевиндовфилтеринг</span><span class="sxs-lookup"><span data-stu-id="fb9dc-332">disableWindowFiltering</span></span>

<span data-ttu-id="fb9dc-333">Указывает, следует ли отключить фильтрацию окон.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-333">Specifies whether to disable window filtering.</span></span> <span data-ttu-id="fb9dc-334">**True** — отключить фильтрацию окон, чтобы можно было перечислить иммерсивное окно с рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-334">**TRUE** disables window filtering so you can enumerate immersive windows from the desktop.</span></span> <span data-ttu-id="fb9dc-335">**дисаблевиндовфилтеринг** был добавлен в Windows 8 и не имеет атрибутов.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-335">**disableWindowFiltering** was added in Windows 8 and has no attributes.</span></span>

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

### <a name="dpiaware"></a><span data-ttu-id="fb9dc-336">дпиаваре</span><span class="sxs-lookup"><span data-stu-id="fb9dc-336">dpiAware</span></span>

<span data-ttu-id="fb9dc-337">Указывает, учитывается ли текущий процесс в точках на дюйм (DPI).</span><span class="sxs-lookup"><span data-stu-id="fb9dc-337">Specifies whether the current process is dots per inch (dpi) aware.</span></span>

<span data-ttu-id="fb9dc-338">**Windows 10, версия 1607:** Элемент **дпиаваре** игнорируется, если имеется элемент **дпиаваренесс** .</span><span class="sxs-lookup"><span data-stu-id="fb9dc-338">**Windows 10, version 1607:** The **dpiAware** element is ignored if the **dpiAwareness** element is present.</span></span> <span data-ttu-id="fb9dc-339">Можно включить оба элемента в манифест, если вы хотите указать другое поведение для Windows 10 версии 1607, чем для более ранней версии операционной системы.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-339">You can include both elements in a manifest if you want to specify a different behavior for Windows 10, version 1607 than for an earlier version of the operating system.</span></span>

<span data-ttu-id="fb9dc-340">В следующей таблице описывается поведение, получаемое в зависимости от наличия элемента **дпиаваре** и содержащегося в нем текста.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-340">The following table describes the behavior that results based upon the presence of the **dpiAware** element and the text that it contains.</span></span> <span data-ttu-id="fb9dc-341">В тексте элемента не учитывается регистр.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-341">The text within the element is not case-sensitive.</span></span>

| <span data-ttu-id="fb9dc-342">Состояние элемента **дпиаваре**</span><span class="sxs-lookup"><span data-stu-id="fb9dc-342">State of the **dpiAware** element</span></span> | <span data-ttu-id="fb9dc-343">Описание</span><span class="sxs-lookup"><span data-stu-id="fb9dc-343">Description</span></span>     |
|-----------------------------------|---------|
| <span data-ttu-id="fb9dc-344">Absent</span><span class="sxs-lookup"><span data-stu-id="fb9dc-344">Absent</span></span>                            | <span data-ttu-id="fb9dc-345">По умолчанию текущий процесс не знает dpi.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-345">The current process is dpi unaware by default.</span></span> <span data-ttu-id="fb9dc-346">Этот параметр можно изменить программным путем, вызвав функцию [**сетпроцессдпиаваренесс**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) или [**сетпроцессдпиаваре**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) .</span><span class="sxs-lookup"><span data-stu-id="fb9dc-346">You can programmatically change this setting by calling the [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) or [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) function.</span></span>                                                                                                                                                            |
| <span data-ttu-id="fb9dc-347">Содержит значение "true"</span><span class="sxs-lookup"><span data-stu-id="fb9dc-347">Contains "true"</span></span>                   | <span data-ttu-id="fb9dc-348">Текущий процесс учитывает dpi системы.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-348">The current process is system dpi aware.</span></span>                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="fb9dc-349">Содержит значение "false"</span><span class="sxs-lookup"><span data-stu-id="fb9dc-349">Contains "false"</span></span>                  | <span data-ttu-id="fb9dc-350">Windows **Vista, Windows 7 и Windows 8:** Поведение аналогично поведению, если **дпиаваре** отсутствует.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-350">**Windows Vista, Windows 7 and Windows 8:** The behavior is the same as when the **dpiAware** is absent.</span></span><br/> <span data-ttu-id="fb9dc-351">**Windows 8.1 и Windows 10:** Текущий процесс не знает dpi, и программное изменение этого параметра невозможно выполнить, вызвав функцию [**сетпроцессдпиаваренесс**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) или [**сетпроцессдпиаваре**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) .</span><span class="sxs-lookup"><span data-stu-id="fb9dc-351">**Windows 8.1 and Windows 10:** The current process is dpi unaware, and you cannot programmatically change this setting by calling the [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) or [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) function.</span></span><br/> |
| <span data-ttu-id="fb9dc-352">Содержит "true/PM"</span><span class="sxs-lookup"><span data-stu-id="fb9dc-352">Contains "true/pm"</span></span>                | <span data-ttu-id="fb9dc-353">Windows **Vista, Windows 7 и Windows 8:** Текущий процесс учитывает dpi системы.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-353">**Windows Vista, Windows 7 and Windows 8:** The current process is system dpi aware.</span></span><br/> <span data-ttu-id="fb9dc-354">**Windows 8.1 и Windows 10:** Текущий процесс учитывает dpi для каждого монитора.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-354">**Windows 8.1 and Windows 10:** The current process is per-monitor dpi aware.</span></span><br/>                                                                                                                                                                                                          |
| <span data-ttu-id="fb9dc-355">Содержит "на монитор"</span><span class="sxs-lookup"><span data-stu-id="fb9dc-355">Contains "per monitor"</span></span>            | <span data-ttu-id="fb9dc-356">Windows **Vista, Windows 7 и Windows 8:** Поведение аналогично поведению, если **дпиаваре** отсутствует.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-356">**Windows Vista, Windows 7 and Windows 8:** The behavior is the same as when the **dpiAware** is absent.</span></span><br/> <span data-ttu-id="fb9dc-357">**Windows 8.1 и Windows 10:** Текущий процесс учитывает dpi для каждого монитора.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-357">**Windows 8.1 and Windows 10:** The current process is per-monitor dpi aware.</span></span><br/>                                                                                                                                                                                      |
| <span data-ttu-id="fb9dc-358">Содержит любую другую строку</span><span class="sxs-lookup"><span data-stu-id="fb9dc-358">Contains any other string</span></span>         | <span data-ttu-id="fb9dc-359">Windows **Vista, Windows 7 и Windows 8:** Поведение аналогично поведению, если **дпиаваре** отсутствует.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-359">**Windows Vista, Windows 7 and Windows 8:** The behavior is the same as when the **dpiAware** is absent.</span></span><br/> <span data-ttu-id="fb9dc-360">**Windows 8.1 и Windows 10:** Текущий процесс не знает dpi, и программное изменение этого параметра невозможно выполнить, вызвав функцию [**сетпроцессдпиаваренесс**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) или [**сетпроцессдпиаваре**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) .</span><span class="sxs-lookup"><span data-stu-id="fb9dc-360">**Windows 8.1 and Windows 10:** The current process is dpi unaware, and you cannot programmatically change this setting by calling the [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) or [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) function.</span></span><br/> |

<span data-ttu-id="fb9dc-361">Дополнительные сведения о параметрах осведомленности о dpi см. в разделе [Сравнение уровней осведомленности о dpi](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot)).</span><span class="sxs-lookup"><span data-stu-id="fb9dc-361">For more information about dpi awareness settings, see [Comparison of DPI Awareness Levels](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot)).</span></span>

<span data-ttu-id="fb9dc-362">**дпиаваре** не имеет атрибутов.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-362">**dpiAware** has no attributes.</span></span>

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

### <a name="dpiawareness"></a><span data-ttu-id="fb9dc-363">дпиаваренесс</span><span class="sxs-lookup"><span data-stu-id="fb9dc-363">dpiAwareness</span></span>

<span data-ttu-id="fb9dc-364">Указывает, учитывается ли текущий процесс в точках на дюйм (DPI).</span><span class="sxs-lookup"><span data-stu-id="fb9dc-364">Specifies whether the current process is dots per inch (dpi) aware.</span></span>

<span data-ttu-id="fb9dc-365">Минимальная версия операционной системы, поддерживающая элемент **дпиаваренесс** , — Windows 10, версия 1607.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-365">The minimum version of the operating system that supports the **dpiAwareness** element is Windows 10, version 1607.</span></span> <span data-ttu-id="fb9dc-366">Для версий, которые поддерживают элемент **дпиаваренесс** , **дпиаваренесс** переопределяет элемент **дпиаваре** .</span><span class="sxs-lookup"><span data-stu-id="fb9dc-366">For versions that support the **dpiAwareness** element, the **dpiAwareness** overrides the **dpiAware** element.</span></span> <span data-ttu-id="fb9dc-367">Можно включить оба элемента в манифест, если вы хотите указать другое поведение для Windows 10 версии 1607, чем для более ранней версии операционной системы.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-367">You can include both elements in a manifest if you want to specify a different behavior for Windows 10, version 1607 than for an earlier version of the operating system.</span></span>

<span data-ttu-id="fb9dc-368">Элемент **дпиаваренесс** может содержать один элемент или список элементов с разделителями-запятыми.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-368">The **dpiAwareness** element can contain a single item or a list of comma-separated items.</span></span> <span data-ttu-id="fb9dc-369">В последнем случае используется первый (крайний левый) элемент в списке, распознанном операционной системой.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-369">In the latter case, the first (leftmost) item in the list recognized by the operating system is used.</span></span> <span data-ttu-id="fb9dc-370">Таким образом можно указать различные варианты поведения, поддерживаемые в будущих версиях операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-370">In this way, you can specify different behaviors supported in future Windows operating system versions.</span></span>

<span data-ttu-id="fb9dc-371">В следующей таблице описывается поведение, получаемое в зависимости от наличия элемента **дпиаваренесс** и содержащегося в нем текста в его левом распознанном элементе.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-371">The following table describes the behavior that results based upon the presence of the **dpiAwareness** element and the text that it contains in its leftmost recognized item.</span></span> <span data-ttu-id="fb9dc-372">В тексте элемента не учитывается регистр.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-372">The text within the element is not case-sensitive.</span></span>

| <span data-ttu-id="fb9dc-373">состояние элемента **дпиаваренесс** :</span><span class="sxs-lookup"><span data-stu-id="fb9dc-373">**dpiAwareness** element status:</span></span>        | <span data-ttu-id="fb9dc-374">Описание</span><span class="sxs-lookup"><span data-stu-id="fb9dc-374">Description</span></span>                          |
|-----------------------------------------|-------------------------------------------|
| <span data-ttu-id="fb9dc-375">Отсутствует элемент</span><span class="sxs-lookup"><span data-stu-id="fb9dc-375">Element is absent</span></span>                       | <span data-ttu-id="fb9dc-376">Элемент **дпиаваре** указывает, учитывается ли в процессе разрешение dpi.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-376">The **dpiAware** element specifies whether the process is dpi aware.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="fb9dc-377">Не содержит распознанные элементы</span><span class="sxs-lookup"><span data-stu-id="fb9dc-377">Contains no recognized items</span></span>            | <span data-ttu-id="fb9dc-378">По умолчанию текущий процесс не знает dpi.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-378">The current process is dpi unaware by default.</span></span> <span data-ttu-id="fb9dc-379">Этот параметр можно изменить программным путем, вызвав функцию [**сетпроцессдпиаваренесс**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) или [**сетпроцессдпиаваре**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) .</span><span class="sxs-lookup"><span data-stu-id="fb9dc-379">You can programmatically change this setting by calling the [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) or [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) function.</span></span> |
| <span data-ttu-id="fb9dc-380">Первый распознанный элемент — "System"</span><span class="sxs-lookup"><span data-stu-id="fb9dc-380">First recognized item is "system"</span></span>       | <span data-ttu-id="fb9dc-381">Текущий процесс учитывает dpi системы.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-381">The current process is system dpi aware.</span></span>                                                                                                                                                                                               |
| <span data-ttu-id="fb9dc-382">Первый распознанный элемент — "пермонитор"</span><span class="sxs-lookup"><span data-stu-id="fb9dc-382">First recognized item is "permonitor"</span></span>   | <span data-ttu-id="fb9dc-383">Текущий процесс учитывает dpi для каждого монитора.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-383">The current process is per-monitor dpi aware.</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="fb9dc-384">Первый распознанный элемент — "permonitorv2"</span><span class="sxs-lookup"><span data-stu-id="fb9dc-384">First recognized item is "permonitorv2"</span></span> | <span data-ttu-id="fb9dc-385">В текущем процессе используется контекст осведомленности по dpi для каждого монитора.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-385">The current process uses the per-monitor-v2 dpi awareness context.</span></span> <span data-ttu-id="fb9dc-386">Этот элемент будет распознан только в Windows 10 версии 1703 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-386">This item will only be recognized on Windows 10 version 1703 or later.</span></span>                                                                                              |
| <span data-ttu-id="fb9dc-387">Первый распознанный элемент «не осведомлен»</span><span class="sxs-lookup"><span data-stu-id="fb9dc-387">First recognized item is "unaware"</span></span>      | <span data-ttu-id="fb9dc-388">Текущий процесс является неосведомленным от dpi.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-388">The current process is dpi unaware.</span></span> <span data-ttu-id="fb9dc-389">Вы **не можете** программно изменить этот параметр, вызвав функцию [**сетпроцессдпиаваренесс**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) или [**сетпроцессдпиаваре**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) .</span><span class="sxs-lookup"><span data-stu-id="fb9dc-389">You **cannot** programmatically change this setting by calling the [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) or [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) function.</span></span>      |

<span data-ttu-id="fb9dc-390">Дополнительные сведения о параметрах осведомленности о разрешении, поддерживаемых этим элементом, см. в разделе [ \_ Поддержка dpi](/windows/desktop/api/windef/ne-windef-dpi_awareness) и [ \_ \_ контекст осведомленности](/windows/desktop/hidpi/dpi-awareness-context)о dpi.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-390">For more information about dpi awareness settings supported by this element, see [DPI\_AWARENESS](/windows/desktop/api/windef/ne-windef-dpi_awareness) and [DPI\_AWARENESS\_CONTEXT](/windows/desktop/hidpi/dpi-awareness-context).</span></span>

<span data-ttu-id="fb9dc-391">**дпиаваренесс** не имеет атрибутов.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-391">**dpiAwareness** has no attributes.</span></span>

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

### <a name="gdiscaling"></a><span data-ttu-id="fb9dc-392">гдискалинг</span><span class="sxs-lookup"><span data-stu-id="fb9dc-392">gdiScaling</span></span>

<span data-ttu-id="fb9dc-393">Указывает, включено ли масштабирование GDI.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-393">Specifies whether GDI scaling is enabled.</span></span> <span data-ttu-id="fb9dc-394">Минимальная версия операционной системы, поддерживающая элемент **гдискалинг** , — Windows 10 версии 1703.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-394">The minimum version of the operating system that supports the **gdiScaling** element is Windows 10 version 1703.</span></span>

<span data-ttu-id="fb9dc-395">Платформа GDI (интерфейс графических устройств) может применять масштабирование DPI к примитивам и тексту на уровне отдельных мониторов без обновления самого приложения.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-395">The GDI (graphics device interface) framework can apply DPI scaling to primitives and text on a per-monitor basis without updates to the application itself.</span></span> <span data-ttu-id="fb9dc-396">Это может быть полезно для приложений GDI, которые больше не обновляются.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-396">This can be useful for GDI applications no longer being actively updated.</span></span>

<span data-ttu-id="fb9dc-397">Невекторная графика (например, точечные рисунки, значки или панели инструментов) не может масштабироваться этим элементом.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-397">Non-vector graphics (such as bitmaps, icons, or toolbars) cannot be scaled by this element.</span></span> <span data-ttu-id="fb9dc-398">Кроме того, графика и текст, отображаемые в растровых изображениях, динамически создаваемые приложениями, также не могут масштабироваться этим элементом.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-398">In addition, graphics and text appearing within bitmaps dynamically constructed by applications also cannot be scaled by this element.</span></span>

<span data-ttu-id="fb9dc-399">**Значение true** указывает, что этот элемент включен.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-399">**TRUE** indicates that this element is enabled.</span></span> <span data-ttu-id="fb9dc-400">У него нет атрибутов.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-400">It has no attributes.</span></span>


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

### <a name="highresolutionscrollingaware"></a><span data-ttu-id="fb9dc-401">хигхресолутионскроллингаваре</span><span class="sxs-lookup"><span data-stu-id="fb9dc-401">highResolutionScrollingAware</span></span>

<span data-ttu-id="fb9dc-402">Указывает, включено ли разрешение на прокрутку с высоким разрешением.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-402">Specifies whether high-resolution-scrolling aware is enabled.</span></span> <span data-ttu-id="fb9dc-403">**Значение true** указывает, что он включен.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-403">**TRUE** indicates that it is enabled.</span></span> <span data-ttu-id="fb9dc-404">У него нет атрибутов.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-404">It has no attributes.</span></span>

<span id="longPathAware"></span><span id="longpathaware"></span><span id="LONGPATHAWARE"></span>

### <a name="longpathaware"></a><span data-ttu-id="fb9dc-405">лонгпасаваре</span><span class="sxs-lookup"><span data-stu-id="fb9dc-405">longPathAware</span></span>

<span data-ttu-id="fb9dc-406">Включает длинные пути, длина которых превышает **MAX_PATH** .</span><span class="sxs-lookup"><span data-stu-id="fb9dc-406">Enables long paths that exceed **MAX_PATH** in length.</span></span> <span data-ttu-id="fb9dc-407">Этот элемент поддерживается в Windows 10, версии 1607 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-407">This element is supported in Windows 10, version 1607, and later.</span></span> <span data-ttu-id="fb9dc-408">Дополнительные сведения см. в [этой статье](../fileio/maximum-file-path-limitation.md).</span><span class="sxs-lookup"><span data-stu-id="fb9dc-408">For more information, see [this article](../fileio/maximum-file-path-limitation.md).</span></span>

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

### <a name="printerdriverisolation"></a><span data-ttu-id="fb9dc-409">принтердриверисолатион</span><span class="sxs-lookup"><span data-stu-id="fb9dc-409">printerDriverIsolation</span></span>

<span data-ttu-id="fb9dc-410">Указывает, включена ли изоляция драйвера принтера.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-410">Specifies whether printer driver isolation is enabled.</span></span> <span data-ttu-id="fb9dc-411">**Значение true** указывает, что он включен.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-411">**TRUE** indicates that it is enabled.</span></span> <span data-ttu-id="fb9dc-412">У него нет атрибутов.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-412">It has no attributes.</span></span> <span data-ttu-id="fb9dc-413">Изоляция драйвера принтера повышает надежность службы печати Windows, позволяя драйверам принтера выполняться в процессах, отдельных от процесса, в котором работает диспетчер очереди печати.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-413">Printer driver isolation improves the reliability of the Windows print service by enabling printer drivers to run in processes that are separate from the process in which the print spooler runs.</span></span> <span data-ttu-id="fb9dc-414">Поддержка изоляции драйвера принтера начата в Windows 7 и Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-414">Support for printer driver isolation started in Windows 7 and Windows Server 2008 R2.</span></span> <span data-ttu-id="fb9dc-415">Приложение может объявить изоляцию драйвера принтера в своем манифесте приложения, чтобы изолировать себя от драйвера принтера и повысить его надежность.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-415">An app can declare printer driver isolation in its app manifest to isolate itself from the printer driver and improve its reliability.</span></span> <span data-ttu-id="fb9dc-416">Это значит, что приложение не будет завершаться сбоем, если в драйвере принтера произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-416">That is, the app won't crash if the printer driver has an error.</span></span>


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

### <a name="ultrahighresolutionscrollingaware"></a><span data-ttu-id="fb9dc-417">ултрахигхресолутионскроллингаваре</span><span class="sxs-lookup"><span data-stu-id="fb9dc-417">ultraHighResolutionScrollingAware</span></span>

<span data-ttu-id="fb9dc-418">Указывает, включено ли разрешение на прокрутку Ultra-High-resolution.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-418">Specifies whether ultra-high-resolution-scrolling aware is enabled.</span></span> <span data-ttu-id="fb9dc-419">**Значение true** указывает, что он включен.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-419">**TRUE** indicates that it is enabled.</span></span> <span data-ttu-id="fb9dc-420">У него нет атрибутов.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-420">It has no attributes.</span></span>

<span id="msix"></span><span id="MSIX"></span>

### <a name="msix"></a><span data-ttu-id="fb9dc-421">msix</span><span class="sxs-lookup"><span data-stu-id="fb9dc-421">msix</span></span>

<span data-ttu-id="fb9dc-422">Указывает сведения об удостоверении [разреженного пакета MSIX](/windows/apps/desktop/modernize/grant-identity-to-nonpackaged-apps) для текущего приложения.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-422">Specifies the identity info of a [sparse MSIX package](/windows/apps/desktop/modernize/grant-identity-to-nonpackaged-apps) for the current application.</span></span> <span data-ttu-id="fb9dc-423">Этот элемент поддерживается в Windows 10, версии 2004 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-423">This element is supported in Windows 10, version 2004, and later versions.</span></span>

<span data-ttu-id="fb9dc-424">Элемент **msix** должен находиться в пространстве имен `urn:schemas-microsoft-com:msix.v1` .</span><span class="sxs-lookup"><span data-stu-id="fb9dc-424">The **msix** element must be in the namespace `urn:schemas-microsoft-com:msix.v1`.</span></span> <span data-ttu-id="fb9dc-425">Он содержит атрибуты, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-425">It has the attributes shown in the following table.</span></span>

| <span data-ttu-id="fb9dc-426">attribute</span><span class="sxs-lookup"><span data-stu-id="fb9dc-426">Attribute</span></span>   | <span data-ttu-id="fb9dc-427">Описание</span><span class="sxs-lookup"><span data-stu-id="fb9dc-427">Description</span></span>                                                                                             |
|-------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb9dc-428">**publisher**</span><span class="sxs-lookup"><span data-stu-id="fb9dc-428">**publisher**</span></span>    | <span data-ttu-id="fb9dc-429">Описание сведений об издателе.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-429">Describes the publisher information.</span></span> <span data-ttu-id="fb9dc-430">Это значение должно соответствовать атрибуту **издателя** в элементе [Identity](/uwp/schemas/appxpackage/uapmanifestschema/element-identity) манифеста разреженного пакета.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-430">This value must match the **Publisher** attribute in the [Identity](/uwp/schemas/appxpackage/uapmanifestschema/element-identity) element in your sparse package manifest.</span></span> |
| <span data-ttu-id="fb9dc-431">**packageName**</span><span class="sxs-lookup"><span data-stu-id="fb9dc-431">**packageName**</span></span> | <span data-ttu-id="fb9dc-432">Описывает содержимое пакета.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-432">Describes the contents of the package.</span></span> <span data-ttu-id="fb9dc-433">Это значение должно соответствовать атрибуту **Name** в элементе [Identity](/uwp/schemas/appxpackage/uapmanifestschema/element-identity) манифеста разреженного пакета.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-433">This value must match the **Name** attribute in the [Identity](/uwp/schemas/appxpackage/uapmanifestschema/element-identity) element in your sparse package manifest.</span></span>    |
| <span data-ttu-id="fb9dc-434">**applicationId**</span><span class="sxs-lookup"><span data-stu-id="fb9dc-434">**applicationId**</span></span>    | <span data-ttu-id="fb9dc-435">Уникальный идентификатор приложения.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-435">The unique identifier of the application.</span></span> <span data-ttu-id="fb9dc-436">Это значение должно соответствовать атрибуту **ID** в элементе [Application](/uwp/schemas/appxpackage/uapmanifestschema/element-application) в манифесте разреженного пакета.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-436">This value must match the **Id** attribute in the [Application](/uwp/schemas/appxpackage/uapmanifestschema/element-application) element in your sparse package manifest.</span></span>  |

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

### <a name="heaptype"></a><span data-ttu-id="fb9dc-437">хеаптипе</span><span class="sxs-lookup"><span data-stu-id="fb9dc-437">heapType</span></span>

<span data-ttu-id="fb9dc-438">Переопределяет реализацию кучи по умолчанию для использования [API кучи Win32](../Memory/heap-functions.md) .</span><span class="sxs-lookup"><span data-stu-id="fb9dc-438">Overrides the default heap implementation for the [Win32 heap APIs](../Memory/heap-functions.md) to use.</span></span>

* <span data-ttu-id="fb9dc-439">Значение **сегменсеап** указывает, что будет использоваться куча сегмента.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-439">The value **SegmentHeap** indicates that segment heap will be used.</span></span> <span data-ttu-id="fb9dc-440">Куча сегментов — это современная реализация кучи, которая обычно сокращает общее использование памяти.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-440">Segment heap is a modern heap implementation that will generally reduce your overall memory usage.</span></span> <span data-ttu-id="fb9dc-441">Этот элемент поддерживается в Windows 10, версия 2004 (сборка 19041) и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-441">This element is supported in Windows 10, version 2004 (build 19041) and later.</span></span>
* <span data-ttu-id="fb9dc-442">Все остальные значения игнорируются.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-442">All other values are ignored.</span></span>

<span data-ttu-id="fb9dc-443">Этот элемент не содержит атрибуты.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-443">This element has no attributes.</span></span>

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

## <a name="example"></a><span data-ttu-id="fb9dc-444">Пример</span><span class="sxs-lookup"><span data-stu-id="fb9dc-444">Example</span></span>

<span data-ttu-id="fb9dc-445">Ниже приведен пример манифеста приложения для приложения с именем MySampleApp.exe.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-445">The following is an example of an application manifest for an application named MySampleApp.exe.</span></span> <span data-ttu-id="fb9dc-446">Приложение использует Самплеассембли параллельную сборку.</span><span class="sxs-lookup"><span data-stu-id="fb9dc-446">The application consumes the SampleAssembly side-by-side assembly.</span></span>

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
