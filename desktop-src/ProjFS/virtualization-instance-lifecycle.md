---
title: Жизненный цикл экземпляра виртуализации
description: Общие сведения о жизненном цикле экземпляра Прожфс Virtualization.
ms.assetid: <GUID-GOES-HERE>
ms.date: 09/17/2018
ms.topic: article
ms.openlocfilehash: 567eff1f7b8acf330dba7c652e2e12b724072b9b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104533239"
---
# <a name="virtualization-instance-lifecycle"></a><span data-ttu-id="e17d0-103">Жизненный цикл экземпляра виртуализации</span><span class="sxs-lookup"><span data-stu-id="e17d0-103">Virtualization Instance Lifecycle</span></span>

<span data-ttu-id="e17d0-104">Приложение поставщика поддерживает один или несколько экземпляров виртуализации.</span><span class="sxs-lookup"><span data-stu-id="e17d0-104">The provider application maintains one or more virtualization instances.</span></span>  <span data-ttu-id="e17d0-105">Каждый экземпляр виртуализации проходит через четыре этапа в своем жизненном цикле:</span><span class="sxs-lookup"><span data-stu-id="e17d0-105">Each virtualization instance goes through four stages in its lifecycle:</span></span>

1. <span data-ttu-id="e17d0-106">Создание</span><span class="sxs-lookup"><span data-stu-id="e17d0-106">Creation</span></span>
2. <span data-ttu-id="e17d0-107">Запуск</span><span class="sxs-lookup"><span data-stu-id="e17d0-107">Startup</span></span>
3. <span data-ttu-id="e17d0-108">Параметры выполнения</span><span class="sxs-lookup"><span data-stu-id="e17d0-108">Runtime</span></span>
4. <span data-ttu-id="e17d0-109">Завершить работу</span><span class="sxs-lookup"><span data-stu-id="e17d0-109">Shutdown</span></span>

<span data-ttu-id="e17d0-110">Обратите внимание, что после завершения работы экземпляра виртуализации поставщику не нужно повторно создавать его для повторного использования.</span><span class="sxs-lookup"><span data-stu-id="e17d0-110">Note that after shutting down a virtualization instance the provider does not need to re-create it to reuse it.</span></span>  <span data-ttu-id="e17d0-111">Его можно просто запустить снова.</span><span class="sxs-lookup"><span data-stu-id="e17d0-111">It can simply start it up again.</span></span>

> <span data-ttu-id="e17d0-112">**Примечание**. в этом разделе приведены примеры API-интерфейсов прожфс.</span><span class="sxs-lookup"><span data-stu-id="e17d0-112">**Note**: This section shows examples of ProjFS APIs.</span></span>  <span data-ttu-id="e17d0-113">Каждый пример предназначен для демонстрации базового использования API.</span><span class="sxs-lookup"><span data-stu-id="e17d0-113">Each example is meant to illustrate basic API usage.</span></span>  <span data-ttu-id="e17d0-114">Документацию по параметрам, не используемым в этих примерах, см. в [справочнике по API прожфс](/windows/desktop/api/_projfs).</span><span class="sxs-lookup"><span data-stu-id="e17d0-114">For documentation of options unused in these examples please consult the [ProjFS API reference](/windows/desktop/api/_projfs).</span></span>

## <a name="creating-a-virtualization-root"></a><span data-ttu-id="e17d0-115">Создание корня виртуализации</span><span class="sxs-lookup"><span data-stu-id="e17d0-115">Creating a virtualization root</span></span>

<span data-ttu-id="e17d0-116">Прежде чем поставщик может запустить экземпляр виртуализации, который будет выполнять проецирование элементов в локальную файловую систему, необходимо создать корень виртуализации.</span><span class="sxs-lookup"><span data-stu-id="e17d0-116">Before a provider can start up the virtualization instance that will project items into the local file system, it must create the virtualization root.</span></span>  <span data-ttu-id="e17d0-117">Корневой узел виртуализации — это каталог, в котором поставщик проецирует дерево каталогов и файлов.</span><span class="sxs-lookup"><span data-stu-id="e17d0-117">The virtualization root is the directory under which the provider projects a tree of directories and files.</span></span>

