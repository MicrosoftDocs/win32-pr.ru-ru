---
title: Основные изменения с момента выпуска Windows 7 для обеспечения совместимости
description: Основные изменения с момента выпуска Windows 7 для обеспечения совместимости
ms.assetid: 6930AA8C-B9AE-44C0-BC7F-12342DBBEB5E
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9ee24b18be55ff498d6c3870f77a32270df68284
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331616"
---
# <a name="key-changes-since-windows-7-to-ensure-compatibility"></a><span data-ttu-id="fe8f4-103">Основные изменения с момента выпуска Windows 7 для обеспечения совместимости</span><span class="sxs-lookup"><span data-stu-id="fe8f4-103">Key changes since Windows 7 to ensure compatibility</span></span>

<span data-ttu-id="fe8f4-104">Мы понимаем, что задача обеспечения совместимости очень важна для разработчиков.</span><span class="sxs-lookup"><span data-stu-id="fe8f4-104">We understand that compatibility matters to developers.</span></span> <span data-ttu-id="fe8f4-105">Независимые поставщики программных продуктов и разработчики хотят, чтобы их приложения работали ожидаемым образом во всех поддерживаемых версиях операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="fe8f4-105">ISVs and developers want to ensure their apps will run as expected on all supported versions of the Windows OS.</span></span> <span data-ttu-id="fe8f4-106">Для потребителей и организаций совместимость также играет ключевую роль в контексте инвестиций — они хотят, чтобы приложения, за которые они заплатили, продолжали работать без перебоев.</span><span class="sxs-lookup"><span data-stu-id="fe8f4-106">Consumers and businesses have a key investment here—they want to ensure that the apps they have paid for will continue to work.</span></span> <span data-ttu-id="fe8f4-107">Мы знаем, что совместимость является основным критерием в вопросе принятия решений о покупке.</span><span class="sxs-lookup"><span data-stu-id="fe8f4-107">We know that compatibility is the primary criteria for purchase decisions.</span></span> <span data-ttu-id="fe8f4-108">Приложения, которые хорошо пишутся на основе рекомендаций, приведут к гораздо меньшему объему обработки кода при выпуске новой версии Windows и снижению фрагментации — эти приложения имеют меньшую рентабельность в сфере обслуживания и быстрее на рынке.</span><span class="sxs-lookup"><span data-stu-id="fe8f4-108">Apps that are well written based on best practices will lead to much less code churn when a new Windows version is released, and will reduce fragmentation—these apps have a reduced engineering investment to maintain, and a faster time to market.</span></span>

<span data-ttu-id="fe8f4-109">В рамках временного периода, в течение которого выполнялась доработка Windows 7, к решению проблем совместимости применялся реактивный подход.</span><span class="sxs-lookup"><span data-stu-id="fe8f4-109">In the Windows 7 timeframe, compatibility was very much a reactive approach.</span></span> <span data-ttu-id="fe8f4-110">Работая над Windows 8, мы взглянули на эту задачу под другим углом и сконцентрировались на том, чтобы совместимость была заложена в ОС изначально, а не являлась доработкой.</span><span class="sxs-lookup"><span data-stu-id="fe8f4-110">In Windows 8, we started looking at this differently, working within Windows to ensure that compatibility was by design rather than an afterthought.</span></span> <span data-ttu-id="fe8f4-111">На данный момент Windows 10 обладает самыми широкими предварительно встроенными возможностями совместимости по сравнению с остальными версиями ОС.</span><span class="sxs-lookup"><span data-stu-id="fe8f4-111">Windows 10 is the most compatible-by-design version of the OS to date.</span></span> <span data-ttu-id="fe8f4-112">Нам удалось добиться этого благодаря следующему.</span><span class="sxs-lookup"><span data-stu-id="fe8f4-112">Here are some key ways we accomplished this:</span></span>

-   <span data-ttu-id="fe8f4-113">Данные телеметрии приложений. Это помогает нам понять популярность приложений в экосистеме Windows, чтобы информировать о тестировании на совместимость.</span><span class="sxs-lookup"><span data-stu-id="fe8f4-113">App telemetry: this helps us understand app popularity in the Windows ecosystem to inform compatibility testing.</span></span>
-   <span data-ttu-id="fe8f4-114">Партнерское по независимых поставщиков программного обеспечения: непосредственная работа с внешними партнерами для предоставления им данных и помощь в устранении проблем, с которыми сталкиваются пользователи.</span><span class="sxs-lookup"><span data-stu-id="fe8f4-114">ISV partnerships: work directly with external partners to provide them with data and help fix issues that our users experience.</span></span>
-   <span data-ttu-id="fe8f4-115">Проверки проектирования, вышестоящее обнаружение: партнер с специализированными группами для уменьшения количества критических изменений в Windows.</span><span class="sxs-lookup"><span data-stu-id="fe8f4-115">Design reviews, upstream detection: partner with feature teams to reduce the number of breaking changes in Windows.</span></span> <span data-ttu-id="fe8f4-116">Проверка совместимости стала обязательным этапом для групп по разработке функций.</span><span class="sxs-lookup"><span data-stu-id="fe8f4-116">Compatibility review is a gate that our feature teams must pass.</span></span>
-   <span data-ttu-id="fe8f4-117">Более строгий контроль над изменениями API & улучшенное взаимодействие</span><span class="sxs-lookup"><span data-stu-id="fe8f4-117">Tighter control over API changes & improved communication</span></span>
-   <span data-ttu-id="fe8f4-118">Цикл рейса и обратной связи. Заполнение программы предварительной оценки Windows позволяет улучшить возможности поиска проблем совместимости до выпуска окончательной сборки для клиентов.</span><span class="sxs-lookup"><span data-stu-id="fe8f4-118">Flighting and feedback loop: The Windows Insider population receives flighted builds that help improve our ability to find compatibility issues before a final build is released to customers.</span></span> <span data-ttu-id="fe8f4-119">Такая обратная связь не только позволяет нам выявлять ошибки, но и гарантирует, что мы предоставляем нашим пользователям нужные функции.</span><span class="sxs-lookup"><span data-stu-id="fe8f4-119">This feedback process not only exposes bugs, but ensures we are shipping features our users want.</span></span>

 

 




