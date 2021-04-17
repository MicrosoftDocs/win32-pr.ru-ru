---
description: Событие изменения каталога Winsock для операции сброса каталога Winsock.
ms.assetid: BE8DC0DB-0F96-4015-87F5-ECF25AE164AA
title: WINSOCK_WS2HELP_LSP_RESET событие
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WINSOCK_WS2HELP_LSP_RESET
api_type:
- NA
api_location: ''
ms.openlocfilehash: 219eb85dec0cdda77ca8741ae42df1f63d1a7dbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693381"
---
# <a name="winsock_ws2help_lsp_reset-event"></a><span data-ttu-id="2c451-103">\_ \_ Событие сброса LSP Winsock WS2HELP \_</span><span class="sxs-lookup"><span data-stu-id="2c451-103">WINSOCK\_WS2HELP\_LSP\_RESET event</span></span>

> [!Note]  
> <span data-ttu-id="2c451-104">Многоуровневые поставщики служб являются устаревшими.</span><span class="sxs-lookup"><span data-stu-id="2c451-104">Layered Service Providers are deprecated.</span></span> <span data-ttu-id="2c451-105">Начиная с Windows 8 и Windows Server 2012, используйте [платформу фильтрации Windows](../fwp/windows-filtering-platform-start-page.md).</span><span class="sxs-lookup"><span data-stu-id="2c451-105">Starting with Windows 8 and Windows Server 2012, use [Windows Filtering Platform](../fwp/windows-filtering-platform-start-page.md).</span></span>

 

<span data-ttu-id="2c451-106">Событием **\_ \_ \_ сброса LSP Winsock WS2HELP** является событием изменения каталога Winsock для операции сброса каталога Winsock.</span><span class="sxs-lookup"><span data-stu-id="2c451-106">The **WINSOCK\_WS2HELP\_LSP\_RESET** event is a Winsock catalog change event for a Winsock catalog reset operation.</span></span>


```C++
const EVENT_DESCRIPTOR WINSOCK_WS2HELP_LSP_RESET = {0x4, 0x0, 0x10, 0x0, 0x0, 0x0, 0x8000000000000000};
```



## <a name="parameters"></a><span data-ttu-id="2c451-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="2c451-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c451-108">*Каталог*</span><span class="sxs-lookup"><span data-stu-id="2c451-108">*Catalog*</span></span> 
</dt> <dd>

<span data-ttu-id="2c451-109">Каталог Winsock (32-разрядный или 64-разрядный), который сбрасывается.</span><span class="sxs-lookup"><span data-stu-id="2c451-109">The Winsock catalog (32-bit or 64-bit) that is being reset.</span></span> <span data-ttu-id="2c451-110">Это целочисленное значение, равное 32 или 64.</span><span class="sxs-lookup"><span data-stu-id="2c451-110">This is an integer value that is either 32 or 64.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2c451-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2c451-111">Remarks</span></span>

<span data-ttu-id="2c451-112">Событие **" \_ \_ \_ Сброс LSP" для Winsock WS2HELP** отслеживается для операции поставщика многоуровневых служб Winsock (LSP) при сбросе каталога Winsock.</span><span class="sxs-lookup"><span data-stu-id="2c451-112">The **WINSOCK\_WS2HELP\_LSP\_RESET** event is traced for an Winsock Layered Service Provider (LSP) operation when the Winsock catalog is reset.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c451-113">Требования</span><span class="sxs-lookup"><span data-stu-id="2c451-113">Requirements</span></span>



| <span data-ttu-id="2c451-114">Требование</span><span class="sxs-lookup"><span data-stu-id="2c451-114">Requirement</span></span> | <span data-ttu-id="2c451-115">Значение</span><span class="sxs-lookup"><span data-stu-id="2c451-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2c451-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2c451-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2c451-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2c451-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2c451-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2c451-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2c451-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2c451-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2c451-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2c451-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c451-121">Управление трассировкой Winsock</span><span class="sxs-lookup"><span data-stu-id="2c451-121">Control of Winsock Tracing</span></span>](control-of-winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="2c451-122">Трассировка Winsock</span><span class="sxs-lookup"><span data-stu-id="2c451-122">Winsock Tracing</span></span>](winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="2c451-123">Уровни трассировки Winsock</span><span class="sxs-lookup"><span data-stu-id="2c451-123">Winsock Tracing Levels</span></span>](winsock-tracing-levels.md)
</dt> <dt>

[<span data-ttu-id="2c451-124">Сведения о трассировке изменений каталога Winsock</span><span class="sxs-lookup"><span data-stu-id="2c451-124">Winsock Catalog Change Tracing Details</span></span>](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 

 
