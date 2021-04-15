---
description: Команды ОПМ
ms.assetid: 52165e1b-a178-4483-bf76-4197281f856d
title: Команды ОПМ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8aa14026123656b26e978bc179d65c3b61913c62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701801"
---
# <a name="opm-commands"></a><span data-ttu-id="28a94-103">Команды ОПМ</span><span class="sxs-lookup"><span data-stu-id="28a94-103">OPM Commands</span></span>

<span data-ttu-id="28a94-104">В этом разделе перечислены доступные команды для [Output Protection Manager](output-protection-manager.md) (ОПМ).</span><span class="sxs-lookup"><span data-stu-id="28a94-104">This section lists the available commands for [Output Protection Manager](output-protection-manager.md) (OPM).</span></span>

<span data-ttu-id="28a94-105">Чтобы отправить команду ОПМ, вызовите [**иопмвидеуутпут:: Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure).</span><span class="sxs-lookup"><span data-stu-id="28a94-105">To send an OPM command, call [**IOPMVideoOutput::Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure).</span></span> <span data-ttu-id="28a94-106">Для каждой команды перечислены следующие сведения.</span><span class="sxs-lookup"><span data-stu-id="28a94-106">For each command, the following information is listed.</span></span>



|              |                                                                                                                                                             |
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28a94-107">Идентификатор GUID команды</span><span class="sxs-lookup"><span data-stu-id="28a94-107">Command GUID</span></span> | <span data-ttu-id="28a94-108">Идентифицирует команду.</span><span class="sxs-lookup"><span data-stu-id="28a94-108">Identifies the command.</span></span> <span data-ttu-id="28a94-109">Задайте для элемента **гуидсеттинг** структуры [**\_ \_ параметров ОПМ**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) значение, равное этому значению.</span><span class="sxs-lookup"><span data-stu-id="28a94-109">Set the **guidSetting** member of the [**OPM\_CONFIGURE\_PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) structure equal to this value.</span></span> |
| <span data-ttu-id="28a94-110">Входные данные</span><span class="sxs-lookup"><span data-stu-id="28a94-110">Input data</span></span>   | <span data-ttu-id="28a94-111">Указывает способ интерпретации массива **абпараметерс** в структуре [**параметров ОПМ \_ Configure \_**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) .</span><span class="sxs-lookup"><span data-stu-id="28a94-111">Specifies how to interpret the **abParameters** array in the [**OPM\_CONFIGURE\_PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) structure.</span></span>                      |



 

<span data-ttu-id="28a94-112">Определены следующие команды:</span><span class="sxs-lookup"><span data-stu-id="28a94-112">The following commands are defined:</span></span>



| <span data-ttu-id="28a94-113">Get-Help</span><span class="sxs-lookup"><span data-stu-id="28a94-113">Command</span></span>                                                                                                       | <span data-ttu-id="28a94-114">Описание</span><span class="sxs-lookup"><span data-stu-id="28a94-114">Description</span></span>                                                                                         |
|---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="28a94-115">**ОПМ \_ Установка \_ \_ сигнала ACP и \_ кгмса \_**</span><span class="sxs-lookup"><span data-stu-id="28a94-115">**OPM\_SET\_ACP\_AND\_CGMSA\_SIGNALING**</span></span>](opm-set-acp-and-cgmsa-signaling.md)                               | <span data-ttu-id="28a94-116">Указывает сведения о видеосигнале, отличном от уровня защиты.</span><span class="sxs-lookup"><span data-stu-id="28a94-116">Specifies information about the video signal, other than the protection level.</span></span>                      |
| [<span data-ttu-id="28a94-117">**ОПМ \_ Set \_ HDCP \_ СРМ**</span><span class="sxs-lookup"><span data-stu-id="28a94-117">**OPM\_SET\_HDCP\_SRM**</span></span>](opm-set-hdcp-srm.md)                                                               | <span data-ttu-id="28a94-118">Обновляет сообщение о возобновлении системы (СРМ) для High-Bandwidth Digital Защита содержимого (HDCP).</span><span class="sxs-lookup"><span data-stu-id="28a94-118">Updates the system renewability message (SRM) for High-Bandwidth Digital Content Protection (HDCP).</span></span> |
| [<span data-ttu-id="28a94-119">**ОПМ \_ установить \_ \_ уровень защиты**</span><span class="sxs-lookup"><span data-stu-id="28a94-119">**OPM\_SET\_PROTECTION\_LEVEL**</span></span>](opm-set-protection-level.md)                                               | <span data-ttu-id="28a94-120">Задает уровень защиты для механизма защиты выходных данных.</span><span class="sxs-lookup"><span data-stu-id="28a94-120">Sets the protection level for an output protection mechanism.</span></span>                                       |
| [<span data-ttu-id="28a94-121">**ОПМ \_ установить \_ \_ уровень защиты \_ в \_ соответствии \_ с \_ DVD-диском CSS**</span><span class="sxs-lookup"><span data-stu-id="28a94-121">**OPM\_SET\_PROTECTION\_LEVEL\_ACCORDING\_TO\_CSS\_DVD**</span></span>](opm-set-protection-level-according-to-css-dvd.md) | <span data-ttu-id="28a94-122">Задает уровень защиты HDCP для воспроизведения DVD-дисков, следующие правила системы расшифровки содержимого DVD-диска (CSS).</span><span class="sxs-lookup"><span data-stu-id="28a94-122">Sets the HDCP protection level for DVD playback, following DVD Content Scramble System (CSS) rules.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="28a94-123">См. также</span><span class="sxs-lookup"><span data-stu-id="28a94-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28a94-124">Справочник по программированию ОПМ</span><span class="sxs-lookup"><span data-stu-id="28a94-124">OPM Programming Reference</span></span>](opm-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="28a94-125">Диспетчер выходной защиты</span><span class="sxs-lookup"><span data-stu-id="28a94-125">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 



