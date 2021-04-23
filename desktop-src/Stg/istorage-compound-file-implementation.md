---
title: Реализация файла IStorage-Compound
description: Реализация составного файла в IStorage позволяет создавать и администрировать вложенные хранилища и потоки в объекте хранилища, размещенном в объекте составного файла.
ms.assetid: 2a2253f6-d3d3-403e-a9ba-53a541c7a31e
keywords:
- Метод IStorage Стрктд STG, реализация составного файла
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bf37b24a7c68bbe357d99f94e666bfcb613c472
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105661741"
---
# <a name="istorage-compound-file-implementation"></a><span data-ttu-id="e2576-104">Реализация файла IStorage-Compound</span><span class="sxs-lookup"><span data-stu-id="e2576-104">IStorage-Compound File Implementation</span></span>

<span data-ttu-id="e2576-105">Реализация составного файла в [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) позволяет создавать и администрировать вложенные хранилища и потоки в объекте хранилища, размещенном в объекте составного файла.</span><span class="sxs-lookup"><span data-stu-id="e2576-105">The compound file implementation of [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) allows you to create and manage substorages and streams within a storage object residing in a compound file object.</span></span> <span data-ttu-id="e2576-106">Чтобы создать объект составного файла и получить указатель **IStorage** , вызовите функцию API [**стгкреатесторажеекс**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex).</span><span class="sxs-lookup"><span data-stu-id="e2576-106">To create a compound file object and get an **IStorage** pointer, call the API function [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex).</span></span> <span data-ttu-id="e2576-107">Чтобы открыть существующий объект составного файла и получить его корневой указатель **IStorage** , вызовите [**стгопенсторажеекс**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex).</span><span class="sxs-lookup"><span data-stu-id="e2576-107">To open an existing compound file object and get its root **IStorage** pointer, call [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex).</span></span>

<span data-ttu-id="e2576-108">Приложения, использующие составное хранилище, должны быть зарегистрированы в \_ \_ корневых СИСТЕМФИЛЕАССОЦИАТИОНС классов hKey \\ и должны предоставлять собственные обработчики свойств.</span><span class="sxs-lookup"><span data-stu-id="e2576-108">Applications that use compound storage should be registered in HKEY\_CLASSES\_ROOT\\SystemFileAssociations and should provide their own property handlers.</span></span> <span data-ttu-id="e2576-109">Дополнительные сведения см. в подразделе «регистрация глаголов и других сведений о сопоставлении файлов» раздела [Регистрация приложения](/windows/desktop/shell/app-registration).</span><span class="sxs-lookup"><span data-stu-id="e2576-109">For more information, see the "Registering Verbs and Other File Association Information" section of [Application Registration](/windows/desktop/shell/app-registration).</span></span>

## <a name="when-to-use"></a><span data-ttu-id="e2576-110">Назначение</span><span class="sxs-lookup"><span data-stu-id="e2576-110">When to Use</span></span>

<span data-ttu-id="e2576-111">Большинство приложений используют эту реализацию для создания хранилищ и потоков и управления ими.</span><span class="sxs-lookup"><span data-stu-id="e2576-111">Most applications use this implementation to create and manage storages and streams.</span></span>

## <a name="methods"></a><span data-ttu-id="e2576-112">Методы</span><span class="sxs-lookup"><span data-stu-id="e2576-112">Methods</span></span>

<dl> <dt>

<span data-ttu-id="e2576-113"><span id="IStorage__CreateStream"></span><span id="istorage__createstream"></span><span id="ISTORAGE__CREATESTREAM"></span>[**IStorage:: Креатестреам**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream)</span><span class="sxs-lookup"><span data-stu-id="e2576-113"><span id="IStorage__CreateStream"></span><span id="istorage__createstream"></span><span id="ISTORAGE__CREATESTREAM"></span>[**IStorage::CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream)</span></span>
</dt> <dd>

<span data-ttu-id="e2576-114">Создает и открывает объект потока с указанным именем, содержащимся в этом объекте хранилища.</span><span class="sxs-lookup"><span data-stu-id="e2576-114">Creates and opens a stream object with the specified name contained in this storage object.</span></span> <span data-ttu-id="e2576-115">Длина имени не должна превышать 31 символ (не включая признак конца строки).</span><span class="sxs-lookup"><span data-stu-id="e2576-115">The name must not exceed 31 characters in length (not including the string terminator).</span></span> <span data-ttu-id="e2576-116">Символы от 000 до 01f, служащие как первый символ имени потока/хранилища, зарезервированы для использования OLE.</span><span class="sxs-lookup"><span data-stu-id="e2576-116">The 000 through 01f characters, serving as the first character of the stream/storage name, are reserved for use by OLE.</span></span> <span data-ttu-id="e2576-117">Это ограничение составного файла, а ограничение структурированного хранения.</span><span class="sxs-lookup"><span data-stu-id="e2576-117">This is a compound file restriction, not a structured storage restriction.</span></span> <span data-ttu-id="e2576-118">Реализация составного файла, предоставленная COM методом [**IStorage:: креатестреам**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) , не поддерживает следующие варианты поведения:</span><span class="sxs-lookup"><span data-stu-id="e2576-118">The COM-provided compound file implementation of the [**IStorage::CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) method does not support the following behaviors:</span></span>

