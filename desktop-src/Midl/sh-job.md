---
title: Ключевое слово sh_job
description: '\_Ключевое слово \ SH Job \ указывает, что системный объект является обработчиком задания.'
keywords:
- sh_job ключевого слова MIDL
topic_type:
- apiref
api_name:
- sh_job
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: db24f9dc84f2bb56f57327090485b406ad1a437f
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/06/2021
ms.locfileid: "103999821"
---
# <a name="sh_job-keyword"></a><span data-ttu-id="ee3b3-104">\_ключевое слово задания SH</span><span class="sxs-lookup"><span data-stu-id="ee3b3-104">sh\_job keyword</span></span>

<span data-ttu-id="ee3b3-105">Ключевое слово **\_ задания SH** указывает, что `system_handle` содержит обработчик для задания.</span><span class="sxs-lookup"><span data-stu-id="ee3b3-105">The **sh\_job** keyword specifies that a `system_handle` holds a handle to a job.</span></span>

``` syntax
[system_handle(sh_job)]

[system_handle(sh_job, access-rights)]
```

## <a name="parameters"></a><span data-ttu-id="ee3b3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ee3b3-106">Parameters</span></span>

<span data-ttu-id="ee3b3-107">Это ключевое слово является параметром для [**system_handle**](system-handle.md).</span><span class="sxs-lookup"><span data-stu-id="ee3b3-107">This keyword is a parameter for [**system_handle**](system-handle.md).</span></span>

<span data-ttu-id="ee3b3-108">В документации по [**system_handle**](system-handle.md) также содержатся сведения о необязательном использовании параметра *Access-Rights* .</span><span class="sxs-lookup"><span data-stu-id="ee3b3-108">The [**system_handle**](system-handle.md) documentation also contains details on optional use of the *access-rights* parameter.</span></span> <span data-ttu-id="ee3b3-109">Поведение по умолчанию `DUPLICATE_SAME_ACCESS` для каждой спецификации [ **функции дупликатехандле**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .</span><span class="sxs-lookup"><span data-stu-id="ee3b3-109">The default behavior is `DUPLICATE_SAME_ACCESS` per [**DuplicateHandle** function](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) specifications.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee3b3-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ee3b3-110">Remarks</span></span>

<span data-ttu-id="ee3b3-111">Чтобы использовать это ключевое слово с `system_handle` атрибутом, `-target` необходимо установить для флага значение `NT100` (или более высокий) при выполнении midl.exe.</span><span class="sxs-lookup"><span data-stu-id="ee3b3-111">In order to use this keyword with the `system_handle` attribute, the `-target` flag must be set to `NT100` (or higher) when running midl.exe.</span></span>

## <a name="examples"></a><span data-ttu-id="ee3b3-112">Примеры</span><span class="sxs-lookup"><span data-stu-id="ee3b3-112">Examples</span></span>

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT SetJob([in, system_handle(sh_job)] HANDLE job);

    HRESULT GetJobForAccounting([out, system_handle(sh_job, JOB_OBJECT_QUERY)] HANDLE* pJob);
}
```

## <a name="requirements"></a><span data-ttu-id="ee3b3-113">Требования</span><span class="sxs-lookup"><span data-stu-id="ee3b3-113">Requirements</span></span>

| &nbsp; | &nbsp; |
|-|-|
| <span data-ttu-id="ee3b3-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ee3b3-114">Minimum supported client</span></span> | <span data-ttu-id="ee3b3-115">Юбилейное обновление Windows 10 (версия 1607, сборка 14393)</span><span class="sxs-lookup"><span data-stu-id="ee3b3-115">Windows 10 Anniversary Update (version 1607, build 14393)</span></span> |
| <span data-ttu-id="ee3b3-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ee3b3-116">Minimum supported server</span></span> | <span data-ttu-id="ee3b3-117">Windows Server 2016 (сборка 14393)</span><span class="sxs-lookup"><span data-stu-id="ee3b3-117">Windows Server 2016 (build 14393)</span></span> |

## <a name="see-also"></a><span data-ttu-id="ee3b3-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ee3b3-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee3b3-119">**system_handle**</span><span class="sxs-lookup"><span data-stu-id="ee3b3-119">**system_handle**</span></span>](system-handle.md)
</dt> <dt>

[<span data-ttu-id="ee3b3-120">Объекты заданий</span><span class="sxs-lookup"><span data-stu-id="ee3b3-120">Job Objects</span></span>](../procthread/job-objects.md)
</dt> <dt>

[<span data-ttu-id="ee3b3-121">Права доступа и безопасности объекта задания</span><span class="sxs-lookup"><span data-stu-id="ee3b3-121">Job Object Security and Access Rights</span></span>](../procthread/job-object-security-and-access-rights.md)
</dt> <dt>

[<span data-ttu-id="ee3b3-122">Функция **креатежобобжект**</span><span class="sxs-lookup"><span data-stu-id="ee3b3-122">**CreateJobObject** function</span></span>](/windows/win32/api/winbase/nf-winbase-createjobobjecta)
</dt> </dl>
