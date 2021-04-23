---
title: Атрибут system_handle
description: Атрибут \ system_handle \ задает тип обрабатываемого системой типа.
keywords:
- system_handle атрибута MIDL
topic_type:
- apiref
api_name:
- system_handle
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: f414654cdbd2eb07837455174f6142005f56a4b5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105720040"
---
# <a name="system_handle-attribute"></a><span data-ttu-id="793bb-104">Атрибут system_handle</span><span class="sxs-lookup"><span data-stu-id="793bb-104">system_handle attribute</span></span>

<span data-ttu-id="793bb-105">Атрибут \[ **system_handle** \] задает системный тип обработчика, представляющий доступ к системному объекту.</span><span class="sxs-lookup"><span data-stu-id="793bb-105">The \[**system_handle**\] attribute specifies a system-defined handle type that represents access to a system object.</span></span>

``` syntax
[system_handle(system-handle-type[,optional-access-mask])]
```

## <a name="parameters"></a><span data-ttu-id="793bb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="793bb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="793bb-107">*System-Handle-Type*</span><span class="sxs-lookup"><span data-stu-id="793bb-107">*system-handle-type*</span></span> 
</dt> <dd>

<span data-ttu-id="793bb-108">Задает один из параметров типа системного обработчика.</span><span class="sxs-lookup"><span data-stu-id="793bb-108">Specifies one of the system handle type options.</span></span>

<span data-ttu-id="793bb-109">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="793bb-109">The valid options are:</span></span>
* <span data-ttu-id="793bb-110">[sh_composition](sh-composition.md) — маркер поверхности DirectComposition</span><span class="sxs-lookup"><span data-stu-id="793bb-110">[sh_composition](sh-composition.md) - A DirectComposition surface handle</span></span>
* <span data-ttu-id="793bb-111">[sh_event](sh-event.md) — объект именованного или безымянного события</span><span class="sxs-lookup"><span data-stu-id="793bb-111">[sh_event](sh-event.md) - A named or unnamed event object</span></span>
* <span data-ttu-id="793bb-112">[sh_file](sh-file.md) -файл или устройство ввода-вывода</span><span class="sxs-lookup"><span data-stu-id="793bb-112">[sh_file](sh-file.md) - A file or I/O device</span></span>
* <span data-ttu-id="793bb-113">[sh_job](sh-job.md) — объект задания</span><span class="sxs-lookup"><span data-stu-id="793bb-113">[sh_job](sh-job.md) - A job object</span></span>
* <span data-ttu-id="793bb-114">[sh_mutex](sh-mutex.md) — именованный или безымянный объект Mutex</span><span class="sxs-lookup"><span data-stu-id="793bb-114">[sh_mutex](sh-mutex.md) - A named or unnamed mutex object</span></span>
* <span data-ttu-id="793bb-115">[sh_pipe](sh-pipe.md) — объект анонимного или именованного канала</span><span class="sxs-lookup"><span data-stu-id="793bb-115">[sh_pipe](sh-pipe.md) - An anonymous or named pipe object</span></span>
* <span data-ttu-id="793bb-116">[sh_process](sh-process.md) — объект процесса</span><span class="sxs-lookup"><span data-stu-id="793bb-116">[sh_process](sh-process.md) - A process object</span></span>
* <span data-ttu-id="793bb-117">[sh_reg_key](sh-reg-key.md) — раздел реестра</span><span class="sxs-lookup"><span data-stu-id="793bb-117">[sh_reg_key](sh-reg-key.md) - A registry key</span></span>
* <span data-ttu-id="793bb-118">[sh_section](sh-section.md) — раздел общей памяти</span><span class="sxs-lookup"><span data-stu-id="793bb-118">[sh_section](sh-section.md) - A shared memory section</span></span>
* <span data-ttu-id="793bb-119">[sh_semaphore](sh-semaphore.md) — именованный или безымянный объект семафора</span><span class="sxs-lookup"><span data-stu-id="793bb-119">[sh_semaphore](sh-semaphore.md) - A named or unnamed semaphore object</span></span>
* <span data-ttu-id="793bb-120">[sh_socket](sh-socket.md) — объект сокета WinSock</span><span class="sxs-lookup"><span data-stu-id="793bb-120">[sh_socket](sh-socket.md) - A WinSock socket object</span></span>
* <span data-ttu-id="793bb-121">[sh_thread](sh-thread.md) — объект потока</span><span class="sxs-lookup"><span data-stu-id="793bb-121">[sh_thread](sh-thread.md) - A thread object</span></span>
* <span data-ttu-id="793bb-122">[sh_token](sh-token.md) — объект маркера доступа</span><span class="sxs-lookup"><span data-stu-id="793bb-122">[sh_token](sh-token.md) - An access token object</span></span>

</dd> <dt>

