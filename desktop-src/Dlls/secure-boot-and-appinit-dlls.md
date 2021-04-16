---
description: Начиная с Windows 8 \_ инфраструктура библиотеки DLL отключена, если включена безопасная загрузка.
ms.assetid: 3ADE71C7-7113-4D26-8D6D-5609CAF13397
title: Библиотеки DLL и безопасная загрузка
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2915dda53959f2a403a62112385fe80e735cbfd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684387"
---
# <a name="appinit-dlls-and-secure-boot"></a><span data-ttu-id="0a4c8-103">Библиотеки DLL и безопасная загрузка</span><span class="sxs-lookup"><span data-stu-id="0a4c8-103">AppInit DLLs and Secure Boot</span></span>

<span data-ttu-id="0a4c8-104">Начиная с Windows 8 \_ инфраструктура библиотеки DLL отключена, если включена безопасная загрузка.</span><span class="sxs-lookup"><span data-stu-id="0a4c8-104">Starting in Windows 8, the AppInit\_DLLs infrastructure is disabled when secure boot is enabled.</span></span>

## <a name="about-appinit_dlls"></a><span data-ttu-id="0a4c8-105">Сведения о \_ библиотеках DLL библиотеки</span><span class="sxs-lookup"><span data-stu-id="0a4c8-105">About AppInit\_DLLs</span></span>

<span data-ttu-id="0a4c8-106">\_Инфраструктура библиотек DLL библиотеки предоставляет простой способ подключения системных API, позволяя загружать пользовательские библиотеки DLL в адресное пространство каждого интерактивного приложения.</span><span class="sxs-lookup"><span data-stu-id="0a4c8-106">The AppInit\_DLLs infrastructure provides an easy way to hook system APIs by allowing custom DLLs to be loaded into the address space of every interactive application.</span></span> <span data-ttu-id="0a4c8-107">Приложения и вредоносные программы используют библиотеки DLL библиотеки для той же основной причины, что заключается в подключении интерфейсов API. После загрузки пользовательской библиотеки DLL она может подключить хорошо известный системный API и реализовать альтернативные функциональные возможности.</span><span class="sxs-lookup"><span data-stu-id="0a4c8-107">Applications and malicious software both use AppInit DLLs for the same basic reason, which is to hook APIs; after the custom DLL is loaded, it can hook a well-known system API and implement alternate functionality.</span></span> <span data-ttu-id="0a4c8-108">Этот механизм используется только небольшим количеством современных законных приложений для загрузки библиотек DLL, в то время как большой набор вредоносных программ использует этот механизм для компрометации систем.</span><span class="sxs-lookup"><span data-stu-id="0a4c8-108">Only a small set of modern legitimate applications use this mechanism to load DLLs, while a large set of malware use this mechanism to compromise systems.</span></span> <span data-ttu-id="0a4c8-109">Даже Библиотекиные \_ библиотеки DLL могут случайным образом привести к взаимоблокировке системы и проблемам с производительностью, поэтому \_ не рекомендуется использовать библиотеки DLL библиотеки.</span><span class="sxs-lookup"><span data-stu-id="0a4c8-109">Even legitimate AppInit\_DLLs can unintentionally cause system deadlocks and performance problems, therefore usage of AppInit\_DLLs is not recommended.</span></span>

## <a name="appinit_dlls-and-secure-boot"></a><span data-ttu-id="0a4c8-110">Библиотеки \_ DLL и безопасная загрузка</span><span class="sxs-lookup"><span data-stu-id="0a4c8-110">AppInit\_DLLs and secure boot</span></span>

<span data-ttu-id="0a4c8-111">Windows 8 предприняла UEFI и безопасную загрузку для повышения общей целостности системы и обеспечения надежной защиты от сложных угроз.</span><span class="sxs-lookup"><span data-stu-id="0a4c8-111">Windows 8 adopted UEFI and secure boot to improve the overall system integrity and to provide strong protection against sophisticated threats.</span></span> <span data-ttu-id="0a4c8-112">Если включена безопасная загрузка, механизм библиотеки \_ DLL отключается в рамках бескомпромиссного подхода к защите клиентов от вредоносных программ и угроз.</span><span class="sxs-lookup"><span data-stu-id="0a4c8-112">When secure boot is enabled, the AppInit\_DLLs mechanism is disabled as part of a no-compromise approach to protect customers against malware and threats.</span></span>

