---
title: Необязательная реализация
description: Следующие функции являются необязательными, но рекомендуется
ms.assetid: 6123bdda-06cf-4b8b-b2a8-89882b6341b4
ms.tgt_platform: multiple
keywords:
- Необязательная реализация ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3074f3ef6b4d36713d483937ad0f6ef10167777a7c36f8d21427d7df2b0485a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117838954"
---
# <a name="optional-implementation"></a>Необязательная реализация

Следующие функции являются необязательными, но рекомендуется:

-   Интерфейс [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) для клиентов, не поддерживающих автоматизацию. Так как поставщик OLE DB ADSI использует **IDirectorySearch** для представления запросов и получения результатов из базовой службы каталогов, поставщики, реализующие этот интерфейс, автоматически предоставляют доступ к базам данных OLE DB стилей, не прибегая к реализации каких-либо дополнительных интерфейсов.
-   Интерфейсы [**иадссекуритидескриптор**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor), [**иадсакцессконтроллист**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)и [**иадсакцессконтролентри**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) . Поставщики служб каталогов, поддерживающие безопасность объектов на основе списков управления доступом, рекомендуется применять к этим дополнительным функциям.

 

 




