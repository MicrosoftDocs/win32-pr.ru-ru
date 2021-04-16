---
description: Доступность SKU родительского контроля
ms.assetid: 5fbf6c4a-3897-4a12-bef6-19478fdb48aa
title: Доступность SKU родительского контроля
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b858bc62e8f10a3b06313befd99d67e497b8d442
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105693046"
---
# <a name="parental-controls-sku-availability"></a><span data-ttu-id="08f46-103">Доступность SKU родительского контроля</span><span class="sxs-lookup"><span data-stu-id="08f46-103">Parental Controls SKU Availability</span></span>

<span data-ttu-id="08f46-104">Пользовательские интерфейсы, функции и API-интерфейсы родительского контроля, описанные в этом разделе, сейчас запланированы на доступ только к номерам SKU, ориентированным на потребителей, например:</span><span class="sxs-lookup"><span data-stu-id="08f46-104">The Parental Controls user interfaces, features, and APIs described in this section are currently planned to be available only on consumer-focused SKUs such as:</span></span>

-   <span data-ttu-id="08f46-105">Windows Vista Starter</span><span class="sxs-lookup"><span data-stu-id="08f46-105">Windows Vista Starter</span></span>
-   <span data-ttu-id="08f46-106">Windows Vista Home Basic</span><span class="sxs-lookup"><span data-stu-id="08f46-106">Windows Vista Home Basic</span></span>
-   <span data-ttu-id="08f46-107">Windows Vista Home Premium</span><span class="sxs-lookup"><span data-stu-id="08f46-107">Windows Vista Home Premium</span></span>
-   <span data-ttu-id="08f46-108">Windows Vista Ultimate</span><span class="sxs-lookup"><span data-stu-id="08f46-108">Windows Vista Ultimate</span></span>

<span data-ttu-id="08f46-109">Родительский контроль устанавливается только на эти номера SKU.</span><span class="sxs-lookup"><span data-stu-id="08f46-109">Parental Controls only installs on these SKUs.</span></span> <span data-ttu-id="08f46-110">Решения, требующие развертывания на SKU для бизнеса, должны иметь одно из следующих:</span><span class="sxs-lookup"><span data-stu-id="08f46-110">Solutions having a requirement to deploy onto business SKUs will need to either:</span></span>

-   <span data-ttu-id="08f46-111">Обнаруживать и не предоставлять функции родительского контроля в SKU для бизнеса.</span><span class="sxs-lookup"><span data-stu-id="08f46-111">Detect and not provide parental controls functionality on business SKUs.</span></span>
-   <span data-ttu-id="08f46-112">Обнаружение и предоставление альтернативных средств настройки, ведения журнала и ограничений.</span><span class="sxs-lookup"><span data-stu-id="08f46-112">Detect and provide an alternative means of configuration, logging, and restrictions.</span></span>

<span data-ttu-id="08f46-113">Рекомендуется, чтобы решения определяли доступность инфраструктуры родительского контроля, проверяя успешность выполнения CoCreateInstance COM в API соответствия.</span><span class="sxs-lookup"><span data-stu-id="08f46-113">It is recommended that solutions detect availability of the Parental Controls Infrastructure by checking for success of COM CoCreateInstance on the Compliance API.</span></span>

<span data-ttu-id="08f46-114">Приложения, поддерживающие родительский контроль, в зависимости от инфраструктуры Windows Vista, также могут подавить отключение любого собственного пользовательского интерфейса, предоставляющего параметры или другие функциональные возможности, когда пользовательский интерфейс родительского контроля подавляется на поддерживаемом SKU.</span><span class="sxs-lookup"><span data-stu-id="08f46-114">Parental Controls-aware applications depending on the Windows Vista infrastructure may also want to suppress any of their own UI exposing settings or other functionality when Parental Controls UI is suppressed on a supported SKU.</span></span> <span data-ttu-id="08f46-115">Функция предназначена для определения видимости, которая охватывает такие случаи, как подавление присоединения к домену.</span><span class="sxs-lookup"><span data-stu-id="08f46-115">A function is provided for visibility determination that covers cases such as domain-joined suppression.</span></span>

 

 



