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
# <a name="system_handle-attribute"></a>Атрибут system_handle

Атрибут \[ **system_handle** \] задает системный тип обработчика, представляющий доступ к системному объекту.

``` syntax
[system_handle(system-handle-type[,optional-access-mask])]
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*System-Handle-Type* 
</dt> <dd>

Задает один из параметров типа системного обработчика.

Допустимые значения:
* [sh_composition](sh-composition.md) — маркер поверхности DirectComposition
* [sh_event](sh-event.md) — объект именованного или безымянного события
* [sh_file](sh-file.md) -файл или устройство ввода-вывода
* [sh_job](sh-job.md) — объект задания
* [sh_mutex](sh-mutex.md) — именованный или безымянный объект Mutex
* [sh_pipe](sh-pipe.md) — объект анонимного или именованного канала
* [sh_process](sh-process.md) — объект процесса
* [sh_reg_key](sh-reg-key.md) — раздел реестра
* [sh_section](sh-section.md) — раздел общей памяти
* [sh_semaphore](sh-semaphore.md) — именованный или безымянный объект семафора
* [sh_socket](sh-socket.md) — объект сокета WinSock
* [sh_thread](sh-thread.md) — объект потока
* [sh_token](sh-token.md) — объект маркера доступа

</dd> <dt>

*Необязательная — доступ к маске*
</dt> <dd>

При необходимости запрашивает определенные права доступа, применяемые к дублированному маркеру. По умолчанию, если этот параметр не указан, то этот маркер будет дублироваться с тем же доступом. 

Чтобы указать другой уровень доступа, используйте специальные права доступа объекта, соответствующие выбранному базовому системному объекту.

Дополнительные сведения о распространении прав доступа во время дублирования можно найти в документации по [дупликатехандле](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .

Ссылки на списки прав доступа для каждого типа объектов можно найти в справочнике по *дупликатехандле* , а также в **разделах** , посвященных заголовкам каждой `sh_*` страницы параметров.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Для использования этого атрибута `-target` флаг должен быть установлен в значение `NT100` (или выше) при выполнении midl.exe.

Дескрипторы системы — это дескрипторы, определяемые операционной системой для предоставления доступа к системному ресурсу. При объявлении атрибута необходимо указать конкретный тип объекта, лежащий в основе этого маркера.

Для маркера, помеченного `[in]` , маркер будет дублироваться в удаленной процедуре и оставаться действительным в течение этой процедуры. При возврате из удаленной процедуры дублированный маркер освобождается. Чтобы обеспечить доступ к базовому объекту, удаленное приложение должно дублировать этот обработчик в его собственное адресное пространство.

Напротив, для маркера, помеченного `[out]` , когда удаленная процедура возвращает маркер из вызова, Удаленная процедура потеряет владение ей. Чтобы обеспечить доступ к базовому объекту, Удаленная процедура должна дублировать этот обработчик и возвращать дубликат. Возвращенный обработчик становится владельцем вызывающей стороны, который принимает ответственность за его закрытие, когда доступ к базовому системному объекту больше не требуется.

Так как это механизм ретрансляции доступа к системному объекту, этот атрибут применим только к вызовам между процедурами на том же компьютере.

Параметры создания и доступа, предоставляемые базовому объекту за системным маркером при его создании, определяют возможность его успешного приема в контексте удаленной процедуры.

Массив `system_handle` можно передать либо в, либо с помощью синтаксиса, который содержится в документации по [**атрибуту size_is**](size-is.md) .

## <a name="examples"></a>Примеры

В следующих примерах используется несколько примеров `system_handle` . Полный пример см. в примере [системхандлепассинг](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SystemHandlePassing) .

```c
interface MyInterface : IUnknown                         
{         
    HRESULT Proc1([in, system_handle(sh_file)] HANDLE writeThisFile);

    HRESULT Proc2([in, system_handle(sh_pipe, FILE_GENERIC_READ)] HANDLE readThisPipe);

    HRESULT Proc3([out, system_handle(sh_composition)] HANDLE* visual);

    HRESULT Proc4([in] DWORD cEvents, [out, system_handle(sh_event), size_is(cEvents)] HANDLE* pWatchAllTheseEvents);
}
```

## <a name="requirements"></a>Требования

| &nbsp; | &nbsp; |
|-|-|
| Минимальная версия клиента | Юбилейное обновление Windows 10 (версия 1607, сборка 14393) |
| Минимальная версия сервера | Windows Server 2016 (сборка 14393) |

## <a name="see-also"></a>См. также раздел

<dl> <dt>
<!--
[System Handle Passing sample code](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SystemHandlePassing)
</dt> <dt>
-->

[Ключ "/target"](./-target.md)
</dt> <dt>

[Привязка и дескрипторы](../Rpc/binding-and-handles.md)
</dt> <dt>

[Дескрипторы и объекты](../sysinfo/handles-and-objects.md)
</dt> <dt>

[Файл определения интерфейса (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**дупликатехандле**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle)
</dt> <dt>

[Дескрипторы безопасности](../secauthz/security-descriptors.md)
</dt></dl>