-   <span data-ttu-id="e2576-119">Флаг СТГМ \_ делетеонрелеасе не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="e2576-119">The STGM\_DELETEONRELEASE flag is not supported.</span></span>
-   <span data-ttu-id="e2576-120">Режим транзакций (СТГМ \_ ) не поддерживается для объектов потока.</span><span class="sxs-lookup"><span data-stu-id="e2576-120">Transacted mode (STGM\_TRANSACTED) is not supported for stream objects.</span></span>
-   <span data-ttu-id="e2576-121">Открытие одного и того же потока более одного раза из одного хранилища не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="e2576-121">Opening the same stream more than once from the same storage is not supported.</span></span> <span data-ttu-id="e2576-122">\_ \_ В параметре *грфмоде* должен быть указан флаг общего доступа к общему ресурсу стгм.</span><span class="sxs-lookup"><span data-stu-id="e2576-122">The STGM\_SHARE\_EXCLUSIVE sharing-mode flag must be specified in the *grfMode* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="e2576-123"><span id="IStorage__OpenStream"></span><span id="istorage__openstream"></span><span id="ISTORAGE__OPENSTREAM"></span>[**IStorage:: Опенстреам**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream)</span><span class="sxs-lookup"><span data-stu-id="e2576-123"><span id="IStorage__OpenStream"></span><span id="istorage__openstream"></span><span id="ISTORAGE__OPENSTREAM"></span>[**IStorage::OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream)</span></span>
</dt> <dd>

<span data-ttu-id="e2576-124">Открывает существующий объект потока в этом объекте хранилища с использованием режимов доступа, указанных в параметре *грфмоде* .</span><span class="sxs-lookup"><span data-stu-id="e2576-124">Opens an existing stream object within this storage object using the access modes specified in the *grfMode* parameter.</span></span> <span data-ttu-id="e2576-125">Символы от 000 до 01f, служащие как первый символ имени потока/хранилища, зарезервированы для использования OLE.</span><span class="sxs-lookup"><span data-stu-id="e2576-125">The 000 through 01f characters, serving as the first character of the stream/storage name, are reserved for use by OLE.</span></span> <span data-ttu-id="e2576-126">Это ограничение составного файла, а ограничение структурированного хранения.</span><span class="sxs-lookup"><span data-stu-id="e2576-126">This is a compound file restriction, not a structured storage restriction.</span></span> <span data-ttu-id="e2576-127">Реализация составного файла, предоставленная COM методом [**IStorage:: опенстреам**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) , не поддерживает следующее поведение:</span><span class="sxs-lookup"><span data-stu-id="e2576-127">The COM-provided compound file implementation of the [**IStorage::OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) method does not support the following behavior:</span></span>

-   <span data-ttu-id="e2576-128">Флаг СТГМ \_ делетеонрелеасе.</span><span class="sxs-lookup"><span data-stu-id="e2576-128">The STGM\_DELETEONRELEASE flag.</span></span>
-   <span data-ttu-id="e2576-129">Режим транзакций (СТГМ \_ ) для потоковых объектов.</span><span class="sxs-lookup"><span data-stu-id="e2576-129">Transacted mode (STGM\_TRANSACTED) for stream objects.</span></span>
-   <span data-ttu-id="e2576-130">Открытие одного и того же потока более одного раза из одного хранилища.</span><span class="sxs-lookup"><span data-stu-id="e2576-130">Opening the same stream more than once from the same storage.</span></span> <span data-ttu-id="e2576-131">\_ \_ Необходимо указать флаг монопольного доступа стгм.</span><span class="sxs-lookup"><span data-stu-id="e2576-131">The STGM\_SHARE\_EXCLUSIVE flag must be specified.</span></span>

</dd> <dt>

