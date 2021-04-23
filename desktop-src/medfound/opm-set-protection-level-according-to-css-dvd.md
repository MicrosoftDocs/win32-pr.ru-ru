---
description: Задает уровень защиты HDCP для воспроизведения DVD-дисков, следующие правила системы расшифровки содержимого DVD-диска (CSS).
ms.assetid: 8d9ecb9b-8528-4b23-ab2f-234ba2cb7ed0
title: OPM_SET_PROTECTION_LEVEL_ACCORDING_TO_CSS_DVD (Опмапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 971d288367bdc5c59e11bdfd5b86fb233755c95e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155339"
---
# <a name="opm_set_protection_level_according_to_css_dvd"></a><span data-ttu-id="290c2-103">ОПМ \_ установить \_ \_ уровень защиты \_ в \_ соответствии \_ с \_ DVD-диском CSS</span><span class="sxs-lookup"><span data-stu-id="290c2-103">OPM\_SET\_PROTECTION\_LEVEL\_ACCORDING\_TO\_CSS\_DVD</span></span>

<span data-ttu-id="290c2-104">Задает уровень защиты HDCP для воспроизведения DVD-дисков, следующие правила системы расшифровки содержимого DVD-диска (CSS).</span><span class="sxs-lookup"><span data-stu-id="290c2-104">Sets the HDCP protection level for DVD playback, following DVD Content Scramble System (CSS) rules.</span></span>



| <span data-ttu-id="290c2-105">Требование</span><span class="sxs-lookup"><span data-stu-id="290c2-105">Requirement</span></span> | <span data-ttu-id="290c2-106">Значение</span><span class="sxs-lookup"><span data-stu-id="290c2-106">Value</span></span> |
|--------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="290c2-107">Идентификатор GUID команды</span><span class="sxs-lookup"><span data-stu-id="290c2-107">Command GUID</span></span> | <span data-ttu-id="290c2-108">ОПМ \_ установить \_ \_ уровень защиты \_ в \_ соответствии \_ с \_ DVD-диском CSS</span><span class="sxs-lookup"><span data-stu-id="290c2-108">OPM\_SET\_PROTECTION\_LEVEL\_ACCORDING\_TO\_CSS\_DVD</span></span>                                                |
| <span data-ttu-id="290c2-109">Входные данные</span><span class="sxs-lookup"><span data-stu-id="290c2-109">Input data</span></span>   | <span data-ttu-id="290c2-110">Структура [**\_ \_ \_ \_ параметров уровня защиты ОПМ Set**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_protection_level_parameters)</span><span class="sxs-lookup"><span data-stu-id="290c2-110">An [**OPM\_SET\_PROTECTION\_LEVEL\_PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_protection_level_parameters) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="290c2-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="290c2-111">Remarks</span></span>

<span data-ttu-id="290c2-112">Эта команда используется для установки High-Bandwidth Digital Защита содержимого (HDCP) при воспроизведении стандартных DVD-дисков.</span><span class="sxs-lookup"><span data-stu-id="290c2-112">This command is used to set High-Bandwidth Digital Content Protection (HDCP) when playing standard DVDs.</span></span> <span data-ttu-id="290c2-113">В отличие от команды [**ОПМ \_ Set \_ Protection \_ Level**](opm-set-protection-level.md) , если HDCP не может быть задан по какой либо причине, эта команда не останавливает воспроизведение.</span><span class="sxs-lookup"><span data-stu-id="290c2-113">Unlike the [**OPM\_SET\_PROTECTION\_LEVEL**](opm-set-protection-level.md) command, if HDCP cannot be set for some reason, this command does not stop playback.</span></span> <span data-ttu-id="290c2-114">(Правила CSS для DVD-дисков содержат «лучшие усилия» для игроков.) В противном случае эта команда идентична команде **ОПМ \_ Set \_ Protection \_ Level** .</span><span class="sxs-lookup"><span data-stu-id="290c2-114">(DVD CSS rules contain a "best effort" provision for players.) Otherwise, this command is identical to the **OPM\_SET\_PROTECTION\_LEVEL** command.</span></span>

## <a name="requirements"></a><span data-ttu-id="290c2-115">Требования</span><span class="sxs-lookup"><span data-stu-id="290c2-115">Requirements</span></span>



| <span data-ttu-id="290c2-116">Требование</span><span class="sxs-lookup"><span data-stu-id="290c2-116">Requirement</span></span> | <span data-ttu-id="290c2-117">Значение</span><span class="sxs-lookup"><span data-stu-id="290c2-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="290c2-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="290c2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="290c2-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="290c2-119">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="290c2-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="290c2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="290c2-121">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="290c2-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="290c2-122">Header</span><span class="sxs-lookup"><span data-stu-id="290c2-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="290c2-123"><dt>Опмапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="290c2-123"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="290c2-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="290c2-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="290c2-125">**Иопмвидеуутпут:: Configure**</span><span class="sxs-lookup"><span data-stu-id="290c2-125">**IOPMVideoOutput::Configure**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure)
</dt> <dt>

[<span data-ttu-id="290c2-126">Команды ОПМ</span><span class="sxs-lookup"><span data-stu-id="290c2-126">OPM Commands</span></span>](opm-commands.md)
</dt> </dl>

 

 




