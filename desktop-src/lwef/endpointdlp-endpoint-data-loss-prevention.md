---
description: Интерфейсы API защиты от потери данных (DLP) Endpoint позволяют приложениям уведомлять ОС до и после определенных операций, таких как открытие или сохранение файла.
title: Защита от потери данных конечной точки
ms.topic: article
ms.date: 03/18/2021
ms.openlocfilehash: 3b8576f9eadd0037eca56c0ba183ea1d1825679a
ms.sourcegitcommit: 8b543a86e551cb5b4270a3cc3590ad0758fb6156
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2021
ms.locfileid: "107526083"
---
# <a name="endpoint-data-loss-prevention"></a><span data-ttu-id="dc590-103">Защита от потери данных конечной точки</span><span class="sxs-lookup"><span data-stu-id="dc590-103">Endpoint data loss prevention</span></span>

<span data-ttu-id="dc590-104">Windows 10 реализует механизмы, помогающие предотвратить потери данных для конфиденциальных файлов.</span><span class="sxs-lookup"><span data-stu-id="dc590-104">Windows 10 implements mechanisms that help to prevent data loss for sensitive files.</span></span> <span data-ttu-id="dc590-105">Интерфейсы API защиты от потери данных (DLP) Endpoint позволяют приложениям уведомлять ОС до и после определенных операций, таких как открытие или сохранение файла.</span><span class="sxs-lookup"><span data-stu-id="dc590-105">The endpoint data loss prevention (DLP) APIs allow applications to notify the OS before and after certain operations, such as opening or saving a file.</span></span> <span data-ttu-id="dc590-106">Эти уведомления служат в качестве подсказок, которые позволяют системе оптимизировать операции потери данных.</span><span class="sxs-lookup"><span data-stu-id="dc590-106">These notifications serve as "hints" that allow the system to optimize data loss operations.</span></span>

## <a name="location-of-the-dlp-dll"></a><span data-ttu-id="dc590-107">Расположение библиотеки DLL DLP</span><span class="sxs-lookup"><span data-stu-id="dc590-107">Location of the DLP dll</span></span>

<span data-ttu-id="dc590-108">Так как библиотека DLL защиты конечной точки не входит в состав Windows SDK, приложениям потребуется вручную загрузить библиотеку DLL во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="dc590-108">Since the endpoint DLP dll isn't bundled with the Windows SDK, applications will need to load the dll manually at runtime.</span></span> <span data-ttu-id="dc590-109">Путь к расположению библиотеки DLL хранится в реестре.</span><span class="sxs-lookup"><span data-stu-id="dc590-109">The path to the dll location is stored in the registry.</span></span> <span data-ttu-id="dc590-110">В следующей таблице перечислены разделы и значения реестра, в которых хранятся эти сведения.</span><span class="sxs-lookup"><span data-stu-id="dc590-110">The following table lists the registry keys and values that store this information.</span></span> <span data-ttu-id="dc590-111">Эти пути определяются как константы в приведенном ниже листинге кода ендпоинтдлп. h для удобства разработчиков.</span><span class="sxs-lookup"><span data-stu-id="dc590-111">These paths are defined as constants in the sample endpointdlp.h code listing provided below as a convenience for developers.</span></span>

