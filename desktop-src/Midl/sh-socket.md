---
title: Ключевое слово sh_socket
description: '\_Ключевое слово \ SH Socket \ указывает, что системный объект является маркером для сокета.'
keywords:
- sh_socket ключевого слова MIDL
topic_type:
- apiref
api_name:
- sh_socket keyword
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 5f5d2506f66f89cd47ecf3f011c8071b79e64177
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/06/2021
ms.locfileid: "105719884"
---
# <a name="sh_socket-keyword"></a><span data-ttu-id="ffe91-104">\_ключевое слово сокета SH</span><span class="sxs-lookup"><span data-stu-id="ffe91-104">sh\_socket keyword</span></span>

<span data-ttu-id="ffe91-105">Ключевое слово **\_ сокета SH** указывает, что `system_handle` содержит маркер для сокета.</span><span class="sxs-lookup"><span data-stu-id="ffe91-105">The **sh\_socket** keyword specifies that a `system_handle` holds a handle to a socket.</span></span>

``` syntax
[system_handle(sh_socket)]

[system_handle(sh_socket, access-rights)]
```

## <a name="parameters"></a><span data-ttu-id="ffe91-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ffe91-106">Parameters</span></span>

<span data-ttu-id="ffe91-107">Это ключевое слово является параметром для [**system_handle**](system-handle.md).</span><span class="sxs-lookup"><span data-stu-id="ffe91-107">This keyword is a parameter for [**system_handle**](system-handle.md).</span></span>

<span data-ttu-id="ffe91-108">В документации по [**system_handle**](system-handle.md) также содержатся сведения о необязательном использовании параметра *Access-Rights* .</span><span class="sxs-lookup"><span data-stu-id="ffe91-108">The [**system_handle**](system-handle.md) documentation also contains details on optional use of the *access-rights* parameter.</span></span> <span data-ttu-id="ffe91-109">Поведение по умолчанию `DUPLICATE_SAME_ACCESS` для каждой спецификации [ **функции дупликатехандле**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .</span><span class="sxs-lookup"><span data-stu-id="ffe91-109">The default behavior is `DUPLICATE_SAME_ACCESS` per [**DuplicateHandle** function](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) specifications.</span></span>

## <a name="remarks"></a><span data-ttu-id="ffe91-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ffe91-110">Remarks</span></span>

<span data-ttu-id="ffe91-111">Чтобы использовать это ключевое слово с `system_handle` атрибутом, `-target` необходимо установить для флага значение `NT100` (или более высокий) при выполнении midl.exe.</span><span class="sxs-lookup"><span data-stu-id="ffe91-111">In order to use this keyword with the `system_handle` attribute, the `-target` flag must be set to `NT100` (or higher) when running midl.exe.</span></span>

## <a name="examples"></a><span data-ttu-id="ffe91-112">Примеры</span><span class="sxs-lookup"><span data-stu-id="ffe91-112">Examples</span></span>

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT ListenToSocket([in, system_handle(sh_socket)] HANDLE socket);
}
```

## <a name="requirements"></a><span data-ttu-id="ffe91-113">Требования</span><span class="sxs-lookup"><span data-stu-id="ffe91-113">Requirements</span></span>

| &nbsp; | &nbsp; |
|-|-|
| <span data-ttu-id="ffe91-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ffe91-114">Minimum supported client</span></span> | <span data-ttu-id="ffe91-115">Юбилейное обновление Windows 10 (версия 1607, сборка 14393)</span><span class="sxs-lookup"><span data-stu-id="ffe91-115">Windows 10 Anniversary Update (version 1607, build 14393)</span></span> |
| <span data-ttu-id="ffe91-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ffe91-116">Minimum supported server</span></span> | <span data-ttu-id="ffe91-117">Windows Server 2016 (сборка 14393)</span><span class="sxs-lookup"><span data-stu-id="ffe91-117">Windows Server 2016 (build 14393)</span></span> |

## <a name="see-also"></a><span data-ttu-id="ffe91-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ffe91-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffe91-119">**system_handle**</span><span class="sxs-lookup"><span data-stu-id="ffe91-119">**system_handle**</span></span>](system-handle.md)
</dt> <dt>

[<span data-ttu-id="ffe91-120">Сокеты Windows 2</span><span class="sxs-lookup"><span data-stu-id="ffe91-120">Windows Sockets 2</span></span>](../winsock/windows-sockets-start-page-2.md)
</dt> </dl>
