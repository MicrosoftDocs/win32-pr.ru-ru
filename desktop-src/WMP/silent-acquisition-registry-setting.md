---
title: Параметр реестра для автоматического приобретения
description: Параметр реестра для автоматического приобретения
ms.assetid: 50e0b27e-ddf8-441f-adcd-d88d36f3edaf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a00bbb6d930cb137ed12ffbcb05af31cee3c99c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700632"
---
# <a name="silent-acquisition-registry-setting"></a><span data-ttu-id="d11dd-103">Параметр реестра для автоматического приобретения</span><span class="sxs-lookup"><span data-stu-id="d11dd-103">Silent Acquisition Registry Setting</span></span>

<span data-ttu-id="d11dd-104">Проигрыватель Microsoft Windows Media использует следующее значение реестра, чтобы определить, следует ли включить автоматическое получение, когда проигрыватель загружает права на использование автоматически, когда пользователь воспроизводит или синхронизирует защищенное содержимое.</span><span class="sxs-lookup"><span data-stu-id="d11dd-104">Microsoft Windows Media Player uses the following registry value to determine whether to enable silent acquisition, a state in which the player downloads usage rights automatically when the user plays or syncs protected content.</span></span>

<span data-ttu-id="d11dd-105">**HKey \_ \_** \\ **Программное обеспечение** локального компьютера \\ **Microsoft** \\ **MediaPlayer** \\ **предпочтения** \\ **силентаккуиситион**</span><span class="sxs-lookup"><span data-stu-id="d11dd-105">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**MediaPlayer**\\**Preferences**\\**SilentAcquisition**</span></span>

<span data-ttu-id="d11dd-106">Значение Силентаккуиситион имеет следующую форму:</span><span class="sxs-lookup"><span data-stu-id="d11dd-106">The SilentAcquisition value has the following form:</span></span>



| <span data-ttu-id="d11dd-107">Имя</span><span class="sxs-lookup"><span data-stu-id="d11dd-107">Name</span></span>              | <span data-ttu-id="d11dd-108">Тип</span><span class="sxs-lookup"><span data-stu-id="d11dd-108">Type</span></span>           | <span data-ttu-id="d11dd-109">Описание</span><span class="sxs-lookup"><span data-stu-id="d11dd-109">Description</span></span>                                                                                                       |
|-------------------|----------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d11dd-110">силентаккуиситион</span><span class="sxs-lookup"><span data-stu-id="d11dd-110">SilentAcquisition</span></span> | <span data-ttu-id="d11dd-111">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="d11dd-111">**REG\_DWORD**</span></span> | <span data-ttu-id="d11dd-112">Задайте для этого параметра значение 1, чтобы включить автоматическое получение, или задайте для него значение 0, чтобы отключить автоматическое получение.</span><span class="sxs-lookup"><span data-stu-id="d11dd-112">Set this value to 1 to enable silent acquisition, or set it to 0 to disable silent acquisition.</span></span> <span data-ttu-id="d11dd-113">Значение по умолчанию — 1.</span><span class="sxs-lookup"><span data-stu-id="d11dd-113">The default is 1.</span></span> |



 

<span data-ttu-id="d11dd-114">Чтобы указать значение, пользователь может запустить проигрыватель Windows Media, открыть диалоговое окно **Параметры** , перейти на вкладку **Конфиденциальность** и установить или снять флажок **загружать права на использование при воспроизведении или синхронизации файла** .</span><span class="sxs-lookup"><span data-stu-id="d11dd-114">To specify a value, the user can start Windows Media Player, open the **Options** dialog box, click the **Privacy** tab, and then select or clear the **Download usage rights automatically when I play or sync a file** check box.</span></span> <span data-ttu-id="d11dd-115">Установка этого флажка устанавливает значение Силентаккуиситион равным 1; Если снять этот флажок, он установится в значение 0.</span><span class="sxs-lookup"><span data-stu-id="d11dd-115">Selecting this check box sets SilentAcquisition to 1; clearing the check box sets it to 0.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d11dd-116">См. также</span><span class="sxs-lookup"><span data-stu-id="d11dd-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d11dd-117">**Параметры реестра**</span><span class="sxs-lookup"><span data-stu-id="d11dd-117">**Registry Settings**</span></span>](registry-settings.md)
</dt> </dl>

 

 