| <span data-ttu-id="dc590-112">Константа</span><span class="sxs-lookup"><span data-stu-id="dc590-112">Constant</span></span> | <span data-ttu-id="dc590-113">Значение</span><span class="sxs-lookup"><span data-stu-id="dc590-113">Value</span></span> | <span data-ttu-id="dc590-114">Описание</span><span class="sxs-lookup"><span data-stu-id="dc590-114">Description</span></span>   |
|----------|-------|---------------|
| <span data-ttu-id="dc590-115">ENDPOINTDLP_DLL_NAME</span><span class="sxs-lookup"><span data-stu-id="dc590-115">ENDPOINTDLP_DLL_NAME</span></span> | <span data-ttu-id="dc590-116">"EndpointDlp.dll"</span><span class="sxs-lookup"><span data-stu-id="dc590-116">"EndpointDlp.dll"</span></span> | <span data-ttu-id="dc590-117">Имя DLL-библиотеки DLP конечной точки, предоставляющей API</span><span class="sxs-lookup"><span data-stu-id="dc590-117">The name of the Endpoint DLP DLL that provides the API</span></span> |
| <span data-ttu-id="dc590-118">ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY</span><span class="sxs-lookup"><span data-stu-id="dc590-118">ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY</span></span> | <span data-ttu-id="dc590-119">"Программное обеспечение \\ \\ защитника Microsoft Windows"</span><span class="sxs-lookup"><span data-stu-id="dc590-119">"SOFTWARE\\Microsoft\\Windows Defender"</span></span> | <span data-ttu-id="dc590-120">Раздел реестра защитника Windows в HKLM, где хранятся параметры DLP конечной точки</span><span class="sxs-lookup"><span data-stu-id="dc590-120">Windows Defender registry key under HKLM where some Endpoint DLP settings are stored</span></span> |
| <span data-ttu-id="dc590-121">ENDPOINTDLP_DLL_INSTALL_LOCATION_REGKEY</span><span class="sxs-lookup"><span data-stu-id="dc590-121">ENDPOINTDLP_DLL_INSTALL_LOCATION_REGKEY</span></span> | <span data-ttu-id="dc590-122">Значение ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY</span><span class="sxs-lookup"><span data-stu-id="dc590-122">Value of ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY</span></span> |  <span data-ttu-id="dc590-123">Путь реестра в разделе HKLM Key, из которого можно получить расположение установки EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="dc590-123">The registry path under HKLM key from which the EndpointDlp.dll install location can be obtained</span></span> |
| <span data-ttu-id="dc590-124">ENDPOINTDLP_DLL_INSTALL_LOCATION_REGVALUE</span><span class="sxs-lookup"><span data-stu-id="dc590-124">ENDPOINTDLP_DLL_INSTALL_LOCATION_REGVALUE</span></span> | <span data-ttu-id="dc590-125">InstallLocation</span><span class="sxs-lookup"><span data-stu-id="dc590-125">"InstallLocation"</span></span> | <span data-ttu-id="dc590-126">Значение реестра в разделе ENDPOINTDLP_DLL_INSTALL_LOCATION_REGKEY, в котором хранится расположение установки EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="dc590-126">The registry value under ENDPOINTDLP_DLL_INSTALL_LOCATION_REGKEY in which the EndpointDlp.dll install location is stored</span></span> |
| <span data-ttu-id="dc590-127">ENDPOINTDLP_DLL_WOW64_X86_INSTALL_LOCATION_SUFFIX</span><span class="sxs-lookup"><span data-stu-id="dc590-127">ENDPOINTDLP_DLL_WOW64_X86_INSTALL_LOCATION_SUFFIX</span></span> | <span data-ttu-id="dc590-128">с</span><span class="sxs-lookup"><span data-stu-id="dc590-128">"x86"</span></span> | <span data-ttu-id="dc590-129">На платформах x64 объедините этот каталог, чтобы получить версию x86 EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="dc590-129">On x64 platforms, concatenate this directory to obtain the x86 version of EndpointDlp.dll</span></span> |

## <a name="check-if-endpoint-dlp-is-enabled"></a><span data-ttu-id="dc590-130">Проверка включения DLP в конечной точке</span><span class="sxs-lookup"><span data-stu-id="dc590-130">Check if endpoint DLP is enabled</span></span>

<span data-ttu-id="dc590-131">Чтобы определить, включена ли в системе поддержка конечной точки DLP, проверьте следующее значение раздела реестра.</span><span class="sxs-lookup"><span data-stu-id="dc590-131">To determine if endpoint DLP is enabled on the system, check the following registry key value.</span></span> 