<span data-ttu-id="793bb-123">*Необязательная — доступ к маске*</span><span class="sxs-lookup"><span data-stu-id="793bb-123">*optional-access-mask*</span></span>
</dt> <dd>

<span data-ttu-id="793bb-124">При необходимости запрашивает определенные права доступа, применяемые к дублированному маркеру.</span><span class="sxs-lookup"><span data-stu-id="793bb-124">Optionally requests specific access rights applied to the duplicated handle.</span></span> <span data-ttu-id="793bb-125">По умолчанию, если этот параметр не указан, то этот маркер будет дублироваться с тем же доступом.</span><span class="sxs-lookup"><span data-stu-id="793bb-125">By default when this is unspecified, the handle will be duplicated with the same access.</span></span> 

<span data-ttu-id="793bb-126">Чтобы указать другой уровень доступа, используйте специальные права доступа объекта, соответствующие выбранному базовому системному объекту.</span><span class="sxs-lookup"><span data-stu-id="793bb-126">To specify a different level of access, use object specific access rights corresponding to the underlying system object selected.</span></span>

<span data-ttu-id="793bb-127">Дополнительные сведения о распространении прав доступа во время дублирования можно найти в документации по [дупликатехандле](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .</span><span class="sxs-lookup"><span data-stu-id="793bb-127">More information on how access rights are propagated during duplication can be found on the [DuplicateHandle](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) documentation.</span></span>

<span data-ttu-id="793bb-128">Ссылки на списки прав доступа для каждого типа объектов можно найти в справочнике по *дупликатехандле* , а также в **разделах** , посвященных заголовкам каждой `sh_*` страницы параметров.</span><span class="sxs-lookup"><span data-stu-id="793bb-128">Links to lists of access rights for each type of object can be found in the *DuplicateHandle* reference as well as in the **See also** headings of each `sh_*` parameter page.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="793bb-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="793bb-129">Remarks</span></span>

<span data-ttu-id="793bb-130">Для использования этого атрибута `-target` флаг должен быть установлен в значение `NT100` (или выше) при выполнении midl.exe.</span><span class="sxs-lookup"><span data-stu-id="793bb-130">In order to use this attribute, the `-target` flag must be set to `NT100` (or higher) when running midl.exe.</span></span>

<span data-ttu-id="793bb-131">Дескрипторы системы — это дескрипторы, определяемые операционной системой для предоставления доступа к системному ресурсу.</span><span class="sxs-lookup"><span data-stu-id="793bb-131">System handles are handles that are defined by the operating system to provide access to a system resource.</span></span> <span data-ttu-id="793bb-132">При объявлении атрибута необходимо указать конкретный тип объекта, лежащий в основе этого маркера.</span><span class="sxs-lookup"><span data-stu-id="793bb-132">The specific type of the object behind the handle must be specified when declaring the attribute.</span></span>

<span data-ttu-id="793bb-133">Для маркера, помеченного `[in]` , маркер будет дублироваться в удаленной процедуре и оставаться действительным в течение этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="793bb-133">For a handle marked `[in]`, the handle will be duplicated into the remote procedure and remains valid for the duration of that procedure.</span></span> <span data-ttu-id="793bb-134">При возврате из удаленной процедуры дублированный маркер освобождается.</span><span class="sxs-lookup"><span data-stu-id="793bb-134">On return from the remote procedure, the duplicated handle is freed.</span></span> <span data-ttu-id="793bb-135">Чтобы обеспечить доступ к базовому объекту, удаленное приложение должно дублировать этот обработчик в его собственное адресное пространство.</span><span class="sxs-lookup"><span data-stu-id="793bb-135">To maintain access to the underlying object, the remote application must duplicate the handle into its own address space.</span></span>

<span data-ttu-id="793bb-136">Напротив, для маркера, помеченного `[out]` , когда удаленная процедура возвращает маркер из вызова, Удаленная процедура потеряет владение ей.</span><span class="sxs-lookup"><span data-stu-id="793bb-136">By contrast, for a handle marked `[out]`, when a remote procedure returns a handle from a call, the remote procedure will lose ownership of it.</span></span> <span data-ttu-id="793bb-137">Чтобы обеспечить доступ к базовому объекту, Удаленная процедура должна дублировать этот обработчик и возвращать дубликат.</span><span class="sxs-lookup"><span data-stu-id="793bb-137">To maintain access to the underlying object, the remote procedure should duplicate the handle and return the duplicate.</span></span> <span data-ttu-id="793bb-138">Возвращенный обработчик становится владельцем вызывающей стороны, который принимает ответственность за его закрытие, когда доступ к базовому системному объекту больше не требуется.</span><span class="sxs-lookup"><span data-stu-id="793bb-138">The returned handle then becomes owned by the caller who assumes a responsibility to close it when access to the underlying system object is no longer necessary.</span></span>

<span data-ttu-id="793bb-139">Так как это механизм ретрансляции доступа к системному объекту, этот атрибут применим только к вызовам между процедурами на том же компьютере.</span><span class="sxs-lookup"><span data-stu-id="793bb-139">As this is a mechanism for relaying access to a system object, this attribute is only applicable to calls between procedures on the same machine.</span></span>

<span data-ttu-id="793bb-140">Параметры создания и доступа, предоставляемые базовому объекту за системным маркером при его создании, определяют возможность его успешного приема в контексте удаленной процедуры.</span><span class="sxs-lookup"><span data-stu-id="793bb-140">The creation and access parameters given to the underlying object behind the system handle on its creation will dictate whether it can be successfully marshalled to the remote procedure context.</span></span>

<span data-ttu-id="793bb-141">Массив `system_handle` можно передать либо в, либо с помощью синтаксиса, который содержится в документации по [**атрибуту size_is**](size-is.md) .</span><span class="sxs-lookup"><span data-stu-id="793bb-141">An array of `system_handle` can be passed either in or out with the syntax found in the [**size_is attribute**](size-is.md) documentation.</span></span>

## <a name="examples"></a><span data-ttu-id="793bb-142">Примеры</span><span class="sxs-lookup"><span data-stu-id="793bb-142">Examples</span></span>

<span data-ttu-id="793bb-143">В следующих примерах используется несколько примеров `system_handle` .</span><span class="sxs-lookup"><span data-stu-id="793bb-143">The following examples several uses of `system_handle`.</span></span> <span data-ttu-id="793bb-144">Полный пример см. в примере [системхандлепассинг](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SystemHandlePassing) .</span><span class="sxs-lookup"><span data-stu-id="793bb-144">For a complete sample, see the [SystemHandlePassing](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SystemHandlePassing) sample.</span></span>

```c
interface MyInterface : IUnknown                         
{         
    HRESULT Proc1([in, system_handle(sh_file)] HANDLE writeThisFile);

    HRESULT Proc2([in, system_handle(sh_pipe, FILE_GENERIC_READ)] HANDLE readThisPipe);

    HRESULT Proc3([out, system_handle(sh_composition)] HANDLE* visual);

    HRESULT Proc4([in] DWORD cEvents, [out, system_handle(sh_event), size_is(cEvents)] HANDLE* pWatchAllTheseEvents);
}
```

## <a name="requirements"></a><span data-ttu-id="793bb-145">Требования</span><span class="sxs-lookup"><span data-stu-id="793bb-145">Requirements</span></span>

| &nbsp; | &nbsp; |
|-|-|
| <span data-ttu-id="793bb-146">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="793bb-146">Minimum supported client</span></span> | <span data-ttu-id="793bb-147">Юбилейное обновление Windows 10 (версия 1607, сборка 14393)</span><span class="sxs-lookup"><span data-stu-id="793bb-147">Windows 10 Anniversary Update (version 1607, build 14393)</span></span> |
| <span data-ttu-id="793bb-148">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="793bb-148">Minimum supported server</span></span> | <span data-ttu-id="793bb-149">Windows Server 2016 (сборка 14393)</span><span class="sxs-lookup"><span data-stu-id="793bb-149">Windows Server 2016 (build 14393)</span></span> |

## <a name="see-also"></a><span data-ttu-id="793bb-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="793bb-150">See also</span></span>

<dl> <dt>
<!--
[System Handle Passing sample code](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SystemHandlePassing)
</dt> <dt>
-->

[<span data-ttu-id="793bb-151">Ключ "/target"</span><span class="sxs-lookup"><span data-stu-id="793bb-151">/target switch</span></span>](./-target.md)
</dt> <dt>

[<span data-ttu-id="793bb-152">Привязка и дескрипторы</span><span class="sxs-lookup"><span data-stu-id="793bb-152">Binding and Handles</span></span>](../Rpc/binding-and-handles.md)
</dt> <dt>

[<span data-ttu-id="793bb-153">Дескрипторы и объекты</span><span class="sxs-lookup"><span data-stu-id="793bb-153">Handles and Objects</span></span>](../sysinfo/handles-and-objects.md)
</dt> <dt>

[<span data-ttu-id="793bb-154">Файл определения интерфейса (IDL)</span><span class="sxs-lookup"><span data-stu-id="793bb-154">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="793bb-155">**дупликатехандле**</span><span class="sxs-lookup"><span data-stu-id="793bb-155">**DuplicateHandle**</span></span>](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle)
</dt> <dt>

[<span data-ttu-id="793bb-156">Дескрипторы безопасности</span><span class="sxs-lookup"><span data-stu-id="793bb-156">Security Descriptors</span></span>](../secauthz/security-descriptors.md)
</dt></dl>
