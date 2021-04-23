---
description: Событие изменения каталога Winsock для операции удаления поставщика многоуровневой службы (LSP).
ms.assetid: 86FF17F7-8CCF-4A03-899F-42BFACDF3F54
title: WINSOCK_WS2HELP_LSP_REMOVE событие
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WINSOCK_WS2HELP_LSP_REMOVE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 597cd2f8cfc3bb7727301e64af53671bafbd9469
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693382"
---
# <a name="winsock_ws2help_lsp_remove-event"></a><span data-ttu-id="8c5a8-103">\_ \_ Событие удаления LSP Winsock WS2HELP \_</span><span class="sxs-lookup"><span data-stu-id="8c5a8-103">WINSOCK\_WS2HELP\_LSP\_REMOVE event</span></span>

> [!Note]  
> <span data-ttu-id="8c5a8-104">Многоуровневые поставщики служб являются устаревшими.</span><span class="sxs-lookup"><span data-stu-id="8c5a8-104">Layered Service Providers are deprecated.</span></span> <span data-ttu-id="8c5a8-105">Начиная с Windows 8 и Windows Server 2012, используйте [платформу фильтрации Windows](../fwp/windows-filtering-platform-start-page.md).</span><span class="sxs-lookup"><span data-stu-id="8c5a8-105">Starting with Windows 8 and Windows Server 2012, use [Windows Filtering Platform](../fwp/windows-filtering-platform-start-page.md).</span></span>

 

<span data-ttu-id="8c5a8-106">Событие **\_ \_ \_ удаления LSP Winsock WS2HELP** является событием изменения каталога Winsock для операции удаления поставщика многоуровневой службы (LSP).</span><span class="sxs-lookup"><span data-stu-id="8c5a8-106">The **WINSOCK\_WS2HELP\_LSP\_REMOVE** event is a Winsock catalog change event for a layered service provider (LSP) removal operation.</span></span>


```C++
const EVENT_DESCRIPTOR WINSOCK_WS2HELP_LSP_REMOVE = {0x2, 0x0, 0x10, 0x0, 0x0, 0x0, 0x8000000000000000};
```



## <a name="parameters"></a><span data-ttu-id="8c5a8-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="8c5a8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c5a8-108">*Имя LSP*</span><span class="sxs-lookup"><span data-stu-id="8c5a8-108">*LSP Name*</span></span> 
</dt> <dd>

<span data-ttu-id="8c5a8-109">Имя LSP, полученное из элемента **сзпротокол** структуры [**\_ сведений о ВСАПРОТОКОЛ**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) для удаляемого LSP.</span><span class="sxs-lookup"><span data-stu-id="8c5a8-109">The name of the LSP as obtained from the **szProtocol** member of the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the LSP being removed.</span></span>

</dd> <dt>

<span data-ttu-id="8c5a8-110">*Каталог*</span><span class="sxs-lookup"><span data-stu-id="8c5a8-110">*Catalog*</span></span> 
</dt> <dd>

<span data-ttu-id="8c5a8-111">Каталог Winsock (32-разрядный или 64-бит), в который удаляется LSP.</span><span class="sxs-lookup"><span data-stu-id="8c5a8-111">The Winsock catalog (32-bit or 64-bit) where the LSP is being removed.</span></span> <span data-ttu-id="8c5a8-112">Это целочисленное значение, равное 32 или 64.</span><span class="sxs-lookup"><span data-stu-id="8c5a8-112">This is an integer value that is either 32 or 64.</span></span>

</dd> <dt>

<span data-ttu-id="8c5a8-113">*Установщик*</span><span class="sxs-lookup"><span data-stu-id="8c5a8-113">*Installer*</span></span> 
</dt> <dd>

<span data-ttu-id="8c5a8-114">Имя файла модуля приложения, вызывающего удаление LSP.</span><span class="sxs-lookup"><span data-stu-id="8c5a8-114">The module filename of the application making the LSP remove call.</span></span>

</dd> <dt>

<span data-ttu-id="8c5a8-115">*GUID*</span><span class="sxs-lookup"><span data-stu-id="8c5a8-115">*GUID*</span></span> 
</dt> <dd>

<span data-ttu-id="8c5a8-116">Значение идентификатора GUID поставщика транспорта Winsock, из которого удаляется LSP.</span><span class="sxs-lookup"><span data-stu-id="8c5a8-116">The GUID value of the Winsock transport provider that the LSP is being removed from.</span></span>

</dd> <dt>

<span data-ttu-id="8c5a8-117">*Категория*</span><span class="sxs-lookup"><span data-stu-id="8c5a8-117">*Category*</span></span> 
</dt> <dd>

<span data-ttu-id="8c5a8-118">Элемент **двкаталожентрид** структуры сведений о [**всапротокол \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) для удаляемого LSP.</span><span class="sxs-lookup"><span data-stu-id="8c5a8-118">The **dwCatalogEntryId** member of the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the LSP being removed.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8c5a8-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8c5a8-119">Remarks</span></span>

<span data-ttu-id="8c5a8-120">Событие **\_ \_ \_ удаления LSP Winsock WS2HELP** будет отслеживаться для операции удаления LSP при удалении записи протокола из каталога Winsock.</span><span class="sxs-lookup"><span data-stu-id="8c5a8-120">The **WINSOCK\_WS2HELP\_LSP\_REMOVE** event is traced for an LSP removal operation when a protocol entry is removed from the Winsock catalog.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c5a8-121">Требования</span><span class="sxs-lookup"><span data-stu-id="8c5a8-121">Requirements</span></span>



| <span data-ttu-id="8c5a8-122">Требование</span><span class="sxs-lookup"><span data-stu-id="8c5a8-122">Requirement</span></span> | <span data-ttu-id="8c5a8-123">Значение</span><span class="sxs-lookup"><span data-stu-id="8c5a8-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8c5a8-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8c5a8-124">Minimum supported client</span></span><br/> | <span data-ttu-id="8c5a8-125">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8c5a8-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8c5a8-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8c5a8-126">Minimum supported server</span></span><br/> | <span data-ttu-id="8c5a8-127">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8c5a8-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8c5a8-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8c5a8-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c5a8-129">Управление трассировкой Winsock</span><span class="sxs-lookup"><span data-stu-id="8c5a8-129">Control of Winsock Tracing</span></span>](control-of-winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="8c5a8-130">Трассировка Winsock</span><span class="sxs-lookup"><span data-stu-id="8c5a8-130">Winsock Tracing</span></span>](winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="8c5a8-131">Уровни трассировки Winsock</span><span class="sxs-lookup"><span data-stu-id="8c5a8-131">Winsock Tracing Levels</span></span>](winsock-tracing-levels.md)
</dt> <dt>

[<span data-ttu-id="8c5a8-132">Сведения о трассировке изменений каталога Winsock</span><span class="sxs-lookup"><span data-stu-id="8c5a8-132">Winsock Catalog Change Tracing Details</span></span>](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 

 