| <span data-ttu-id="dc590-132">Константа</span><span class="sxs-lookup"><span data-stu-id="dc590-132">Constant</span></span> | <span data-ttu-id="dc590-133">Значение</span><span class="sxs-lookup"><span data-stu-id="dc590-133">Value</span></span> | <span data-ttu-id="dc590-134">Описание</span><span class="sxs-lookup"><span data-stu-id="dc590-134">Description</span></span>   |
|----------|-------|---------------|
| <span data-ttu-id="dc590-135">ENDPOINTDLP_ENABLED_FLAG_REGKEY</span><span class="sxs-lookup"><span data-stu-id="dc590-135">ENDPOINTDLP_ENABLED_FLAG_REGKEY</span></span> |  <span data-ttu-id="dc590-136">" \\ Функции"</span><span class="sxs-lookup"><span data-stu-id="dc590-136">"\\Features"</span></span> | <span data-ttu-id="dc590-137">Путь к ключу флага включения защиты от потери данных в разделе (HKLM) ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY</span><span class="sxs-lookup"><span data-stu-id="dc590-137">The path to the Endpoint DLP enabled flag key under (HKLM) ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY</span></span> |
| <span data-ttu-id="dc590-138">ENDPOINTDLP_ENABLED_FLAG_REGVALUE</span><span class="sxs-lookup"><span data-stu-id="dc590-138">ENDPOINTDLP_ENABLED_FLAG_REGVALUE</span></span> | <span data-ttu-id="dc590-139">"Сенседлпенаблед"</span><span class="sxs-lookup"><span data-stu-id="dc590-139">"SenseDlpEnabled"</span></span> | <span data-ttu-id="dc590-140">Значение реестра в разделе ENDPOINTDLP_ENABLED_FLAG_REGKEY, содержащее раздел реестра с флагом DLP Enabled</span><span class="sxs-lookup"><span data-stu-id="dc590-140">The registry value under ENDPOINTDLP_ENABLED_FLAG_REGKEY containing the DLP enabled flag registry key</span></span>

## <a name="endpoint-dlp-apis"></a><span data-ttu-id="dc590-141">API-интерфейсы защиты конечной точки</span><span class="sxs-lookup"><span data-stu-id="dc590-141">Endpoint DLP APIs</span></span>

<span data-ttu-id="dc590-142">В следующих таблицах перечислены интерфейсы API, предоставляемые библиотекой DLL DLP конечной точки.</span><span class="sxs-lookup"><span data-stu-id="dc590-142">The following tables list the APIs provided by the endpoint DLP dll.</span></span>

### <a name="initialization-and-versioning"></a><span data-ttu-id="dc590-143">Инициализация и управление версиями</span><span class="sxs-lookup"><span data-stu-id="dc590-143">Initialization and versioning</span></span>

| <span data-ttu-id="dc590-144">API</span><span class="sxs-lookup"><span data-stu-id="dc590-144">API</span></span> | <span data-ttu-id="dc590-145">Описание</span><span class="sxs-lookup"><span data-stu-id="dc590-145">Description</span></span> |
|-----|-------------|
| [<span data-ttu-id="dc590-146">длпинитиализинфорцементмоде</span><span class="sxs-lookup"><span data-stu-id="dc590-146">DlpInitializeEnforcementMode</span></span>](endpointdlp-dlpinitializeenforcementmode.md)                       | <span data-ttu-id="dc590-147">Уведомляет систему о требуемых режимах применения для набора операций защиты от потери данных в конечной точке.</span><span class="sxs-lookup"><span data-stu-id="dc590-147">Notifies the system of the desired enforcement modes for a set of endpoint Data Loss Prevention (DLP) operations.</span></span>                                  |
| [<span data-ttu-id="dc590-148">длпжетенфорцементапиверсион</span><span class="sxs-lookup"><span data-stu-id="dc590-148">DlpGetEnforcementApiVersion</span></span>](endpointdlp-dlpgetenforcementapiversion.md)                       | <span data-ttu-id="dc590-149">Извлекает версию API защиты от потери данных для конечной точки на текущем устройстве.</span><span class="sxs-lookup"><span data-stu-id="dc590-149">Retrieves the version of the endpoint Data Loss Prevention (DLP) API on the current device.</span></span>                                  |


### <a name="document-operations"></a><span data-ttu-id="dc590-150">Операции с документом</span><span class="sxs-lookup"><span data-stu-id="dc590-150">Document operations</span></span>

