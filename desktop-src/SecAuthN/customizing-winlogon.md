---
description: Настройка поведения Winlogon путем реализации поставщика учетных данных.
ms.assetid: 70b47e29-c755-4c59-a493-d7fcbbc94b83
title: Настройка Winlogon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b64da4baae9b52dd53e288c631f35d33ea5a3085
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647201"
---
# <a name="customizing-winlogon"></a><span data-ttu-id="df396-103">Настройка Winlogon</span><span class="sxs-lookup"><span data-stu-id="df396-103">Customizing Winlogon</span></span>

<span data-ttu-id="df396-104">Настройка поведения [*Winlogon*](/windows/desktop/SecGloss/w-gly) путем реализации поставщика учетных данных.</span><span class="sxs-lookup"><span data-stu-id="df396-104">Customize [*Winlogon*](/windows/desktop/SecGloss/w-gly) behavior by implementing a Credential Provider.</span></span> <span data-ttu-id="df396-105">Дополнительные сведения о поставщиках учетных данных см. в разделе [**интерфейс икредентиалпровидер**](/windows/win32/api/credentialprovider/nn-credentialprovider-icredentialprovider).</span><span class="sxs-lookup"><span data-stu-id="df396-105">For information about Credential Providers, see [**ICredentialProvider Interface**](/windows/win32/api/credentialprovider/nn-credentialprovider-icredentialprovider).</span></span>

<span data-ttu-id="df396-106">**Windows Server 2003 и Windows XP:** Поставщики учетных данных не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="df396-106">**Windows Server 2003 and Windows XP:** Credential Providers are not supported.</span></span>

<span data-ttu-id="df396-107">В следующих разделах описаны способы настройки Winlogon в версиях Windows, предшествовавших Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="df396-107">The following sections describe ways to customize Winlogon in Windows versions prior to Windows Vista.</span></span>

> [!Note]  
> <span data-ttu-id="df396-108">Библиотеки DLL GINA и пакеты уведомлений Winlogon игнорируются в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="df396-108">GINA DLLs and Winlogon notification packages are ignored in Windows Vista.</span></span>

 

