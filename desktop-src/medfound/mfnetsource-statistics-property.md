---
description: Содержит статистику сети для сетевого источника.
ms.assetid: 1948481b-febd-434b-a5dc-faef592ea0ed
title: Свойство MFNETSOURCE_STATISTICS (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a09e6c0fe4697595ff3600135327ba093350e0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143081"
---
# <a name="mfnetsource_statistics-property"></a><span data-ttu-id="9f94a-103">\_Свойство статистики мфнетсаурце</span><span class="sxs-lookup"><span data-stu-id="9f94a-103">MFNETSOURCE\_STATISTICS Property</span></span>

<span data-ttu-id="9f94a-104">Содержит статистику сети для сетевого источника.</span><span class="sxs-lookup"><span data-stu-id="9f94a-104">Contains network statistics for the network source.</span></span>

## <a name="data-type"></a><span data-ttu-id="9f94a-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="9f94a-105">Data Type</span></span>

<span data-ttu-id="9f94a-106">Различать см. раздел Примечания.</span><span class="sxs-lookup"><span data-stu-id="9f94a-106">Varies; see Remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f94a-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9f94a-107">Remarks</span></span>

<span data-ttu-id="9f94a-108">Постоянная \_ Статистика мфнетсаурце определяет идентификатор GUID, используемый в сочетании с перечислением [**\_ \_ идентификаторов мфнетсаурце Statistics**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids) для определения набора ключей свойств.</span><span class="sxs-lookup"><span data-stu-id="9f94a-108">The constant MFNETSOURCE\_STATISTICS defines a GUID that is used in conjunction with the [**MFNETSOURCE\_STATISTICS\_IDS**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids) enumeration to define a set of property keys.</span></span> <span data-ttu-id="9f94a-109">Каждый ключ свойства в наборе имеет **fmtid** , равный \_ статистике мфнетсаурце, и **PID** , равный одному элементу перечисления.</span><span class="sxs-lookup"><span data-stu-id="9f94a-109">Each property key in the set has **fmtid** equal to MFNETSOURCE\_STATISTICS and **pid** equal to one member of the enumeration.</span></span> <span data-ttu-id="9f94a-110">Дополнительные сведения см. в разделе [**мфнетсаурце \_ Statistics \_ IDS**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids).</span><span class="sxs-lookup"><span data-stu-id="9f94a-110">For more information, see [**MFNETSOURCE\_STATISTICS\_IDS**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids).</span></span>

## <a name="requirements"></a><span data-ttu-id="9f94a-111">Требования</span><span class="sxs-lookup"><span data-stu-id="9f94a-111">Requirements</span></span>



| <span data-ttu-id="9f94a-112">Требование</span><span class="sxs-lookup"><span data-stu-id="9f94a-112">Requirement</span></span> | <span data-ttu-id="9f94a-113">Значение</span><span class="sxs-lookup"><span data-stu-id="9f94a-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9f94a-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9f94a-114">Minimum supported client</span></span><br/> | <span data-ttu-id="9f94a-115">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9f94a-115">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="9f94a-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9f94a-116">Minimum supported server</span></span><br/> | <span data-ttu-id="9f94a-117">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9f94a-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9f94a-118">Header</span><span class="sxs-lookup"><span data-stu-id="9f94a-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f94a-119"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f94a-119"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f94a-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9f94a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f94a-121">Ведение журнала клиента</span><span class="sxs-lookup"><span data-stu-id="9f94a-121">Client Logging</span></span>](client-logging.md)
</dt> <dt>

[<span data-ttu-id="9f94a-122">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9f94a-122">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="9f94a-123">Сетевые подключения в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9f94a-123">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