| <span data-ttu-id="dc590-151">API</span><span class="sxs-lookup"><span data-stu-id="dc590-151">API</span></span> | <span data-ttu-id="dc590-152">Описание</span><span class="sxs-lookup"><span data-stu-id="dc590-152">Description</span></span> |
|-----|-------------|
| [<span data-ttu-id="dc590-153">длпнотифипреопендокумент</span><span class="sxs-lookup"><span data-stu-id="dc590-153">DlpNotifyPreOpenDocument</span></span>](endpointdlp-dlpnotifypreopendocument.md) | <span data-ttu-id="dc590-154">Предоставляет системе сведения о документе до запуска операции открытия.</span><span class="sxs-lookup"><span data-stu-id="dc590-154">Provides the system with information about a document before the open operation is initiated.</span></span> |
| [<span data-ttu-id="dc590-155">длпнотифипостопендокумент</span><span class="sxs-lookup"><span data-stu-id="dc590-155">DlpNotifyPostOpenDocument</span></span>](endpointdlp-dlpnotifypostopendocument.md) | <span data-ttu-id="dc590-156">Предоставляет системе сведения о документе после завершения операции открытия.</span><span class="sxs-lookup"><span data-stu-id="dc590-156">Provides the system with information about a document after the open operation is completed.</span></span>  |
| [<span data-ttu-id="dc590-157">длпнотификлоседокумент</span><span class="sxs-lookup"><span data-stu-id="dc590-157">DlpNotifyCloseDocument</span></span>](endpointdlp-dlpnotifyclosedocument.md)                       | <span data-ttu-id="dc590-158">Предоставляет системе сведения о документе до инициирования операции закрытия документа.</span><span class="sxs-lookup"><span data-stu-id="dc590-158">Provides the system with information about a document before the document close operation is initiated.</span></span>                                  |
| [<span data-ttu-id="dc590-159">длпнотифипреопендокументфиле</span><span class="sxs-lookup"><span data-stu-id="dc590-159">DlpNotifyPreOpenDocumentFile</span></span>](endpointdlp-dlpnotifypreopendocumentfile.md)                         | <span data-ttu-id="dc590-160">Предоставляет системе сведения о документе до запуска операции открытия.</span><span class="sxs-lookup"><span data-stu-id="dc590-160">Provides the system with information about a document before the open operation is initiated.</span></span>  |
| [<span data-ttu-id="dc590-161">длпнотифипостопендокументфиле</span><span class="sxs-lookup"><span data-stu-id="dc590-161">DlpNotifyPostOpenDocumentFile</span></span>](endpointdlp-dlpnotifypostopendocumentfile.md)                       | <span data-ttu-id="dc590-162">Предоставляет системе сведения о документе после завершения операции открытия.</span><span class="sxs-lookup"><span data-stu-id="dc590-162">Provides the system with information about a document after the open operation is completed.</span></span>                                  |
| [<span data-ttu-id="dc590-163">длпнотификлоседокументфиле</span><span class="sxs-lookup"><span data-stu-id="dc590-163">DlpNotifyCloseDocumentFile</span></span>](endpointdlp-dlpnotifyclosedocumentfile.md)                       | <span data-ttu-id="dc590-164">Предоставляет системе сведения о документе до инициирования операции закрытия документа.</span><span class="sxs-lookup"><span data-stu-id="dc590-164">Provides the system with information about a document before the document close operation is initiated.</span></span>                                  |

### <a name="save-as-operations"></a><span data-ttu-id="dc590-165">Сохранить как операции</span><span class="sxs-lookup"><span data-stu-id="dc590-165">Save as operations</span></span>
| <span data-ttu-id="dc590-166">API</span><span class="sxs-lookup"><span data-stu-id="dc590-166">API</span></span> | <span data-ttu-id="dc590-167">Описание</span><span class="sxs-lookup"><span data-stu-id="dc590-167">Description</span></span> |
|-----|-------------|
| [<span data-ttu-id="dc590-168">длпнотифипресавеасдокумент</span><span class="sxs-lookup"><span data-stu-id="dc590-168">DlpNotifyPreSaveAsDocument</span></span>](endpointdlp-dlpnotifypresaveasdocument.md)                       | <span data-ttu-id="dc590-169">Предоставляет системе сведения о документе до инициации операции сохранения.</span><span class="sxs-lookup"><span data-stu-id="dc590-169">Provides the system with information about a document before a save as operation is initiated.</span></span>                                  |
| [<span data-ttu-id="dc590-170">длпнотифипостсавеасдокумент</span><span class="sxs-lookup"><span data-stu-id="dc590-170">DlpNotifyPostSaveAsDocument</span></span>](endpointdlp-dlpnotifypostsaveasdocument.md)                       | <span data-ttu-id="dc590-171">Предоставляет системе сведения о документе после завершения операции Сохранить как.</span><span class="sxs-lookup"><span data-stu-id="dc590-171">Provides the system with information about a document after the save as operation is completed.</span></span>                                  |


### <a name="drag-and-drop-operations"></a><span data-ttu-id="dc590-172">Операции перетаскивания</span><span class="sxs-lookup"><span data-stu-id="dc590-172">Drag and drop operations</span></span>