<span data-ttu-id="e17d0-118">Чтобы создать корень виртуализации, поставщик должен выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="e17d0-118">To create a virtualization root the provider must:</span></span>

1. <span data-ttu-id="e17d0-119">Создайте каталог, который будет служить корнем виртуализации.</span><span class="sxs-lookup"><span data-stu-id="e17d0-119">Create a directory to serve as the virtualization root.</span></span>

    <span data-ttu-id="e17d0-120">Поставщик создает каталог, используемый в качестве корня виртуализации, с помощью, например **[CreateDirectory](/windows/desktop/api/fileapi/nf-fileapi-createdirectoryw)**:</span><span class="sxs-lookup"><span data-stu-id="e17d0-120">The provider creates a directory to serve as the virtualization root using, for example **[CreateDirectory](/windows/desktop/api/fileapi/nf-fileapi-createdirectoryw)**:</span></span>

    ```C++
    HRESULT hr;
    const wchar_t* rootName = LR"(C:\virtRoot)";
    if (!CreateDirectoryW(rootName, nullptr))
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
        wprintf(L"Failed to create virtualization root (0x%08x)\n", hr);
        return;
    }
    ```

1. <span data-ttu-id="e17d0-121">Создайте идентификатор экземпляра виртуализации.</span><span class="sxs-lookup"><span data-stu-id="e17d0-121">Create a virtualization instance ID.</span></span>

    <span data-ttu-id="e17d0-122">Каждый экземпляр виртуализации имеет уникальный идентификатор, именуемый _идентификатором экземпляра виртуализации_.</span><span class="sxs-lookup"><span data-stu-id="e17d0-122">Every virtualization instance has a unique ID called the _virtualization instance ID_.</span></span>  <span data-ttu-id="e17d0-123">Система использует это значение для указания того, с каким экземпляром виртуализации связано его содержимое.</span><span class="sxs-lookup"><span data-stu-id="e17d0-123">The system uses this value to identify which virtualization instance its contents are associated to.</span></span>

    ```C++
    GUID instanceId;
    hr = CoCreateGuid(&instanceId);
    if (FAILED(hr))
    {
        wprintf(L"Failed to create instance ID (0x%08x)\n", hr);
        return;
    }
    ```

1. <span data-ttu-id="e17d0-124">Пометьте новый каталог как корень виртуализации.</span><span class="sxs-lookup"><span data-stu-id="e17d0-124">Mark the new directory as the virtualization root.</span></span>

    <span data-ttu-id="e17d0-125">Поставщик вызывает **[пржмаркдиректорясплацехолдер](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjmarkdirectoryasplaceholder)** , чтобы пометить новый каталог как корень виртуализации и назначить его экземпляру виртуализации.</span><span class="sxs-lookup"><span data-stu-id="e17d0-125">The provider calls **[PrjMarkDirectoryAsPlaceholder](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjmarkdirectoryasplaceholder)** to mark the new directory as the virtualization root and assign it to the virtualization instance.</span></span>

    ```C++
    hr = PrjMarkDirectoryAsPlaceholder(rootName,
                                       nullptr,
                                       nullptr,
                                       &instanceId);
    if (FAILED(hr))
    {
        wprintf(L"Failed to mark virtualization root (0x%08x)\n", hr);
        return;
    }
    ```

