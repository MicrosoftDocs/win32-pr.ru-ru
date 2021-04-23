---
title: Ключевое слово sh_token
description: '\_Ключевое слово \ SH Token \ указывает, что системный объект является маркером маркера.'
keywords:
- sh_token ключевого слова MIDL
topic_type:
- apiref
api_name:
- sh_token keyword
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: a33b070af5cd43a095fd6ad45a0dee86f1868171
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/06/2021
ms.locfileid: "105719883"
---
# <a name="sh_token-keyword"></a><span data-ttu-id="06c5e-104">\_ключевое слово токена SH</span><span class="sxs-lookup"><span data-stu-id="06c5e-104">sh\_token keyword</span></span>

<span data-ttu-id="06c5e-105">Ключевое слово **\_ токена SH** указывает, что `system_handle` содержит маркер маркера.</span><span class="sxs-lookup"><span data-stu-id="06c5e-105">The **sh\_token** keyword specifies that a `system_handle` holds a handle to a token.</span></span>

``` syntax
[system_handle(sh_token)]

[system_handle(sh_token, access-rights)]
```

## <a name="parameters"></a><span data-ttu-id="06c5e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="06c5e-106">Parameters</span></span>

<span data-ttu-id="06c5e-107">Это ключевое слово является параметром для [**system_handle**](system-handle.md).</span><span class="sxs-lookup"><span data-stu-id="06c5e-107">This keyword is a parameter for [**system_handle**](system-handle.md).</span></span>

<span data-ttu-id="06c5e-108">В документации по [**system_handle**](system-handle.md) также содержатся сведения о необязательном использовании параметра *Access-Rights* .</span><span class="sxs-lookup"><span data-stu-id="06c5e-108">The [**system_handle**](system-handle.md) documentation also contains details on optional use of the *access-rights* parameter.</span></span> <span data-ttu-id="06c5e-109">Поведение по умолчанию `DUPLICATE_SAME_ACCESS` для каждой спецификации [ **функции дупликатехандле**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .</span><span class="sxs-lookup"><span data-stu-id="06c5e-109">The default behavior is `DUPLICATE_SAME_ACCESS` per [**DuplicateHandle** function](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) specifications.</span></span>

## <a name="remarks"></a><span data-ttu-id="06c5e-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="06c5e-110">Remarks</span></span>

<span data-ttu-id="06c5e-111">Чтобы использовать это ключевое слово с `system_handle` атрибутом, `-target` необходимо установить для флага значение `NT100` (или более высокий) при выполнении midl.exe.</span><span class="sxs-lookup"><span data-stu-id="06c5e-111">In order to use this keyword with the `system_handle` attribute, the `-target` flag must be set to `NT100` (or higher) when running midl.exe.</span></span>

## <a name="examples"></a><span data-ttu-id="06c5e-112">Примеры</span><span class="sxs-lookup"><span data-stu-id="06c5e-112">Examples</span></span>

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT SetToken([in, system_handle(sh_token)] HANDLE token);

    HRESULT GetToken([out, system_handle(sh_token, TOKEN_QUERY)] HANDLE* pToken);
}
```

## <a name="requirements"></a><span data-ttu-id="06c5e-113">Требования</span><span class="sxs-lookup"><span data-stu-id="06c5e-113">Requirements</span></span>

| &nbsp; | &nbsp; |
|-|-|
| <span data-ttu-id="06c5e-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="06c5e-114">Minimum supported client</span></span> | <span data-ttu-id="06c5e-115">Юбилейное обновление Windows 10 (версия 1607, сборка 14393)</span><span class="sxs-lookup"><span data-stu-id="06c5e-115">Windows 10 Anniversary Update (version 1607, build 14393)</span></span> |
| <span data-ttu-id="06c5e-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="06c5e-116">Minimum supported server</span></span> | <span data-ttu-id="06c5e-117">Windows Server 2016 (сборка 14393)</span><span class="sxs-lookup"><span data-stu-id="06c5e-117">Windows Server 2016 (build 14393)</span></span> |

## <a name="see-also"></a><span data-ttu-id="06c5e-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="06c5e-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06c5e-119">**system_handle**</span><span class="sxs-lookup"><span data-stu-id="06c5e-119">**system_handle**</span></span>](system-handle.md)
</dt> <dt>

[<span data-ttu-id="06c5e-120">Маркеры доступа</span><span class="sxs-lookup"><span data-stu-id="06c5e-120">Access Tokens</span></span>](../secauthz/access-tokens.md)
</dt> <dt>

[<span data-ttu-id="06c5e-121">Права доступа для объектов Access-Token</span><span class="sxs-lookup"><span data-stu-id="06c5e-121">Access Rights for Access-Token Objects</span></span>](../secauthz/access-rights-for-access-token-objects.md)
</dt> </dl>