| <span data-ttu-id="dc590-173">API</span><span class="sxs-lookup"><span data-stu-id="dc590-173">API</span></span> | <span data-ttu-id="dc590-174">Описание</span><span class="sxs-lookup"><span data-stu-id="dc590-174">Description</span></span> |
|-----|-------------|
| [<span data-ttu-id="dc590-175">длпнотифентердроптаржет</span><span class="sxs-lookup"><span data-stu-id="dc590-175">DlpNotifyEnterDropTarget</span></span>](endpointdlp-dlpnotifyenterdroptarget.md)                       | <span data-ttu-id="dc590-176">Предоставляет системе сведения о документе при входе в цель перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="dc590-176">Provides the system with information about a document when a drop target is entered.</span></span>                                  |
| [<span data-ttu-id="dc590-177">длпнотифилеаведроптаржет</span><span class="sxs-lookup"><span data-stu-id="dc590-177">DlpNotifyLeaveDropTarget</span></span>](endpointdlp-dlpnotifyleavedroptarget.md)                       | <span data-ttu-id="dc590-178">Предоставляет системе сведения о документе при выходе из целевого объекта перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="dc590-178">Provides the system with information about a document when a drop target is exited.</span></span>                                  |
| [<span data-ttu-id="dc590-179">длпнотифипредрагдроп</span><span class="sxs-lookup"><span data-stu-id="dc590-179">DlpNotifyPreDragDrop</span></span>](endpointdlp-dlpnotifypredragdrop.md)                         | <span data-ttu-id="dc590-180">Предоставляет системе сведения о документе до инициирования операции перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="dc590-180">Provides the system with information about a document before a drag drop operation is initiated.</span></span>  |
| [<span data-ttu-id="dc590-181">длпнотифипостдрагдроп</span><span class="sxs-lookup"><span data-stu-id="dc590-181">DlpNotifyPostDragDrop</span></span>](endpointdlp-dlpnotifypostdragdrop.md)                         | <span data-ttu-id="dc590-182">Предоставляет системе сведения о документе после завершения операции перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="dc590-182">Provides the system with information about a document after a drag drop operation is completed.</span></span>  |


### <a name="clipboard-operations"></a><span data-ttu-id="dc590-183">Clipboard - операции</span><span class="sxs-lookup"><span data-stu-id="dc590-183">Clipboard operations</span></span>

| <span data-ttu-id="dc590-184">API</span><span class="sxs-lookup"><span data-stu-id="dc590-184">API</span></span> | <span data-ttu-id="dc590-185">Описание</span><span class="sxs-lookup"><span data-stu-id="dc590-185">Description</span></span> |
|-----|-------------|
| [<span data-ttu-id="dc590-186">длпнотифипрекопитоклипбоард</span><span class="sxs-lookup"><span data-stu-id="dc590-186">DlpNotifyPreCopyToClipboard</span></span>](endpointdlp-dlpnotifyprecopytoclipboard.md)                         | <span data-ttu-id="dc590-187">Предоставляет системе сведения о документе до инициирования операции копирования в буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="dc590-187">Provides the system with information about a document before a copy to clipboard operation is initiated.</span></span>  |
| [<span data-ttu-id="dc590-188">длпнотифипосткопитоклипбоард</span><span class="sxs-lookup"><span data-stu-id="dc590-188">DlpNotifyPostCopyToClipboard</span></span>](endpointdlp-dlpnotifypostcopytoclipboard.md)                         | <span data-ttu-id="dc590-189">Предоставляет системе сведения о документе после завершения операции копирования в буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="dc590-189">Provides the system with information about a document after a copy to clipboard operation is completed.</span></span>  |
| [<span data-ttu-id="dc590-190">длпнотифипрепастефромклипбоард</span><span class="sxs-lookup"><span data-stu-id="dc590-190">DlpNotifyPrePasteFromClipboard</span></span>](endpointdlp-dlpnotifyprepastefromclipboard.md)                         | <span data-ttu-id="dc590-191">Предоставляет системе сведения о документе до начала операции вставки из буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="dc590-191">Provides the system with information about a document before a paste from clipboard operation is initiated.</span></span>  |
| [<span data-ttu-id="dc590-192">длпнотифипостпастефромклипбоард</span><span class="sxs-lookup"><span data-stu-id="dc590-192">DlpNotifyPostPasteFromClipboard</span></span>](endpointdlp-dlpnotifypostpastefromclipboard.md)                       | <span data-ttu-id="dc590-193">Предоставляет системе сведения о документе после завершения операции вставки из буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="dc590-193">Provides the system with information about a document after a paste from clipboard operation has completed.</span></span>                                  |
| [<span data-ttu-id="dc590-194">длпнотифипостсташклипбоард</span><span class="sxs-lookup"><span data-stu-id="dc590-194">DlpNotifyPostStashClipboard</span></span>](endpointdlp-dlpnotifypoststashclipboard.md)                       | <span data-ttu-id="dc590-195">Предоставляет систему со сведениями о состоянии после завершения операции скрытого буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="dc590-195">Provides the system with status information after a stash clipboard operation is completed.</span></span>                                  |
| [<span data-ttu-id="dc590-196">длпнотифипресташклипбоард</span><span class="sxs-lookup"><span data-stu-id="dc590-196">DlpNotifyPreStashClipboard</span></span>](endpointdlp-dlpnotifyprestashclipboard.md)                       | <span data-ttu-id="dc590-197">Уведомляет систему перед инициированием операции скрытого буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="dc590-197">Notifies the system before a stash clipboard operation is initiated.</span></span>                                  |
| [<span data-ttu-id="dc590-198">длпмустпастефромсистемклипбоард</span><span class="sxs-lookup"><span data-stu-id="dc590-198">DlpMustPasteFromSystemClipboard</span></span>](endpointdlp-dlpmustpastefromsystemclipboard.md)                       | <span data-ttu-id="dc590-199">Определяет, следует ли приложению извлекать данные из системного буфера обмена, вместо того чтобы брать их из внутреннего кэша.</span><span class="sxs-lookup"><span data-stu-id="dc590-199">Determines whether the app must pull the data from the system clipboard rather than taking it from its internal cache.</span></span>                                  |

