---
description: Архитектуру сетевой монитор можно разделить на два набора концепций программирования, связанных с экспертом и разработкой анализатора, а также с разработчиками, связанными с разработкой мониторов.
ms.assetid: a775a46d-6f0f-4f21-8774-a061ccd55491
title: Архитектура сетевой монитор
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e75c1172d15211e64b425a87ccb9015339256b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664735"
---
# <a name="network-monitor-architecture"></a><span data-ttu-id="1048b-103">Архитектура сетевой монитор</span><span class="sxs-lookup"><span data-stu-id="1048b-103">Network Monitor Architecture</span></span>

<span data-ttu-id="1048b-104">Архитектуру сетевой монитор можно разделить на два набора концепций программирования, связанных с [*экспертом*](e.md) и разработкой [*анализатора*](p.md) , а также с разработчиками, связанными с разработкой [*мониторов*](m.md) .</span><span class="sxs-lookup"><span data-stu-id="1048b-104">The Network Monitor architecture can be separated into two sets of programming concepts, those related to [*expert*](e.md) and [*parser*](p.md) development and those related to [*monitor*](m.md) development.</span></span>

<span data-ttu-id="1048b-105">Хотя оба компонента используют одни и те же компоненты для захвата сетевого трафика, каждый из них использует разные интерфейсы для записи данных и различных компонентов для анализа того, что было захвачено.</span><span class="sxs-lookup"><span data-stu-id="1048b-105">Although both use the same components to capture the network traffic, they each use different interfaces to capture the data and different components to analyze what was captured.</span></span>



| <span data-ttu-id="1048b-106">Для получения информации о</span><span class="sxs-lookup"><span data-stu-id="1048b-106">For information on</span></span>                                                         | <span data-ttu-id="1048b-107">Перейти</span><span class="sxs-lookup"><span data-stu-id="1048b-107">Go to</span></span>                                                                |
|----------------------------------------------------------------------------|----------------------------------------------------------------------|
| <span data-ttu-id="1048b-108">Компоненты сетевой монитор, связанные с разработкой экспертов и средств синтаксического анализа</span><span class="sxs-lookup"><span data-stu-id="1048b-108">The components of Network Monitor related to expert and parser development</span></span> | [<span data-ttu-id="1048b-109">Архитектура эксперта и анализатора</span><span class="sxs-lookup"><span data-stu-id="1048b-109">Expert and Parser Architecture</span></span>](expert-and-parser-architecture.md) |
| <span data-ttu-id="1048b-110">Компоненты сетевой монитор, связанные с разработкой мониторов</span><span class="sxs-lookup"><span data-stu-id="1048b-110">The components of Network Monitor related to monitor development</span></span>           | [<span data-ttu-id="1048b-111">Мониторинг архитектуры</span><span class="sxs-lookup"><span data-stu-id="1048b-111">Monitor Architecture</span></span>](monitor-architecture.md)                     |



 

 

 



