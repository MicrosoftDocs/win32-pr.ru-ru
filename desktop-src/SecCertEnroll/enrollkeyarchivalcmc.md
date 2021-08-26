---
description: Создает запрос на сертификат CMC для архивации закрытого ключа в центре сертификации (ЦС).
ms.assetid: b063989a-fe92-4c2c-9d66-8a14bc830f6b
title: енроллкэйарчивалкмк
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9e2e9856309560e982e7e1dda7ba724fefd0759e6fa10196b321eb66947cf64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119882954"
---
# <a name="enrollkeyarchivalcmc"></a>енроллкэйарчивалкмк

Пример Енроллкэйарчивалкмк создает запрос на сертификат CMC для архивации закрытого ключа в центре сертификации (ЦС). Дополнительные сведения см. в разделе [запрос на архивирование ключа CMC](cmc-key-archival-request.md).

## <a name="location"></a>Расположение

при установке пакета microsoft Windows Software Development Kit (SDK) образец устанавливается по умолчанию в папке *% ProgramFiles%* \\ Microsoft sdk \\ Windows \\ v 7.0 \\ samples \\ Security ssl \\ Certificate \\ \\ енроллкэйарчивалкмк.

## <a name="discussion"></a>Разговор

Пример Енроллкэйарчивалкмк:

1.  Обрабатывает аргументы командной строки. Командная строка должна содержать имя шаблона сертификата, который будет использоваться для регистрации.
2.  Создает объект запроса сертификата [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) и инициализирует его для контекста конечного пользователя с помощью имени шаблона.
3.  Задает свойство [**арчивеприватекэй**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_archiveprivatekey) для запроса CMC.
4.  Создает объект [**ицертконфиг**](/windows/desktop/api/certcli/nn-certcli-icertconfig) и использует его для получения строки, СОДЕРЖАЩЕЙ конфигурацию ЦС.
5.  Создает объект CryptoAPI [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) и использует его для получения сертификата Exchange для центра сертификации.
6.  Создает объект [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) , инициализирует его с помощью запроса CMC, создает строку в кодировке Base64, содержащую запрос на архивацию ключа, и отправляет его в центр сертификации.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Запрос на архивацию ключа CMC](cmc-key-archival-request.md)
</dt> <dt>

[Запрос CMC](cmc-request.md)
</dt> <dt>

[Использование прилагаемых примеров](using-the-included-samples.md)
</dt> </dl>

 

 
