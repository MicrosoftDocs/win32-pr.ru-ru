---
description: Решение для обеспечения безопасности продуктов семейства Windows
ms.assetid: b89cf0c7-bf9f-4bcb-b008-8b7c792f3300
title: Решение для обеспечения безопасности продуктов семейства Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a2d8776893468df4f4877c7220436f505ab1e6f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647690"
---
# <a name="windows-family-safety-solution"></a><span data-ttu-id="d9b2c-103">Решение для обеспечения безопасности продуктов семейства Windows</span><span class="sxs-lookup"><span data-stu-id="d9b2c-103">Windows Family Safety Solution</span></span>

<span data-ttu-id="d9b2c-104">Ниже приведены основные требования, определяемые корпорацией Майкрософт для более полного решения.</span><span class="sxs-lookup"><span data-stu-id="d9b2c-104">Key requirements defined by Microsoft for a more comprehensive solution are as follows.</span></span> <span data-ttu-id="d9b2c-105">Обратите внимание, что определение Online — это основная технология, доступная в Интернете, в отличие от автономного клиента, который обычно ограничен на компьютере.</span><span class="sxs-lookup"><span data-stu-id="d9b2c-105">Note the definition for online is a primarily Internet-facing technology, unlike an offline client which is usually bounded at the computer.</span></span>

-   <span data-ttu-id="d9b2c-106">Предоставьте единую, простую в поиске область в пользовательском интерфейсе операционной системы, где все политики родительского контроля, контроль активности и данные о действиях для идентификации могут быть легко обнаружены.</span><span class="sxs-lookup"><span data-stu-id="d9b2c-106">Provide a single, easy to find area in the operating system user interface where all parental controls policies, control of activity monitoring, and activity data for an identity may be readily discovered.</span></span>

-   <span data-ttu-id="d9b2c-107">Поддержка мониторинга достаточных действий контролируемого пользователя, чтобы у родителя или опекуна была разумная уверенность в том, что могут быть обнаружены рискованные действия.</span><span class="sxs-lookup"><span data-stu-id="d9b2c-107">Support monitoring of sufficient activity of the controlled user so that a parent or guardian has reasonable confidence that risky activities may be discovered.</span></span> <span data-ttu-id="d9b2c-108">Кроме того, можно также перенастроить политики контролируемого пользователя, чтобы выявить ненужные или несанкционированные изменения.</span><span class="sxs-lookup"><span data-stu-id="d9b2c-108">Also, log reconfiguration of the controlled user's policies so that unintended or unauthorized changes are discoverable.</span></span>

-   <span data-ttu-id="d9b2c-109">Предоставьте возможности мониторинга действий с помощью стандартных интерфейсов для ведения журнала событий Windows Vista и предоставим решение в виде встроенного средства просмотра.</span><span class="sxs-lookup"><span data-stu-id="d9b2c-109">Expose activity monitoring capabilities through standard Windows Vista event logging interfaces, and provide an in-box viewer solution.</span></span> <span data-ttu-id="d9b2c-110">Определение стандартных событий действий и обеспечение расширяемости для создания пользовательских событий с помощью независимых поставщиков программных продуктов.</span><span class="sxs-lookup"><span data-stu-id="d9b2c-110">Define standard activity events, and provide for extensibility to custom event generation by ISVs.</span></span>

-   <span data-ttu-id="d9b2c-111">Продвигайте, что все мониторинг и ограничения для пользователя включаются только на основе родителей или опекунов.</span><span class="sxs-lookup"><span data-stu-id="d9b2c-111">Promote that all monitoring and restrictions for a user are turned on only on an opt-in basis by parents or guardians.</span></span> <span data-ttu-id="d9b2c-112">Везде, где это возможно, функции ограничений должны быть полностью неактивны для пользователей без контроля, чтобы снизить риски безопасности и угрозы совместимости приложений.</span><span class="sxs-lookup"><span data-stu-id="d9b2c-112">Wherever possible, restrictions functionality should be completely inactive for non-controlled users to minimize security and application compatibility risks.</span></span>

-   <span data-ttu-id="d9b2c-113">Корпорация Майкрософт стремится постараться, когда это возможно, не отказаться от значения возраста или других параметров для контролируемого пользователя (третьи стороны могут это сделать).</span><span class="sxs-lookup"><span data-stu-id="d9b2c-113">Microsoft shall strive, whenever possible, not to make value judgments by age or other parameters for the controlled user (third parties may choose to do so).</span></span> <span data-ttu-id="d9b2c-114">Такие решения остаются на родительском или опекуне, часто на которые влияют сообщества или организации.</span><span class="sxs-lookup"><span data-stu-id="d9b2c-114">Such decisions are left up to the parent or guardian, often influenced by communities or organizations.</span></span>

-   <span data-ttu-id="d9b2c-115">Предоставьте реализации в продукте для мониторинга автономных действий и ограничений, в которых нет доступных предложений в настоящее время, в которых имеется соответствующая функция риска, связанная с безопасностью, или решение Майкрософт, обеспечивающее поддержку и устойчивую функциональность, полностью интегрированную с архитектурой операционной системы.</span><span class="sxs-lookup"><span data-stu-id="d9b2c-115">Provide implementations in the product for offline activity monitoring and restrictions where few or no offerings are available today, where the associated safety-risk functionality is available in the product, or where a Microsoft solution provides capable and robust functionality fully integrated with the design of the operating system.</span></span>

-   <span data-ttu-id="d9b2c-116">Как правило, необходимо повысить уровень ведения журнала приложений и ограничений для лучшего контекста и пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="d9b2c-116">Generally, promote that applications perform their own logging and restrictions for best context and UI experience.</span></span>

    <span data-ttu-id="d9b2c-117">Исключение. предоставляет полный мониторинг активности в сети и ограничения в выбранных областях, в которых преимущество для потребителей и отрасли перевешивает затраты.</span><span class="sxs-lookup"><span data-stu-id="d9b2c-117">Exception: Provide comprehensive online activity monitoring and restrictions in selected areas where the benefit to consumers and industry outweigh the costs.</span></span>

-   <span data-ttu-id="d9b2c-118">Предоставьте родительским элементам управления параметры пользовательского интерфейса и определения событий действий с помощью общедоступных API, чтобы третьи стороны могли запрашивать состояние, изменять параметры и читать журналы действий, если они работают с достаточными привилегиями учетной записи Windows.</span><span class="sxs-lookup"><span data-stu-id="d9b2c-118">Expose parental controls user interface settings and activity event definitions by using public APIs so that third parties may query for state, modify settings, and read activity logs if they are running with sufficient Windows account privileges.</span></span>

<span data-ttu-id="d9b2c-119">Задача чрезмерного распространения состоит в том, чтобы повысить сосуществование сторонних решений для родительского контроля с помощью встроенной функциональности и поддерживать добавление ценности путем интеграции с, расширения или предоставления альтернативных возможностей, где это уместно.</span><span class="sxs-lookup"><span data-stu-id="d9b2c-119">An overarching goal is to promote third-party parental controls solutions' coexistence with the in-box functionality, and support adding value by integrating with, extending, or providing alternative capabilities where suitable.</span></span>

 

 