<span data-ttu-id="0a4c8-113">Обратите внимание, что безопасная загрузка является протоколом UEFI, а не компонентом Windows 8.</span><span class="sxs-lookup"><span data-stu-id="0a4c8-113">Please note that secure boot is a UEFI protocol and not a Windows 8 feature.</span></span> <span data-ttu-id="0a4c8-114">Дополнительные сведения о UEFI и спецификации протокола безопасной загрузки можно найти по адресу [https://www.uefi.org](https://www.uefi.org/) .</span><span class="sxs-lookup"><span data-stu-id="0a4c8-114">More info on UEFI and the secure boot protocol specification can be found at [https://www.uefi.org](https://www.uefi.org/).</span></span>

## <a name="appinit_dlls-certification-requirement-for-windows-8-desktop-apps"></a><span data-ttu-id="0a4c8-115">\_Требования к сертификации библиотеки DLL для классических приложений Windows 8</span><span class="sxs-lookup"><span data-stu-id="0a4c8-115">AppInit\_DLLs certification requirement for Windows 8 desktop apps</span></span>

<span data-ttu-id="0a4c8-116">Одним из требований сертификации для классических приложений Windows 8 является то, что приложение не должно загружать произвольные библиотеки DLL для перехвата вызовов API Win32 с помощью \_ механизма DLL библиотеки.</span><span class="sxs-lookup"><span data-stu-id="0a4c8-116">One of the certification requirements for Windows 8 desktop apps is that the app must not load arbitrary DLLs to intercept Win32 API calls using the AppInit\_DLLs mechanism.</span></span> <span data-ttu-id="0a4c8-117">Более подробные сведения о требованиях к сертификации см. в разделе 1,1 [требования к сертификации для классических приложений Windows 8](../win_cert/certification-requirements-for-windows-desktop-apps.md).</span><span class="sxs-lookup"><span data-stu-id="0a4c8-117">For more detailed information about the certification requirements, refer to section 1.1 of [Certification requirements for Windows 8 desktop apps](../win_cert/certification-requirements-for-windows-desktop-apps.md).</span></span>

## <a name="summary"></a><span data-ttu-id="0a4c8-118">Сводка</span><span class="sxs-lookup"><span data-stu-id="0a4c8-118">Summary</span></span>

-   <span data-ttu-id="0a4c8-119">Механизм библиотеки \_ DLL не является рекомендуемым подходом для легальных приложений, поскольку он может привести к взаимоблокировке системы и проблемам с производительностью.</span><span class="sxs-lookup"><span data-stu-id="0a4c8-119">The AppInit\_DLLs mechanism is not a recommended approach for legitimate applications because it can lead to system deadlocks and performance problems.</span></span>
-   <span data-ttu-id="0a4c8-120">Механизм библиотеки \_ DLL отключен по умолчанию, если включена безопасная загрузка.</span><span class="sxs-lookup"><span data-stu-id="0a4c8-120">The AppInit\_DLLs mechanism is disabled by default when secure boot is enabled.</span></span>
-   <span data-ttu-id="0a4c8-121">Использование \_ библиотек DLL библиотеки в классическом приложении Windows 8 является ошибкой сертификации для настольных приложений Windows.</span><span class="sxs-lookup"><span data-stu-id="0a4c8-121">Using AppInit\_DLLs in a Windows 8 desktop app is a Windows desktop app certification failure.</span></span>

<span data-ttu-id="0a4c8-122">Сведения о \_ библиотеках DLL библиотеки в Windows 7 и Windows server 2008 R2: [библиотеки DLL в Windows 7 и windows Server 2008 R2](/previous-versions/windows/hardware/download/dn550976(v=vs.85))см. в следующем техническом документе.</span><span class="sxs-lookup"><span data-stu-id="0a4c8-122">See the following whitepaper for info about AppInit\_DLLs on Windows 7 and Windows Server 2008 R2: [AppInit DLLs in Windows 7 and Windows Server 2008 R2](/previous-versions/windows/hardware/download/dn550976(v=vs.85)).</span></span>

 

 
