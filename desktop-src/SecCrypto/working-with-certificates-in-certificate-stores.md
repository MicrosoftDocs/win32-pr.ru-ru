---
description: Несколько функций добавляют контекст сертификата или ссылку на контекст в \[ пакет средств разработки для платформы магазина (SDK) \] .
ms.assetid: 0355b254-be52-4af4-9567-ee2df092075f
title: Работа с сертификатами в хранилищах сертификатов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ba1ce89c9b9352ef787ed65230b709967125532
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347662"
---
# <a name="working-with-certificates-in-certificate-stores"></a>Работа с сертификатами в хранилищах сертификатов

Несколько функций добавляют контекст сертификата или ссылку на контекст в хранилище.

Для сертификатов, которые уже находятся в форме контекста сертификата:

-   [**цертаддцертификатеконтексттосторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatecontexttostore)
-   [**цертаддкрлконтексттосторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcrlcontexttostore)
-   [**цертаддктлконтексттосторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddctlcontexttostore)
-   [**цертаддцертификателинктосторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatelinktostore)
-   [**цертаддкрллинктосторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcrllinktostore)
-   [**цертаддктллинктосторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddctllinktostore)

Для сертификатов в кодированной форме, но не полных контекстов сертификатов:

-   [**CertAddEncodedCertificateToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedcertificatetostore)
-   [**цертадденкодедкрлтосторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedcrltostore)
-   [**цертадденкодедктлтосторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedctltostore)

Следующие функции удаляют сертификат, список отзыва сертификатов или CTL из хранилища, уменьшая число ссылок на единицу. Если это приводит к тому, что счетчик ссылок будет обнулен, то память, используемая для хранения сертификата, списка отзыва сертификатов или CTL, освобождается.

-   [**цертделетецертификатефромсторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletecertificatefromstore)
-   [**цертделетекрлфромсторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletecrlfromstore)
-   [**цертделетектлфромсторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletectlfromstore)

 

 