### <a name="print-operations"></a><span data-ttu-id="dc590-200">Операции печати</span><span class="sxs-lookup"><span data-stu-id="dc590-200">Print operations</span></span>

| <span data-ttu-id="dc590-201">API</span><span class="sxs-lookup"><span data-stu-id="dc590-201">API</span></span> | <span data-ttu-id="dc590-202">Описание</span><span class="sxs-lookup"><span data-stu-id="dc590-202">Description</span></span> |
|-----|-------------|
| [<span data-ttu-id="dc590-203">длпнотифипрепринт</span><span class="sxs-lookup"><span data-stu-id="dc590-203">DlpNotifyPrePrint</span></span>](endpointdlp-dlpnotifypreprint.md)                         | <span data-ttu-id="dc590-204">Предоставляет системе сведения о документе до начала операции печати.</span><span class="sxs-lookup"><span data-stu-id="dc590-204">Provides the system with information about a document before a print operation is initiated.</span></span>  |
| [<span data-ttu-id="dc590-205">длпнотифипостстартпринт</span><span class="sxs-lookup"><span data-stu-id="dc590-205">DlpNotifyPostStartPrint</span></span>](endpointdlp-dlpnotifypoststartprint.md)                       | <span data-ttu-id="dc590-206">Предоставляет системе сведения о документе после запуска операции печати.</span><span class="sxs-lookup"><span data-stu-id="dc590-206">Provides the system with information about a document after an print operation has started.</span></span>                                  |
| [<span data-ttu-id="dc590-207">длпнотифипостпринт</span><span class="sxs-lookup"><span data-stu-id="dc590-207">DlpNotifyPostPrint</span></span>](endpointdlp-dlpnotifypostprint.md)                       | <span data-ttu-id="dc590-208">Предоставляет системе сведения о документе после завершения операции печати.</span><span class="sxs-lookup"><span data-stu-id="dc590-208">Provides the system with information about a document after a print operation has completed.</span></span>                                  |

## <a name="endpoint-dlp-example-header"></a><span data-ttu-id="dc590-209">Заголовок Endpoint DLP, пример</span><span class="sxs-lookup"><span data-stu-id="dc590-209">Endpoint DLP example header</span></span>

