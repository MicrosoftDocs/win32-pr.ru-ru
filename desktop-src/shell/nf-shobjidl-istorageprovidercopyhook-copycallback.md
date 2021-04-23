---
description: Определяет, будет ли оболочка разрешать перемещение, копирование, удаление или переименование папки в корне синхронизации поставщика облачных служб.
title: IStorageProviderCopyHook::CopyCallback
ms.topic: reference
ms.date: 11/11/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- IStorageProviderCopyHook::CopyCallback
api_type:
- COM
api_location:
- shobjidl.h
ms.openlocfilehash: c7df9296f2261e3907702067ca36265095102f34
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "104997986"
---
# <a name="istorageprovidercopyhookcopycallback-method"></a><span data-ttu-id="0afc2-103">Метод Исторажепровидеркопихук:: Копикаллбакк</span><span class="sxs-lookup"><span data-stu-id="0afc2-103">IStorageProviderCopyHook::CopyCallback method</span></span>

<span data-ttu-id="0afc2-104">Определяет, будет ли оболочка разрешать перемещение, копирование, удаление или переименование папки в корне синхронизации поставщика облачных служб.</span><span class="sxs-lookup"><span data-stu-id="0afc2-104">Determines whether the Shell will be allowed to move, copy, delete, or rename a folder in a cloud provider's sync root.</span></span>

## <a name="syntax"></a><span data-ttu-id="0afc2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0afc2-105">Syntax</span></span>

```C++
HRESULT CopyCallback( 
    HWND hwnd,
    UINT operation,
    UINT flags,
    LPCWSTR srcFile,
    DWORD srcAttribs,
    LPCWSTR destFile,
    DWORD destAttribs,
    UINT* result
);
```

## <a name="parameters"></a><span data-ttu-id="0afc2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0afc2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0afc2-107">*HWND* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0afc2-107">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0afc2-108">Дескриптор окна, который должен использоваться обработчиком ловушки копирования в качестве родителя для любых элементов пользовательского интерфейса, которые может потребоваться отобразить обработчику.</span><span class="sxs-lookup"><span data-stu-id="0afc2-108">A handle to the window that the copy hook handler should use as the parent for any user interface elements the handler may need to display.</span></span> <span data-ttu-id="0afc2-109">Если в *операции* указан **FOF_SILENT** , метод должен игнорировать этот параметр.</span><span class="sxs-lookup"><span data-stu-id="0afc2-109">If **FOF_SILENT** is specified in *operation*, the method should ignore this parameter.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="0afc2-110">*Операция* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0afc2-110">*operation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0afc2-111">Выполняемая операция.</span><span class="sxs-lookup"><span data-stu-id="0afc2-111">The operation to perform.</span></span> <span data-ttu-id="0afc2-112">Этот параметр может быть одним из значений, перечисленных под элементом **вфунк** структуры [шфилеопструкт](/windows/win32/api/shellapi/ns-shellapi-shfileopstructa) .</span><span class="sxs-lookup"><span data-stu-id="0afc2-112">This parameter can be one of the values listed under the **wFunc** member of the [SHFILEOPSTRUCT](/windows/win32/api/shellapi/ns-shellapi-shfileopstructa) structure.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="0afc2-113">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0afc2-113">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0afc2-114">Флаги, управляющие операцией.</span><span class="sxs-lookup"><span data-stu-id="0afc2-114">The flags that control the operation.</span></span> <span data-ttu-id="0afc2-115">Этот параметр может быть одним или несколькими значениями, перечисленными в элементе *ффлагс* структуры [шфилеопструкт](/windows/desktop/api/shellapi/ns-shellapi-shfileopstructa) .</span><span class="sxs-lookup"><span data-stu-id="0afc2-115">This parameter can be one or more of the values listed under the *fFlags* member of the [SHFILEOPSTRUCT](/windows/desktop/api/shellapi/ns-shellapi-shfileopstructa) structure.</span></span>

<span data-ttu-id="0afc2-116">Для обработчиков копий принтера это значение является одним из следующих значений, определенных в шеллапи. h.</span><span class="sxs-lookup"><span data-stu-id="0afc2-116">For printer copy hooks, this value is one of the following values defined in shellapi.h.</span></span>