<span data-ttu-id="e2576-132"><span id="IStorage__CreateStorage"></span><span id="istorage__createstorage"></span><span id="ISTORAGE__CREATESTORAGE"></span>[**IStorage:: Креатестораже**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstorage)</span><span class="sxs-lookup"><span data-stu-id="e2576-132"><span id="IStorage__CreateStorage"></span><span id="istorage__createstorage"></span><span id="ISTORAGE__CREATESTORAGE"></span>[**IStorage::CreateStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstorage)</span></span>
</dt> <dd>

<span data-ttu-id="e2576-133">Создает и открывает новый объект хранилища с указанным именем в указанном режиме доступа.</span><span class="sxs-lookup"><span data-stu-id="e2576-133">Creates and opens a new storage object with the specified name in the specified access mode.</span></span> <span data-ttu-id="e2576-134">Длина имени не должна превышать 31 символ (не включая признак конца строки).</span><span class="sxs-lookup"><span data-stu-id="e2576-134">The name must not exceed 31 characters in length (not including the string terminator).</span></span> <span data-ttu-id="e2576-135">Символы от 000 до 01f, служащие как первый символ имени потока/хранилища, зарезервированы для использования OLE.</span><span class="sxs-lookup"><span data-stu-id="e2576-135">The 000 through 01f characters, serving as the first character of the stream/storage name, are reserved for use by OLE.</span></span> <span data-ttu-id="e2576-136">Это ограничение составного файла, а ограничение структурированного хранения.</span><span class="sxs-lookup"><span data-stu-id="e2576-136">This is a compound file restriction, not a structured storage restriction.</span></span> <span data-ttu-id="e2576-137">Реализация составного файла, предоставленная COM методом [**IStorage:: креатестораже**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstorage) , не поддерживает следующее поведение:</span><span class="sxs-lookup"><span data-stu-id="e2576-137">The COM-provided compound file implementation of the [**IStorage::CreateStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstorage) method does not support the following behavior:</span></span>

-   <span data-ttu-id="e2576-138">\_Флаг приоритета стгм для некорневых хранилищ.</span><span class="sxs-lookup"><span data-stu-id="e2576-138">The STGM\_PRIORITY flag for nonroot storages.</span></span>
-   <span data-ttu-id="e2576-139">Открытие одного и того же объекта хранилища более одного раза из одного родительского хранилища.</span><span class="sxs-lookup"><span data-stu-id="e2576-139">Opening the same storage object more than once from the same parent storage.</span></span> <span data-ttu-id="e2576-140">\_ \_ Необходимо указать флаг монопольного доступа стгм.</span><span class="sxs-lookup"><span data-stu-id="e2576-140">The STGM\_SHARE\_EXCLUSIVE flag must be specified.</span></span>
-   <span data-ttu-id="e2576-141">Флаг СТГМ \_ делетеонрелеасе.</span><span class="sxs-lookup"><span data-stu-id="e2576-141">The STGM\_DELETEONRELEASE flag.</span></span> <span data-ttu-id="e2576-142">Если этот флаг указан, функция возвращает STG \_ E \_ инвалидфлаг.</span><span class="sxs-lookup"><span data-stu-id="e2576-142">If this flag is specified, the function returns STG\_E\_INVALIDFLAG.</span></span>

</dd> <dt>

<span data-ttu-id="e2576-143"><span id="IStorage__OpenStorage"></span><span id="istorage__openstorage"></span><span id="ISTORAGE__OPENSTORAGE"></span>[**IStorage:: Опенстораже**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage)</span><span class="sxs-lookup"><span data-stu-id="e2576-143"><span id="IStorage__OpenStorage"></span><span id="istorage__openstorage"></span><span id="ISTORAGE__OPENSTORAGE"></span>[**IStorage::OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage)</span></span>
</dt> <dd>

<span data-ttu-id="e2576-144">Открывает существующий объект хранилища с указанным именем в указанном режиме доступа.</span><span class="sxs-lookup"><span data-stu-id="e2576-144">Opens an existing storage object with the specified name in the specified access mode.</span></span> <span data-ttu-id="e2576-145">Символы от 000 до 01f, служащие как первый символ имени потока/хранилища, зарезервированы для использования OLE.</span><span class="sxs-lookup"><span data-stu-id="e2576-145">The 000 through 01f characters, serving as the first character of the stream/storage name, are reserved for use by OLE.</span></span> <span data-ttu-id="e2576-146">Это ограничение составного файла, а ограничение структурированного хранения.</span><span class="sxs-lookup"><span data-stu-id="e2576-146">This is a compound file restriction, not a structured storage restriction.</span></span> <span data-ttu-id="e2576-147">Реализация составного файла, предоставленная COM методом [**IStorage:: опенстораже**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) , не поддерживает следующее поведение:</span><span class="sxs-lookup"><span data-stu-id="e2576-147">The COM-provided compound file implementation of the [**IStorage::OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) method does not support the following behavior:</span></span>