<span data-ttu-id="dc590-210">Поскольку заголовок DLP конечной точки не включен в Windows SDK, необходимо создать файл заголовка самостоятельно, чтобы получить сигнатуры API для использования в реализации.</span><span class="sxs-lookup"><span data-stu-id="dc590-210">Because the endpoint DLP header is not included in the Windows SDK, you must create the header file yourself to get API signatures to use in your implementation.</span></span> <span data-ttu-id="dc590-211">Для удобства мы предоставляем пример кода, который можно скопировать и вставить в приложение.</span><span class="sxs-lookup"><span data-stu-id="dc590-211">For your convenience we're providing example code that you can copy and paste into your application.</span></span> <span data-ttu-id="dc590-212">Помимо объявлений функций, этот листинг кода также определяет полезные константы, такие как сведения об управлении версиями и пути к разделам реестра.</span><span class="sxs-lookup"><span data-stu-id="dc590-212">In addition to function declarations, this code listing also defines useful constants such as versioning information and registry key paths.</span></span>

```cpp
//
// EndpointDlp DLL name containing the Endpoint DLP API
//

#define ENDPOINTDLP_DLL_NAME L"EndpointDlp.dll"

//
// Windows Defender registry key under HKLM where some Endpoint DLP settings are stored
//

#define ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY L"SOFTWARE\\Microsoft\\Windows Defender"

//
// EndpointDlp.dll install location can be obtained from the registry under the following HKLM key
//

#define ENDPOINTDLP_DLL_INSTALL_LOCATION_REGKEY ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY

//
// EndpointDlp.dll install location is stored under ENDPOINTDLP_DLL_INSTALL_LOCATION_REGKEY in the following registry value
//

#define ENDPOINTDLP_DLL_INSTALL_LOCATION_REGVALUE L"InstallLocation"

//
// On x64 platforms, concatanate the following directory to obtain the x86 version of EndpointDlp.dll
//

#define ENDPOINTDLP_DLL_WOW64_X86_INSTALL_LOCATION_SUFFIX L"x86"

//
// Endpoint DLP enabled flag can be found under the following HKLM key
//

#define ENDPOINTDLP_ENABLED_FLAG_REGKEY ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY L"\\Features"

//
// Endpoint DLP enabled flag can be found under ENDPOINTDLP_ENABLED_REGKEY in the following registry value
//

#define ENDPOINTDLP_ENABLED_FLAG_REGVALUE L"SenseDlpEnabled"


#define DLP_DOCUMENT_INFO_V_1 0x1     

#define DLP_DOCUMENT_INFO_V_LATEST DLP_DOCUMENT_INFO_V_1


//
//  Enlightened app enforcement capablities.
//

typedef enum _DlpAppEnforceLevel {
    DlpAppEnforceLevelNone = 0, // No enforcement, DLP enforces operation.
    DlpAppEnforceLevelNotify,   // App send notifications on operation, DLP enforces operation.
    DlpAppEnforceLevelPrevent,  // Currently not supported (App allows or blocks operation, DLP enforces warning, eventing and UI). 
    DlpAppEnforceLevelFull,     // Currently not supported (App handles all enforcement (blocks operation, enforces warning, UI), DLP will only handle auditing.)
    DlpAppEnforceLevelCount,
}DlpAppEnforceLevel;

typedef enum  
{
    DlpActionTypeCopyToRemovableMedia = 0,
    DlpActionTypeCopyToNetworkShare = 1,
    DlpActionTypeCopyToClipboard = 2,
    DlpActionTypePrint = 3,
    DlpActionTypeScreenClip = 4,
    DlpActionTypeAccessByUnallowedApp = 5,
    DlpActionTypeCloudAppEgress = 6,
    DlpActionTypeAccessByBluetoothApp = 7,
    DlpActionTypeAccessByRDPApp = 8,
    DlpActionTypeCount = 9
} DlpActionType;
    
//
//  The stucture describes the enforcement level for each operation.
//
    
typedef struct _DLP_APP_OP_ENLIGHTENED_LEVEL{
    DlpActionType Operation;
    DlpAppEnforceLevel AppEnforcementLevel;
}DLP_APP_OP_ENLIGHTENED_LEVEL, *PDLP_APP_OP_ENLIGHTENED_LEVEL;


/*
Function description:
     The application calls this functio to declares the enforcement level for each operation.

Parameters:
    _In_ DWORD Count - Number of operations. 
    _In_reads_opt_(Count) PDLP_APP_OP_ENLIGHTENED_LEVEL* OperationEnforcement - Array indicating operations
    supported by the application and enforcement level:
        DlpAppEnforceLevelNone - No enforcement, DLP enforces operation.
        DlpAppEnforceLevelNotify -  App send notifications on operation, DLP enforces operation.

Return:
    S_OK - Function completed successfully.
    E_INVALIDARG - Invalid parameters passed to function.
    E_OUTOFMEMORY - Memory allocation failed.
    E_XXX - Varius error codes.
*/       
HRESULT WINAPI DlpInitializeEnforcementMode(_In_ DWORD Count, _In_reads_(Count) PDLP_APP_OP_ENLIGHTENED_LEVEL OperationEnforcement);


/*
Function description:
    Returns the version of the enforcement API.
    MajorVersion indicates a new interfaces/API.
    MinorVersion indicates changes to existing interfaces/API-s.
   
Parameters:
    None.

Return:
    S_OK - Function completed successfully
    E_XXX - Varius error codes.
*/
HRESULT WINAPI DlpGetEnforcementApiVersion(_Out_ DWORD* MajorVersion, _Out_ DWORD* MinorVersion);


typedef struct _DLP_DOCUMENT_INFO {

    //
    //  Information version. Always set it to DLP_DOCUMENT_INFO_V_LATEST
    //
    
    DWORD Version;

    //
    //  Original path of the document.
    //  
    
    LPCWSTR PersistentFileName;

    //
    //  Path to the real backing file.
    //
    
    LPCWSTR LocalFileName;

}DLP_DOCUMENT_INFO, *PDLP_DOCUMENT_INFO;

//
//  Post operation status information.
//
    
#define DLP_POSTOP_STATUS_V_1 0x1     
        
#define DLP_POSTOP_STATUS_V_LATEST DLP_POSTOP_STATUS_V_1;
    
       
typedef struct _DLP_POSTOP_STATUS {

    //
    //  Information version. Always set it to DLP_POSTOP_STATUS_V_LATEST
    //
    
    DWORD Version;

    //
    //  Set to TRUE if app's operation succeeded, FALSE otherwise. 
    //
    
    BOOL OperationSuccess;  

} DLP_POSTOP_STATUS, *PDLP_POSTOP_STATUS;    


#define DLP_PRINT_INFO_V_1 0x1     
    
#define DLP_PRINT_INFO_V_LATEST DLP_PRINT_INFO_V_1;

typedef struct _DLP_PRINT_INFO {

    //
    //  Information version. Always set it to DLP_PRINT_INFO_V_LATEST
    //
    
    DWORD Version;

    //
    //  Destination printer.
    //
    
    LPCWSTR PrinterName;

    //
    //  Print job name.
    //
    
    LPCWSTR JobName;

    //
    //  Output file, if printing to file.
    //

    LPCWSTR OutputFileName;
    
}DLP_PRINT_INFO, *PDLP_PRINT_INFO;

    
void WINAPI DlpNotifyPreOpenDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
void WINAPI DlpNotifyPostOpenDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus); 

void WINAPI DlpNotifyCloseDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);

void WINAPI DlpNotifyPreOpenDocumentFile(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
void WINAPI DlpNotifyPostOpenDocumentFile(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus); 

void WINAPI DlpNotifyCloseDocumentFile(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);

void WINAPI DlpNotifyPreSaveAsDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ LPCWSTR Destination);
void WINAPI DlpNotifyPostSaveAsDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ LPCWSTR Destination, _In_ const PDLP_POSTOP_STATUS OpStatus); 

void WINAPI DlpNotifyPrePrint(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_PRINT_INFO PrintInfo);
void WINAPI DlpNotifyPostStartPrint(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_PRINT_INFO PrintInfo);
void WINAPI DlpNotifyPostPrint(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_PRINT_INFO PrintInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);

void WINAPI DlpNotifyPreCopyToClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
void WINAPI DlpNotifyPostCopyToClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);

void WINAPI DlpNotifyPrePasteFromClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
void WINAPI DlpNotifyPostPasteFromClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);

void WINAPI DlpNotifyPreStashClipboard();
void WINAPI DlpNotifyPostStashClipboard(_In_ const PDLP_POSTOP_STATUS OpStatus);

void WINAPI DlpNotifyPreDragDrop(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
void WINAPI DlpNotifyPostDragDrop(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);
    
void WINAPI DlpNotifyEnterDropTarget(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
void WINAPI DlpNotifyLeaveDropTarget(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus); 


/*
Function description:
    Determines whether the app must pull the data from the system clipboard rather than taking it from its internal cache.

Parameters:
    None

Return:
    TRUE if calling into the OS clipboard is mandatory, FALSE otherwise
*/
BOOL WINAPI DlpMustPasteFromSystemClipboard();

```


