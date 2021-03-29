---
description: Сопоставление сертификатов
ms.assetid: 4139f927-54f4-4968-a9eb-020401bb536d
title: Сопоставление сертификатов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 397a9ef8822d4f191ae37cdb998166fa54c2b12d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103816033"
---
# <a name="mapping-certificates"></a>Сопоставление сертификатов

> [!Note]  
> Сведения в этом разделе действительны только для серверов, которым требуется проверка подлинности клиента.

 

Если серверное приложение требует проверки подлинности клиента, Schannel автоматически пытается сопоставить сертификат, предоставленный клиентом, с учетной записью пользователя.

После установки [*контекста безопасности*](../secgloss/s-gly.md) серверное приложение может использовать функцию [**куерисекуритиконтексттокен**](/windows/desktop/api/Sspi/nf-sspi-querysecuritycontexttoken) для получения [*маркера доступа*](../secgloss/a-gly.md) для учетной записи пользователя, с которой был сопоставлен [*сертификат клиента*](../secgloss/c-gly.md) . Кроме того, сервер может использовать функцию [**имперсонатесекуритиконтекст**](/windows/desktop/api/Sspi/nf-sspi-impersonatesecuritycontext) для олицетворения клиента.

Дополнительные сведения о проверке подлинности см. в разделе [выполнение проверки подлинности с помощью канала Schannel](performing-authentication-using-schannel.md).

 

 
