---
description: Для программной настройки сервера политики регистрации сертификатов (CEP) можно использовать следующие интерфейсы.
ms.assetid: 48c7c21c-1b20-4a79-932d-bed19ff9833e
title: Интерфейсы сервера политики сертификатов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e50c16373c2bac364a91af2cdadf6a8d33445e8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543535"
---
# <a name="certificate-policy-server-interfaces"></a>Интерфейсы сервера политики сертификатов

Для программной настройки сервера политики регистрации сертификатов (CEP) можно использовать следующие интерфейсы.



| Интерфейс                                                            | Описание                                                                                                   |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [**IX509EnrollmentPolicyServer**](/windows/desktop/api/Certenroll/nn-certenroll-ix509enrollmentpolicyserver)   | Представляет сервер обработки сложных событий.                                                                                      |
| [**IX509PolicyServerListManager**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509policyserverlistmanager) | Управляет коллекцией объектов [**IX509PolicyServerUrl**](/windows/desktop/api/Certenroll/nn-certenroll-ix509policyserverurl) .                         |
| [**IX509PolicyServerUrl**](/windows/desktop/api/Certenroll/nn-certenroll-ix509policyserverurl)                 | Указывает или получает значения свойств, связанные с сервером обработки сложных событий, и обновляет связанные значения реестра. |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Интерфейсы Цертенролл](certenroll-interfaces.md)
</dt> </dl>

 

 



