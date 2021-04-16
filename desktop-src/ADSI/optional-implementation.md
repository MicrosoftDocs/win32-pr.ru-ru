---
title: Необязательная реализация
description: Следующие функции являются необязательными, но рекомендуется
ms.assetid: 6123bdda-06cf-4b8b-b2a8-89882b6341b4
ms.tgt_platform: multiple
keywords:
- Необязательная реализация ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 043b07f3a9bcfaef4bde8e95458d64828d4e46be
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104531841"
---
# <a name="optional-implementation"></a>Необязательная реализация

Следующие функции являются необязательными, но рекомендуется:

-   Интерфейс [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) для клиентов, не поддерживающих автоматизацию. Так как поставщик OLE DB ADSI использует **IDirectorySearch** для представления запросов и получения результатов из базовой службы каталогов, поставщики, реализующие этот интерфейс, автоматически предоставляют доступ к базам данных OLE DB стилей, не прибегая к реализации каких-либо дополнительных интерфейсов.
-   Интерфейсы [**иадссекуритидескриптор**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor), [**иадсакцессконтроллист**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)и [**иадсакцессконтролентри**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) . Поставщики служб каталогов, поддерживающие безопасность объектов на основе списков управления доступом, рекомендуется применять к этим дополнительным функциям.

 

 




