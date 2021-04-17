---
description: Подключаемые терминалы классифицируются в подклассы терминала.
ms.assetid: 0ab2896e-3634-47f7-b1f4-e7d1ffcb3592
title: Записи реестра (API телефонии)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 035126f614e526f3b1557f5323d52b3bf6b2b12c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684668"
---
# <a name="registry-entries-telephony-api"></a><span data-ttu-id="f9488-103">Записи реестра (API телефонии)</span><span class="sxs-lookup"><span data-stu-id="f9488-103">Registry Entries (Telephony API)</span></span>

<span data-ttu-id="f9488-104">Подключаемые терминалы классифицируются в подклассы терминала.</span><span class="sxs-lookup"><span data-stu-id="f9488-104">The pluggable terminals are classified into Terminal Superclasses.</span></span> <span data-ttu-id="f9488-105">Каждый суперкласс терминала имеет запись в реестре в следующем разделе:</span><span class="sxs-lookup"><span data-stu-id="f9488-105">Each Terminal Superclass has an entry in the registry under the following key:</span></span>

<span data-ttu-id="f9488-106">**HKey \_ \_** \\ **Программное обеспечение** локального компьютера \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Телефон** \\ **терминалманажер**</span><span class="sxs-lookup"><span data-stu-id="f9488-106">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Telephony**\\**TerminalManager**</span></span>

<span data-ttu-id="f9488-107">Под ключом суперкласса терминала находятся записи для каждого подключаемого терминала в суперклассе терминала.</span><span class="sxs-lookup"><span data-stu-id="f9488-107">Below the Terminal Superclass key are entries for each pluggable terminal within the Terminal Superclass.</span></span>

<span data-ttu-id="f9488-108">Запись для каждого суперкласса терминала определяется идентификатором CLSID суперкласса терминала.</span><span class="sxs-lookup"><span data-stu-id="f9488-108">The entry for each Terminal Superclass is identified by a Terminal Superclass CLSID.</span></span> <span data-ttu-id="f9488-109">Это уникальный идентификатор для класса терминала.</span><span class="sxs-lookup"><span data-stu-id="f9488-109">This is a unique identifier for a terminal class.</span></span> <span data-ttu-id="f9488-110">Класс Terminal имеет необязательный атрибут: Name, который является понятным именем для класса Terminal.</span><span class="sxs-lookup"><span data-stu-id="f9488-110">The terminal class has an optional attribute: name, which is a friendly name for the terminal class.</span></span> <span data-ttu-id="f9488-111">Каждый подключаемый терминал определяется классом терминала CLSID. то есть GUID.</span><span class="sxs-lookup"><span data-stu-id="f9488-111">Each pluggable terminal is identified by a CLSID Terminal class; that is, a GUID.</span></span> <span data-ttu-id="f9488-112">Атрибуты для подключаемого терминала сохраняются в значениях подключаемого ключа терминала.</span><span class="sxs-lookup"><span data-stu-id="f9488-112">The attributes for pluggable terminal are stored into pluggable terminal key values.</span></span> <span data-ttu-id="f9488-113">Ниже приведены атрибуты для подключаемого терминала.</span><span class="sxs-lookup"><span data-stu-id="f9488-113">The attributes for a pluggable terminal are the following.</span></span>



| <span data-ttu-id="f9488-114">Класс терминала</span><span class="sxs-lookup"><span data-stu-id="f9488-114">Terminal class</span></span> | <span data-ttu-id="f9488-115">Имя раздела</span><span class="sxs-lookup"><span data-stu-id="f9488-115">Key name</span></span> | <span data-ttu-id="f9488-116">Общедоступный идентификатор</span><span class="sxs-lookup"><span data-stu-id="f9488-116">Public identifier</span></span>                                                                 |
|----------------|----------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="f9488-117">Имя</span><span class="sxs-lookup"><span data-stu-id="f9488-117">Name</span></span>           | <span data-ttu-id="f9488-118">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="f9488-118">REG\_SZ</span></span>  | <span data-ttu-id="f9488-119">Понятное имя терминала</span><span class="sxs-lookup"><span data-stu-id="f9488-119">Terminal friendly name</span></span>                                                            |
| <span data-ttu-id="f9488-120">Company</span><span class="sxs-lookup"><span data-stu-id="f9488-120">Company</span></span>        | <span data-ttu-id="f9488-121">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="f9488-121">REG\_SZ</span></span>  | <span data-ttu-id="f9488-122">Название организации</span><span class="sxs-lookup"><span data-stu-id="f9488-122">Company name</span></span>                                                                      |
| <span data-ttu-id="f9488-123">Версия</span><span class="sxs-lookup"><span data-stu-id="f9488-123">Version</span></span>        | <span data-ttu-id="f9488-124">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="f9488-124">REG\_SZ</span></span>  | <span data-ttu-id="f9488-125">Сведения о версии</span><span class="sxs-lookup"><span data-stu-id="f9488-125">Version information</span></span>                                                               |
| <span data-ttu-id="f9488-126">CLSID</span><span class="sxs-lookup"><span data-stu-id="f9488-126">CLSID</span></span>          | <span data-ttu-id="f9488-127">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="f9488-127">REG\_SZ</span></span>  | <span data-ttu-id="f9488-128">CLSID терминала (используется в методе COM [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) )</span><span class="sxs-lookup"><span data-stu-id="f9488-128">Terminal CLSID (used in COM [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) method)</span></span> |
| <span data-ttu-id="f9488-129">Маршруты</span><span class="sxs-lookup"><span data-stu-id="f9488-129">Directions</span></span>     | <span data-ttu-id="f9488-130">DWORD</span><span class="sxs-lookup"><span data-stu-id="f9488-130">DWORD</span></span>    | <span data-ttu-id="f9488-131">Направление терминала</span><span class="sxs-lookup"><span data-stu-id="f9488-131">Terminal direction</span></span>                                                                |
| <span data-ttu-id="f9488-132">MediaTypes</span><span class="sxs-lookup"><span data-stu-id="f9488-132">MediaTypes</span></span>     | <span data-ttu-id="f9488-133">DWORD</span><span class="sxs-lookup"><span data-stu-id="f9488-133">DWORD</span></span>    | <span data-ttu-id="f9488-134">Поддерживаемые типы носителей терминала</span><span class="sxs-lookup"><span data-stu-id="f9488-134">Terminal media types supported</span></span>                                                    |



 

<span data-ttu-id="f9488-135">Для класса терминала используются следующие атрибуты.</span><span class="sxs-lookup"><span data-stu-id="f9488-135">For a terminal class the attributes are the following.</span></span>



| <span data-ttu-id="f9488-136">CLSID</span><span class="sxs-lookup"><span data-stu-id="f9488-136">CLSID</span></span> | <span data-ttu-id="f9488-137">Имя раздела</span><span class="sxs-lookup"><span data-stu-id="f9488-137">Key name</span></span> | <span data-ttu-id="f9488-138">Общедоступный идентификатор</span><span class="sxs-lookup"><span data-stu-id="f9488-138">Public identifier</span></span>            |
|-------|----------|------------------------------|
| <span data-ttu-id="f9488-139">Имя</span><span class="sxs-lookup"><span data-stu-id="f9488-139">Name</span></span>  | <span data-ttu-id="f9488-140">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="f9488-140">REG\_SZ</span></span>  | <span data-ttu-id="f9488-141">Понятное имя класса терминала</span><span class="sxs-lookup"><span data-stu-id="f9488-141">Terminal class friendly name</span></span> |



 

 

 
