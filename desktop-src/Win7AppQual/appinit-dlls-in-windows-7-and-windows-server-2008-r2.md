---
description: .
ms.assetid: 6d1f9703-6dc9-4fdc-b52f-e6bb60a2fe8d
title: AppInit_DLLs в Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31db695805b751e5dcd39293d0170c7fb78a11ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693690"
---
# <a name="appinit_dlls-in-windows-7-and-windows-server-2008-r2"></a><span data-ttu-id="1b7f7-103">Библиотеки \_ библиотеки DLL в Windows 7 и Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1b7f7-103">AppInit\_DLLs in Windows 7 and Windows Server 2008 R2</span></span>

## <a name="platform"></a><span data-ttu-id="1b7f7-104">Платформа</span><span class="sxs-lookup"><span data-stu-id="1b7f7-104">Platform</span></span>

<span data-ttu-id="1b7f7-105">**Клиенты** — Windows 7</span><span class="sxs-lookup"><span data-stu-id="1b7f7-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="1b7f7-106">**Серверы** — Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1b7f7-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="1b7f7-107">Воздействие на функции</span><span class="sxs-lookup"><span data-stu-id="1b7f7-107">Feature Impact</span></span>

 <span data-ttu-id="1b7f7-108">**Серьезность** — низкая</span><span class="sxs-lookup"><span data-stu-id="1b7f7-108">**Severity** - Low</span></span>  
<span data-ttu-id="1b7f7-109">**Частота** -низкая</span><span class="sxs-lookup"><span data-stu-id="1b7f7-109">**Frequency** - Low</span></span>  





## <a name="description"></a><span data-ttu-id="1b7f7-110">Описание</span><span class="sxs-lookup"><span data-stu-id="1b7f7-110">Description</span></span>

<span data-ttu-id="1b7f7-111">\_Библиотеки DLL библиотеки — это механизм, позволяющий загружать произвольный список библиотек DLL в каждый процесс пользовательского режима в системе.</span><span class="sxs-lookup"><span data-stu-id="1b7f7-111">AppInit\_DLLs is a mechanism that allows an arbitrary list of DLLs to be loaded into each user mode process on the system.</span></span> <span data-ttu-id="1b7f7-112">Корпорация Майкрософт изменяет средство библиотеки DLL в Windows 7 и Windows Server 2008 R2 для добавления нового требования подписывания кода.</span><span class="sxs-lookup"><span data-stu-id="1b7f7-112">Microsoft is modifying the AppInit DLLs facility in Windows 7 and Windows Server 2008 R2 to add a new code-signing requirement.</span></span> <span data-ttu-id="1b7f7-113">Это поможет повысить надежность и производительность системы, а также улучшить видимость происхождения программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="1b7f7-113">This will help improve the system reliability and performance, as well as improve visibility into the origin of software.</span></span>

## <a name="configuration"></a><span data-ttu-id="1b7f7-114">Конфигурация</span><span class="sxs-lookup"><span data-stu-id="1b7f7-114">Configuration</span></span>