<span data-ttu-id="e17d0-126">Поставщику необходимо только один раз создать корень виртуализации для каждого экземпляра виртуализации.</span><span class="sxs-lookup"><span data-stu-id="e17d0-126">The provider only needs to create the virtualization root once for each virtualization instance.</span></span>  <span data-ttu-id="e17d0-127">После создания корня его связанный экземпляр может многократно запускаться и останавливаться без повторного создания корня.</span><span class="sxs-lookup"><span data-stu-id="e17d0-127">Once a root has been created, its associated instance can be repeatedly started and stopped without recreating the root.</span></span>

## <a name="starting-a-virtualization-instance"></a><span data-ttu-id="e17d0-128">Запуск экземпляра виртуализации</span><span class="sxs-lookup"><span data-stu-id="e17d0-128">Starting a virtualization instance</span></span>

<span data-ttu-id="e17d0-129">После создания корня виртуализации поставщик должен запустить экземпляр виртуализации.</span><span class="sxs-lookup"><span data-stu-id="e17d0-129">Once the virtualization root has been created the provider must start the virtualization instance.</span></span>  <span data-ttu-id="e17d0-130">Это сигнализирует Прожфс, что поставщик готов получить обратные вызовы и предоставить данные.</span><span class="sxs-lookup"><span data-stu-id="e17d0-130">This signals ProjFS that the provider is ready to receive callbacks and provide data.</span></span>

<span data-ttu-id="e17d0-131">Чтобы запустить экземпляр виртуализации, поставщик должен выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="e17d0-131">To start the virtualization instance the provider must:</span></span>

1. <span data-ttu-id="e17d0-132">Настройте таблицу обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="e17d0-132">Set up the callback table.</span></span>

    <span data-ttu-id="e17d0-133">Прожфс взаимодействует с поставщиком, вызывая подпрограммы обратного вызова, реализованные поставщиком.</span><span class="sxs-lookup"><span data-stu-id="e17d0-133">ProjFS communicates with the provider by invoking callback routines implemented by the provider.</span></span>  <span data-ttu-id="e17d0-134">Поставщик заполняет [PRJ_CALLBACKS](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_callbacks) структуру указателями на подпрограммы обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="e17d0-134">The provider populates a [PRJ_CALLBACKS](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_callbacks) struct with pointers to its callback routines.</span></span>

    ```C++
    PRJ_CALLBACKS callbackTable;

    // Supply required callbacks.
    callbackTable.StartDirectoryEnumerationCallback = MyStartEnumCallback;
    callbackTable.EndDirectoryEnumerationCallback = MyEndEnumCallback;
    callbackTable.GetDirectoryEnumerationCallback = MyGetEnumCallback;
    callbackTable.GetPlaceholderInfoCallback = MyGetPlaceholderInfoCallback;
    callbackTable.GetFileDataCallback = MyGetFileDataCallback;

    // The rest of the callbacks are optional.
    callbackTable.QueryFileNameCallback = nullptr;
    callbackTable.NotificationCallback = nullptr;
    callbackTable.CancelCommandCallback = nullptr;
    ```

1. <span data-ttu-id="e17d0-135">Запустите экземпляр.</span><span class="sxs-lookup"><span data-stu-id="e17d0-135">Start the instance.</span></span>

    <span data-ttu-id="e17d0-136">Поставщик вызывает **[пржстартвиртуализинг](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjstartvirtualizing)** для запуска экземпляра виртуализации.</span><span class="sxs-lookup"><span data-stu-id="e17d0-136">The provider calls **[PrjStartVirtualizing](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjstartvirtualizing)** to start the virtualization instance.</span></span>

    ```C++
    PRJ_NAMESPACE_VIRTUALIZATION_CONTEXT instanceHandle;
    hr = PrjStartVirtualizing(rootName,
                              &callbackTable,
                              nullptr,
                              nullptr,
                              &instanceHandle);
    if (FAILED(hr))
    {
        wprintf(L"Failed to start the virtualization instance (0x%08x)\n", hr);
        return;
    }
    ```
    <span data-ttu-id="e17d0-137">Параметр _InstanceHandle_ **пржстартвиртуализинг** возвращает дескриптор экземпляра виртуализации.</span><span class="sxs-lookup"><span data-stu-id="e17d0-137">**PrjStartVirtualizing**'s _instanceHandle_ parameter returns a handle to the virtualization instance.</span></span>  <span data-ttu-id="e17d0-138">Поставщик использует этот обработчик при вызове других интерфейсов API Прожфс.</span><span class="sxs-lookup"><span data-stu-id="e17d0-138">The provider uses this handle when calling other ProjFS APIs.</span></span>