-   <span data-ttu-id="e2576-148">\_Флаг приоритета стгм для некорневых хранилищ.</span><span class="sxs-lookup"><span data-stu-id="e2576-148">The STGM\_PRIORITY flag for nonroot storages.</span></span>
-   <span data-ttu-id="e2576-149">Открытие одного и того же объекта хранилища более одного раза из одного родительского хранилища.</span><span class="sxs-lookup"><span data-stu-id="e2576-149">Opening the same storage object more than once from the same parent storage.</span></span> <span data-ttu-id="e2576-150">\_ \_ Необходимо указать флаг монопольного доступа стгм.</span><span class="sxs-lookup"><span data-stu-id="e2576-150">The STGM\_SHARE\_EXCLUSIVE flag must be specified.</span></span>
-   <span data-ttu-id="e2576-151">Флаг СТГМ \_ делетеонрелеасе.</span><span class="sxs-lookup"><span data-stu-id="e2576-151">The STGM\_DELETEONRELEASE flag.</span></span> <span data-ttu-id="e2576-152">Если этот флаг указан, функция возвращает STG \_ E \_ инвалидфунктион.</span><span class="sxs-lookup"><span data-stu-id="e2576-152">If this flag is specified, the function returns STG\_E\_INVALIDFUNCTION.</span></span>

</dd> <dt>

<span data-ttu-id="e2576-153"><span id="IStorage__CopyTo"></span><span id="istorage__copyto"></span><span id="ISTORAGE__COPYTO"></span>[**IStorage:: CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-copyto)</span><span class="sxs-lookup"><span data-stu-id="e2576-153"><span id="IStorage__CopyTo"></span><span id="istorage__copyto"></span><span id="ISTORAGE__COPYTO"></span>[**IStorage::CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-copyto)</span></span>
</dt> <dd>

<span data-ttu-id="e2576-154">Копирует только подхранилища и потоки этого открытого объекта хранилища в другой объект хранилища.</span><span class="sxs-lookup"><span data-stu-id="e2576-154">Copies only the substorages and streams of this open storage object into another storage object.</span></span> <span data-ttu-id="e2576-155">Параметр *ргиидексклуде* может иметь значение IID \_ IStream, чтобы копировать только подхранилища или IID \_ IStorage, чтобы копировать только потоки.</span><span class="sxs-lookup"><span data-stu-id="e2576-155">The *rgiidExclude* parameter can be set to IID\_IStream to copy only substorages, or to IID\_IStorage to copy only streams.</span></span>

</dd> <dt>

<span data-ttu-id="e2576-156"><span id="IStorage__MoveElementTo"></span><span id="istorage__moveelementto"></span><span id="ISTORAGE__MOVEELEMENTTO"></span>[**IStorage:: Мовилементто**](/windows/desktop/api/Objidl/nf-objidl-istorage-moveelementto)</span><span class="sxs-lookup"><span data-stu-id="e2576-156"><span id="IStorage__MoveElementTo"></span><span id="istorage__moveelementto"></span><span id="ISTORAGE__MOVEELEMENTTO"></span>[**IStorage::MoveElementTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-moveelementto)</span></span>
</dt> <dd>

<span data-ttu-id="e2576-157">Копирует или перемещает подхранилище или поток из этого объекта хранилища в другой объект хранилища.</span><span class="sxs-lookup"><span data-stu-id="e2576-157">Copies or moves a substorage or stream from this storage object to another storage object.</span></span>

</dd> <dt>

<span data-ttu-id="e2576-158"><span id="IStorage__Commit"></span><span id="istorage__commit"></span><span id="ISTORAGE__COMMIT"></span>[**IStorage:: Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit)</span><span class="sxs-lookup"><span data-stu-id="e2576-158"><span id="IStorage__Commit"></span><span id="istorage__commit"></span><span id="ISTORAGE__COMMIT"></span>[**IStorage::Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit)</span></span>
</dt> <dd>

<span data-ttu-id="e2576-159">Гарантирует, что все изменения, вносимые в объект хранилища, открытые в режиме транзакций, отражаются в родительском хранилище. для корневого хранилища отражает изменения в фактическом устройстве; Например, файл на диске.</span><span class="sxs-lookup"><span data-stu-id="e2576-159">Ensures that any changes made to a storage object open in transacted mode are reflected in the parent storage; for a root storage, reflects the changes in the actual device; for example, a file on disk.</span></span> <span data-ttu-id="e2576-160">Для объекта корневого хранилища, открытого в режиме прямого доступа, этот метод не действует, кроме сброса всех буферов памяти на диск.</span><span class="sxs-lookup"><span data-stu-id="e2576-160">For a root storage object opened in direct mode, this method has no effect except to flush all memory buffers to the disk.</span></span> <span data-ttu-id="e2576-161">Для объектов некорневого хранилища в прямом режиме этот метод не действует.</span><span class="sxs-lookup"><span data-stu-id="e2576-161">For nonroot storage objects in direct mode, this method has no effect.</span></span>

