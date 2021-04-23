---
title: Ключевое слово sh_process
description: '\_Ключевое слово \ SH Process \ указывает, что системный объект является обработчиком процесса.'
keywords:
- sh_process ключевого слова MIDL
topic_type:
- apiref
api_name:
- sh_process
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 3652c6889c687173bbf7b397cddff4659c0329f1
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/06/2021
ms.locfileid: "105719887"
---
# <a name="sh_process-keyword"></a><span data-ttu-id="d9f6e-104">SH \_ Process, ключевое слово</span><span class="sxs-lookup"><span data-stu-id="d9f6e-104">sh\_process keyword</span></span>

<span data-ttu-id="d9f6e-105">Ключевое слово **sh \_ Process** указывает, что `system_handle` содержит обработчик для процесса.</span><span class="sxs-lookup"><span data-stu-id="d9f6e-105">The **sh\_process** keyword specifies that a `system_handle` holds a handle to a process.</span></span>

``` syntax
[system_handle(sh_process)]

[system_handle(sh_process, access-rights)]
```

## <a name="parameters"></a><span data-ttu-id="d9f6e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d9f6e-106">Parameters</span></span>

<span data-ttu-id="d9f6e-107">Это ключевое слово является параметром для [**system_handle**](system-handle.md).</span><span class="sxs-lookup"><span data-stu-id="d9f6e-107">This keyword is a parameter for [**system_handle**](system-handle.md).</span></span>

<span data-ttu-id="d9f6e-108">В документации по [**system_handle**](system-handle.md) также содержатся сведения о необязательном использовании параметра *Access-Rights* .</span><span class="sxs-lookup"><span data-stu-id="d9f6e-108">The [**system_handle**](system-handle.md) documentation also contains details on optional use of the *access-rights* parameter.</span></span> <span data-ttu-id="d9f6e-109">Поведение по умолчанию `DUPLICATE_SAME_ACCESS` для каждой спецификации [ **функции дупликатехандле**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .</span><span class="sxs-lookup"><span data-stu-id="d9f6e-109">The default behavior is `DUPLICATE_SAME_ACCESS` per [**DuplicateHandle** function](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) specifications.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9f6e-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d9f6e-110">Remarks</span></span>

<span data-ttu-id="d9f6e-111">Чтобы использовать это ключевое слово с `system_handle` атрибутом, `-target` необходимо установить для флага значение `NT100` (или более высокий) при выполнении midl.exe.</span><span class="sxs-lookup"><span data-stu-id="d9f6e-111">In order to use this keyword with the `system_handle` attribute, the `-target` flag must be set to `NT100` (or higher) when running midl.exe.</span></span>

## <a name="examples"></a><span data-ttu-id="d9f6e-112">Примеры</span><span class="sxs-lookup"><span data-stu-id="d9f6e-112">Examples</span></span>

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT GetStubProcess([out, system_handle(sh_process)] HANDLE* processHandle);

    HRESULT WatchProcess([in, system_handle(sh_process, PROCESS_QUERY_INFORMATION | PROCESS_QUERY_LIMITED_INFORMATION)] HANDLE processHandle);
}
```

## <a name="requirements"></a><span data-ttu-id="d9f6e-113">Требования</span><span class="sxs-lookup"><span data-stu-id="d9f6e-113">Requirements</span></span>

| &nbsp; | &nbsp; |
|-|-|
| <span data-ttu-id="d9f6e-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d9f6e-114">Minimum supported client</span></span> | <span data-ttu-id="d9f6e-115">Юбилейное обновление Windows 10 (версия 1607, сборка 14393)</span><span class="sxs-lookup"><span data-stu-id="d9f6e-115">Windows 10 Anniversary Update (version 1607, build 14393)</span></span> |
| <span data-ttu-id="d9f6e-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d9f6e-116">Minimum supported server</span></span> | <span data-ttu-id="d9f6e-117">Windows Server 2016 (сборка 14393)</span><span class="sxs-lookup"><span data-stu-id="d9f6e-117">Windows Server 2016 (build 14393)</span></span> |

## <a name="see-also"></a><span data-ttu-id="d9f6e-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d9f6e-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9f6e-119">**system_handle**</span><span class="sxs-lookup"><span data-stu-id="d9f6e-119">**system_handle**</span></span>](system-handle.md)
</dt> <dt>

[<span data-ttu-id="d9f6e-120">Процессы и потоки</span><span class="sxs-lookup"><span data-stu-id="d9f6e-120">About Processes and Threads</span></span>](../procthread/about-processes-and-threads.md)
</dt> <dt>

[<span data-ttu-id="d9f6e-121">Безопасность процессов и права доступа</span><span class="sxs-lookup"><span data-stu-id="d9f6e-121">Process Security and Access Rights</span></span>](../procthread/process-security-and-access-rights.md)
</dt> <dt>

[<span data-ttu-id="d9f6e-122">Функция **CreateProcess**</span><span class="sxs-lookup"><span data-stu-id="d9f6e-122">**CreateProcess** function</span></span>](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)
</dt> <dt>

[<span data-ttu-id="d9f6e-123">Функция **OpenProcess**</span><span class="sxs-lookup"><span data-stu-id="d9f6e-123">**OpenProcess** function</span></span>](/win32/api/processthreadsapi/nf-processthreadsapi-openprocess)
</dt> </dl>