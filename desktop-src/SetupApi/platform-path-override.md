---
description: Переопределение пути платформы
ms.assetid: f430fd9a-f865-4cdb-b0ea-4e6d79913308
title: Переопределение пути платформы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a9a6ae6795b444c44db91d90ecd93efd19ea9dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664619"
---
# <a name="platform-path-override"></a><span data-ttu-id="e9918-103">Переопределение пути платформы</span><span class="sxs-lookup"><span data-stu-id="e9918-103">Platform Path Override</span></span>

<span data-ttu-id="e9918-104">Функция [**сетупсетплатформпасоверриде**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetplatformpathoverridea) используется для задания переопределения пути платформы для целевого компьютера при работе с INF-файлами с другого компьютера.</span><span class="sxs-lookup"><span data-stu-id="e9918-104">The [**SetupSetPlatformPathOverride**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetplatformpathoverridea) function is used to set a platform path override for a target machine when working with INF files from a different machine.</span></span> <span data-ttu-id="e9918-105">Таким образом, он может ссылаться на другую платформу, отличную от той, на которой она выполняется в данный момент.</span><span class="sxs-lookup"><span data-stu-id="e9918-105">As such, it can refer to a different platform than the one it is currently running on.</span></span> <span data-ttu-id="e9918-106">Для работы с источниками мультимедиа он может ссылаться на платформы, которые больше не поддерживаются, например Alpha, MIPS и PPC.</span><span class="sxs-lookup"><span data-stu-id="e9918-106">For dealing with media sources, it can refer to platforms that are no longer supported, such as Alpha, MIPS, and PPC.</span></span> <span data-ttu-id="e9918-107">Он удаляет переопределение пути платформы, если не указано ни одного.</span><span class="sxs-lookup"><span data-stu-id="e9918-107">It removes the platform path override if none is specified.</span></span>

<span data-ttu-id="e9918-108">После того как переопределение пути платформы задается вызовом [**сетупсетплатформпасоверриде**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetplatformpathoverridea), любая функция установки, которая помещает в очередь операции копирования файлов, будет проверять окончательный компонент исходного пути.</span><span class="sxs-lookup"><span data-stu-id="e9918-108">After a platform path override is set by a call to [**SetupSetPlatformPathOverride**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetplatformpathoverridea), any setup function that queues file copy operations will examine the final component of the source path.</span></span> <span data-ttu-id="e9918-109">Если последний компонент соответствует имени платформы пользователя, функция установки заменит ее на строку переопределения, заданную параметром **сетупсетплатформпасоверриде**.</span><span class="sxs-lookup"><span data-stu-id="e9918-109">If the final component matches the name of the user's platform, the setup function will replace it with the override string set by **SetupSetPlatformPathOverride**.</span></span>

<span data-ttu-id="e9918-110">Например, при установке драйверов принтеров на сервер MIPS может потребоваться установить драйверы для всех поддерживаемых платформ.</span><span class="sxs-lookup"><span data-stu-id="e9918-110">For example, when installing printer drivers onto a MIPS server, you might want to install drivers for all supported platforms.</span></span> <span data-ttu-id="e9918-111">В очередь файлы обычно устанавливают файлы, указанные в разделах INF-файлов, зависящих от MIPS, с исходными путями, такими как \\ \\ \\ MIPS root source \\ .</span><span class="sxs-lookup"><span data-stu-id="e9918-111">Queuing the files normally would install the files specified in the MIPS-dependent sections of the INF file, with source paths such as \\\\root\\source\\mips.</span></span> <span data-ttu-id="e9918-112">Чтобы установить файлы для второй платформы, необходимо вызвать [**сетупсетплатформпасоверриде**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetplatformpathoverridea) с *переопределением* , указывающим на платформу замены.</span><span class="sxs-lookup"><span data-stu-id="e9918-112">To install the files for a second platform, you must call [**SetupSetPlatformPathOverride**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetplatformpathoverridea) with *Override* indicating the replacement platform.</span></span> <span data-ttu-id="e9918-113">Если расположение, указанное в параметре *override* , содержит строковое значение "Alpha", операции копирования файлов, отправляемые в очередь с исходным путем к \\ \\ корневому \\ источнику \\ MIPS, будут заменены исходными \\ \\ \\ исходными \\ .</span><span class="sxs-lookup"><span data-stu-id="e9918-113">If the location indicated by *Override* contains the string value "alpha", file copy operations sent to the queue with a source path of \\\\root\\source\\mips would have their source path changed to \\\\root\\source\\alpha.</span></span> <span data-ttu-id="e9918-114">Этот процесс будет повторен для каждой интересующей платформы.</span><span class="sxs-lookup"><span data-stu-id="e9918-114">You would repeat this process for each platform of interest.</span></span>

 

 



