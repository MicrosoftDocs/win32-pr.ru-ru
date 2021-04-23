---
title: Преимущества использования SIS
description: Ниже приведены преимущества использования SIS и архитектуры резервного копирования SIS.
ms.assetid: c72a14a1-92ae-4875-ae73-e277ed2b0c0d
keywords:
- Резервное копирование хранилища единственных экземпляров (SIS), преимущества
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcd1856ce54e817c25830f15f133c7d76c6a80fc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067429"
---
# <a name="advantages-of-using-sis"></a><span data-ttu-id="c40ae-104">Преимущества использования SIS</span><span class="sxs-lookup"><span data-stu-id="c40ae-104">Advantages of Using SIS</span></span>

<span data-ttu-id="c40ae-105">Ниже приведены преимущества использования SIS и архитектуры резервного копирования SIS.</span><span class="sxs-lookup"><span data-stu-id="c40ae-105">The advantages of using SIS and the SIS backup architecture are the following:</span></span>

-   <span data-ttu-id="c40ae-106">Подключения между SIS и резервными файлами автоматически обслуживаются архитектурой SIS, так как приложения резервного копирования вызывают функции API резервного копирования SIS.</span><span class="sxs-lookup"><span data-stu-id="c40ae-106">The connections between the SIS links and the backing files are automatically maintained by the SIS architecture as your backup applications call the SIS backup API functions.</span></span>
-   <span data-ttu-id="c40ae-107">Содержимое точек повторного анализа SIS непрозрачно для приложений резервного копирования и восстановления, что гарантирует, что обновления для внутренних компонентов SIS не потребует изменения в API-интерфейсе SIS или в приложениях резервного копирования и восстановления, вызывающих функции API-интерфейса SIS.</span><span class="sxs-lookup"><span data-stu-id="c40ae-107">The contents of the SIS reparse points are opaque to your backup and restore applications, ensuring that upgrades to the SIS internals will not require a change in the SIS API or your backup and restore applications that call SIS API functions.</span></span> <span data-ttu-id="c40ae-108">Необходимо только перекомпилировать приложение с помощью новой версии библиотеки DLL SIS с именем Sisbkup.dll.</span><span class="sxs-lookup"><span data-stu-id="c40ae-108">You need only recompile your application with a new version of the SIS DLL, named Sisbkup.dll.</span></span>
-   <span data-ttu-id="c40ae-109">Так как хранилище единственных копий реализовано как драйвер фильтра файловой системы, он постоянно отслеживает соединения между SIS-ссылками и резервными файлами.</span><span class="sxs-lookup"><span data-stu-id="c40ae-109">Because SIS is implemented as a file system filter driver, it constantly tracks the connections between the SIS links and the backing files.</span></span> <span data-ttu-id="c40ae-110">При резервном копировании и восстановлении файлов хранилище единственных копий гарантирует, что резервное копирование и восстановление выполняется только для одного экземпляра резервного файла, независимо от числа ссылок на SIS, которые указывают на него.</span><span class="sxs-lookup"><span data-stu-id="c40ae-110">When the files are backed up and restored, SIS backup ensures that only one instance of the backing file will be backed up and restored, regardless of the number of SIS links that point to it.</span></span>

 

 




