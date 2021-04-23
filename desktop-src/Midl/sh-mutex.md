---
title: Ключевое слово sh_mutex
description: '\_Ключевое слово \ SH Mutex \ указывает, что системный объект является обработчиком мьютекса.'
keywords:
- sh_mutex ключевого слова MIDL
topic_type:
- apiref
api_name:
- sh_mutex
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 8616ded29d1d8c106af21e6cd1252535f4da8457
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105720821"
---
# <a name="sh_mutex-keyword"></a><span data-ttu-id="de17b-104">\_ключевое слово мьютекса SH</span><span class="sxs-lookup"><span data-stu-id="de17b-104">sh\_mutex keyword</span></span>

<span data-ttu-id="de17b-105">Ключевое слово **\_ мьютекса SH** указывает, что объект `system_handle` содержит маркер для мьютекса.</span><span class="sxs-lookup"><span data-stu-id="de17b-105">The **sh\_mutex** keyword specifies that a `system_handle` holds a handle to a mutex.</span></span>

``` syntax
[system_handle(sh_mutex)]

[system_handle(sh_mutex, access-rights)]
```

## <a name="parameters"></a><span data-ttu-id="de17b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="de17b-106">Parameters</span></span>

<span data-ttu-id="de17b-107">Это ключевое слово является параметром для [**system_handle**](system-handle.md).</span><span class="sxs-lookup"><span data-stu-id="de17b-107">This keyword is a parameter for [**system_handle**](system-handle.md).</span></span>

<span data-ttu-id="de17b-108">В документации по [**system_handle**](system-handle.md) также содержатся сведения о необязательном использовании параметра *Access-Rights* .</span><span class="sxs-lookup"><span data-stu-id="de17b-108">The [**system_handle**](system-handle.md) documentation also contains details on optional use of the *access-rights* parameter.</span></span> <span data-ttu-id="de17b-109">Поведение по умолчанию `DUPLICATE_SAME_ACCESS` для каждой спецификации [ **функции дупликатехандле**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .</span><span class="sxs-lookup"><span data-stu-id="de17b-109">The default behavior is `DUPLICATE_SAME_ACCESS` per [**DuplicateHandle** function](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) specifications.</span></span>

## <a name="remarks"></a><span data-ttu-id="de17b-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="de17b-110">Remarks</span></span>

<span data-ttu-id="de17b-111">Чтобы использовать это ключевое слово с `system_handle` атрибутом, `-target` необходимо установить для флага значение `NT100` (или более высокий) при выполнении midl.exe.</span><span class="sxs-lookup"><span data-stu-id="de17b-111">In order to use this keyword with the `system_handle` attribute, the `-target` flag must be set to `NT100` (or higher) when running midl.exe.</span></span>

## <a name="examples"></a><span data-ttu-id="de17b-112">Примеры</span><span class="sxs-lookup"><span data-stu-id="de17b-112">Examples</span></span>

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT WaitOnThisMutex([in, system_handle(sh_mutex)] HANDLE mutex);
}
```

## <a name="requirements"></a><span data-ttu-id="de17b-113">Требования</span><span class="sxs-lookup"><span data-stu-id="de17b-113">Requirements</span></span>

| &nbsp; | &nbsp; |
|-|-|
| <span data-ttu-id="de17b-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="de17b-114">Minimum supported client</span></span> | <span data-ttu-id="de17b-115">Юбилейное обновление Windows 10 (версия 1607, сборка 14393)</span><span class="sxs-lookup"><span data-stu-id="de17b-115">Windows 10 Anniversary Update (version 1607, build 14393)</span></span> |
| <span data-ttu-id="de17b-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="de17b-116">Minimum supported server</span></span> | <span data-ttu-id="de17b-117">Windows Server 2016 (сборка 14393)</span><span class="sxs-lookup"><span data-stu-id="de17b-117">Windows Server 2016 (build 14393)</span></span> |

## <a name="see-also"></a><span data-ttu-id="de17b-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="de17b-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de17b-119">**system_handle**</span><span class="sxs-lookup"><span data-stu-id="de17b-119">**system_handle**</span></span>](system-handle.md)
</dt> <dt>

[<span data-ttu-id="de17b-120">Мьютексные объекты</span><span class="sxs-lookup"><span data-stu-id="de17b-120">Mutex Objects</span></span>](../sync/mutex-objects.md)
</dt> <dt>

[<span data-ttu-id="de17b-121">Безопасность объекта синхронизации и права доступа</span><span class="sxs-lookup"><span data-stu-id="de17b-121">Synchronization Object Security and Access Rights</span></span>](../sync/synchronization-object-security-and-access-rights.md)
</dt> <dt>

[<span data-ttu-id="de17b-122">Функция **CreateMutex**</span><span class="sxs-lookup"><span data-stu-id="de17b-122">**CreateMutex** function</span></span>](/windows/win32/api/synchapi/nf-synchapi-createmutexa)
</dt> <dt>

[<span data-ttu-id="de17b-123">Функция **креатемутексекс**</span><span class="sxs-lookup"><span data-stu-id="de17b-123">**CreateMutexEx** function</span></span>](/windows/win32/api/synchapi/nf-synchapi-createmutexexa)
</dt> </dl>