<span data-ttu-id="1b7f7-115">Значения, хранящиеся в разделе « \_ \_ \\ программное обеспечение локального компьютера» \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Windows в реестре, определяют поведение \_ инфраструктуры библиотек DLL библиотеки.</span><span class="sxs-lookup"><span data-stu-id="1b7f7-115">Values stored under the HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion \\Windows key in the registry determine the behavior of the AppInit\_DLLs infrastructure.</span></span> <span data-ttu-id="1b7f7-116">Следующие значения реестра описаны в таблице ниже.</span><span class="sxs-lookup"><span data-stu-id="1b7f7-116">The table below describes these registry values:</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1b7f7-117">Значение</span><span class="sxs-lookup"><span data-stu-id="1b7f7-117">Value</span></span></th>
<th><span data-ttu-id="1b7f7-118">Описание</span><span class="sxs-lookup"><span data-stu-id="1b7f7-118">Description</span></span></th>
<th><span data-ttu-id="1b7f7-119">Примеры значений</span><span class="sxs-lookup"><span data-stu-id="1b7f7-119">Sample Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="1b7f7-120">LoadAppInit_DLLs (REG_DWORD) $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="1b7f7-120">LoadAppInit_DLLs (REG_DWORD)${REMOVE}$</span></span><br />
</td>
<td rowspan="2"><span data-ttu-id="1b7f7-121">Глобально включает или отключает AppInit_DLLs. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="1b7f7-121">Globally enables or disables AppInit_DLLs.${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="1b7f7-122">0x0 — AppInit_DLLs отключены.</span><span class="sxs-lookup"><span data-stu-id="1b7f7-122">0x0 – AppInit_DLLs are disabled.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b7f7-123">0x1 — AppInit_DLLs включены.</span><span class="sxs-lookup"><span data-stu-id="1b7f7-123">0x1 – AppInit_DLLs are enabled.</span></span></td>


</tr>
<tr class="odd">
<td><span data-ttu-id="1b7f7-124">AppInit_DLLs (REG_SZ)</span><span class="sxs-lookup"><span data-stu-id="1b7f7-124">AppInit_DLLs (REG_SZ)</span></span></td>
<td><span data-ttu-id="1b7f7-125">Разделенный запятыми список библиотек DLL для загрузки.</span><span class="sxs-lookup"><span data-stu-id="1b7f7-125">Space or comma delimited list of DLLs to load.</span></span> <span data-ttu-id="1b7f7-126">Полный путь к библиотеке DLL должен быть указан с использованием коротких имен.</span><span class="sxs-lookup"><span data-stu-id="1b7f7-126">The complete path to the DLL should be specified using Short Names.</span></span></td>
<td><span data-ttu-id="1b7f7-127">C:\ РОГРАММА ~ 1 \ WID288 ~ 1 \ MICROS ~1.DLL</span><span class="sxs-lookup"><span data-stu-id="1b7f7-127">C:\ PROGRA~1\WID288~1\MICROS~1.DLL</span></span></td>
</tr>
<tr class="even">
<td rowspan="2"><span data-ttu-id="1b7f7-128">RequireSignedAppInit_DLLs (REG_DWORD) $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="1b7f7-128">RequireSignedAppInit_DLLs (REG_DWORD)${REMOVE}$</span></span><br />
</td>
<td rowspan="2"><span data-ttu-id="1b7f7-129">Загружать только подписанные на код библиотеки DLL. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="1b7f7-129">Only load code-signed DLLs.${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="1b7f7-130">0x0 — Загрузка любых библиотек DLL.</span><span class="sxs-lookup"><span data-stu-id="1b7f7-130">0x0 – Load any DLLs.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b7f7-131">0x1 — загружать только подписанные кодом библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="1b7f7-131">0x1 – Load only code-signed DLLs.</span></span></td>


</tr>
</tbody>
</table>



 

<span data-ttu-id="1b7f7-132">**Windows 7**</span><span class="sxs-lookup"><span data-stu-id="1b7f7-132">**Windows 7**</span></span>

<span data-ttu-id="1b7f7-133">Все библиотеки DLL, загруженные \_ инфраструктурой библиотек DLL библиотеки, должны быть подписаны кодом.</span><span class="sxs-lookup"><span data-stu-id="1b7f7-133">All DLLs that are loaded by the AppInit\_DLLs infrastructure should be code-signed.</span></span> <span data-ttu-id="1b7f7-134">В интересах совместимости приложений операционная система Windows 7 будет загружать все библиотеки библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="1b7f7-134">In the interests of application compatibility, the Windows 7 Operating System will load all AppInit DLLs.</span></span> <span data-ttu-id="1b7f7-135">Однако корпорация Майкрософт рекомендует всем разработчикам приложений подписывать свои библиотеки DLL, чтобы помочь повысить надежность Windows и подготовить подписывание кода в будущих версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="1b7f7-135">However, Microsoft recommends that all application developers code-sign their DLLs to help improve the reliability of Windows and prepare for code-signing enforcement in future versions of Windows.</span></span> <span data-ttu-id="1b7f7-136">\_Раздел реестра рекуиресигнедаппинит dllss управляет этим поведением, и его значение в Windows 7 по умолчанию равно 0.</span><span class="sxs-lookup"><span data-stu-id="1b7f7-136">The RequireSignedAppInit\_DLLs registry key controls this behavior and its value on Windows 7 is set to 0 by default.</span></span>

<span data-ttu-id="1b7f7-137">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1b7f7-137">**Windows Server 2008 R2**</span></span>

<span data-ttu-id="1b7f7-138">Все библиотеки DLL, загруженные \_ инфраструктурой библиотек DLL библиотеки, должны быть подписаны кодом.</span><span class="sxs-lookup"><span data-stu-id="1b7f7-138">All DLLs that are loaded by the AppInit\_DLLs infrastructure must be code-signed.</span></span> <span data-ttu-id="1b7f7-139">\_Раздел реестра рекуиресигнедаппинит dllss управляет этим поведением, и его значение в Windows Server 2008 R2 по умолчанию равно 1.</span><span class="sxs-lookup"><span data-stu-id="1b7f7-139">The RequireSignedAppInit\_DLLs registry key controls this behavior and its value on Windows Server 2008 R2 is set to 1 by default.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="1b7f7-140">Ссылки на другие ресурсы</span><span class="sxs-lookup"><span data-stu-id="1b7f7-140">Links to Other Resources</span></span>

<dl>

[<span data-ttu-id="1b7f7-141">Библиотеки библиотеки DLL в Windows 7 и Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1b7f7-141">AppInit DLLs in Windows 7 and Windows Server 2008 R2</span></span>](/windows-hardware/drivers/install/)  
</dl>

 

 
