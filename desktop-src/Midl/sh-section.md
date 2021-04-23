---
title: Ключевое слово sh_section
description: '\_Ключевое слово \ SH Section \ указывает, что системный объект является маркером раздела.'
keywords:
- sh_section ключевого слова MIDL
topic_type:
- apiref
api_name:
- sh_section keyword
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 056112deb790e727206a5ac1a1a2a5043a68f5e1
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/06/2021
ms.locfileid: "105719885"
---
# <a name="sh_section-keyword"></a><span data-ttu-id="a0434-104">\_зарезервированное слово раздела SH</span><span class="sxs-lookup"><span data-stu-id="a0434-104">sh\_section keyword</span></span>

<span data-ttu-id="a0434-105">Ключевое слово **sh \_ section** указывает, что `system_handle` содержит маркер раздела.</span><span class="sxs-lookup"><span data-stu-id="a0434-105">The **sh\_section** keyword specifies that a `system_handle` holds a handle to a section.</span></span>

``` syntax
[system_handle(sh_section)]

[system_handle(sh_section, access-rights)]
```

## <a name="parameters"></a><span data-ttu-id="a0434-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a0434-106">Parameters</span></span>

<span data-ttu-id="a0434-107">Это ключевое слово является параметром для [**system_handle**](system-handle.md).</span><span class="sxs-lookup"><span data-stu-id="a0434-107">This keyword is a parameter for [**system_handle**](system-handle.md).</span></span>

<span data-ttu-id="a0434-108">В документации по [**system_handle**](system-handle.md) также содержатся сведения о необязательном использовании параметра *Access-Rights* .</span><span class="sxs-lookup"><span data-stu-id="a0434-108">The [**system_handle**](system-handle.md) documentation also contains details on optional use of the *access-rights* parameter.</span></span> <span data-ttu-id="a0434-109">Поведение по умолчанию `DUPLICATE_SAME_ACCESS` для каждой спецификации [ **функции дупликатехандле**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .</span><span class="sxs-lookup"><span data-stu-id="a0434-109">The default behavior is `DUPLICATE_SAME_ACCESS` per [**DuplicateHandle** function](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) specifications.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0434-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a0434-110">Remarks</span></span>

<span data-ttu-id="a0434-111">Чтобы использовать это ключевое слово с `system_handle` атрибутом, `-target` необходимо установить для флага значение `NT100` (или более высокий) при выполнении midl.exe.</span><span class="sxs-lookup"><span data-stu-id="a0434-111">In order to use this keyword with the `system_handle` attribute, the `-target` flag must be set to `NT100` (or higher) when running midl.exe.</span></span>

## <a name="examples"></a><span data-ttu-id="a0434-112">Примеры</span><span class="sxs-lookup"><span data-stu-id="a0434-112">Examples</span></span>

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT GiveSection([in, system_handle(sh_section)] HANDLE section);

    HRESULT GetSectionToWatch([out, system_handle(sh_section, SECTION_MAP_READ)] HANDLE* pSection);
}
```

## <a name="requirements"></a><span data-ttu-id="a0434-113">Требования</span><span class="sxs-lookup"><span data-stu-id="a0434-113">Requirements</span></span>

| &nbsp; | &nbsp; |
|-|-|
| <span data-ttu-id="a0434-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a0434-114">Minimum supported client</span></span> | <span data-ttu-id="a0434-115">Юбилейное обновление Windows 10 (версия 1607, сборка 14393)</span><span class="sxs-lookup"><span data-stu-id="a0434-115">Windows 10 Anniversary Update (version 1607, build 14393)</span></span> |
| <span data-ttu-id="a0434-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a0434-116">Minimum supported server</span></span> | <span data-ttu-id="a0434-117">Windows Server 2016 (сборка 14393)</span><span class="sxs-lookup"><span data-stu-id="a0434-117">Windows Server 2016 (build 14393)</span></span> |

## <a name="see-also"></a><span data-ttu-id="a0434-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a0434-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0434-119">**system_handle**</span><span class="sxs-lookup"><span data-stu-id="a0434-119">**system_handle**</span></span>](system-handle.md)
</dt> <dt>

[<span data-ttu-id="a0434-120">Объекты и представления раздела</span><span class="sxs-lookup"><span data-stu-id="a0434-120">Section Objects and Views</span></span>](/windows-hardware/drivers/kernel/section-objects-and-views)
</dt> <dt>

[<span data-ttu-id="a0434-121">Функция **звкреатесектион** (включая спецификации доступа)</span><span class="sxs-lookup"><span data-stu-id="a0434-121">**ZwCreateSection** function (including access specifications)</span></span>](/windows-hardware/drivers/ddi/wdm/nf-wdm-zwcreatesection)
</dt> </dl>
