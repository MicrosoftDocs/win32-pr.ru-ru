---
description: Если операция резервного копирования VSS выполняется без участия модуля записи, создание теневой копии может выполняться.
ms.assetid: 2058e894-bde5-4690-a7aa-849d2e9cdc71
title: Резервные копии без участия в записи
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b9a782fbcb9afe532f2f123151dc7998307157b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105651159"
---
# <a name="backups-without-writer-participation"></a><span data-ttu-id="17b47-103">Резервные копии без участия в записи</span><span class="sxs-lookup"><span data-stu-id="17b47-103">Backups without Writer Participation</span></span>

<span data-ttu-id="17b47-104">Если операция резервного копирования VSS выполняется без участия модуля записи, создание теневой копии может выполняться.</span><span class="sxs-lookup"><span data-stu-id="17b47-104">When a VSS backup operation is conducted without the involvement of a writer, the shadow copy creation can still occur.</span></span>

<span data-ttu-id="17b47-105">Как отмечалось в других местах (см. сведения о [состоянии теневого копирования по умолчанию](shadow-copies-and-shadow-copy-sets.md)), результат этого типа теневого копирования — это том, отражающий состояние диска на момент создания теневой копии. данные на тенев скопированном томе могут отражать незавершенные или частичные операции ввода-вывода, которые описаны как наблюдаются в [*состоянии, соответствующем сбоям*](vssgloss-c.md).</span><span class="sxs-lookup"><span data-stu-id="17b47-105">As noted elsewhere (see [Default Shadow Copy State](shadow-copies-and-shadow-copy-sets.md)), the result of this type of shadow copy is a volume reflecting the state of a disk at the time of the shadow copy: data on the shadow-copied volume may reflect incomplete or partial I/O operations and is described as being in a [*crash-consistent state*](vssgloss-c.md).</span></span>

<span data-ttu-id="17b47-106">Существует несколько ситуаций, в которых для работы с отказоустойчивыми теневыми скопированными данными потребуется приложение резервного копирования:</span><span class="sxs-lookup"><span data-stu-id="17b47-106">There are several situations that will require a backup application to work with crash consistent shadow copied data:</span></span>

-   <span data-ttu-id="17b47-107">**Управление данными осуществляется с помощью приложений, не поддерживающих VSS**</span><span class="sxs-lookup"><span data-stu-id="17b47-107">**Data is managed by VSS-unaware applications**</span></span>

    <span data-ttu-id="17b47-108">Почти каждая система будет иметь некоторые приложения — текстовые редакторы, средства чтения почты, текстовые процессоры и т. д., которые не знаются с помощью VSS, поэтому, скорее всего, необходимо считать, что некоторые данные в теневой копии будут рассматриваться как находящиеся в состоянии сбоя.</span><span class="sxs-lookup"><span data-stu-id="17b47-108">Almost every system will have some applications—text editors, mail readers, word processors, and so forth—that are VSS unaware, so it is always likely that some of the data on a shadow copy will need to be thought of as being in a crash consistent state.</span></span>

    <span data-ttu-id="17b47-109">Такой тип данных обычно не является критически важным для системы или службы, поэтому резервное копирование не должно быть проблематичным или по крайней мере более проблематичным, чем во время обычной архивации.</span><span class="sxs-lookup"><span data-stu-id="17b47-109">This sort of data is not typically system- or service-critical, so backing it up should not be problematic, or at least no more problematic than during a conventional backup.</span></span>

    <span data-ttu-id="17b47-110">Как и при подготовке к обычной резервной копии, если это возможно, операторы резервного копирования должны попытаться приостановить или завершить такие приложения перед запуском задания резервного копирования VSS.</span><span class="sxs-lookup"><span data-stu-id="17b47-110">As with preparations for conventional backups, if possible, backup operators should attempt to suspend or terminate such applications prior to starting a VSS backup job.</span></span>

-   <span data-ttu-id="17b47-111">**Система без модулей записи, совместимых с VSS**</span><span class="sxs-lookup"><span data-stu-id="17b47-111">**System with no VSS-compatible writers**</span></span>

    <span data-ttu-id="17b47-112">Такая ситуация может быть сравнительно редким, так как большинство систем, для которых может быть создана резервная копия с помощью приложения резервного копирования VSS, будут иметь версию Windows с поддержкой VSS, которая должна содержать модули записи.</span><span class="sxs-lookup"><span data-stu-id="17b47-112">This situation may be relatively rare because most systems that can be backed up by a VSS backup application will have a VSS-enabled version of Windows, which should contain writers.</span></span>

    <span data-ttu-id="17b47-113">Однако существуют определенные обстоятельства, при которых эта проблема может возникнуть, например, при резервном копировании системы без поддержки VSS, но система использует сетевое устройство с поддержкой VSS для своего хранилища.</span><span class="sxs-lookup"><span data-stu-id="17b47-113">However, there are certain circumstances where this problem could arise—for instance, if you are backing up a system without VSS support but the system uses a VSS-enabled networked appliance for its storage.</span></span>

    <span data-ttu-id="17b47-114">Несмотря на то, что резервное копирование состояния системы из отказоустойчивого образа не является оптимальным, может быть достаточно для перезагрузки компьютера в рабочее состояние.</span><span class="sxs-lookup"><span data-stu-id="17b47-114">Although backing up a system's state from a crash-consistent image is not optimal, it may be sufficient for a computer to reboot to an operational status.</span></span> <span data-ttu-id="17b47-115">Во многих случаях компьютер будет восстанавливаться после любых незавершенных операций ввода-вывода в файловых системах и будет работать нормально.</span><span class="sxs-lookup"><span data-stu-id="17b47-115">In many cases, the computer will recover from any incomplete I/O operations to the file systems and will operate normally.</span></span>

-   <span data-ttu-id="17b47-116">**Инициатор запроса, который выбрал не работать с модулями записи системы**</span><span class="sxs-lookup"><span data-stu-id="17b47-116">**A requester choosing not to work with the system writers**</span></span>

    <span data-ttu-id="17b47-117">Это может произойти, если инициатор запроса решил добавить компоненты модуля записи или отключить все модули записи.</span><span class="sxs-lookup"><span data-stu-id="17b47-117">This circumstance would occur if a requester chose to add no writer components, or disabling all writers.</span></span>

    <span data-ttu-id="17b47-118">Создание резервных копий таким способом обычно не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="17b47-118">Performing backups in this way is generally discouraged.</span></span> <span data-ttu-id="17b47-119">Хотя теневое копирование копируемого тома может быть достаточным для восстановления системы до ее выполнения, это нежелательно.</span><span class="sxs-lookup"><span data-stu-id="17b47-119">Although the shadow-copied volume to back up might be sufficient to restore a system to running, it is not desirable.</span></span> <span data-ttu-id="17b47-120">Фактически, учитывая, что модули записи, работающие в системе, спроектированы с учетом функциональности для взаимодействия с VSS и теневыми копиями, резервное копирование данных таким образом может привести к нестабильной работе.</span><span class="sxs-lookup"><span data-stu-id="17b47-120">In fact, given that the writers running on the system are designed with functionality to cooperate with VSS and shadow copies, backing up their data in this way might result in instability.</span></span>

 

 



