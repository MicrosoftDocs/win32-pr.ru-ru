---
description: Следующие административные функции позволяют поставщику сети принимать действия, связанные с сетью, для отображения сетевых каталогов и управления ими, иными словами, каталоги, сопоставленные с протоколами, не связанными с Windows.
ms.assetid: df2f1bd6-5257-46e4-a4d4-ad2f5c0a1517
title: Административные функции
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b83cb5b7c515fe8e22dc5542a4d29e54e8b01329
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105651052"
---
# <a name="administrative-functions"></a><span data-ttu-id="38a65-103">Административные функции</span><span class="sxs-lookup"><span data-stu-id="38a65-103">Administrative Functions</span></span>

<span data-ttu-id="38a65-104">Следующие административные функции позволяют поставщику сети принимать действия, связанные с сетью, для отображения сетевых каталогов и управления ими, иными словами, каталоги, сопоставленные с протоколами, не связанными с Windows.</span><span class="sxs-lookup"><span data-stu-id="38a65-104">The following administrative functions enable a network provider to take network-specific action to display and manipulate network-specific directories, in other words, directories mapped to non-Windows protocols.</span></span>



| <span data-ttu-id="38a65-105">Функция</span><span class="sxs-lookup"><span data-stu-id="38a65-105">Function</span></span>                                         | <span data-ttu-id="38a65-106">Описание</span><span class="sxs-lookup"><span data-stu-id="38a65-106">Description</span></span>                                                                                                                                                   |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="38a65-107">**нпжетдиректоритипе**</span><span class="sxs-lookup"><span data-stu-id="38a65-107">**NPGetDirectoryType**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npgetdirectorytype) | <span data-ttu-id="38a65-108">Вызывается диспетчером файлов для определения типа сетевого каталога.</span><span class="sxs-lookup"><span data-stu-id="38a65-108">Called by File Manager to determine the type of a network directory.</span></span>                                                                                          |
| [<span data-ttu-id="38a65-109">**нпдиректоринотифи**</span><span class="sxs-lookup"><span data-stu-id="38a65-109">**NPDirectoryNotify**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npdirectorynotify)   | <span data-ttu-id="38a65-110">Вызывается диспетчером файлов для уведомления поставщика сети об операциях с каталогом.</span><span class="sxs-lookup"><span data-stu-id="38a65-110">Called by File Manager to notify the network provider of directory operations.</span></span> <span data-ttu-id="38a65-111">Эта функция может использоваться для выполнения специального поведения определенных каталогов.</span><span class="sxs-lookup"><span data-stu-id="38a65-111">This function can be used to perform special behavior for certain directories.</span></span> |



 

 

 



