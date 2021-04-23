---
description: В следующем списке содержатся Поддерживаемые функции TAPI MSP.
ms.assetid: e36bba94-1fa7-4514-9f8a-bcd690b04d73
title: Поддерживаемые возможности
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00d10fd9ac787483b8dfa6e15046a733992adb97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263103"
---
# <a name="features-supported"></a><span data-ttu-id="17653-103">Поддерживаемые возможности</span><span class="sxs-lookup"><span data-stu-id="17653-103">Features Supported</span></span>

<span data-ttu-id="17653-104">В следующем списке содержатся Поддерживаемые функции TAPI MSP.</span><span class="sxs-lookup"><span data-stu-id="17653-104">The following list contains the TAPI MSP supported features.</span></span>

-   <span data-ttu-id="17653-105">Реализует MSP, который обрабатывает один адрес для каждого экземпляра MSP.</span><span class="sxs-lookup"><span data-stu-id="17653-105">Implements an MSP that handles a single address per instance of the MSP.</span></span> <span data-ttu-id="17653-106">Несколько таких адресов обрабатываются путем многократного создания экземпляра MSP.</span><span class="sxs-lookup"><span data-stu-id="17653-106">Multiple like addresses are handled by instantiating the MSP multiple times.</span></span> <span data-ttu-id="17653-107">Это значительно упрощает реализацию MSP и базовых классов.</span><span class="sxs-lookup"><span data-stu-id="17653-107">This greatly simplifies the implementation of the MSP and the base classes.</span></span>
-   <span data-ttu-id="17653-108">Реализует все интерфейсы МСПИ, включая [**итмспаддресс**](/windows/desktop/api/msp/nn-msp-itmspaddress), [**иттерминалсуппорт**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport), [**итстреамконтрол**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol)и [**итстреам**](/windows/win32/api/tapi3if/nn-tapi3if-itstream).</span><span class="sxs-lookup"><span data-stu-id="17653-108">Implements all the MSPI interfaces, including [**ITMSPAddress**](/windows/desktop/api/msp/nn-msp-itmspaddress), [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport), [**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol), and [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream).</span></span>
-   <span data-ttu-id="17653-109">Реализует готовые к использованию статические терминалы как для аудио, так и для видео.</span><span class="sxs-lookup"><span data-stu-id="17653-109">Implements ready-to-use static terminals for both audio and video.</span></span>
-   <span data-ttu-id="17653-110">Реализует универсальные базовые классы терминала.</span><span class="sxs-lookup"><span data-stu-id="17653-110">Implements generic terminal base classes.</span></span> <span data-ttu-id="17653-111">Эти базовые классы терминала используются как упомянутые выше статическими реализациями терминалов, так и реализациями динамических терминалов, которые находятся в Termmgr.dll.</span><span class="sxs-lookup"><span data-stu-id="17653-111">These terminal base classes are used by both the above-mentioned static terminal implementations and the implementations of dynamic terminals that are found in Termmgr.dll.</span></span> <span data-ttu-id="17653-112">MSP также может использовать их для реализации дополнительных терминалов.</span><span class="sxs-lookup"><span data-stu-id="17653-112">The MSP can also use them to implement additional terminals.</span></span>
-   <span data-ttu-id="17653-113">Использует диспетчер терминалов для управления динамическими терминалами.</span><span class="sxs-lookup"><span data-stu-id="17653-113">Uses the Terminal Manager to handle dynamic terminals.</span></span> <span data-ttu-id="17653-114">Создает динамические терминалы в рабочем потоке с помощью конвейера сообщений (для высвобождения консольных приложений от необходимости обработки сообщений окон для терминалов рендеринга видео и упрощения проблем синхронизации).</span><span class="sxs-lookup"><span data-stu-id="17653-114">Creates dynamic terminals on a worker thread with a message pump (to free console applications from having to process window messages for video render terminals and to simplify synchronization issues).</span></span>
-   <span data-ttu-id="17653-115">Поддерживает вызовы, использующие граф фильтра для каждого потока.</span><span class="sxs-lookup"><span data-stu-id="17653-115">Supports calls that use a filter graph per stream.</span></span>
-   <span data-ttu-id="17653-116">Реализует обработку событий графа.</span><span class="sxs-lookup"><span data-stu-id="17653-116">Implements handling of graph events.</span></span>
-   <span data-ttu-id="17653-117">Использует API пула потоков в сочетании с собственным рабочим потоком для обработки событий.</span><span class="sxs-lookup"><span data-stu-id="17653-117">Uses the thread pooling APIs, in conjunction with a worker thread of its own, to handle events.</span></span>
-   <span data-ttu-id="17653-118">Использует API-интерфейсы трассировки Windows 2000 (изначально разработанные для проекта маршрутизации) и дополнительную логику для предоставления гибкого универсального механизма ведения журнала, который может одновременно входить в любое сочетание следующих параметров: режим пользователя или отладчика режима ядра; отдельное окно консоли с сообщениями журнала, разделенными компонентом; файл журнала.</span><span class="sxs-lookup"><span data-stu-id="17653-118">Uses the tracing APIs of Windows 2000 (originally developed for the Routing project) along with additional logic to provide a flexible, generic logging mechanism that can simultaneously log to any combination of the following: a user or kernel-mode debugger; a separate console window with log messages separated by component; a log file.</span></span>
-   <span data-ttu-id="17653-119">Работает в свободной потоке.</span><span class="sxs-lookup"><span data-stu-id="17653-119">Runs free-threaded.</span></span>

 

 
