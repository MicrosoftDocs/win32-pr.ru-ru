---
description: Уровень данных часто содержит статическую информацию&\# 8212; сведения, сохраненные на устойчивом носителе.
ms.assetid: d2bce8b6-1f88-4e4a-bb08-fc7ee4c039da
title: Оптимизация вызовов между бизнес-логикой и данными COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3346f628344e7505fde03c3a64b7420d199312ee
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701206"
---
# <a name="optimizing-interactions-between-the-com-business-logic-tier-and-the-data-tier"></a><span data-ttu-id="82538-103">Оптимизация взаимодействия между уровнем бизнес-логики COM+ и уровнем данных</span><span class="sxs-lookup"><span data-stu-id="82538-103">Optimizing Interactions Between the COM+ Business Logic Tier and the Data Tier</span></span>

<span data-ttu-id="82538-104">Уровень данных часто содержит статическую информацию — информацию, сохраненную на устойчивом носителе.</span><span class="sxs-lookup"><span data-stu-id="82538-104">The data tier often contains mostly static information—information persisted on durable media.</span></span> <span data-ttu-id="82538-105">Поскольку этот уровень охватывает информацию, которая в основном является статичной, она требует тщательного анализа возможных узких мест.</span><span class="sxs-lookup"><span data-stu-id="82538-105">Because this tier encompasses information that is mostly static, it requires a thorough analysis for potential bottlenecks.</span></span> <span data-ttu-id="82538-106">В дополнение к очевидным возможным узким местам при подключении, горячие участки могут быть вызваны часто используемыми записями, неэффективными методами доступа к данным и нуждаются в координации доступа к устаревшим системам.</span><span class="sxs-lookup"><span data-stu-id="82538-106">In addition to the obvious possibility for connection bottlenecks, hot spots can be caused by frequently accessed records, inefficient data access methods, and the need to coordinate access to legacy systems.</span></span>

## <a name="connecting-to-the-data-tier"></a><span data-ttu-id="82538-107">Подключение к уровню данных</span><span class="sxs-lookup"><span data-stu-id="82538-107">Connecting to the Data Tier</span></span>

<span data-ttu-id="82538-108">При проектировании уровня данных для приложения COM+ необходимо учитывать два фактора: создание пулов подключений и JIT- [Активация COM+](com--just-in-time-activation.md), а также использование DSN.</span><span class="sxs-lookup"><span data-stu-id="82538-108">Two considerations play an important role in designing a data tier for a COM+ application: connection pooling and [COM+ just-in-time (JIT) activation](com--just-in-time-activation.md), and the use of DSNs.</span></span> <span data-ttu-id="82538-109">Компоненты, которые устанавливают соединения с уровнем данных, должны использовать для компонента набор [группирования объектов COM+](com--object-pooling.md) .</span><span class="sxs-lookup"><span data-stu-id="82538-109">Components that make connections to the data tier should use [COM+ object pooling](com--object-pooling.md) set on the component.</span></span>

<span data-ttu-id="82538-110">При создании имен DSN используйте строки конструктора объектов, указанные в компоненте, а не создавая Файловый DSN.</span><span class="sxs-lookup"><span data-stu-id="82538-110">When creating DSNs, use object constructor strings specified on the component instead of creating a File DSN.</span></span> <span data-ttu-id="82538-111">Файловые DSN выполняются медленнее, чем соединение с помощью строки конструктора объекта.</span><span class="sxs-lookup"><span data-stu-id="82538-111">File DSNs are slower than a connection using an object constructor string.</span></span> <span data-ttu-id="82538-112">Строки конструктора объектов можно указать на странице свойств компонента.</span><span class="sxs-lookup"><span data-stu-id="82538-112">Object constructor strings can be specified on the component property sheet.</span></span> <span data-ttu-id="82538-113">Дополнительные сведения см. в разделе [строки конструктора объектов COM+](com--object-constructor-strings.md).</span><span class="sxs-lookup"><span data-stu-id="82538-113">For more information, see [COM+ Object Constructor Strings](com--object-constructor-strings.md).</span></span>

<span data-ttu-id="82538-114">Если для доступа к SQL Server базе данных используются компоненты, используйте пул объектов COM+, а не пулы соединений SQL.</span><span class="sxs-lookup"><span data-stu-id="82538-114">If you are using components to access a SQL Server database, use COM+ object pooling instead of SQL connection pooling.</span></span>

<span data-ttu-id="82538-115">Если компонент использует ADO для выборки нескольких наборов записей, установите несколько соединений для компонента.</span><span class="sxs-lookup"><span data-stu-id="82538-115">If your component is using ADO to fetch multiple recordsets, establish multiple connections for the component.</span></span> <span data-ttu-id="82538-116">Когда ADO извлекает несколько наборов записей, он создает несколько соединений в фоновом режиме, если они не созданы.</span><span class="sxs-lookup"><span data-stu-id="82538-116">When ADO retrieves multiple recordsets, it creates multiple connections in the background if you do not create them.</span></span> <span data-ttu-id="82538-117">Если вы создали их, их можно создать в пул и получить больший контроль над количеством используемых подключений.</span><span class="sxs-lookup"><span data-stu-id="82538-117">If you create them, you can pool them and have more control over the number of the connections used.</span></span>

## <a name="related-topics"></a><span data-ttu-id="82538-118">См. также</span><span class="sxs-lookup"><span data-stu-id="82538-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82538-119">Оптимизация взаимодействия между уровнем представления и бизнес-логики COM+</span><span class="sxs-lookup"><span data-stu-id="82538-119">Optimizing Interactions Between the COM+ Business Logic Tier and the Presentation Tier</span></span>](optimizing-interactions-between-the-com--business-logic-tier-and-the-presentation-tier.md)
</dt> </dl>

 

 