| <span data-ttu-id="0afc2-117">Значение</span><span class="sxs-lookup"><span data-stu-id="0afc2-117">Value</span></span>       | <span data-ttu-id="0afc2-118">Описание</span><span class="sxs-lookup"><span data-stu-id="0afc2-118">Description</span></span> |
|-------------|------------|
|  <span data-ttu-id="0afc2-119">**PO_DELETE**</span><span class="sxs-lookup"><span data-stu-id="0afc2-119">**PO_DELETE**</span></span>      | <span data-ttu-id="0afc2-120">Идет удаление принтера.</span><span class="sxs-lookup"><span data-stu-id="0afc2-120">A printer is being deleted.</span></span> <span data-ttu-id="0afc2-121">Параметр *srcFile* указывает на полный путь к указанному принтеру.</span><span class="sxs-lookup"><span data-stu-id="0afc2-121">The *srcFile* parameter points to the full path to the specified printer.</span></span>           |
|  <span data-ttu-id="0afc2-122">**PO_RENAME**</span><span class="sxs-lookup"><span data-stu-id="0afc2-122">**PO_RENAME**</span></span>       | <span data-ttu-id="0afc2-123">Выполняется переименование принтера.</span><span class="sxs-lookup"><span data-stu-id="0afc2-123">A printer is being renamed.</span></span> <span data-ttu-id="0afc2-124">Параметр *srcFile* указывает на новое имя принтера.</span><span class="sxs-lookup"><span data-stu-id="0afc2-124">The *srcFile* parameter points to the printer's new name.</span></span> <span data-ttu-id="0afc2-125">Параметр *дестфиле* указывает на старое имя.</span><span class="sxs-lookup"><span data-stu-id="0afc2-125">The *destFile* parameter points to the old name.</span></span>           |
| <span data-ttu-id="0afc2-126">**PO_PORTCHANGE**</span><span class="sxs-lookup"><span data-stu-id="0afc2-126">**PO_PORTCHANGE**</span></span>    | <span data-ttu-id="0afc2-127">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="0afc2-127">Not supported.</span></span> <span data-ttu-id="0afc2-128">Не используйте.</span><span class="sxs-lookup"><span data-stu-id="0afc2-128">Do not use.</span></span>          |
| <span data-ttu-id="0afc2-129">**PO_REN_PORT**</span><span class="sxs-lookup"><span data-stu-id="0afc2-129">**PO_REN_PORT**</span></span>    | <span data-ttu-id="0afc2-130">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="0afc2-130">Not supported.</span></span> <span data-ttu-id="0afc2-131">Не используйте.</span><span class="sxs-lookup"><span data-stu-id="0afc2-131">Do not use.</span></span>           |

</dd> </dl>

<dl> <dt>

<span data-ttu-id="0afc2-132">*srcFile* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0afc2-132">*srcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0afc2-133">Указатель на строку, содержащую имя исходной папки.</span><span class="sxs-lookup"><span data-stu-id="0afc2-133">A pointer to a string that contains the name of the source folder.</span></span>

</dd> </dl>

<span data-ttu-id="0afc2-134">*сркаттрибс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0afc2-134">*srcAttribs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0afc2-135">Атрибуты исходной папки.</span><span class="sxs-lookup"><span data-stu-id="0afc2-135">The attributes of the source folder.</span></span> <span data-ttu-id="0afc2-136">Этот параметр может быть сочетанием любого из флагов файлового атрибута (FILE_ATTRIBUTE_ \*), определенных в файлах заголовков.</span><span class="sxs-lookup"><span data-stu-id="0afc2-136">This parameter can be a combination of any of the file attribute flags (FILE_ATTRIBUTE_\*) defined in the header files.</span></span> <span data-ttu-id="0afc2-137">См. раздел [константы атрибутов файлов](../fileio/file-attribute-constants.md).</span><span class="sxs-lookup"><span data-stu-id="0afc2-137">See [File Attribute Constants](../fileio/file-attribute-constants.md).</span></span>

</dd> </dl>

<span data-ttu-id="0afc2-138">*дестфиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0afc2-138">*destFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0afc2-139">Указатель на строку, содержащую имя папки назначения.</span><span class="sxs-lookup"><span data-stu-id="0afc2-139">A pointer to a string that contains the name of the destination folder.</span></span>

</dd> </dl>

<span data-ttu-id="0afc2-140">*дестаттрибс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0afc2-140">*destAttribs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0afc2-141">Атрибуты конечной папки.</span><span class="sxs-lookup"><span data-stu-id="0afc2-141">The attributes of the destination folder.</span></span> <span data-ttu-id="0afc2-142">Этот параметр может быть сочетанием любого из флагов файлового атрибута (FILE_ATTRIBUTE_ \*), определенных в файлах заголовков.</span><span class="sxs-lookup"><span data-stu-id="0afc2-142">This parameter can be a combination of any of the file attribute flags (FILE_ATTRIBUTE_\*) defined in the header files.</span></span> <span data-ttu-id="0afc2-143">См. раздел [константы атрибутов файлов](../fileio/file-attribute-constants.md).</span><span class="sxs-lookup"><span data-stu-id="0afc2-143">See [File Attribute Constants](../fileio/file-attribute-constants.md).</span></span>

</dd> </dl>

<span data-ttu-id="0afc2-144">*результат* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="0afc2-144">*result* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0afc2-145">Целочисленное значение, указывающее, должна ли оболочка выполнить операцию.</span><span class="sxs-lookup"><span data-stu-id="0afc2-145">The integer value that indicates whether the Shell should perform the operation.</span></span> <span data-ttu-id="0afc2-146">Это может быть:</span><span class="sxs-lookup"><span data-stu-id="0afc2-146">One of the following:</span></span>

