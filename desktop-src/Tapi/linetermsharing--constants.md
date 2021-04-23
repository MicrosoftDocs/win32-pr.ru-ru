---
description: '\_Константы побитового флага линетермшаринг описывают различные способы совместного использования терминала между устройствами, адресами или вызовами.'
ms.assetid: 50a52a50-4d94-4068-9ea4-bea862400036
title: Константы LINETERMSHARING_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2587621b6362195a610339ba5620b32f1d4f761
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685374"
---
# <a name="linetermsharing_-constants"></a><span data-ttu-id="4cedf-103">\_Константы линетермшаринг</span><span class="sxs-lookup"><span data-stu-id="4cedf-103">LINETERMSHARING\_ Constants</span></span>

<span data-ttu-id="4cedf-104">Константы побитового флага **линетермшаринг \_** описывают различные способы совместного использования терминала между устройствами, адресами или вызовами.</span><span class="sxs-lookup"><span data-stu-id="4cedf-104">The **LINETERMSHARING\_** bit-flag constants describe different ways in which a terminal can be shared between line devices, addresses, or calls.</span></span>

<dl> <dt>

<span data-ttu-id="4cedf-105"><span id="LINETERMSHARING_PRIVATE"></span><span id="linetermsharing_private"></span>**ЛИНЕТЕРМШАРИНГ \_ закрытый**</span><span class="sxs-lookup"><span data-stu-id="4cedf-105"><span id="LINETERMSHARING_PRIVATE"></span><span id="linetermsharing_private"></span>**LINETERMSHARING\_PRIVATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4cedf-106">Устройство терминала является частным для устройства с одной линией.</span><span class="sxs-lookup"><span data-stu-id="4cedf-106">The terminal device is private to a single line device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4cedf-107"><span id="LINETERMSHARING_SHAREDCONF"></span><span id="linetermsharing_sharedconf"></span>**ЛИНЕТЕРМШАРИНГ \_ шаредконф**</span><span class="sxs-lookup"><span data-stu-id="4cedf-107"><span id="LINETERMSHARING_SHAREDCONF"></span><span id="linetermsharing_sharedconf"></span>**LINETERMSHARING\_SHAREDCONF**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4cedf-108">Устройство терминала может использоваться несколькими строками.</span><span class="sxs-lookup"><span data-stu-id="4cedf-108">The terminal device can be used by multiple lines.</span></span> <span data-ttu-id="4cedf-109">[**Линесеттерминал**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) запросы различных терминалов, которые в итоге объединяются или обрабатываются в терминале.</span><span class="sxs-lookup"><span data-stu-id="4cedf-109">The [**lineSetTerminal**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) requests of the various terminals end up being merged or conferenced at the terminal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4cedf-110"><span id="LINETERMSHARING_SHAREDEXCL"></span><span id="linetermsharing_sharedexcl"></span>**ЛИНЕТЕРМШАРИНГ \_ шаредекскл**</span><span class="sxs-lookup"><span data-stu-id="4cedf-110"><span id="LINETERMSHARING_SHAREDEXCL"></span><span id="linetermsharing_sharedexcl"></span>**LINETERMSHARING\_SHAREDEXCL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4cedf-111">Устройство терминала может использоваться несколькими строками.</span><span class="sxs-lookup"><span data-stu-id="4cedf-111">The terminal device can be used by multiple lines.</span></span> <span data-ttu-id="4cedf-112">Последнее устройство, [**линесеттерминал**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) или [**тспи \_ линесеттерминал**](/windows/win32/api/tspi/nf-tspi-tspi_linesetterminal) на терминал для данного режима терминала, будет иметь Эксклюзивное подключение к терминалу для этого режима.</span><span class="sxs-lookup"><span data-stu-id="4cedf-112">The last line device to do a [**lineSetTerminal**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) or [**TSPI\_lineSetTerminal**](/windows/win32/api/tspi/nf-tspi-tspi_linesetterminal) to the terminal for a given terminal mode will have exclusive connection to the terminal for that mode.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4cedf-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4cedf-113">Remarks</span></span>

<span data-ttu-id="4cedf-114">Без расширяемости.</span><span class="sxs-lookup"><span data-stu-id="4cedf-114">No extensibility.</span></span> <span data-ttu-id="4cedf-115">Все 32 бит зарезервированы.</span><span class="sxs-lookup"><span data-stu-id="4cedf-115">All 32 bits are reserved.</span></span>

<span data-ttu-id="4cedf-116">Эти константы описывают классы элементов управления и информационных потоков, которые могут направляться напрямую между линейным устройством и устройством терминала (например, набором телефонов).</span><span class="sxs-lookup"><span data-stu-id="4cedf-116">These constants describe the classes of control and information streams that can be routed directly between a line device and a terminal device (such as a phone set).</span></span>

## <a name="requirements"></a><span data-ttu-id="4cedf-117">Требования</span><span class="sxs-lookup"><span data-stu-id="4cedf-117">Requirements</span></span>



| <span data-ttu-id="4cedf-118">Требование</span><span class="sxs-lookup"><span data-stu-id="4cedf-118">Requirement</span></span> | <span data-ttu-id="4cedf-119">Значение</span><span class="sxs-lookup"><span data-stu-id="4cedf-119">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="4cedf-120">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="4cedf-120">TAPI version</span></span><br/> | <span data-ttu-id="4cedf-121">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="4cedf-121">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="4cedf-122">Header</span><span class="sxs-lookup"><span data-stu-id="4cedf-122">Header</span></span><br/>       | <dl> <span data-ttu-id="4cedf-123"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="4cedf-123"><dt>Tapi.h</dt></span></span> </dl> |



 

