---
description: Встроенные преобразования хранятся в файле MSI пакета. Это гарантирует, что преобразование всегда доступно для пользователей, если пакет установки доступен. Кроме того, преобразования могут предоставляться пользователям в виде автономных файлов MST.
ms.assetid: f7b265df-4b34-44ea-85ab-8dbca4797517
title: Встроенные преобразования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 301e7f188da1a46411636ef90b7e6ae327a06c22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104080918"
---
# <a name="embedded-transforms"></a><span data-ttu-id="d9f52-105">Встроенные преобразования</span><span class="sxs-lookup"><span data-stu-id="d9f52-105">Embedded Transforms</span></span>

<span data-ttu-id="d9f52-106">Встроенные преобразования хранятся в файле MSI пакета.</span><span class="sxs-lookup"><span data-stu-id="d9f52-106">Embedded transforms are stored inside the .msi file of the package.</span></span> <span data-ttu-id="d9f52-107">Это гарантирует, что преобразование всегда доступно для пользователей, если пакет установки доступен.</span><span class="sxs-lookup"><span data-stu-id="d9f52-107">This guarantees to users that the transform is always available when the installation package is available.</span></span> <span data-ttu-id="d9f52-108">Кроме того, преобразования могут предоставляться пользователям в виде автономных файлов MST.</span><span class="sxs-lookup"><span data-stu-id="d9f52-108">Alternatively, transforms may be provided to users as standalone .mst files.</span></span>

<span data-ttu-id="d9f52-109">Чтобы добавить встроенное преобразование в список преобразования, добавьте двоеточие (:) в качестве префикса к имени файла.</span><span class="sxs-lookup"><span data-stu-id="d9f52-109">To add an embedded transform to the transforms list, add a colon (:) prefix to the file name.</span></span> <span data-ttu-id="d9f52-110">Поскольку установщик всегда может получить преобразование из хранилища в MSI-файле, встроенные преобразования не кэшируются на компьютере пользователя.</span><span class="sxs-lookup"><span data-stu-id="d9f52-110">Because the installer can always obtain the transform from storage in the .msi file, embedded transforms are not cached on the user's computer.</span></span> <span data-ttu-id="d9f52-111">Встроенные преобразования могут использоваться в сочетании с [защищенными преобразованиями](secured-transforms.md) или [незащищенными](unsecured-transforms.md)преобразованиями.</span><span class="sxs-lookup"><span data-stu-id="d9f52-111">Embedded transforms may be used in combination with [secured transforms](secured-transforms.md) or [unsecured transforms](unsecured-transforms.md).</span></span> <span data-ttu-id="d9f52-112">Дополнительные сведения см. в разделе [применение преобразований](applying-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="d9f52-112">For more information, see [Applying Transforms](applying-transforms.md).</span></span>

 

 