-   [<span data-ttu-id="df396-109">Пакеты уведомлений Winlogon</span><span class="sxs-lookup"><span data-stu-id="df396-109">Winlogon Notification Packages</span></span>](#winlogon-notification-packages)
-   [<span data-ttu-id="df396-110">Заглушки GINA</span><span class="sxs-lookup"><span data-stu-id="df396-110">GINA Stubs</span></span>](#gina-stubs)
-   [<span data-ttu-id="df396-111">Перехватчики GINA</span><span class="sxs-lookup"><span data-stu-id="df396-111">GINA Hooks</span></span>](#gina-hooks)

## <a name="winlogon-notification-packages"></a><span data-ttu-id="df396-112">Пакеты уведомлений Winlogon</span><span class="sxs-lookup"><span data-stu-id="df396-112">Winlogon Notification Packages</span></span>

<span data-ttu-id="df396-113">Пакет уведомлений Winlogon — это библиотека DLL, которая экспортирует функции, которые обрабатывали события Winlogon.</span><span class="sxs-lookup"><span data-stu-id="df396-113">A Winlogon notification package is a DLL that exports functions that handle Winlogon events.</span></span> <span data-ttu-id="df396-114">Например, когда пользователь входит в систему, Winlogon вызывает каждый пакет уведомлений, чтобы предоставить сведения о событии.</span><span class="sxs-lookup"><span data-stu-id="df396-114">For example, when a user logs onto the system, Winlogon calls each notification package to provide information about the event.</span></span> <span data-ttu-id="df396-115">Дополнительные сведения см. в разделе [пакеты уведомлений Winlogon](winlogon-notification-packages.md).</span><span class="sxs-lookup"><span data-stu-id="df396-115">For more information, see [Winlogon Notification Packages](winlogon-notification-packages.md).</span></span>

## <a name="gina-stubs"></a><span data-ttu-id="df396-116">Заглушки GINA</span><span class="sxs-lookup"><span data-stu-id="df396-116">GINA Stubs</span></span>

<span data-ttu-id="df396-117">Заглушка [*GINA*](/windows/desktop/SecGloss/g-gly) — это ПОЛЬЗОВАТЕЛЬСКАЯ библиотека GINA, которая использует реализации функции экспорта ранее установленной библиотеки GINA DLL (обычно MsGina.dll).</span><span class="sxs-lookup"><span data-stu-id="df396-117">A [*GINA*](/windows/desktop/SecGloss/g-gly) stub is a custom GINA DLL that uses the export function implementations of a previously installed GINA DLL (typically MsGina.dll).</span></span> <span data-ttu-id="df396-118">Заглушка GINA получает указатели на каждую функцию, экспортируемую ранее установленной DLL-библиотекой GINA.</span><span class="sxs-lookup"><span data-stu-id="df396-118">A GINA stub gets pointers to each function exported by the previously installed GINA DLL.</span></span> <span data-ttu-id="df396-119">Каждая функция-заглушка GINA затем использует соответствующий указатель на функцию для вызова соответствующей функции в ранее установленной библиотеке DLL GINA.</span><span class="sxs-lookup"><span data-stu-id="df396-119">Each GINA stub function then uses the appropriate function pointer to call the corresponding function in the previously installed GINA DLL.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="df396-120">Каждая функция-заглушка GINA должна вызывать соответствующую функцию в ранее установленной модели GINA.</span><span class="sxs-lookup"><span data-stu-id="df396-120">Each GINA stub function must call the corresponding function in the previously installed GINA.</span></span>

 

<span data-ttu-id="df396-121">Функция-заглушка GINA может реализовать дополнительные функциональные возможности в одной или нескольких функциях экспорта.</span><span class="sxs-lookup"><span data-stu-id="df396-121">A GINA stub function can implement additional functionality in one or more of its export functions.</span></span> <span data-ttu-id="df396-122">Например, функция [**влкслогжедаутсас**](/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas) заглушки GINA может проверить текущее время перед вызовом функции **влкслогжедаутсас** MsGina.dll.</span><span class="sxs-lookup"><span data-stu-id="df396-122">For example, the [**WlxLoggedOutSAS**](/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas) function of a GINA stub might check the current time before calling the **WlxLoggedOutSAS** function of the MsGina.dll.</span></span> <span data-ttu-id="df396-123">Если текущее время находилось в определенном диапазоне, функция-заглушка может отобразить сообщение о том, что вход в систему не разрешен в течение этого периода времени, и вернуть **влкс \_ SAS \_ Action \_ None** в Winlogon.</span><span class="sxs-lookup"><span data-stu-id="df396-123">If the current time was within a specific range, the stub function could display a message that indicates logon is disallowed during that time period and return **WLX\_SAS\_ACTION\_NONE** to Winlogon.</span></span> <span data-ttu-id="df396-124">Функция **влкслогжедаутсас** MsGina.dll будет вызываться только в течение допустимого периода времени.</span><span class="sxs-lookup"><span data-stu-id="df396-124">The **WlxLoggedOutSAS** function of the MsGina.dll would then be called only during the allowed time period.</span></span>

<span data-ttu-id="df396-125">Приложение-заглушка GINA получает таблицу диспетчеризации для функций поддержки Winlogon с помощью параметра *пвинлогонфунктионс* функции [**влксинитиализе**](/windows/desktop/api/Winwlx/nf-winwlx-wlxinitialize) .</span><span class="sxs-lookup"><span data-stu-id="df396-125">The GINA stub application gets a dispatch table to Winlogon support functions through the *pWinlogonFunctions* parameter of the [**WlxInitialize**](/windows/desktop/api/Winwlx/nf-winwlx-wlxinitialize) function.</span></span> <span data-ttu-id="df396-126">Приложение-заглушка GINA может использовать эту таблицу диспетчеризации для вызова функций поддержки Winlogon.</span><span class="sxs-lookup"><span data-stu-id="df396-126">The GINA stub application can use this dispatch table to call Winlogon support functions.</span></span> <span data-ttu-id="df396-127">Например, приложение-заглушка GINA может вызвать функцию [**влкссаснотифи**](/windows/win32/api/winwlx/nc-winwlx-pwlx_sas_notify) , чтобы вызвать событие [*последовательности безопасности*](/windows/desktop/SecGloss/s-gly) (SAS) при вставке [*смарт-карты*](/windows/desktop/SecGloss/s-gly) в [*средство чтения*](/windows/desktop/SecGloss/r-gly).</span><span class="sxs-lookup"><span data-stu-id="df396-127">For example, A GINA stub application can call the [**WlxSasNotify**](/windows/win32/api/winwlx/nc-winwlx-pwlx_sas_notify) function to cause a [*secure attention sequence*](/windows/desktop/SecGloss/s-gly) (SAS) event when a [*smart card*](/windows/desktop/SecGloss/s-gly) is inserted into a [*reader*](/windows/desktop/SecGloss/r-gly).</span></span>

<span data-ttu-id="df396-128">Дополнительные сведения о создании заглушек GINA см. в образце заглушек GINA в \\ каталоге Samples \\ Security \\ GINA \\ Гинастуб (пакет средств разработки программного обеспечения для платформы).</span><span class="sxs-lookup"><span data-stu-id="df396-128">For more information about creating a GINA stub, see the Gina Stubs sample in the \\Samples\\Security\\Gina\\GinaStub directory of a Platform Software Development Kit (SDK) installation.</span></span>

> [!Note]  
> <span data-ttu-id="df396-129">Все вызовы между GINA и Winlogon должны находиться в одном потоке.</span><span class="sxs-lookup"><span data-stu-id="df396-129">All calls between a GINA and Winlogon must be within a single thread.</span></span>

 

## <a name="gina-hooks"></a><span data-ttu-id="df396-130">Перехватчики GINA</span><span class="sxs-lookup"><span data-stu-id="df396-130">GINA Hooks</span></span>

<span data-ttu-id="df396-131">Ловушка GINA — это заглушка GINA, которая в своей реализации функции [**влксинитиализе**](/windows/desktop/api/Winwlx/nf-winwlx-wlxinitialize) заменяет указатель на функцию поддержки [**влксдиалогбокспарам**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_param) в таблице диспетчеризации указателем на собственную реализацию функции **влксдиалогбокспарам** .</span><span class="sxs-lookup"><span data-stu-id="df396-131">A GINA hook is a GINA stub that, in its implementation of the [**WlxInitialize**](/windows/desktop/api/Winwlx/nf-winwlx-wlxinitialize) function, replaces the pointer to the [**WlxDialogBoxParam**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_param) support function in the dispatch table with a pointer to its own implementation of the **WlxDialogBoxParam** function.</span></span> <span data-ttu-id="df396-132">В результате каждый раз, когда ранее установленная GINA (обычно MsGina.dll) вызывает функцию **влксдиалогбокспарам** , вызывается функция, реализованная обработчиком GINA.</span><span class="sxs-lookup"><span data-stu-id="df396-132">As a result, each time the previously installed GINA (typically MsGina.dll) calls the **WlxDialogBoxParam** function, the function implemented by the GINA hook is called.</span></span>

<span data-ttu-id="df396-133">Функция [**влксдиалогбокспарам**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_param) , реализованная с помощью ловушки GINA, может заменить процедуру обратного вызова [**DialogProc**](/windows/win32/api/winuser/nc-winuser-dlgproc) , которая реагирует на определенное событие диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="df396-133">The [**WlxDialogBoxParam**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_param) function implemented by the GINA hook can replace the [**DialogProc**](/windows/win32/api/winuser/nc-winuser-dlgproc) callback procedure that responds to a specific dialog box event.</span></span>

<span data-ttu-id="df396-134">Это дает обработчику GINA полный контроль над внешним видом и поведением всех диалоговых окон, создаваемых MsGina.dll.</span><span class="sxs-lookup"><span data-stu-id="df396-134">This gives the GINA hook full control over the appearance and behavior of all of the dialog boxes that MsGina.dll creates.</span></span>

<span data-ttu-id="df396-135">Дополнительные сведения о создании ловушки GINA см. в образце ловушек GINA в \\ каталоге Samples \\ Security \\ GINA \\ Гинахук в установке пакета Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="df396-135">For more information about creating a GINA hook, see the Gina Hooks sample in the \\Samples\\Security\\Gina\\GinaHook directory of a Platform SDK installation.</span></span>

> [!Note]  
> <span data-ttu-id="df396-136">Все вызовы между GINA и Winlogon должны находиться в одном потоке.</span><span class="sxs-lookup"><span data-stu-id="df396-136">All calls between a GINA and Winlogon must be within a single thread.</span></span>

 

 

 