| <span data-ttu-id="0afc2-147">Значение</span><span class="sxs-lookup"><span data-stu-id="0afc2-147">Value</span></span>       | <span data-ttu-id="0afc2-148">Описание</span><span class="sxs-lookup"><span data-stu-id="0afc2-148">Description</span></span> |
|-------------|------------|
| <span data-ttu-id="0afc2-149">**IDYES**</span><span class="sxs-lookup"><span data-stu-id="0afc2-149">**IDYES**</span></span>       | <span data-ttu-id="0afc2-150">Разрешает операцию.</span><span class="sxs-lookup"><span data-stu-id="0afc2-150">Allows the operation.</span></span>           |
| <span data-ttu-id="0afc2-151">**IDNO**</span><span class="sxs-lookup"><span data-stu-id="0afc2-151">**IDNO**</span></span>        | <span data-ttu-id="0afc2-152">Предотвращает операцию в этой папке, но продолжит работу с другими утвержденными операциями (например, операцией пакетного копирования).</span><span class="sxs-lookup"><span data-stu-id="0afc2-152">Prevents the operation on this folder but continues with any other operations that have been approved (for example, a batch copy operation).</span></span>           |
| <span data-ttu-id="0afc2-153">**IDCANCEL**</span><span class="sxs-lookup"><span data-stu-id="0afc2-153">**IDCANCEL**</span></span>    | <span data-ttu-id="0afc2-154">Предотвращает текущую операцию и отменяет все ожидающие операции.</span><span class="sxs-lookup"><span data-stu-id="0afc2-154">Prevents the current operation and cancels any pending operations.</span></span>           |


</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="0afc2-155">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0afc2-155">Return value</span></span>

<span data-ttu-id="0afc2-156">Возвращает **S_OK** в случае успеха или код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="0afc2-156">Returns **S_OK** if successful, or an error code otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="0afc2-157">Примечания</span><span class="sxs-lookup"><span data-stu-id="0afc2-157">Remarks</span></span>

<span data-ttu-id="0afc2-158">Оболочка вызывает обработчик ловушки копирования поставщика облачных служб для каждой папки в зарегистрированном корне синхронизации.</span><span class="sxs-lookup"><span data-stu-id="0afc2-158">The Shell calls the cloud provider's copy hook handler for every folder under the registered sync root.</span></span> <span data-ttu-id="0afc2-159">Чтобы зарегистрировать обработчик события копирования для облачных папок, установите значение **копихук** в разделе **HKEY_LOCAL_MACHINE/Софтваре/Микрософт/Виндовс/куррентверсион/Експлорер/синкрутманажер/{синкрутид}** в качестве значения идентификатора CLSID объекта-ловушки копирования.</span><span class="sxs-lookup"><span data-stu-id="0afc2-159">To register a copy hook handler for cloud folders, set the **CopyHook** value under the **HKEY_LOCAL_MACHINE/Software/Microsoft/Windows/CurrentVersion/Explorer/SyncRootManager/{SyncRootId}** key to the CLSID of the copy hook object.</span></span>

<span data-ttu-id="0afc2-160">При вызове метода **Копикаллбакк** оболочка инициализирует интерфейс [исторажепровидеркопихук](nn-shobjidl-istorageprovidercopyhook.md) напрямую без использования интерфейса [ишеллекстинит](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) First.</span><span class="sxs-lookup"><span data-stu-id="0afc2-160">When the **CopyCallback** method is called, the Shell initializes the [IStorageProviderCopyHook](nn-shobjidl-istorageprovidercopyhook.md) interface directly without using an [IShellExtInit](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) interface first.</span></span>

## <a name="requirements"></a><span data-ttu-id="0afc2-161">Требования</span><span class="sxs-lookup"><span data-stu-id="0afc2-161">Requirements</span></span>

| <span data-ttu-id="0afc2-162">Требование</span><span class="sxs-lookup"><span data-stu-id="0afc2-162">Requirement</span></span> | <span data-ttu-id="0afc2-163">Значение</span><span class="sxs-lookup"><span data-stu-id="0afc2-163">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0afc2-164">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0afc2-164">Minimum supported client</span></span> | <span data-ttu-id="0afc2-165">Windows 10 Insider Preview Build 19624</span><span class="sxs-lookup"><span data-stu-id="0afc2-165">Windows 10 Insider Preview Build 19624</span></span>                                |
| <span data-ttu-id="0afc2-166">Header</span><span class="sxs-lookup"><span data-stu-id="0afc2-166">Header</span></span>                   | <span data-ttu-id="0afc2-167">shobjidl. h</span><span class="sxs-lookup"><span data-stu-id="0afc2-167">shobjidl.h</span></span>   |

## <a name="see-also"></a><span data-ttu-id="0afc2-168">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0afc2-168">See also</span></span>

[<span data-ttu-id="0afc2-169">Создание облачного модуля синхронизации, поддерживающего файлы заполнителей</span><span class="sxs-lookup"><span data-stu-id="0afc2-169">Build a Cloud Sync Engine that Supports Placeholder Files</span></span>](../cfapi/build-a-cloud-file-sync-engine.md)