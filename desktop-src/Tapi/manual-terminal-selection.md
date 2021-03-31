---
description: Если правила выбора по умолчанию не соответствуют потребностям приложения, приложение может выбрать терминал вручную.
ms.assetid: 12d7781e-a27d-4cbe-b7c4-6c0dfef11074
title: Выбор терминала вручную
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95335402690c57cc3f564f5d238ca031df4b3549
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812485"
---
# <a name="manual-terminal-selection"></a><span data-ttu-id="b60d5-103">Выбор терминала вручную</span><span class="sxs-lookup"><span data-stu-id="b60d5-103">Manual Terminal Selection</span></span>

<span data-ttu-id="b60d5-104">Если правила выбора по умолчанию не соответствуют потребностям приложения, приложение имеет возможность выбрать терминал, как всегда имеет значение. это значит, что он может использовать [**итстреам**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) для перечисления потоков, имеющихся в вызове, и выбора терминала в соответствующих потоках (или, в случае с многодорожкными терминалами, создавать дорожки для потоков и выбрать созданные записи в потоках).</span><span class="sxs-lookup"><span data-stu-id="b60d5-104">If the rules of Default selection do not meet the needs of the application, the application has the option of selecting the terminal as it always has: that is, it can use [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) to enumerate the streams present on the call and select the terminal on the appropriate streams (or, in case of multitrack terminals, create tracks for the streams and select created tracks on the streams).</span></span>

 

 
