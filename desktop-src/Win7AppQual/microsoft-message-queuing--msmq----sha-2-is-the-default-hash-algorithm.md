---
description: .
ms.assetid: 43cca5bc-6675-4f29-925e-19d3fb19ef0f
title: Очередь сообщений Майкрософт (MSMQ) — SHA 2 является алгоритмом хэширования по умолчанию.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61f0d2476133ca7939bc90effa3842c0b90482ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265892"
---
# <a name="microsoft-message-queuing-msmq---sha-2-is-the-default-hash-algorithm"></a><span data-ttu-id="f7858-103">Очередь сообщений Майкрософт (MSMQ) — SHA 2 является алгоритмом хэширования по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f7858-103">Microsoft Message Queuing (MSMQ) - SHA 2 Is the Default Hash Algorithm</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="f7858-104">Затронутые платформы</span><span class="sxs-lookup"><span data-stu-id="f7858-104">Affected Platforms</span></span>

 <span data-ttu-id="f7858-105">**Клиенты** — Windows XP Windows Vista, Windows \| \| 7</span><span class="sxs-lookup"><span data-stu-id="f7858-105">**Clients** - Windows XP \| Windows Vista \| Windows 7</span></span>  
<span data-ttu-id="f7858-106">**Серверы** — windows Server 2003 windows \| Server 2008 \| Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f7858-106">**Servers** - Windows Server 2003 \| Windows Server 2008 \| Windows Server 2008 R2</span></span>  










## <a name="feature-impact"></a><span data-ttu-id="f7858-107">Воздействие на функции</span><span class="sxs-lookup"><span data-stu-id="f7858-107">Feature Impact</span></span>

 <span data-ttu-id="f7858-108">**Серьезность** — низкая</span><span class="sxs-lookup"><span data-stu-id="f7858-108">**Severity** - Low</span></span>  
<span data-ttu-id="f7858-109">**Частота** -низкая</span><span class="sxs-lookup"><span data-stu-id="f7858-109">**Frequency** - Low</span></span>  





## <a name="description"></a><span data-ttu-id="f7858-110">Описание</span><span class="sxs-lookup"><span data-stu-id="f7858-110">Description</span></span>

<span data-ttu-id="f7858-111">В Windows 7 MSMQ использует SHA-2 в качестве значения по умолчанию при подписывании исходящего сообщения.</span><span class="sxs-lookup"><span data-stu-id="f7858-111">In Windows 7, MSMQ uses SHA-2 as the default when signing an outgoing message.</span></span> <span data-ttu-id="f7858-112">Кроме того, все входящие сообщения должны быть подписаны SHA-2.</span><span class="sxs-lookup"><span data-stu-id="f7858-112">Additionally, all incoming messages must be signed with SHA-2.</span></span> <span data-ttu-id="f7858-113">Вы можете включить поддержку более низкого алгоритма шифрования с помощью раздела реестра, доступного для администратора.</span><span class="sxs-lookup"><span data-stu-id="f7858-113">You can enable support for a lower encryption algorithm through an administrator-accessible registry key.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="f7858-114">Влияние на манифесты</span><span class="sxs-lookup"><span data-stu-id="f7858-114">Manifestation of Impact</span></span>

-   <span data-ttu-id="f7858-115">MSMQ в Windows 2003 или ниже не будет принимать подписанные сообщения, поступающие от MSMQ в Windows 7</span><span class="sxs-lookup"><span data-stu-id="f7858-115">MSMQ in Windows 2003 or below will not accept signed messages originating from MSMQ in Windows 7</span></span>
-   <span data-ttu-id="f7858-116">MSMQ в Windows 7 не будет принимать подписанные сообщения, полученные из Windows 2008 или ниже</span><span class="sxs-lookup"><span data-stu-id="f7858-116">MSMQ in Windows 7 will not accept signed messages originating from Windows 2008 or below</span></span>

## <a name="mitigation"></a><span data-ttu-id="f7858-117">Меры по снижению риска</span><span class="sxs-lookup"><span data-stu-id="f7858-117">Mitigation</span></span>

<span data-ttu-id="f7858-118">Чтобы использовать более надежный алгоритм подписи, пользователям следует рассмотреть возможность обновления до Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f7858-118">Users should consider upgrading to Windows 7 to leverage the stronger signing algorithm.</span></span> <span data-ttu-id="f7858-119">Чтобы обеспечить простой обмен подписанными сообщениями между Windows 7 и любой операционной системой нижнего уровня, администратор должен добавить соответствующие исключения на компьютерах MSMQ.</span><span class="sxs-lookup"><span data-stu-id="f7858-119">To enable seamless signed message exchange between Windows 7 and any down-level operating system, the Administrator must add appropriate exceptions on the MSMQ machines.</span></span>

 

 