## <a name="virtualization-instance-runtime"></a><span data-ttu-id="e17d0-139">Среда выполнения экземпляра виртуализации</span><span class="sxs-lookup"><span data-stu-id="e17d0-139">Virtualization instance runtime</span></span>

<span data-ttu-id="e17d0-140">После того как вызов **пржстартвиртуализинг** возвращает, прожфс будет вызывать подпрограммы обратного вызова поставщика в ответ на операции файловой системы в экземпляре виртуализации.</span><span class="sxs-lookup"><span data-stu-id="e17d0-140">Once the call to **PrjStartVirtualizing** returns, ProjFS will invoke the provider's callback routines in response to file system operations in the virtualization instance.</span></span>  <span data-ttu-id="e17d0-141">Сведения о том, как поставщик может управлять различными операциями файловой системы, см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="e17d0-141">For information on how the provider can handle various file system operations, refer to the following sections:</span></span>

* [<span data-ttu-id="e17d0-142">Перечисление файлов и каталогов</span><span class="sxs-lookup"><span data-stu-id="e17d0-142">Enumerating Files and Directories</span></span>](enumerating-files-and-directories.md)
* [<span data-ttu-id="e17d0-143">Предоставление данных файлов</span><span class="sxs-lookup"><span data-stu-id="e17d0-143">Providing File Data</span></span>](providing-file-data.md)
* [<span data-ttu-id="e17d0-144">Уведомления операций файловой системы</span><span class="sxs-lookup"><span data-stu-id="e17d0-144">File System Operation Notifications</span></span>](file-system-operation-notifications.md)
* [<span data-ttu-id="e17d0-145">Обработка изменений представления</span><span class="sxs-lookup"><span data-stu-id="e17d0-145">Handling View Changes</span></span>](handling-view-changes.md)

## <a name="shutting-down-a-virtualization-instance"></a><span data-ttu-id="e17d0-146">Завершение работы экземпляра виртуализации</span><span class="sxs-lookup"><span data-stu-id="e17d0-146">Shutting down a virtualization instance</span></span>

<span data-ttu-id="e17d0-147">Чтобы сообщить Прожфс о том, что поставщик желает приостанавливаться на получении обратных вызовов и предоставить данные, поставщик должен прерывать экземпляр виртуализации.</span><span class="sxs-lookup"><span data-stu-id="e17d0-147">To signal ProjFS that the provider wants to stop receiving callbacks and providing data, the provider must stop the virtualization instance.</span></span>  <span data-ttu-id="e17d0-148">Для этого поставщик вызывает **[пржстопвиртуализинг](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjstopvirtualizing)**, передавая ему обработчик на экземпляр виртуализации, полученный из вызова **пржстартвиртуализинг**.</span><span class="sxs-lookup"><span data-stu-id="e17d0-148">To do this the provider calls **[PrjStopVirtualizing](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjstopvirtualizing)**, passing it the handle to the virtualization instance that it received from the call to **PrjStartVirtualizing**.</span></span>

```C++
PrjStopVirtualizing(instanceHandle);
```

<span data-ttu-id="e17d0-149">Обратите внимание, что до возвращения этого вызова Прожфс может продолжать вызывать подпрограммы обратного вызова поставщика.</span><span class="sxs-lookup"><span data-stu-id="e17d0-149">Note that until this call returns, ProjFS may continue to invoke the provider's callback routines.</span></span>