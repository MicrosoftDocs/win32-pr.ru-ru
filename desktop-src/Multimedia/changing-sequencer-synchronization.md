---
title: Изменение синхронизации Sequencer
description: Изменение синхронизации Sequencer
ms.assetid: 5c3acb47-e6cc-4957-a306-7039ec110827
keywords:
- Сообщение команды MCI_SET
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bffdc1606624f63fa05a9cc03c68fe64781620f
ms.sourcegitcommit: 8276af9231bdbf5a7334299f0d13fc8ff069a065
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/12/2021
ms.locfileid: "105651226"
---
# <a name="changing-sequencer-synchronization"></a><span data-ttu-id="a8b03-104">Изменение синхронизации Sequencer</span><span class="sxs-lookup"><span data-stu-id="a8b03-104">Changing Sequencer Synchronization</span></span>

> [!NOTE]
> <span data-ttu-id="a8b03-105">Обмен данными без смещения — Корпорация Майкрософт поддерживает различные и включенные среды.</span><span class="sxs-lookup"><span data-stu-id="a8b03-105">Bias-free Communication Microsoft supports a diverse and inclusionary environment.</span></span>  <span data-ttu-id="a8b03-106">В этом документе есть ссылки на слово "Slave".</span><span class="sxs-lookup"><span data-stu-id="a8b03-106">Within this document, there are references to the word 'slave.'</span></span> <span data-ttu-id="a8b03-107">В соответствии с руководством корпорации Майкрософт в [стиле Bias-Freeного обмена данными](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) это слово является исключаемым.</span><span class="sxs-lookup"><span data-stu-id="a8b03-107">Microsoft's [Style Guide for Bias-Free Communications](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) recognizes this as an exclusionary word.</span></span>  <span data-ttu-id="a8b03-108">Эта формулировка используется в том виде, в котором в настоящее время используется в программном обеспечении.</span><span class="sxs-lookup"><span data-stu-id="a8b03-108">This wording is used as it is currently the wording used within the software.</span></span> <span data-ttu-id="a8b03-109">Для обеспечения согласованности этот документ содержит это слово.</span><span class="sxs-lookup"><span data-stu-id="a8b03-109">For consistency, this document contains this word.</span></span> <span data-ttu-id="a8b03-110">При удалении этого слова из программного обеспечения мы будем исправлять этот документ для выравнивания.</span><span class="sxs-lookup"><span data-stu-id="a8b03-110">When this word is removed from the software, we will correct this document to be in alignment.</span></span>

<span data-ttu-id="a8b03-111">Чтобы изменить режим синхронизации устройства Sequencer, используйте командное сообщение [**MCI \_ Set**](mci-set.md) с MCI \_ Seq \_ Set \_ master и MCI \_ Seq \_ Set \_ Slave.</span><span class="sxs-lookup"><span data-stu-id="a8b03-111">To change the synchronization mode of a sequencer device, use the [**MCI\_SET**](mci-set.md) command message with the MCI\_SEQ\_SET\_MASTER and MCI\_SEQ\_SET\_SLAVE flags.</span></span> <span data-ttu-id="a8b03-112">Два элемента в элементе [**MCI \_ Seq \_ Set \_ пармс**](mci-seq-set-parms.md) Structure, **двмастер** и **двславе** используются для указания главных и подчиненных режимов синхронизации.</span><span class="sxs-lookup"><span data-stu-id="a8b03-112">Two members in the [**MCI\_SEQ\_SET\_PARMS**](mci-seq-set-parms.md) structure, **dwMaster** and **dwSlave**, are used to specify the master and subordinate synchronization modes.</span></span>

<span data-ttu-id="a8b03-113">Главный режим синхронизации управляет данными синхронизации, отправленными секвенсором, в порт вывода.</span><span class="sxs-lookup"><span data-stu-id="a8b03-113">The master synchronization mode controls synchronization information sent by the sequencer to an output port.</span></span> <span data-ttu-id="a8b03-114">Ниже приведены константы для элемента **двмастер** и их соответствующие режимы синхронизации с главной.</span><span class="sxs-lookup"><span data-stu-id="a8b03-114">Following are the constants for the **dwMaster** member and their corresponding master synchronization modes.</span></span>



| <span data-ttu-id="a8b03-115">Константа</span><span class="sxs-lookup"><span data-stu-id="a8b03-115">Constant</span></span>        | <span data-ttu-id="a8b03-116">Режим синхронизации</span><span class="sxs-lookup"><span data-stu-id="a8b03-116">Synchronization mode</span></span>                                                                             |
|-----------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8b03-117">MCI \_ Seq \_ MIDI</span><span class="sxs-lookup"><span data-stu-id="a8b03-117">MCI\_SEQ\_MIDI</span></span>  | <span data-ttu-id="a8b03-118">Синхронизация MIDI.</span><span class="sxs-lookup"><span data-stu-id="a8b03-118">MIDI Synchronization.</span></span> <span data-ttu-id="a8b03-119">Отправка сведений о времени на выходной порт с помощью сообщений о времени MIDI.</span><span class="sxs-lookup"><span data-stu-id="a8b03-119">Send timing information to output port using MIDI timing clock messages.</span></span>   |
| <span data-ttu-id="a8b03-120">MCI \_ Seq \_ SMPTE</span><span class="sxs-lookup"><span data-stu-id="a8b03-120">MCI\_SEQ\_SMPTE</span></span> | <span data-ttu-id="a8b03-121">Синхронизация SMPTE.</span><span class="sxs-lookup"><span data-stu-id="a8b03-121">SMPTE Synchronization.</span></span> <span data-ttu-id="a8b03-122">Отправка сведений о времени на выходной порт с помощью сообщений MIDI четвертого кадра.</span><span class="sxs-lookup"><span data-stu-id="a8b03-122">Send timing information to output port using MIDI quarter-frame messages.</span></span> |
| <span data-ttu-id="a8b03-123">MCI \_ Seq \_ нет</span><span class="sxs-lookup"><span data-stu-id="a8b03-123">MCI\_SEQ\_NONE</span></span>  | <span data-ttu-id="a8b03-124">Без синхронизации.</span><span class="sxs-lookup"><span data-stu-id="a8b03-124">No Synchronization.</span></span> <span data-ttu-id="a8b03-125">Не отправляйте сведения о времени.</span><span class="sxs-lookup"><span data-stu-id="a8b03-125">Send no timing information.</span></span>                                                  |



 

