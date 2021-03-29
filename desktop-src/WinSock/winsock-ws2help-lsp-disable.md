---
description: Событие изменения каталога Winsock для операции отключения поставщика многоуровневой службы (LSP).
ms.assetid: 6BCEECB1-92AD-47D8-952B-D0FD2A78EB45
title: WINSOCK_WS2HELP_LSP_DISABLE событие
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WINSOCK_WS2HELP_LSP_DISABLE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 6d785bfbd96d35717be7bbf76dab8f28f41c9fc6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647529"
---
# <a name="winsock_ws2help_lsp_disable-event"></a><span data-ttu-id="38c4b-103">\_ \_ Событие отключения LSP Winsock WS2HELP \_</span><span class="sxs-lookup"><span data-stu-id="38c4b-103">WINSOCK\_WS2HELP\_LSP\_DISABLE event</span></span>

> [!Note]  
> <span data-ttu-id="38c4b-104">Многоуровневые поставщики служб являются устаревшими.</span><span class="sxs-lookup"><span data-stu-id="38c4b-104">Layered Service Providers are deprecated.</span></span> <span data-ttu-id="38c4b-105">Начиная с Windows 8 и Windows Server 2012, используйте [платформу фильтрации Windows](../fwp/windows-filtering-platform-start-page.md).</span><span class="sxs-lookup"><span data-stu-id="38c4b-105">Starting with Windows 8 and Windows Server 2012, use [Windows Filtering Platform](../fwp/windows-filtering-platform-start-page.md).</span></span>

 

<span data-ttu-id="38c4b-106">Событие **Winsock \_ WS2HELP \_ LSP \_ Disable** — это событие изменения каталога Winsock для операции отключения поставщика многоуровневой службы (LSP).</span><span class="sxs-lookup"><span data-stu-id="38c4b-106">The **WINSOCK\_WS2HELP\_LSP\_DISABLE** event is a Winsock catalog change event for a layered service provider (LSP) disable operation.</span></span>


```C++
const EVENT_DESCRIPTOR WINSOCK_WS2HELP_LSP_DISABLE = {0x3, 0x0, 0x10, 0x0, 0x0, 0x0, 0x8000000000000000};
```



## <a name="parameters"></a><span data-ttu-id="38c4b-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="38c4b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38c4b-108">*Имя LSP*</span><span class="sxs-lookup"><span data-stu-id="38c4b-108">*LSP Name*</span></span> 
</dt> <dd>

<span data-ttu-id="38c4b-109">Имя LSP, полученное из элемента **сзпротокол** структуры [**\_ сведений о всапротокол**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) для неактивного LSP.</span><span class="sxs-lookup"><span data-stu-id="38c4b-109">The name of the LSP as obtained from the **szProtocol** member of the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the LSP being disabled.</span></span>

</dd> <dt>

<span data-ttu-id="38c4b-110">*Каталог*</span><span class="sxs-lookup"><span data-stu-id="38c4b-110">*Catalog*</span></span> 
</dt> <dd>

<span data-ttu-id="38c4b-111">Каталог Winsock (32-разрядный или 64-бит), в котором отключается LSP.</span><span class="sxs-lookup"><span data-stu-id="38c4b-111">The Winsock catalog (32-bit or 64-bit) where the LSP is being disabled.</span></span> <span data-ttu-id="38c4b-112">Это целочисленное значение, равное 32 или 64.</span><span class="sxs-lookup"><span data-stu-id="38c4b-112">This is an integer value that is either 32 or 64.</span></span>

</dd> <dt>

<span data-ttu-id="38c4b-113">*Установщик*</span><span class="sxs-lookup"><span data-stu-id="38c4b-113">*Installer*</span></span> 
</dt> <dd>

<span data-ttu-id="38c4b-114">Имя файла модуля приложения, которое делает вызов функции LSP отключить.</span><span class="sxs-lookup"><span data-stu-id="38c4b-114">The module filename of the application making the LSP disable call.</span></span>

</dd> <dt>

<span data-ttu-id="38c4b-115">*GUID*</span><span class="sxs-lookup"><span data-stu-id="38c4b-115">*GUID*</span></span> 
</dt> <dd>

<span data-ttu-id="38c4b-116">Значение идентификатора GUID поставщика транспорта Winsock, для которого отключается LSP.</span><span class="sxs-lookup"><span data-stu-id="38c4b-116">The GUID value of the Winsock transport provider that the LSP is being disabled.</span></span>

</dd> <dt>

<span data-ttu-id="38c4b-117">*Категория*</span><span class="sxs-lookup"><span data-stu-id="38c4b-117">*Category*</span></span> 
</dt> <dd>

<span data-ttu-id="38c4b-118">Элемент **двкаталожентрид** структуры [**\_ сведений о всапротокол**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) для LSP, который был отключен.</span><span class="sxs-lookup"><span data-stu-id="38c4b-118">The **dwCatalogEntryId** member of the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the LSP being disabled.</span></span>

</dd> </dl>

<span data-ttu-id="38c4b-119">У этого события нет параметров.</span><span class="sxs-lookup"><span data-stu-id="38c4b-119">This event has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="38c4b-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="38c4b-120">Remarks</span></span>

<span data-ttu-id="38c4b-121">Событие **Winsock \_ WS2HELP \_ LSP \_ Disable** ОТСЛЕЖИВАЕТся для операции отключения LSP, если запись протокола отключена в каталоге Winsock.</span><span class="sxs-lookup"><span data-stu-id="38c4b-121">The **WINSOCK\_WS2HELP\_LSP\_DISABLE** event is traced for an LSP disable operation when a protocol entry is disabled in the Winsock catalog.</span></span>

## <a name="requirements"></a><span data-ttu-id="38c4b-122">Требования</span><span class="sxs-lookup"><span data-stu-id="38c4b-122">Requirements</span></span>



| <span data-ttu-id="38c4b-123">Требование</span><span class="sxs-lookup"><span data-stu-id="38c4b-123">Requirement</span></span> | <span data-ttu-id="38c4b-124">Значение</span><span class="sxs-lookup"><span data-stu-id="38c4b-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="38c4b-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="38c4b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="38c4b-126">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="38c4b-126">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="38c4b-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="38c4b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="38c4b-128">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="38c4b-128">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="38c4b-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="38c4b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38c4b-130">Управление трассировкой Winsock</span><span class="sxs-lookup"><span data-stu-id="38c4b-130">Control of Winsock Tracing</span></span>](control-of-winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="38c4b-131">Трассировка Winsock</span><span class="sxs-lookup"><span data-stu-id="38c4b-131">Winsock Tracing</span></span>](winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="38c4b-132">Уровни трассировки Winsock</span><span class="sxs-lookup"><span data-stu-id="38c4b-132">Winsock Tracing Levels</span></span>](winsock-tracing-levels.md)
</dt> <dt>

[<span data-ttu-id="38c4b-133">Сведения о трассировке изменений каталога Winsock</span><span class="sxs-lookup"><span data-stu-id="38c4b-133">Winsock Catalog Change Tracing Details</span></span>](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 

 
