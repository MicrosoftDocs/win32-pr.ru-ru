---
title: Примеры расширения вспомогательного класса NDF
description: Эти примеры применяются только в том случае, если разработчики считают, что необходимо расширить функциональные возможности вспомогательного класса Microsoft NDF, который объявлен как расширяемый.
ms.assetid: 048e42f5-66d8-41c6-9e97-8da68c9ad151
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b3ecf34bb8e90aad8c28f582860d44e81706e77
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103772608"
---
# <a name="ndf-helper-class-extension-examples"></a><span data-ttu-id="eb6da-103">Примеры расширения вспомогательного класса NDF</span><span class="sxs-lookup"><span data-stu-id="eb6da-103">NDF Helper Class Extension Examples</span></span>

<span data-ttu-id="eb6da-104">Эти примеры применяются только в том случае, если разработчики считают, что необходимо расширить функциональные возможности вспомогательного класса Microsoft NDF, который объявлен как расширяемый.</span><span class="sxs-lookup"><span data-stu-id="eb6da-104">These examples apply only when developers believe it is necessary to extend the functionality of a Microsoft NDF Helper Class that is declared to be extensible.</span></span> <span data-ttu-id="eb6da-105">Как правило, это необязательно, но в некоторых случаях уникальные диагностические возможности представляют себя в связи с определенными требованиями к оборудованию или программному обеспечению компонента.</span><span class="sxs-lookup"><span data-stu-id="eb6da-105">This is generally not necessary, but in some cases, unique diagnostic opportunities present themselves because of the specific hardware or software requirements of the component.</span></span>

<span data-ttu-id="eb6da-106">Два приведенных ниже примера связаны друг с другом, прежде чем анализировать вторую.</span><span class="sxs-lookup"><span data-stu-id="eb6da-106">The two examples that follow are related and the first should be understood before analyzing the second.</span></span> <span data-ttu-id="eb6da-107">Первый предоставляет реализацию [расширения вспомогательного класса ndf](ndf-helper-class-example.md) с помощью класса с именем симплехелперфилекласс.</span><span class="sxs-lookup"><span data-stu-id="eb6da-107">The first provides an implementation of an [NDF Helper Class Extension](ndf-helper-class-example.md) using a class called SimpleHelperFileClass.</span></span>

<span data-ttu-id="eb6da-108">Второе, [вспомогательное расширение класса ndf с](ndf-helper-class-example-with-handoff.md)передачей, предоставляет пример расширения, которое не выполняет определенные диагностические задачи, но создает низкую гипотезу о работоспособности для симплехелперфилекласс в первом примере.</span><span class="sxs-lookup"><span data-stu-id="eb6da-108">The second, [NDF Helper Class Extension with Handoff](ndf-helper-class-example-with-handoff.md), provides an example of an extension that does not perform specific diagnostic tasks but only generates a low health hypothesis for the SimpleHelperFileClass in the first example.</span></span>

 

 




