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
ms.openlocfilehash: c3584eed86abcaef019f0fc8f8bd794a80abca1143286317189889231bbc2cc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118882950"
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

 

 

 




