---
description: Задает уровень защиты для механизма защиты выходных данных.
ms.assetid: f4e63bf5-0749-4054-9f86-7fd88f2881ad
title: OPM_SET_PROTECTION_LEVEL (Опмапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17a80fb674c9347dafc3bcf1a62dc4bc909f0471
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711427"
---
# <a name="opm_set_protection_level"></a><span data-ttu-id="3fc50-103">ОПМ \_ установить \_ \_ уровень защиты</span><span class="sxs-lookup"><span data-stu-id="3fc50-103">OPM\_SET\_PROTECTION\_LEVEL</span></span>

<span data-ttu-id="3fc50-104">Задает уровень защиты для механизма защиты выходных данных.</span><span class="sxs-lookup"><span data-stu-id="3fc50-104">Sets the protection level for an output protection mechanism.</span></span>



| <span data-ttu-id="3fc50-105">Требование</span><span class="sxs-lookup"><span data-stu-id="3fc50-105">Requirement</span></span> | <span data-ttu-id="3fc50-106">Значение</span><span class="sxs-lookup"><span data-stu-id="3fc50-106">Value</span></span> |
|--------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3fc50-107">Идентификатор GUID команды</span><span class="sxs-lookup"><span data-stu-id="3fc50-107">Command GUID</span></span> | <span data-ttu-id="3fc50-108">ОПМ \_ установить \_ \_ уровень защиты</span><span class="sxs-lookup"><span data-stu-id="3fc50-108">OPM\_SET\_PROTECTION\_LEVEL</span></span>                                                                         |
| <span data-ttu-id="3fc50-109">Входные данные</span><span class="sxs-lookup"><span data-stu-id="3fc50-109">Input data</span></span>   | <span data-ttu-id="3fc50-110">Структура [**\_ \_ \_ \_ параметров уровня защиты ОПМ Set**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_protection_level_parameters)</span><span class="sxs-lookup"><span data-stu-id="3fc50-110">An [**OPM\_SET\_PROTECTION\_LEVEL\_PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_protection_level_parameters) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="3fc50-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3fc50-111">Remarks</span></span>

<span data-ttu-id="3fc50-112">Некоторые соединители могут поддерживать несколько механизмов защиты.</span><span class="sxs-lookup"><span data-stu-id="3fc50-112">Some connectors can support multiple protection mechanisms.</span></span> <span data-ttu-id="3fc50-113">С помощью этого типа соединителя можно применить несколько механизмов защиты к одному и тому же соединителю с разными настройками для каждого из них.</span><span class="sxs-lookup"><span data-stu-id="3fc50-113">With that type of connector, you can apply several protection mechanisms to the same connector, with different settings for each.</span></span>

## <a name="requirements"></a><span data-ttu-id="3fc50-114">Требования</span><span class="sxs-lookup"><span data-stu-id="3fc50-114">Requirements</span></span>



| <span data-ttu-id="3fc50-115">Требование</span><span class="sxs-lookup"><span data-stu-id="3fc50-115">Requirement</span></span> | <span data-ttu-id="3fc50-116">Значение</span><span class="sxs-lookup"><span data-stu-id="3fc50-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3fc50-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3fc50-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3fc50-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3fc50-118">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="3fc50-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3fc50-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3fc50-120">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3fc50-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="3fc50-121">Header</span><span class="sxs-lookup"><span data-stu-id="3fc50-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="3fc50-122"><dt>Опмапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="3fc50-122"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3fc50-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3fc50-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fc50-124">**Иопмвидеуутпут:: Configure**</span><span class="sxs-lookup"><span data-stu-id="3fc50-124">**IOPMVideoOutput::Configure**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure)
</dt> <dt>

[<span data-ttu-id="3fc50-125">Команды ОПМ</span><span class="sxs-lookup"><span data-stu-id="3fc50-125">OPM Commands</span></span>](opm-commands.md)
</dt> </dl>

 

 




