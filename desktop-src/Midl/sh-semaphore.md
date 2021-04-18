---
title: Ключевое слово sh_semaphore
description: '\_Ключевое слово \ SH семафор \ указывает, что системный объект является обработчиком семафора.'
keywords:
- sh_semaphore ключевого слова MIDL
topic_type:
- apiref
api_name:
- sh_semaphore
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 2a5c33e4c44b67e3106a48cde244abaf13f41ad5
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/06/2021
ms.locfileid: "105719877"
---
# <a name="sh_semaphore-keyword"></a><span data-ttu-id="2d2b1-104">\_ключевое слово семафора SH</span><span class="sxs-lookup"><span data-stu-id="2d2b1-104">sh\_semaphore keyword</span></span>

<span data-ttu-id="2d2b1-105">Ключевое слово **\_ семафора SH** указывает, что объект `system_handle` содержит маркер для семафора.</span><span class="sxs-lookup"><span data-stu-id="2d2b1-105">The **sh\_semaphore** keyword specifies that a `system_handle` holds a handle to a semaphore.</span></span>

``` syntax
[system_handle(sh_semaphore)]

[system_handle(sh_semaphore, access-rights)]
```

## <a name="parameters"></a><span data-ttu-id="2d2b1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2d2b1-106">Parameters</span></span>

<span data-ttu-id="2d2b1-107">Это ключевое слово является параметром для [**system_handle**](system-handle.md).</span><span class="sxs-lookup"><span data-stu-id="2d2b1-107">This keyword is a parameter for [**system_handle**](system-handle.md).</span></span>

<span data-ttu-id="2d2b1-108">В документации по [**system_handle**](system-handle.md) также содержатся сведения о необязательном использовании параметра *Access-Rights* .</span><span class="sxs-lookup"><span data-stu-id="2d2b1-108">The [**system_handle**](system-handle.md) documentation also contains details on optional use of the *access-rights* parameter.</span></span> <span data-ttu-id="2d2b1-109">Поведение по умолчанию `DUPLICATE_SAME_ACCESS` для каждой спецификации [ **функции дупликатехандле**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .</span><span class="sxs-lookup"><span data-stu-id="2d2b1-109">The default behavior is `DUPLICATE_SAME_ACCESS` per [**DuplicateHandle** function](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) specifications.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d2b1-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2d2b1-110">Remarks</span></span>

<span data-ttu-id="2d2b1-111">Чтобы использовать это ключевое слово с `system_handle` атрибутом, `-target` необходимо установить для флага значение `NT100` (или более высокий) при выполнении midl.exe.</span><span class="sxs-lookup"><span data-stu-id="2d2b1-111">In order to use this keyword with the `system_handle` attribute, the `-target` flag must be set to `NT100` (or higher) when running midl.exe.</span></span>

## <a name="examples"></a><span data-ttu-id="2d2b1-112">Примеры</span><span class="sxs-lookup"><span data-stu-id="2d2b1-112">Examples</span></span>

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT SignalThisSemaphore([in, system_handle(sh_semaphore)] HANDLE semaphore);
}
```

## <a name="requirements"></a><span data-ttu-id="2d2b1-113">Требования</span><span class="sxs-lookup"><span data-stu-id="2d2b1-113">Requirements</span></span>

| &nbsp; | &nbsp; |
|-|-|
| <span data-ttu-id="2d2b1-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2d2b1-114">Minimum supported client</span></span> | <span data-ttu-id="2d2b1-115">Юбилейное обновление Windows 10 (версия 1607, сборка 14393)</span><span class="sxs-lookup"><span data-stu-id="2d2b1-115">Windows 10 Anniversary Update (version 1607, build 14393)</span></span> |
| <span data-ttu-id="2d2b1-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2d2b1-116">Minimum supported server</span></span> | <span data-ttu-id="2d2b1-117">Windows Server 2016 (сборка 14393)</span><span class="sxs-lookup"><span data-stu-id="2d2b1-117">Windows Server 2016 (build 14393)</span></span> |

## <a name="see-also"></a><span data-ttu-id="2d2b1-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2d2b1-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d2b1-119">**system_handle**</span><span class="sxs-lookup"><span data-stu-id="2d2b1-119">**system_handle**</span></span>](system-handle.md)
</dt> <dt>

[<span data-ttu-id="2d2b1-120">Объекты семафора</span><span class="sxs-lookup"><span data-stu-id="2d2b1-120">Semaphore Objects</span></span>](../sync/semaphore-objects.md)
</dt> <dt>

[<span data-ttu-id="2d2b1-121">Безопасность объекта синхронизации и права доступа</span><span class="sxs-lookup"><span data-stu-id="2d2b1-121">Synchronization Object Security and Access Rights</span></span>](../sync/synchronization-object-security-and-access-rights.md)
</dt> <dt>

[<span data-ttu-id="2d2b1-122">Функция **createsemaphore-**</span><span class="sxs-lookup"><span data-stu-id="2d2b1-122">**CreateSemaphore** function</span></span>](/windows/win32/api/winbase/nf-winbase-createsemaphorea)
</dt> <dt>

[<span data-ttu-id="2d2b1-123">Функция **креатесемафорикс**</span><span class="sxs-lookup"><span data-stu-id="2d2b1-123">**CreateSemaphoreEx** function</span></span>](/windows/win32/api/winbase/nf-winbase-createsemaphoreexa)
</dt> </dl>
