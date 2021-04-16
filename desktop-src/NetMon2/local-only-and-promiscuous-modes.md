---
description: Мониторы могут проверять кадры в режиме "только локальный режим" или в неизбирательном режиме.
ms.assetid: 4646f5bb-e3e3-4929-91b7-f68c5b70ccb3
title: Local-Only и неизбирательные режимы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd1188760d8de31836de3fbd437854a5df138402
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662452"
---
# <a name="local-only-and-promiscuous-modes"></a><span data-ttu-id="edc98-103">Local-Only и неизбирательные режимы</span><span class="sxs-lookup"><span data-stu-id="edc98-103">Local-Only and Promiscuous Modes</span></span>

<span data-ttu-id="edc98-104">Мониторы могут проверять кадры в режиме "только локальный режим" или в неизбирательном режиме.</span><span class="sxs-lookup"><span data-stu-id="edc98-104">Monitors can examine frames in local-only mode or promiscuous mode.</span></span>

<span data-ttu-id="edc98-105">В режиме "только локальная" поставщик сетевых пакетов (НПП) возвращает кадры, которые отправляются на компьютер, на котором выполняется монитор, и на него, включая широковещательные и многоадресные рассылки, направляемые на локальный компьютер.</span><span class="sxs-lookup"><span data-stu-id="edc98-105">In local-only mode, the network packet provider (NPP) returns frames that are sent to or from the computer on which the monitor is running, including broadcasts and multicasts directed to the local machine.</span></span> <span data-ttu-id="edc98-106">Несмотря на то, что ограничено локально направляемыми кадрами, локальный режим также значительно снижает нагрузку на процессор.</span><span class="sxs-lookup"><span data-stu-id="edc98-106">Although limited to locally directed frames, local-mode is also much less processor intensive.</span></span>

<span data-ttu-id="edc98-107">В неизбирательном режиме монитор также может отслеживать трафик, который не направляется на локальный компьютер или с него.</span><span class="sxs-lookup"><span data-stu-id="edc98-107">In promiscuous mode, the monitor can also watch for traffic that is not directed to or from the local computer.</span></span> <span data-ttu-id="edc98-108">Если монитор не указал флаг, то \_ \_ \_ \_ в функции [онлоадингдлл](onloadingdll.md) для службы управления монитором (мксвк) предполагается, что для монитора требуется неизбирательный режим, когда он загружает библиотеку DLL монитора, а пмоде не требуется.</span><span class="sxs-lookup"><span data-stu-id="edc98-108">Unless the monitor has specified the flag, MCS\_CREATE\_PMODE\_NOT\_REQUIRED, in the [OnLoadingDLL](onloadingdll.md) function, the Monitor Control Service (MCSVC) assumes that the monitor requires promiscuous mode when it loads the monitor DLL.</span></span>

 

 