<span data-ttu-id="e2576-162">Реализация составных файлов, предоставляемых COM, использует двухэтапный процесс фиксации, если \_ в параметре *грфкоммитфлагс* не указано значение стгк rewrite.</span><span class="sxs-lookup"><span data-stu-id="e2576-162">The COM-provided compound files implementation uses a two-phase commit process unless STGC\_OVERWRITE is specified in the *grfCommitFlags* parameter.</span></span> <span data-ttu-id="e2576-163">Этот двухэтапный процесс обеспечивает устойчивость данных в случае сбоя операции фиксации.</span><span class="sxs-lookup"><span data-stu-id="e2576-163">This two-phase process ensures the robustness of data, in case the commit operation fails.</span></span> <span data-ttu-id="e2576-164">Во-первых, все новые данные записываются в неиспользуемое пространство в базовом файле.</span><span class="sxs-lookup"><span data-stu-id="e2576-164">First, all new data is written to unused space in the underlying file.</span></span> <span data-ttu-id="e2576-165">При необходимости для файла выделяется новое пространство.</span><span class="sxs-lookup"><span data-stu-id="e2576-165">If necessary, new space is allocated to the file.</span></span> <span data-ttu-id="e2576-166">После завершения этого шага таблица в файле обновляется с помощью операции записи в один сектор, чтобы указать, что новые данные будут использоваться вместо старого.</span><span class="sxs-lookup"><span data-stu-id="e2576-166">After this step has been completed, a table in the file is updated using a single-sector write operation to indicate that the new data is to be used in place of the old.</span></span> <span data-ttu-id="e2576-167">Старые данные становятся свободным пространством для использования при следующей операции фиксации.</span><span class="sxs-lookup"><span data-stu-id="e2576-167">The old data becomes free space to be used at the next commit operation.</span></span> <span data-ttu-id="e2576-168">Поэтому старые данные доступны и могут быть восстановлены при возникновении ошибки при фиксации изменений.</span><span class="sxs-lookup"><span data-stu-id="e2576-168">Thus, the old data is available and can be restored if an error occurs when committing changes.</span></span> <span data-ttu-id="e2576-169">Если \_ указана перезапись стгк, используется однофазная операция фиксации.</span><span class="sxs-lookup"><span data-stu-id="e2576-169">If STGC\_OVERWRITE is specified, a single phase commit operation is used.</span></span> <span data-ttu-id="e2576-170">Дополнительные сведения о флагах режима транзакций см. в разделе [**стгк**](/windows/win32/api/wtypes/ne-wtypes-stgc) Enumeration.</span><span class="sxs-lookup"><span data-stu-id="e2576-170">For more information about transacted mode flags, see [**STGC**](/windows/win32/api/wtypes/ne-wtypes-stgc) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="e2576-171"><span id="IStorage__Revert"></span><span id="istorage__revert"></span><span id="ISTORAGE__REVERT"></span>[**IStorage:: revert**](/windows/desktop/api/Objidl/nf-objidl-istorage-revert)</span><span class="sxs-lookup"><span data-stu-id="e2576-171"><span id="IStorage__Revert"></span><span id="istorage__revert"></span><span id="ISTORAGE__REVERT"></span>[**IStorage::Revert**](/windows/desktop/api/Objidl/nf-objidl-istorage-revert)</span></span>
</dt> <dd>

<span data-ttu-id="e2576-172">Отменяет все изменения, внесенные в объект хранилища с момента последней операции фиксации.</span><span class="sxs-lookup"><span data-stu-id="e2576-172">Discards all changes that have been made to the storage object since the last commit operation.</span></span>

</dd> <dt>

<span data-ttu-id="e2576-173"><span id="IStorage__EnumElements"></span><span id="istorage__enumelements"></span><span id="ISTORAGE__ENUMELEMENTS"></span>[**IStorage:: Енумелементс**](/windows/desktop/api/Objidl/nf-objidl-istorage-enumelements)</span><span class="sxs-lookup"><span data-stu-id="e2576-173"><span id="IStorage__EnumElements"></span><span id="istorage__enumelements"></span><span id="ISTORAGE__ENUMELEMENTS"></span>[**IStorage::EnumElements**](/windows/desktop/api/Objidl/nf-objidl-istorage-enumelements)</span></span>
</dt> <dd>

