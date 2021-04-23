---
title: Службы BITS и восстановление системы
description: Не все версии BITS используют один и тот же формат для хранения заданий.
ms.assetid: 97c7fa69-1b35-445b-a0a1-b4d60c3ede42
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: e386084e7556b472c538308b8066875a4287a8d8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067514"
---
# <a name="bits-and-system-restore"></a><span data-ttu-id="00936-103">Службы BITS и восстановление системы</span><span class="sxs-lookup"><span data-stu-id="00936-103">BITS and System Restore</span></span>

<span data-ttu-id="00936-104">Не все версии BITS используют один и тот же формат для хранения заданий.</span><span class="sxs-lookup"><span data-stu-id="00936-104">Not all versions of BITS use the same format to store jobs.</span></span> <span data-ttu-id="00936-105">Если вы вернете компьютер к точке восстановления до обновления BITS, старая версия BITS не сможет считать текущие сведения о задании.</span><span class="sxs-lookup"><span data-stu-id="00936-105">If you return the computer to a restore point prior to a BITS upgrade, the old version of BITS may not be able to read the current job information.</span></span> <span data-ttu-id="00936-106">В этом случае служба BITS удалит список заданий и создаст новый список пустых заданий.</span><span class="sxs-lookup"><span data-stu-id="00936-106">If this happens, BITS will delete the jobs list and create a new empty jobs list.</span></span> <span data-ttu-id="00936-107">В результате временные файлы, связанные с списком предыдущих заданий, не очищаются; чтобы освободить место на диске, необходимо удалить файлы вручную.</span><span class="sxs-lookup"><span data-stu-id="00936-107">As a result, the temporary files associated with the previous jobs list are not cleaned up; to reclaim the disk space, you must delete the files manually.</span></span>

<span data-ttu-id="00936-108">Пользователи, знакомые с командной строкой Windows, могут избежать этой проблемы с помощью [средства битсадмин](bitsadmin-tool.md) , чтобы очистить список заданий BITS перед выполнением восстановления системы.</span><span class="sxs-lookup"><span data-stu-id="00936-108">Users familiar with the Windows command line can avoid this problem by using the [BITSAdmin tool](bitsadmin-tool.md) to clear the BITS jobs list before running System Restore.</span></span> <span data-ttu-id="00936-109">Чтобы очистить список заданий BITS, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="00936-109">To clear the BITS jobs list, run the following command:</span></span>

<span data-ttu-id="00936-110">**битсадмин/Reset/аллусерс**</span><span class="sxs-lookup"><span data-stu-id="00936-110">**bitsadmin /reset /allusers**</span></span>

<span data-ttu-id="00936-111">Обратите внимание, что для выполнения этой команды необходимы права администратора.</span><span class="sxs-lookup"><span data-stu-id="00936-111">Note that you must have administrator privileges to run this command.</span></span>

 

 




