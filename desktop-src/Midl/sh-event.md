---
title: Ключевое слово sh_event
description: '\_Ключевое слово \ SH Event \ указывает, что системный объект является обработчиком события.'
keywords:
- sh_event ключевого слова MIDL
topic_type:
- apiref
api_name:
- sh_event
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 1a9b6dc7cc9dc4de4abd5dcc88a53588167db59d
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/06/2021
ms.locfileid: "105719881"
---
# <a name="sh_event-keyword"></a><span data-ttu-id="3d7b0-104">\_ключевое слово события SH</span><span class="sxs-lookup"><span data-stu-id="3d7b0-104">sh\_event keyword</span></span>

<span data-ttu-id="3d7b0-105">Ключевое слово **\_ события SH** указывает, что `system_handle` содержит обработчик для события.</span><span class="sxs-lookup"><span data-stu-id="3d7b0-105">The **sh\_event** keyword specifies that a `system_handle` holds a handle to an event.</span></span>

``` syntax
[system_handle(sh_event)]

[system_handle(sh_event, access-rights)]
```

## <a name="parameters"></a><span data-ttu-id="3d7b0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3d7b0-106">Parameters</span></span>

<span data-ttu-id="3d7b0-107">Это ключевое слово является параметром для [**system_handle**](system-handle.md).</span><span class="sxs-lookup"><span data-stu-id="3d7b0-107">This keyword is a parameter for [**system_handle**](system-handle.md).</span></span>

<span data-ttu-id="3d7b0-108">В документации по [**system_handle**](system-handle.md) также содержатся сведения о необязательном использовании параметра *Access-Rights* .</span><span class="sxs-lookup"><span data-stu-id="3d7b0-108">The [**system_handle**](system-handle.md) documentation also contains details on optional use of the *access-rights* parameter.</span></span> <span data-ttu-id="3d7b0-109">Поведение по умолчанию `DUPLICATE_SAME_ACCESS` для каждой спецификации [ **функции дупликатехандле**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .</span><span class="sxs-lookup"><span data-stu-id="3d7b0-109">The default behavior is `DUPLICATE_SAME_ACCESS` per [**DuplicateHandle** function](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) specifications.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d7b0-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3d7b0-110">Remarks</span></span>

<span data-ttu-id="3d7b0-111">Чтобы использовать это ключевое слово с `system_handle` атрибутом, `-target` необходимо установить для флага значение `NT100` (или более высокий) при выполнении midl.exe.</span><span class="sxs-lookup"><span data-stu-id="3d7b0-111">In order to use this keyword with the `system_handle` attribute, the `-target` flag must be set to `NT100` (or higher) when running midl.exe.</span></span>

## <a name="examples"></a><span data-ttu-id="3d7b0-112">Примеры</span><span class="sxs-lookup"><span data-stu-id="3d7b0-112">Examples</span></span>

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT NotifyThisEvent([in, system_handle(sh_event)] HANDLE listeningToThisEvent);
}
```

## <a name="requirements"></a><span data-ttu-id="3d7b0-113">Требования</span><span class="sxs-lookup"><span data-stu-id="3d7b0-113">Requirements</span></span>

| &nbsp; | &nbsp; |
|-|-|
| <span data-ttu-id="3d7b0-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3d7b0-114">Minimum supported client</span></span> | <span data-ttu-id="3d7b0-115">Юбилейное обновление Windows 10 (версия 1607, сборка 14393)</span><span class="sxs-lookup"><span data-stu-id="3d7b0-115">Windows 10 Anniversary Update (version 1607, build 14393)</span></span> |
| <span data-ttu-id="3d7b0-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3d7b0-116">Minimum supported server</span></span> | <span data-ttu-id="3d7b0-117">Windows Server 2016 (сборка 14393)</span><span class="sxs-lookup"><span data-stu-id="3d7b0-117">Windows Server 2016 (build 14393)</span></span> |

## <a name="see-also"></a><span data-ttu-id="3d7b0-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3d7b0-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d7b0-119">**system_handle**</span><span class="sxs-lookup"><span data-stu-id="3d7b0-119">**system_handle**</span></span>](system-handle.md)
</dt> <dt>

[<span data-ttu-id="3d7b0-120">Объекты событий</span><span class="sxs-lookup"><span data-stu-id="3d7b0-120">Event Objects</span></span>](../sync/event-objects.md)
</dt> <dt>

[<span data-ttu-id="3d7b0-121">Безопасность объекта синхронизации и права доступа</span><span class="sxs-lookup"><span data-stu-id="3d7b0-121">Synchronization Object Security and Access Rights</span></span>](../sync/synchronization-object-security-and-access-rights.md)
</dt> <dt>

[<span data-ttu-id="3d7b0-122">Функция **CreateEvent**</span><span class="sxs-lookup"><span data-stu-id="3d7b0-122">**CreateEvent** function</span></span>](/windows/win32/api/synchapi/nf-synchapi-createeventa)
</dt> <dt>

[<span data-ttu-id="3d7b0-123">Функция **креативентекс**</span><span class="sxs-lookup"><span data-stu-id="3d7b0-123">**CreateEventEx** function</span></span>](/windows/win32/api/synchapi/nf-synchapi-createeventexa)
</dt> </dl>
