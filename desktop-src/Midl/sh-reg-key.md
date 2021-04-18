---
title: Ключевое слово sh_reg_key
description: '\_ \_ Ключевое слово \ SH reg Key \ указывает, что системный объект является маркером раздела реестра.'
keywords:
- sh_reg_key ключевого слова MIDL
topic_type:
- apiref
api_name:
- sh_reg_key keyword
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: cec526bed766534f82d5a1bc24c55050dea814ed
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/06/2021
ms.locfileid: "105719886"
---
# <a name="sh_reg_key-keyword"></a><span data-ttu-id="7c5f8-104">\_ \_ ключевое слово реестра SH reg</span><span class="sxs-lookup"><span data-stu-id="7c5f8-104">sh\_reg\_key keyword</span></span>

<span data-ttu-id="7c5f8-105">Ключевое слово **sh \_ reg \_ Key** указывает, что `system_handle` содержит маркер раздела реестра.</span><span class="sxs-lookup"><span data-stu-id="7c5f8-105">The **sh\_reg\_key** keyword specifies that a `system_handle` holds a handle to a registry key.</span></span>

``` syntax
[system_handle(sh_reg_key)]

[system_handle(sh_reg_key, access-rights)]
```

## <a name="parameters"></a><span data-ttu-id="7c5f8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7c5f8-106">Parameters</span></span>

<span data-ttu-id="7c5f8-107">Это ключевое слово является параметром для [**system_handle**](system-handle.md).</span><span class="sxs-lookup"><span data-stu-id="7c5f8-107">This keyword is a parameter for [**system_handle**](system-handle.md).</span></span>

<span data-ttu-id="7c5f8-108">В документации по [**system_handle**](system-handle.md) также содержатся сведения о необязательном использовании параметра *Access-Rights* .</span><span class="sxs-lookup"><span data-stu-id="7c5f8-108">The [**system_handle**](system-handle.md) documentation also contains details on optional use of the *access-rights* parameter.</span></span> <span data-ttu-id="7c5f8-109">Поведение по умолчанию `DUPLICATE_SAME_ACCESS` для каждой спецификации [ **функции дупликатехандле**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .</span><span class="sxs-lookup"><span data-stu-id="7c5f8-109">The default behavior is `DUPLICATE_SAME_ACCESS` per [**DuplicateHandle** function](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) specifications.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c5f8-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7c5f8-110">Remarks</span></span>

<span data-ttu-id="7c5f8-111">Чтобы использовать это ключевое слово с `system_handle` атрибутом, `-target` необходимо установить для флага значение `NT100` (или более высокий) при выполнении midl.exe.</span><span class="sxs-lookup"><span data-stu-id="7c5f8-111">In order to use this keyword with the `system_handle` attribute, the `-target` flag must be set to `NT100` (or higher) when running midl.exe.</span></span>

## <a name="examples"></a><span data-ttu-id="7c5f8-112">Примеры</span><span class="sxs-lookup"><span data-stu-id="7c5f8-112">Examples</span></span>

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT GetConfigurationKey([out, system_handle(sh_reg_key)] HANDLE* key);

    HRESULT SetKeyForWatch([in, system_handle(sh_reg_key, KEY_READ)] HANDLE watchKey);
}
```

## <a name="requirements"></a><span data-ttu-id="7c5f8-113">Требования</span><span class="sxs-lookup"><span data-stu-id="7c5f8-113">Requirements</span></span>

| &nbsp; | &nbsp; |
|-|-|
| <span data-ttu-id="7c5f8-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7c5f8-114">Minimum supported client</span></span> | <span data-ttu-id="7c5f8-115">Юбилейное обновление Windows 10 (версия 1607, сборка 14393)</span><span class="sxs-lookup"><span data-stu-id="7c5f8-115">Windows 10 Anniversary Update (version 1607, build 14393)</span></span> |
| <span data-ttu-id="7c5f8-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7c5f8-116">Minimum supported server</span></span> | <span data-ttu-id="7c5f8-117">Windows Server 2016 (сборка 14393)</span><span class="sxs-lookup"><span data-stu-id="7c5f8-117">Windows Server 2016 (build 14393)</span></span> |

## <a name="see-also"></a><span data-ttu-id="7c5f8-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7c5f8-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c5f8-119">**system_handle**</span><span class="sxs-lookup"><span data-stu-id="7c5f8-119">**system_handle**</span></span>](system-handle.md)
</dt> <dt>

[<span data-ttu-id="7c5f8-120">Реестр</span><span class="sxs-lookup"><span data-stu-id="7c5f8-120">Registry</span></span>](../sysinfo/registry.md)
</dt> <dt>

[<span data-ttu-id="7c5f8-121">Безопасность раздела реестра и права доступа</span><span class="sxs-lookup"><span data-stu-id="7c5f8-121">Registry Key Security and Access Rights</span></span>](../sysinfo/registry-key-security-and-access-rights.md)
</dt> <dt>

[<span data-ttu-id="7c5f8-122">Функция **RegOpenKeyEx**</span><span class="sxs-lookup"><span data-stu-id="7c5f8-122">**RegOpenKeyEx** function</span></span>](/windows/win32/api/winreg/nf-winreg-regopenkeyexa)
</dt> <dt>
