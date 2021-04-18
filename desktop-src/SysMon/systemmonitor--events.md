---
title: События Системмонитор
description: Класс Системмонитор содержит следующие события.
ms.assetid: 64d9befd-5ea0-4888-b0fb-cff889f1d188
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 94247cf81fcaf57f373c731cd4eaf06a3ca897ba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105661481"
---
# <a name="systemmonitor-events"></a>События Системмонитор

Класс [**системмонитор**](systemmonitor.md) имеет следующие события:

-   [**онкаунтераддед**](systemmonitor-oncounteradded.md)
-   [**онкаунтерделетед**](-systemmonitor-oncounterdeleted.md)
-   [**онкаунтерселектед**](-systemmonitor-oncounterselected.md)
-   [**ондблкликк**](-systemmonitor-ondblclick.md)
-   [**онсамплеколлектед**](-systemmonitor-onsamplecollected.md)

> [!Note]  
> Необходимо возвратить из обработчика событий до истечения [**интервала обновления**](systemmonitor-updateinterval.md) . в противном случае СИСМОН отображает окно сообщения, указывающее пользователю, что ему не удалось выполнить выборку значений счетчиков для предыдущего интервала обновления.

 

 

 