<span data-ttu-id="e2576-174">Создает и получает указатель на объект перечислителя, который можно использовать для перечисления объектов хранилища и потоков, содержащихся в этом объекте хранилища.</span><span class="sxs-lookup"><span data-stu-id="e2576-174">Creates and retrieves a pointer to an enumerator object that can be used to enumerate the storage and stream objects contained within this storage object.</span></span> <span data-ttu-id="e2576-175">Реализация составного файла, предоставляемая моделью COM, создает моментальный снимок этой информации.</span><span class="sxs-lookup"><span data-stu-id="e2576-175">The COM-provided compound file implementation takes a snapshot of that information.</span></span> <span data-ttu-id="e2576-176">Поэтому изменения в потоках и хранилищах не отражаются в перечислителе до получения нового перечислителя.</span><span class="sxs-lookup"><span data-stu-id="e2576-176">Therefore, changes to the streams and storages are not reflected in the enumerator until a new enumerator is obtained.</span></span>

</dd> <dt>

<span data-ttu-id="e2576-177"><span id="IStorage__DestroyElement"></span><span id="istorage__destroyelement"></span><span id="ISTORAGE__DESTROYELEMENT"></span>[**IStorage::D Естройелемент**](/windows/desktop/api/Objidl/nf-objidl-istorage-destroyelement)</span><span class="sxs-lookup"><span data-stu-id="e2576-177"><span id="IStorage__DestroyElement"></span><span id="istorage__destroyelement"></span><span id="ISTORAGE__DESTROYELEMENT"></span>[**IStorage::DestroyElement**](/windows/desktop/api/Objidl/nf-objidl-istorage-destroyelement)</span></span>
</dt> <dd>

<span data-ttu-id="e2576-178">Удаляет указанный элемент (вложенное хранилище или поток) из этого объекта хранилища.</span><span class="sxs-lookup"><span data-stu-id="e2576-178">Removes the specified element (substorage or stream) from this storage object.</span></span>

</dd> <dt>

<span data-ttu-id="e2576-179"><span id="IStorage__RenameElement"></span><span id="istorage__renameelement"></span><span id="ISTORAGE__RENAMEELEMENT"></span>[**IStorage:: Ренамилемент**](/windows/desktop/api/Objidl/nf-objidl-istorage-renameelement)</span><span class="sxs-lookup"><span data-stu-id="e2576-179"><span id="IStorage__RenameElement"></span><span id="istorage__renameelement"></span><span id="ISTORAGE__RENAMEELEMENT"></span>[**IStorage::RenameElement**](/windows/desktop/api/Objidl/nf-objidl-istorage-renameelement)</span></span>
</dt> <dd>

<span data-ttu-id="e2576-180">Переименовывает указанное подхранилище или поток в этом объекте хранилища.</span><span class="sxs-lookup"><span data-stu-id="e2576-180">Renames the specified substorage or stream in this storage object.</span></span> <span data-ttu-id="e2576-181">Символы от 000 до 01f, служащие как первый символ имени потока/хранилища, зарезервированы для использования OLE.</span><span class="sxs-lookup"><span data-stu-id="e2576-181">The 000 through 01f characters, serving as the first character of the stream/storage name, are reserved for use by OLE.</span></span> <span data-ttu-id="e2576-182">Это ограничение составного файла, а ограничение структурированного хранения.</span><span class="sxs-lookup"><span data-stu-id="e2576-182">This is a compound file restriction, not a structured storage restriction.</span></span>

</dd> <dt>

<span data-ttu-id="e2576-183"><span id="IStorage__SetElementTimes"></span><span id="istorage__setelementtimes"></span><span id="ISTORAGE__SETELEMENTTIMES"></span>[**IStorage:: Сетелементтимес**](/windows/desktop/api/Objidl/nf-objidl-istorage-setelementtimes)</span><span class="sxs-lookup"><span data-stu-id="e2576-183"><span id="IStorage__SetElementTimes"></span><span id="istorage__setelementtimes"></span><span id="ISTORAGE__SETELEMENTTIMES"></span>[**IStorage::SetElementTimes**](/windows/desktop/api/Objidl/nf-objidl-istorage-setelementtimes)</span></span>
</dt> <dd>

