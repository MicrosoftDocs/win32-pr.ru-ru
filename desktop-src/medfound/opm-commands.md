---
description: Команды ОПМ
ms.assetid: 52165e1b-a178-4483-bf76-4197281f856d
title: Команды ОПМ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b00240925c28322b911ab55a0e4f026f051d6ec
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119149"
---
# <a name="opm-commands"></a><span data-ttu-id="b0663-103">Команды ОПМ</span><span class="sxs-lookup"><span data-stu-id="b0663-103">OPM Commands</span></span>

<span data-ttu-id="b0663-104">В этом разделе перечислены доступные команды для [Output Protection Manager](output-protection-manager.md) (ОПМ).</span><span class="sxs-lookup"><span data-stu-id="b0663-104">This section lists the available commands for [Output Protection Manager](output-protection-manager.md) (OPM).</span></span>

<span data-ttu-id="b0663-105">Чтобы отправить команду ОПМ, вызовите [**иопмвидеуутпут:: Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure).</span><span class="sxs-lookup"><span data-stu-id="b0663-105">To send an OPM command, call [**IOPMVideoOutput::Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure).</span></span> <span data-ttu-id="b0663-106">Для каждой команды перечислены следующие сведения.</span><span class="sxs-lookup"><span data-stu-id="b0663-106">For each command, the following information is listed.</span></span>



| <span data-ttu-id="b0663-107">Значение</span><span class="sxs-lookup"><span data-stu-id="b0663-107">Value</span></span>             | <span data-ttu-id="b0663-108">Описание</span><span class="sxs-lookup"><span data-stu-id="b0663-108">Description</span></span>                                                                                                                                                            |
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0663-109">Идентификатор GUID команды</span><span class="sxs-lookup"><span data-stu-id="b0663-109">Command GUID</span></span> | <span data-ttu-id="b0663-110">Идентифицирует команду.</span><span class="sxs-lookup"><span data-stu-id="b0663-110">Identifies the command.</span></span> <span data-ttu-id="b0663-111">Задайте для элемента **гуидсеттинг** структуры [**\_ \_ параметров ОПМ**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) значение, равное этому значению.</span><span class="sxs-lookup"><span data-stu-id="b0663-111">Set the **guidSetting** member of the [**OPM\_CONFIGURE\_PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) structure equal to this value.</span></span> |
| <span data-ttu-id="b0663-112">Входные данные</span><span class="sxs-lookup"><span data-stu-id="b0663-112">Input data</span></span>   | <span data-ttu-id="b0663-113">Указывает способ интерпретации массива **абпараметерс** в структуре [**параметров ОПМ \_ Configure \_**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) .</span><span class="sxs-lookup"><span data-stu-id="b0663-113">Specifies how to interpret the **abParameters** array in the [**OPM\_CONFIGURE\_PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) structure.</span></span>                      |



 

<span data-ttu-id="b0663-114">Определены следующие команды:</span><span class="sxs-lookup"><span data-stu-id="b0663-114">The following commands are defined:</span></span>



| <span data-ttu-id="b0663-115">Команда</span><span class="sxs-lookup"><span data-stu-id="b0663-115">Command</span></span>                                                                                                       | <span data-ttu-id="b0663-116">Описание</span><span class="sxs-lookup"><span data-stu-id="b0663-116">Description</span></span>                                                                                         |
|---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b0663-117">**ОПМ \_ Установка \_ \_ сигнала ACP и \_ кгмса \_**</span><span class="sxs-lookup"><span data-stu-id="b0663-117">**OPM\_SET\_ACP\_AND\_CGMSA\_SIGNALING**</span></span>](opm-set-acp-and-cgmsa-signaling.md)                               | <span data-ttu-id="b0663-118">Указывает сведения о видеосигнале, отличном от уровня защиты.</span><span class="sxs-lookup"><span data-stu-id="b0663-118">Specifies information about the video signal, other than the protection level.</span></span>                      |
| [<span data-ttu-id="b0663-119">**ОПМ \_ Set \_ HDCP \_ СРМ**</span><span class="sxs-lookup"><span data-stu-id="b0663-119">**OPM\_SET\_HDCP\_SRM**</span></span>](opm-set-hdcp-srm.md)                                                               | <span data-ttu-id="b0663-120">Обновляет сообщение о возобновлении системы (СРМ) для High-Bandwidth Digital Защита содержимого (HDCP).</span><span class="sxs-lookup"><span data-stu-id="b0663-120">Updates the system renewability message (SRM) for High-Bandwidth Digital Content Protection (HDCP).</span></span> |
| [<span data-ttu-id="b0663-121">**ОПМ \_ установить \_ \_ уровень защиты**</span><span class="sxs-lookup"><span data-stu-id="b0663-121">**OPM\_SET\_PROTECTION\_LEVEL**</span></span>](opm-set-protection-level.md)                                               | <span data-ttu-id="b0663-122">Задает уровень защиты для механизма защиты выходных данных.</span><span class="sxs-lookup"><span data-stu-id="b0663-122">Sets the protection level for an output protection mechanism.</span></span>                                       |
| [<span data-ttu-id="b0663-123">**ОПМ \_ установить \_ \_ уровень защиты \_ в \_ соответствии \_ с \_ DVD-диском CSS**</span><span class="sxs-lookup"><span data-stu-id="b0663-123">**OPM\_SET\_PROTECTION\_LEVEL\_ACCORDING\_TO\_CSS\_DVD**</span></span>](opm-set-protection-level-according-to-css-dvd.md) | <span data-ttu-id="b0663-124">Задает уровень защиты HDCP для воспроизведения DVD-дисков, следующие правила системы расшифровки содержимого DVD-диска (CSS).</span><span class="sxs-lookup"><span data-stu-id="b0663-124">Sets the HDCP protection level for DVD playback, following DVD Content Scramble System (CSS) rules.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="b0663-125">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="b0663-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0663-126">Справочник по программированию ОПМ</span><span class="sxs-lookup"><span data-stu-id="b0663-126">OPM Programming Reference</span></span>](opm-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="b0663-127">Диспетчер выходной защиты</span><span class="sxs-lookup"><span data-stu-id="b0663-127">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 



