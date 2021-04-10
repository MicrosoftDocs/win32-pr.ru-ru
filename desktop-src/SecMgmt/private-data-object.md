---
description: В каждой системе доступно ограниченное количество частных объектов данных для хранения информации в защищенном зашифрованном виде.
ms.assetid: 927473d7-b5bc-4b6f-b303-8a0f8680731d
title: Закрытый объект данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccacd1334c9859495acf89075b77a0f10af4cb64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144443"
---
# <a name="private-data-object"></a><span data-ttu-id="238f8-103">Закрытый объект данных</span><span class="sxs-lookup"><span data-stu-id="238f8-103">Private Data Object</span></span>

<span data-ttu-id="238f8-104">В каждой системе доступно ограниченное количество частных объектов данных для хранения информации в защищенном зашифрованном виде.</span><span class="sxs-lookup"><span data-stu-id="238f8-104">A limited number of private data objects are available on each system for the purpose of storing information in a protected, encrypted, fashion.</span></span>

<span data-ttu-id="238f8-105">Закрытые объекты данных предоставляются в основном для поддержки хранения паролей учетных записей сервера.</span><span class="sxs-lookup"><span data-stu-id="238f8-105">Private data objects are provided primarily to support storage of server account passwords.</span></span> <span data-ttu-id="238f8-106">Это полезно для серверов, работающих в определенной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="238f8-106">This is useful for servers that run in a specific account.</span></span> <span data-ttu-id="238f8-107">Пароль учетной записи сервера — это частные данные, которые должны быть защищены, но необходимы для регистрации сервера.</span><span class="sxs-lookup"><span data-stu-id="238f8-107">The password of the server account is private data that should be secured but is needed to log the server on.</span></span>

<span data-ttu-id="238f8-108">Закрытые объекты данных могут быть общими, или они могут иметь один из трех специализированных типов: локальный, глобальный и компьютер.</span><span class="sxs-lookup"><span data-stu-id="238f8-108">Private data objects may be general purpose, or they may be one of three specialized types: local, global, and machine.</span></span>

<span data-ttu-id="238f8-109">Локальные частные объекты данных можно считывать только локально с компьютера, на котором хранится объект.</span><span class="sxs-lookup"><span data-stu-id="238f8-109">Local private data objects can only be read locally from the computer storing the object.</span></span> <span data-ttu-id="238f8-110">Попытка удаленной чтения приводит \_ к \_ ошибке "доступ запрещен".</span><span class="sxs-lookup"><span data-stu-id="238f8-110">Attempting to read them remotely results in a STATUS\_ACCESS\_DENIED error.</span></span> <span data-ttu-id="238f8-111">Локальные закрытые объекты данных содержат имена ключей, которые начинаются с префикса "L $".</span><span class="sxs-lookup"><span data-stu-id="238f8-111">Local private data objects have key names that begin with the prefix "L$".</span></span> <span data-ttu-id="238f8-112">Помимо создаваемых локальных закрытых объектов, операционная система определяет следующие локальные закрытые объекты: $machine. ACC, SAC, Саи и САНСК.</span><span class="sxs-lookup"><span data-stu-id="238f8-112">In addition to the local private objects you create, the operating system defines the following local private objects: $machine.acc, SAC, SAI, and SANSC.</span></span>

<span data-ttu-id="238f8-113">Глобальные частные объекты данных являются глобальными в том смысле, что если они созданы на контроллере домена, они будут автоматически реплицированы на все контроллеры домена в этом домене.</span><span class="sxs-lookup"><span data-stu-id="238f8-113">Global private data objects are global in the sense that if they are created on a domain controller, they will be automatically replicated to all domain controllers in that domain.</span></span> <span data-ttu-id="238f8-114">Иными словами, каждый контроллер домена в этом домене будет иметь доступ к значениям, содержащимся в глобальном частном объекте данных.</span><span class="sxs-lookup"><span data-stu-id="238f8-114">In other words, each domain controller in that domain will have access to the values the global private data object contains.</span></span> <span data-ttu-id="238f8-115">В отличие от этого, глобальные закрытые объекты данных, созданные в системе, которая не является контроллером домена, а также неглобальными закрытыми объектами данных, не реплицируются.</span><span class="sxs-lookup"><span data-stu-id="238f8-115">In contrast, global private data objects created on a system that is not a domain controller, as well as nonglobal private data objects, are not replicated.</span></span> <span data-ttu-id="238f8-116">Глобальные частные объекты данных содержат имена ключей, начинающиеся с "G $".</span><span class="sxs-lookup"><span data-stu-id="238f8-116">Global private data objects have key names beginning with "G$".</span></span>

<span data-ttu-id="238f8-117">Закрытые объекты данных компьютера доступны только операционной системе.</span><span class="sxs-lookup"><span data-stu-id="238f8-117">Machine private data objects can be accessed only by the operating system.</span></span> <span data-ttu-id="238f8-118">Эти объекты имеют имена ключей, которые начинаются с "M $".</span><span class="sxs-lookup"><span data-stu-id="238f8-118">These objects have key names that begin with "M$".</span></span>

<span data-ttu-id="238f8-119">**Примечание**  .  Вы можете задать, но не можете получать, объекты частных данных компьютера.</span><span class="sxs-lookup"><span data-stu-id="238f8-119">**Note**  You can set, but you cannot retrieve, machine private data objects.</span></span>

<span data-ttu-id="238f8-120">Помимо этих префиксов, следующие значения также указывают на локальные или машинные объекты.</span><span class="sxs-lookup"><span data-stu-id="238f8-120">In addition to these prefixes, the following values also indicate local or machine objects.</span></span> <span data-ttu-id="238f8-121">Эти значения поддерживаются для обеспечения обратной совместимости и не должны использоваться при создании новых локальных или машинных объектов.</span><span class="sxs-lookup"><span data-stu-id="238f8-121">These values are supported for backward compatibility and should not be used when you create new local or machine objects.</span></span> <span data-ttu-id="238f8-122">Имя ключа локальных частных объектов данных также может начинаться с "Расдиалпармс" или "Раскредентиалс".</span><span class="sxs-lookup"><span data-stu-id="238f8-122">The key name of local private data objects may also start with "RasDialParms" or "RasCredentials".</span></span> <span data-ttu-id="238f8-123">Имя ключа для объектов машины также может начинаться с "NL $" или " \_ SC \_ ".</span><span class="sxs-lookup"><span data-stu-id="238f8-123">The key name for machine objects may also start with, "NL$" or "\_sc\_".</span></span>

<span data-ttu-id="238f8-124">Закрытые объекты данных, не являющиеся одним из предыдущих специализированных типов, используют имена ключей, которые не начинаются с префикса.</span><span class="sxs-lookup"><span data-stu-id="238f8-124">Private data objects that are not one of the preceding specialized types use key names that do not start with a prefix.</span></span> <span data-ttu-id="238f8-125">Эти объекты не реплицируются и могут быть считаны приложениями как локально, так и удаленно.</span><span class="sxs-lookup"><span data-stu-id="238f8-125">These objects are not replicated and can be read either locally or remotely by applications.</span></span>

 

 