<span data-ttu-id="a8b03-126">Подчиненный режим синхронизации управляет тем, где секвенсор получает сведения о времени для воспроизведения файла MIDI.</span><span class="sxs-lookup"><span data-stu-id="a8b03-126">The subordinate synchronization mode controls where the sequencer gets its timing information to play a MIDI file.</span></span> <span data-ttu-id="a8b03-127">Ниже приведены константы для элемента **двславе** и соответствующие режимы их подчиненного режима синхронизации.</span><span class="sxs-lookup"><span data-stu-id="a8b03-127">Following are the constants for the **dwSlave** member and their corresponding subordinate synchronization modes.</span></span>



| <span data-ttu-id="a8b03-128">Константа</span><span class="sxs-lookup"><span data-stu-id="a8b03-128">Constant</span></span>        | <span data-ttu-id="a8b03-129">Режим синхронизации</span><span class="sxs-lookup"><span data-stu-id="a8b03-129">Synchronization mode</span></span>                                                                                                                               |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8b03-130">\_файл MCI Seq \_</span><span class="sxs-lookup"><span data-stu-id="a8b03-130">MCI\_SEQ\_FILE</span></span>  | <span data-ttu-id="a8b03-131">Синхронизация файлов.</span><span class="sxs-lookup"><span data-stu-id="a8b03-131">File Synchronization.</span></span> <span data-ttu-id="a8b03-132">Получение сведений о времени из файла MIDI.</span><span class="sxs-lookup"><span data-stu-id="a8b03-132">Get timing information from MIDI file.</span></span>                                                                                       |
| <span data-ttu-id="a8b03-133">MCI \_ Seq \_ MIDI</span><span class="sxs-lookup"><span data-stu-id="a8b03-133">MCI\_SEQ\_MIDI</span></span>  | <span data-ttu-id="a8b03-134">Синхронизация MIDI.</span><span class="sxs-lookup"><span data-stu-id="a8b03-134">MIDI Synchronization.</span></span> <span data-ttu-id="a8b03-135">Получение сведений о времени из входного порта с помощью сообщений о времени MIDI.</span><span class="sxs-lookup"><span data-stu-id="a8b03-135">Get timing information from input port using MIDI timing clock messages.</span></span>                                                     |
| <span data-ttu-id="a8b03-136">MCI \_ Seq \_ SMPTE</span><span class="sxs-lookup"><span data-stu-id="a8b03-136">MCI\_SEQ\_SMPTE</span></span> | <span data-ttu-id="a8b03-137">Синхронизация SMPTE.</span><span class="sxs-lookup"><span data-stu-id="a8b03-137">SMPTE Synchronization.</span></span> <span data-ttu-id="a8b03-138">Получение сведений о времени из входного порта с помощью сообщений MIDI четвертого кадра.</span><span class="sxs-lookup"><span data-stu-id="a8b03-138">Get timing information from input port using MIDI quarter-frame messages.</span></span>                                                   |
| <span data-ttu-id="a8b03-139">MCI \_ Seq \_ нет</span><span class="sxs-lookup"><span data-stu-id="a8b03-139">MCI\_SEQ\_NONE</span></span>  | <span data-ttu-id="a8b03-140">Без синхронизации.</span><span class="sxs-lookup"><span data-stu-id="a8b03-140">No Synchronization.</span></span> <span data-ttu-id="a8b03-141">Получение сведений о времени только из команд MCI и игнорирование сведений о времени (например, темп изменений), которые находятся в файле MIDI.</span><span class="sxs-lookup"><span data-stu-id="a8b03-141">Get timing information from MCI commands only and ignore timing information (such as tempo changes) that are in the MIDI file.</span></span> |



 

> [!Note]  
> <span data-ttu-id="a8b03-142">В настоящее время для главной синхронизации секвенсор MIDI MCI поддерживает только режим без синхронизации (MCI \_ Seq \_ None).</span><span class="sxs-lookup"><span data-stu-id="a8b03-142">Currently, for master synchronization, the MCI MIDI sequencer supports only the No Synchronization mode (MCI\_SEQ\_NONE).</span></span> <span data-ttu-id="a8b03-143">Для подчиненной синхронизации он поддерживает только режим синхронизации файлов (файл MCI \_ Seq \_ ) и режим без синхронизации (MCI \_ Seq \_ None).</span><span class="sxs-lookup"><span data-stu-id="a8b03-143">For subordinate synchronization, it supports only the File Synchronization mode (MCI\_SEQ\_FILE) and the No Synchronization mode (MCI\_SEQ\_NONE).</span></span>

 

 

 




