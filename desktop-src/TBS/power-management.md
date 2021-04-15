---
title: Управление питанием (базовые службы TPM)
description: TBS получает события управления питанием.
ms.assetid: 21f76bea-a313-46b7-99b3-422f17376a5a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71e21f2c6a2292b7d49fae3b15691703fa34667a
ms.sourcegitcommit: 8ea1a82717bd3dbb3457be0697329aa37fb13f08
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2019
ms.locfileid: "105661677"
---
# <a name="power-management-tpm-base-services"></a><span data-ttu-id="59b3d-103">Управление питанием (базовые службы TPM)</span><span class="sxs-lookup"><span data-stu-id="59b3d-103">Power Management (TPM Base Services)</span></span>

<span data-ttu-id="59b3d-104">TBS получает события управления питанием.</span><span class="sxs-lookup"><span data-stu-id="59b3d-104">The TBS receives power management events.</span></span> <span data-ttu-id="59b3d-105">При получении свидетельства о том, что доверенный платформенный модуль или другие части платформы собирается войти в состояние электропитания, при котором выполнение будет прервано или состояние доверенного платформенного модуля будет потеряно, TBS проверяет, может ли выполнение выполняемой в данный момент команды завершиться, прежде чем система выдаст питание.</span><span class="sxs-lookup"><span data-stu-id="59b3d-105">When an indication is received that the TPM or other parts of the platform are about to enter a power state in which execution will be interrupted or TPM state will be lost, the TBS checks to determine whether the currently executing command is likely to finish before the system powers down.</span></span> <span data-ttu-id="59b3d-106">Как правило, TBS позволяет выполнять команды короткой и средней длительности, но отменяет команды длительной длительности.</span><span class="sxs-lookup"><span data-stu-id="59b3d-106">In general, the TBS allows short and medium duration commands to finish, but cancels long duration commands.</span></span> <span data-ttu-id="59b3d-107">После возврата команды TBS перестает отправлять новые команды доверенному платформенному модулю и готовится к переходу в спящий режим.</span><span class="sxs-lookup"><span data-stu-id="59b3d-107">After the command has returned, the TBS stops sending new commands to the TPM and prepares itself for hibernation.</span></span> <span data-ttu-id="59b3d-108">После восстановления питания TBS возвращает результат команды вызывающему объекту, а затем продолжает обработку ожидающих команд TBS.</span><span class="sxs-lookup"><span data-stu-id="59b3d-108">When power is restored, the TBS returns the result of the command to the caller, and then proceeds with processing pending TBS commands.</span></span> <span data-ttu-id="59b3d-109">Код управления питанием TBS выполняется асинхронно, поэтому он может обрабатывать запросы управления питанием даже в случае, если доверенный платформенный модуль обрабатывает длинную команду.</span><span class="sxs-lookup"><span data-stu-id="59b3d-109">The TBS power management code runs asynchronously, so it can handle power management requests even if the TPM is processing a long command.</span></span>

<span data-ttu-id="59b3d-110">Когда компьютер переходит в состояние сна, включая S3 (спящий режим) и S4 (спящий режим), доверенный платформенный модуль выключен.</span><span class="sxs-lookup"><span data-stu-id="59b3d-110">When a computer enters sleep states, including S3 (sleep) and S4 (hibernation), the TPM is powered off.</span></span> <span data-ttu-id="59b3d-111">Поэтому все неустойчивые состояния TPM теряются.</span><span class="sxs-lookup"><span data-stu-id="59b3d-111">Thus, all nonpersistent TPM states are lost.</span></span> <span data-ttu-id="59b3d-112">Перед вводом этих состояний Ожидается, что программное обеспечение приложения готовится к утрате временных состояний доверенного платформенного модуля.</span><span class="sxs-lookup"><span data-stu-id="59b3d-112">Before entering these states, application software is expected to prepare for the loss of volatile TPM states.</span></span> <span data-ttu-id="59b3d-113">Когда система возвращается из состояния сна, TBS синхронизируется с доверенным платформенным модулем, чтобы состояние TBS соответствовало состоянию доверенного платформенного модуля.</span><span class="sxs-lookup"><span data-stu-id="59b3d-113">When the system returns from a sleep state, the TBS synchronizes with the TPM so that the TBS state is consistent with the TPM state.</span></span> <span data-ttu-id="59b3d-114">Программному обеспечению может потребоваться повторное выдача команд, которые были прерваны.</span><span class="sxs-lookup"><span data-stu-id="59b3d-114">Application software may need to reissue commands that were interrupted.</span></span>

 

 




