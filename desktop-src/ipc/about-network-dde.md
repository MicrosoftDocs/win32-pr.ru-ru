---
description: Сетевой DDE используется для инициации и обслуживания сетевых подключений, необходимых для сеансов DDE между приложениями, работающими на разных компьютерах в сети.
ms.assetid: f9eee391-2b4a-4c17-bea5-72cda5124e1c
title: О сетевом DDE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 412971f6bef8d2782dce38b5aef413e4d073f6b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345085"
---
# <a name="about-network-dde"></a><span data-ttu-id="21661-103">О сетевом DDE</span><span class="sxs-lookup"><span data-stu-id="21661-103">About Network DDE</span></span>

<span data-ttu-id="21661-104">\[Сетевой DDE больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="21661-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="21661-105">Nddeapi.dll имеется в Windows Vista, но все вызовы функций возвращают НДДЕ \_ не \_ реализован.\]</span><span class="sxs-lookup"><span data-stu-id="21661-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="21661-106">Сетевой DDE используется для инициации и обслуживания сетевых подключений, необходимых для сеансов DDE между приложениями, работающими на разных компьютерах в сети.</span><span class="sxs-lookup"><span data-stu-id="21661-106">Network DDE is used to initiate and maintain the network connections needed for DDE conversations between applications running on different computers in a network.</span></span> <span data-ttu-id="21661-107">*Сеанс* DDE — это взаимодействие между клиентскими и серверными приложениями.</span><span class="sxs-lookup"><span data-stu-id="21661-107">A DDE *conversation* is the interaction between client and server applications.</span></span> <span data-ttu-id="21661-108">В приложении вы используете сетевой DDE, а также DDE и библиотеку управления DDE (ДДЕМЛ).</span><span class="sxs-lookup"><span data-stu-id="21661-108">You use network DDE along with DDE and the DDE management library (DDEML) in your application.</span></span>

<span data-ttu-id="21661-109">DDE — это форма межпроцессного взаимодействия, которая использует общую память для обмена данными между приложениями.</span><span class="sxs-lookup"><span data-stu-id="21661-109">DDE is a form of interprocess communication that uses shared memory to exchange data between applications.</span></span> <span data-ttu-id="21661-110">Приложения могут использовать DDE для однократной передачи данных или для текущих операций обмена и обновления данных.</span><span class="sxs-lookup"><span data-stu-id="21661-110">Applications can use DDE for one time data transfers or for ongoing exchanges and updating data.</span></span> <span data-ttu-id="21661-111">Дополнительные сведения о DDE см. в разделе [Платформа динамических данных Exchange](../dataxchg/dynamic-data-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="21661-111">For more information on DDE, see [Dynamic Data Exchange](../dataxchg/dynamic-data-exchange.md).</span></span>

<span data-ttu-id="21661-112">ДДЕМЛ упрощает задачу добавления возможностей DDE в приложение.</span><span class="sxs-lookup"><span data-stu-id="21661-112">DDEML simplifies the task of adding DDE capability to an application.</span></span> <span data-ttu-id="21661-113">Вместо отправки, публикации и обработки сообщений DDE напрямую приложение использует функции, предоставляемые ДДЕМЛ для управления сеансами DDE.</span><span class="sxs-lookup"><span data-stu-id="21661-113">Instead of sending, posting, and processing DDE messages directly, an application uses the functions provided by the DDEML to manage DDE conversations.</span></span> <span data-ttu-id="21661-114">Дополнительные сведения о ДДЕМЛ см. в статье [Платформа динамических данных Exchange Management Library](../dataxchg/dynamic-data-exchange-management-library.md).</span><span class="sxs-lookup"><span data-stu-id="21661-114">For more information on DDEML, see [Dynamic Data Exchange Management Library](../dataxchg/dynamic-data-exchange-management-library.md).</span></span>

## <a name="network-dde-files"></a><span data-ttu-id="21661-115">Файлы сетевого DDE</span><span class="sxs-lookup"><span data-stu-id="21661-115">Network DDE Files</span></span>

<span data-ttu-id="21661-116">Чтобы использовать элементы API сетевого DDE, необходимо включить файл заголовка Нддеапи. h в исходные файлы и включить файл Нддеапи. lib в строку связи.</span><span class="sxs-lookup"><span data-stu-id="21661-116">To use the API elements of network DDE, you must include the NDDEApi.h header file in your source files and include NDDEApi.lib file on your link line.</span></span> <span data-ttu-id="21661-117">Необходимо также убедиться, что файл NDDEApi.dll загружен.</span><span class="sxs-lookup"><span data-stu-id="21661-117">You must also make sure that the NDDEApi.dll file is loaded.</span></span>

<span data-ttu-id="21661-118">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="21661-118">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="21661-119">Агент сетевого DDE</span><span class="sxs-lookup"><span data-stu-id="21661-119">Network DDE Agent</span></span>](network-dde-agent.md)
-   [<span data-ttu-id="21661-120">Общие ресурсы DDE</span><span class="sxs-lookup"><span data-stu-id="21661-120">DDE Shares</span></span>](dde-shares.md)
-   [<span data-ttu-id="21661-121">Доверенные общие ресурсы и безопасность</span><span class="sxs-lookup"><span data-stu-id="21661-121">Trusted Shares and Security</span></span>](trusted-shares-and-security.md)
-   [<span data-ttu-id="21661-122">Управление общими ресурсами DDE</span><span class="sxs-lookup"><span data-stu-id="21661-122">Managing DDE Shares</span></span>](managing-dde-shares.md)

 

 
