---
description: Общие сведения об API родительского контроля
ms.assetid: 647e5df8-7c6d-466a-a3d4-eac13efa797d
title: Общие сведения об API родительского контроля
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0aa88592f2262b89f98cfd5baaac5ad2f35f959
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712905"
---
# <a name="parental-controls-api-overview"></a><span data-ttu-id="2bb84-103">Общие сведения об API родительского контроля</span><span class="sxs-lookup"><span data-stu-id="2bb84-103">Parental Controls API Overview</span></span>

<span data-ttu-id="2bb84-104">API-интерфейсы, используемые для родительского контроля, предоставляют политику и параметры встроенных ограничений, а также функции ведения журнала.</span><span class="sxs-lookup"><span data-stu-id="2bb84-104">APIs used for Parental Controls expose the policy and in-box restrictions settings, and logging functionality.</span></span>

## <a name="settings"></a><span data-ttu-id="2bb84-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="2bb84-105">Settings</span></span>

<span data-ttu-id="2bb84-106">Предоставляются два общедоступных API:</span><span class="sxs-lookup"><span data-stu-id="2bb84-106">Two public APIs are provided:</span></span>

-   <span data-ttu-id="2bb84-107">Упрощенный API-интерфейс минимального соответствия на основе COM (называемый API соответствия) в основном для приложений, чтобы определить, следует ли включать ведение журнала.</span><span class="sxs-lookup"><span data-stu-id="2bb84-107">A lightweight COM-based minimum compliance API (called the Compliance API) primarily for applications to determine whether logging should be turned on.</span></span> <span data-ttu-id="2bb84-108">Кроме того, предоставляются простые методы для:</span><span class="sxs-lookup"><span data-stu-id="2bb84-108">In addition, simple methods are provided for:</span></span>
    -   <span data-ttu-id="2bb84-109">Получение состояния ограничений для веб-ограничений, ограничений по времени, ограничений игр и ограничений приложений.</span><span class="sxs-lookup"><span data-stu-id="2bb84-109">Retrieving the restrictions state for web restrictions, time limits, games restrictions, and application restrictions.</span></span>
    -   <span data-ttu-id="2bb84-110">Получение идентификатора активного фильтра веб-содержимого.</span><span class="sxs-lookup"><span data-stu-id="2bb84-110">Retrieving the ID of the active Web content filter.</span></span>
    -   <span data-ttu-id="2bb84-111">Определение того, должны ли отображаться элементы пользовательского интерфейса поставщика способом, согласованным с встроенным скрытием при присоединении к домену.</span><span class="sxs-lookup"><span data-stu-id="2bb84-111">Determining whether vendor user interface elements should be shown, in a manner consistent with the in-box hiding when joined to a domain.</span></span>
    -   <span data-ttu-id="2bb84-112">Получение времени последнего изменения параметра для пользователя.</span><span class="sxs-lookup"><span data-stu-id="2bb84-112">Retrieving the last time a setting has been changed for a user.</span></span>
    -   <span data-ttu-id="2bb84-113">Получение сведений о том, требуется ли заблокировать загрузку файлов на основе браузера или браузера для пользователя, а также возможность запросить URL-адрес, явно разрешенный фильтром веб-содержимого для этого пользователя.</span><span class="sxs-lookup"><span data-stu-id="2bb84-113">Retrieving whether browser-based or browser-like file downloads need to be blocked for a user, and the ability to request a URL to be specifically allowed by the Web Content Filter for that user.</span></span>
    -   <span data-ttu-id="2bb84-114">Определение того, заблокирована ли данная игра для пользователя.</span><span class="sxs-lookup"><span data-stu-id="2bb84-114">Determining whether a given game is blocked for a user.</span></span>
-   <span data-ttu-id="2bb84-115">Доступ к пространству имен родительского элемента управления с помощью API инструментарий управления Windows (WMI) (WMI) для полной записи и доступа на чтение ко всем предоставленным параметрам.</span><span class="sxs-lookup"><span data-stu-id="2bb84-115">Windows Management Instrumentation (WMI) API access to a Parental Controls namespace for full write and read access to all exposed settings.</span></span> <span data-ttu-id="2bb84-116">Родительский контроль развертывает поставщик WMI для управления разрешениями на чтение и запись в базовом хранилище параметров с надлежащей принудительной защитой прав для администраторов и контролируемых пользователей.</span><span class="sxs-lookup"><span data-stu-id="2bb84-116">Parental Controls deploys a WMI Provider to manage read/write permissions to the underlying settings store with proper enforcement of privileges for administrators and controlled users.</span></span>

<span data-ttu-id="2bb84-117">Независимые поставщики программного обеспечения запрашивают использование API соответствия и API инструментария WMI, чтобы управлять ограничениями, необходимыми для обеспечения дочерней безопасности в зависимости от функциональности приложения или решения.</span><span class="sxs-lookup"><span data-stu-id="2bb84-117">ISVs are requested to use the Compliance API, and the WMI API as necessary, to control restrictions as appropriate for child safety based on the functionality of the application or solution.</span></span>

## <a name="logging"></a><span data-ttu-id="2bb84-118">Ведение журнала</span><span class="sxs-lookup"><span data-stu-id="2bb84-118">Logging</span></span>

-   <span data-ttu-id="2bb84-119">Для мониторинга активности родительских элементов управления используются стандартные API-интерфейсы для публикации и использования стандартных событий Windows.</span><span class="sxs-lookup"><span data-stu-id="2bb84-119">Windows standard event publishing and consuming APIs are used for Parental Controls activity monitoring.</span></span> <span data-ttu-id="2bb84-120">Система отчетов о событиях и трассировки Windows Vista улучшила производительность по сравнению с предыдущими функциями трассировки событий Windows (ETW).</span><span class="sxs-lookup"><span data-stu-id="2bb84-120">The Windows Vista Event Reporting and Tracing system has improved performance over previous Event Tracing for Windows (ETW) functionality.</span></span> <span data-ttu-id="2bb84-121">Родительский контроль определяет уникальный канал для своих данных в ETW.</span><span class="sxs-lookup"><span data-stu-id="2bb84-121">Parental Controls defines a unique channel for its data in ETW.</span></span>
-   <span data-ttu-id="2bb84-122">Независимые поставщики программного обеспечения должны использовать API публикации событий для регистрации действий пользователя, как указано в разделе Использование API-интерфейсов родительского контроля.</span><span class="sxs-lookup"><span data-stu-id="2bb84-122">ISVs are requested to use the event publishing API to log user activity as specified in the Using Parental Controls APIs section.</span></span>

 

 