<span data-ttu-id="e2576-184">Задает время изменения, доступа и создания указанного элемента хранилища.</span><span class="sxs-lookup"><span data-stu-id="e2576-184">Sets the modification, access, and creation times of the specified storage element.</span></span> <span data-ttu-id="e2576-185">Реализация составных файлов, предоставляемая моделью COM, сохраняет изменения и время изменения для внутренних объектов хранилища.</span><span class="sxs-lookup"><span data-stu-id="e2576-185">The COM-provided compound-file implementation maintains modification and change times for internal storage objects.</span></span> <span data-ttu-id="e2576-186">Объекты корневого хранилища поддерживают все, что поддерживается базовой файловой системой (или [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes)).</span><span class="sxs-lookup"><span data-stu-id="e2576-186">Root storage objects support whatever is supported by the underlying file system (or by [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes)).</span></span> <span data-ttu-id="e2576-187">Реализация составного файла не поддерживает никакие отметки времени для внутренних потоков.</span><span class="sxs-lookup"><span data-stu-id="e2576-187">The compound file implementation does not maintain any time stamps for internal streams.</span></span> <span data-ttu-id="e2576-188">Неподдерживаемые метки времени отмечаются как нулевые, что позволяет вызывающему объекту проверить поддержку.</span><span class="sxs-lookup"><span data-stu-id="e2576-188">Unsupported time stamps are reported as zero, which allows the caller to test for support.</span></span>

</dd> <dt>

<span data-ttu-id="e2576-189"><span id="IStorage__SetClass"></span><span id="istorage__setclass"></span><span id="ISTORAGE__SETCLASS"></span>[**IStorage:: Сеткласс**](/windows/desktop/api/Objidl/nf-objidl-istorage-setclass)</span><span class="sxs-lookup"><span data-stu-id="e2576-189"><span id="IStorage__SetClass"></span><span id="istorage__setclass"></span><span id="ISTORAGE__SETCLASS"></span>[**IStorage::SetClass**](/windows/desktop/api/Objidl/nf-objidl-istorage-setclass)</span></span>
</dt> <dd>

<span data-ttu-id="e2576-190">Присваивает указанный идентификатор CLSID этому объекту хранилища.</span><span class="sxs-lookup"><span data-stu-id="e2576-190">Assigns the specified CLSID to this storage object.</span></span>

</dd> <dt>

<span data-ttu-id="e2576-191"><span id="IStorage__SetStateBits"></span><span id="istorage__setstatebits"></span><span id="ISTORAGE__SETSTATEBITS"></span>[**IStorage:: Сетстатебитс**](/windows/desktop/api/Objidl/nf-objidl-istorage-setstatebits)</span><span class="sxs-lookup"><span data-stu-id="e2576-191"><span id="IStorage__SetStateBits"></span><span id="istorage__setstatebits"></span><span id="ISTORAGE__SETSTATEBITS"></span>[**IStorage::SetStateBits**](/windows/desktop/api/Objidl/nf-objidl-istorage-setstatebits)</span></span>
</dt> <dd>

<span data-ttu-id="e2576-192">Сохраняет до 32 бит информации о состоянии в этом объекте хранилища.</span><span class="sxs-lookup"><span data-stu-id="e2576-192">Stores up to 32 bits of state information in this storage object.</span></span> <span data-ttu-id="e2576-193">Состояние, заданное этим методом, предназначено только для внешнего использования.</span><span class="sxs-lookup"><span data-stu-id="e2576-193">The state set by this method is for external use only.</span></span> <span data-ttu-id="e2576-194">Реализация составного файла, предоставляемая моделью COM, не выполняет никаких действий в зависимости от состояния.</span><span class="sxs-lookup"><span data-stu-id="e2576-194">The COM-provided compound file implementation does not perform any action based on the state.</span></span>

</dd> <dt>

<span data-ttu-id="e2576-195"><span id="IStorage__Stat"></span><span id="istorage__stat"></span><span id="ISTORAGE__STAT"></span>[**IStorage:: stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat)</span><span class="sxs-lookup"><span data-stu-id="e2576-195"><span id="IStorage__Stat"></span><span id="istorage__stat"></span><span id="ISTORAGE__STAT"></span>[**IStorage::Stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat)</span></span>
</dt> <dd>

<span data-ttu-id="e2576-196">Извлекает структуру [**статстг**](/windows/win32/api/objidl/ns-objidl-statstg) для этого открытого объекта хранилища.</span><span class="sxs-lookup"><span data-stu-id="e2576-196">Retrieves the [**STATSTG**](/windows/win32/api/objidl/ns-objidl-statstg) structure for this open storage object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e2576-197">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e2576-197">Remarks</span></span>

