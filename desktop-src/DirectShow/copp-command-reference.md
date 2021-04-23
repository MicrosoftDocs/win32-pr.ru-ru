---
description: Справочник по командам Копп
ms.assetid: b21db1cf-cac3-41d6-8189-6e01c8f91a7d
title: Справочник по командам Копп
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50dfeebe42b877604ab880ef1855035242d6eca8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105673097"
---
# <a name="copp-command-reference"></a><span data-ttu-id="4c494-103">Справочник по командам Копп</span><span class="sxs-lookup"><span data-stu-id="4c494-103">COPP Command Reference</span></span>

<span data-ttu-id="4c494-104">В этом разделе описываются команды сертифицированного протокола выходной защиты (Копп).</span><span class="sxs-lookup"><span data-stu-id="4c494-104">This section describes the Certified Output Protection Protocol (COPP) commands.</span></span> <span data-ttu-id="4c494-105">Определены следующие команды.</span><span class="sxs-lookup"><span data-stu-id="4c494-105">The following commands are defined.</span></span>



| <span data-ttu-id="4c494-106">Get-Help</span><span class="sxs-lookup"><span data-stu-id="4c494-106">Command</span></span>              | <span data-ttu-id="4c494-107">Код GUID</span><span class="sxs-lookup"><span data-stu-id="4c494-107">GUID</span></span>                             |
|----------------------|----------------------------------|
| <span data-ttu-id="4c494-108">Задать уровень защиты</span><span class="sxs-lookup"><span data-stu-id="4c494-108">Set Protection Level</span></span> | <span data-ttu-id="4c494-109">**ДКСВА \_ коппсетпротектионлевел**</span><span class="sxs-lookup"><span data-stu-id="4c494-109">**DXVA\_COPPSetProtectionLevel**</span></span> |
| <span data-ttu-id="4c494-110">Настройка сигнализации</span><span class="sxs-lookup"><span data-stu-id="4c494-110">Set Signaling</span></span>        | <span data-ttu-id="4c494-111">**ДКСВА \_ коппсетсигналинг**</span><span class="sxs-lookup"><span data-stu-id="4c494-111">**DXVA\_COPPSetSignaling**</span></span>       |



 

<span data-ttu-id="4c494-112">Команда "задать уровень защиты"</span><span class="sxs-lookup"><span data-stu-id="4c494-112">Set Protection Level Command</span></span>

<span data-ttu-id="4c494-113">Задает уровень защиты для указанного механизма защиты выходных данных.</span><span class="sxs-lookup"><span data-stu-id="4c494-113">Sets the protection level for a specified output protection mechanism.</span></span> <span data-ttu-id="4c494-114">В зависимости от соединителя можно применить несколько механизмов защиты для одного соединителя с разными параметрами для каждого механизма.</span><span class="sxs-lookup"><span data-stu-id="4c494-114">Depending on the connector, it might be possible to apply more than one protection mechanism on the same connector, with different settings for each mechanism.</span></span>

<span data-ttu-id="4c494-115">**GUID**: дксва \_ коппсетпротектионлевел</span><span class="sxs-lookup"><span data-stu-id="4c494-115">**GUID**: DXVA\_COPPSetProtectionLevel</span></span>

<span data-ttu-id="4c494-116">**Входные данные**: [**Структура \_ коппсетпротектионлевелкмддата дксва**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppsetprotectionlevelcmddata) .</span><span class="sxs-lookup"><span data-stu-id="4c494-116">**Input data**: A [**DXVA\_COPPSetProtectionLevelCmdData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppsetprotectionlevelcmddata) structure.</span></span>

<span data-ttu-id="4c494-117">Команда "задать сигнализацию"</span><span class="sxs-lookup"><span data-stu-id="4c494-117">Set Signaling Command</span></span>

<span data-ttu-id="4c494-118">Указывает сведения о видеосигнале, отличном от уровня защиты.</span><span class="sxs-lookup"><span data-stu-id="4c494-118">Specifies information about the video signal other than the protection level.</span></span>

<span data-ttu-id="4c494-119">Для некоторых стандартов защиты с поддержкой CGMS-A требуется, чтобы сигнал телевсион содержал информацию о пропорции и другую информацию в тех же ВБИах, что и биты CGMS-A.</span><span class="sxs-lookup"><span data-stu-id="4c494-119">For CGMS-A, certain protection standards require that the televsion signal contains information about the aspect ratio and other information within the same VBI waveform packets as the CGMS-A bits.</span></span> <span data-ttu-id="4c494-120">Телевизоры могут плохо отображаться, если сведения о пропорции не соответствуют потоку видео.</span><span class="sxs-lookup"><span data-stu-id="4c494-120">Televisions may display poorly if the aspect ratio information is not consistent with the video stream.</span></span> <span data-ttu-id="4c494-121">Приложение может использовать эту команду, чтобы задать пропорции, чтобы графический драйвер мог формировать правильные пакеты ВБИ.</span><span class="sxs-lookup"><span data-stu-id="4c494-121">The application can use this command to specify the aspect ratio so that the graphics driver can generate the correct VBI packets.</span></span>

<span data-ttu-id="4c494-122">Эта команда также предназначена для расширения, если в будущих стандартах требуются дополнительные сведения о сигналах.</span><span class="sxs-lookup"><span data-stu-id="4c494-122">This command is also designed to be extensible if additional signal information is required in future standards.</span></span>

<span data-ttu-id="4c494-123">**GUID**: дксва \_ коппсетсигналинг</span><span class="sxs-lookup"><span data-stu-id="4c494-123">**GUID**: DXVA\_COPPSetSignaling</span></span>

<span data-ttu-id="4c494-124">**Входные данные**: [**Структура \_ коппсетсигналингкмддата дксва**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppsetsignalingcmddata) .</span><span class="sxs-lookup"><span data-stu-id="4c494-124">**Input data**: A [**DXVA\_COPPSetSignalingCmdData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppsetsignalingcmddata) structure.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4c494-125">См. также</span><span class="sxs-lookup"><span data-stu-id="4c494-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c494-126">Использование протокола сертифицированной выходной защиты (Копп)</span><span class="sxs-lookup"><span data-stu-id="4c494-126">Using Certified Output Protection Protocol (COPP)</span></span>](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