<span data-ttu-id="e2576-198">Если объект хранилища открыт в простом режиме, использование описанных выше методов будет ограничено.</span><span class="sxs-lookup"><span data-stu-id="e2576-198">If the storage object is opened in simple mode, use of the above methods is restricted.</span></span> <span data-ttu-id="e2576-199">Хранилище находится в простом режиме, если он открыт с помощью \_ простого элемента стгм, указанного в параметре *Грфмоде* функции [**стгкреатесторажеекс**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) или [**стгопенсторажеекс**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) .</span><span class="sxs-lookup"><span data-stu-id="e2576-199">A storage is in simple mode if it is opened with the STGM\_SIMPLE element specified in the *grfMode* parameter of the [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) or [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) function.</span></span> <span data-ttu-id="e2576-200">Дополнительные сведения о хранилищах в простых режимах см. в разделе [**константы стгм**](stgm-constants.md).</span><span class="sxs-lookup"><span data-stu-id="e2576-200">For more information about simple-mode storages, see [**STGM Constants**](stgm-constants.md).</span></span> <span data-ttu-id="e2576-201">Если объект хранилища простого режима был получен из функции **стгкреатесторажеекс** , то метод [**креатестреам**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) можно вызвать, но метод [**опенстреам**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) не может.</span><span class="sxs-lookup"><span data-stu-id="e2576-201">If the simple-mode storage object was obtained from the **StgCreateStorageEx** function, then the [**CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) method can be called but the [**OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) method cannot.</span></span> <span data-ttu-id="e2576-202">Если объект хранилища простого режима был получен из функции **стгопенсторажеекс** , то метод **опенстреам** можно вызвать, но метод **креатестреам** не может.</span><span class="sxs-lookup"><span data-stu-id="e2576-202">If the simple mode storage object was obtained from the **StgOpenStorageEx** function, then the **OpenStream** method can be called but the **CreateStream** method cannot.</span></span>

<span data-ttu-id="e2576-203">Если для создания потока используется объект хранилища простого режима, минимальный размер этого потока обычно составляет 4096 байт.</span><span class="sxs-lookup"><span data-stu-id="e2576-203">When a simple-mode storage object is used to create a stream, the minimum size of that stream typically is 4096 bytes.</span></span> <span data-ttu-id="e2576-204">Если в поток записывается меньше данных, размер округляется до 4096 байт.</span><span class="sxs-lookup"><span data-stu-id="e2576-204">If less data is written to the stream, the size is rounded up to 4096 bytes.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e2576-205">См. также</span><span class="sxs-lookup"><span data-stu-id="e2576-205">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2576-206">Ограничения реализации составных файлов</span><span class="sxs-lookup"><span data-stu-id="e2576-206">Compound File Implementation Limits</span></span>](structured-storage-interfaces.md)
</dt> <dt>

[<span data-ttu-id="e2576-207">**ифилллоккбитес**</span><span class="sxs-lookup"><span data-stu-id="e2576-207">**IFillLockBytes**</span></span>](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes)
</dt> <dt>

[<span data-ttu-id="e2576-208">**ILockBytes**</span><span class="sxs-lookup"><span data-stu-id="e2576-208">**ILockBytes**</span></span>](/windows/desktop/api/Objidl/nn-objidl-ilockbytes)
</dt> <dt>

[<span data-ttu-id="e2576-209">**ирутстораже**</span><span class="sxs-lookup"><span data-stu-id="e2576-209">**IRootStorage**</span></span>](/windows/desktop/api/Objidl/nn-objidl-irootstorage)
</dt> <dt>

[<span data-ttu-id="e2576-210">**Метод IStorage**</span><span class="sxs-lookup"><span data-stu-id="e2576-210">**IStorage**</span></span>](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> <dt>

[<span data-ttu-id="e2576-211">**IStream**</span><span class="sxs-lookup"><span data-stu-id="e2576-211">**IStream**</span></span>](/windows/desktop/api/Objidl/nn-objidl-istream)
</dt> <dt>

[<span data-ttu-id="e2576-212">**стгкреатедокфиле**</span><span class="sxs-lookup"><span data-stu-id="e2576-212">**StgCreateDocfile**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile)
</dt> <dt>

[<span data-ttu-id="e2576-213">**стгкреатесторажеекс**</span><span class="sxs-lookup"><span data-stu-id="e2576-213">**StgCreateStorageEx**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex)
</dt> <dt>

[<span data-ttu-id="e2576-214">**стгопенстораже**</span><span class="sxs-lookup"><span data-stu-id="e2576-214">**StgOpenStorage**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage)
</dt> <dt>

[<span data-ttu-id="e2576-215">**стгопенсторажеекс**</span><span class="sxs-lookup"><span data-stu-id="e2576-215">**StgOpenStorageEx**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex)
</dt> </dl>

 

 