---
description: Инициализирует \# объект запроса сертификата PKCS 10, заключает его в объект запроса CMC, отправляет запрос CMC в центр сертификации (ЦС) предприятия и сохраняет сертификат, возвращенный ЦС, в файле.
ms.assetid: 0231da3b-a183-4443-8735-5affd24b145a
title: енроллфромпубликкэй
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21b336d04727f4bb4b90674bad6bb6c429465a0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810696"
---
# <a name="enrollfrompublickey"></a>енроллфромпубликкэй

Пример Енроллфромпубликкэй инициализирует \# объект запроса сертификата PKCS 10, заключает его в объект запроса CMC, отправляет запрос CMC в центр сертификации предприятия (CA) и сохраняет сертификат, возвращенный ЦС, в файле.

## <a name="location"></a>Расположение

При установке пакета средств разработки программного обеспечения (SDK) для Microsoft Windows этот образец устанавливается по умолчанию в папке *% ProgramFiles%* \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ Security SSL \\ Certificate \\ \\ енроллфромпубликкэй.

## <a name="discussion"></a>Разговор

Пример Енроллфромпубликкэй:

1.  Обрабатывает следующие аргументы командной строки:
    -   Имя шаблона сертификата.
    -   Имя файла, в котором следует сохранить установленный сертификат в виде массива байтов в кодировке Base64.
    -   Необязательное имя шаблона сертификата подписи. Шаблон используется для создания сертификата подписи, если он отсутствует в хранилище сертификатов.
2.  Создает объект закрытого ключа [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) и вызывает метод [**CREATE**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-create) для создания асимметричного закрытого ключа с использованием поставщика служб шифрования по умолчанию, размера ключа и значений [**keySpec**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_keyspec) для текущего компьютера.
3.  Возвращает часть открытого ключа объекта [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) .
4.  Создает объект [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) и инициализирует его с помощью шаблона, указанного в командной строке и открытом ключе.
5.  Создает объект [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) и инициализирует его с помощью \# объекта запроса PKCS 10.
6.  Извлекает существующий сертификат подписи или, если его не удается найти, создает запрос сертификата из шаблона, указанного в командной строке, и пытается его зарегистрировать. Финдцертбикэйусаже определяется в Енроллкоммон. cpp.
7.  Проверяет цепочку сертификатов.
8.  Создает объект [**исигнерцертификате**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) , инициализирует его с помощью сертификата для подписи, получает коллекцию [**исигнерцертификатес**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates) из объекта запроса CMC и добавляет объект сертификата подписи в коллекцию.
9.  Кодирует запрос CMC с помощью [*distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (Der).
10. Создает объект [**ицертконфиг**](/windows/desktop/api/certcli/nn-certcli-icertconfig) и использует его для получения строки, СОДЕРЖАЩЕЙ конфигурацию ЦС.
11. Создает объект CryptoAPI [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) и использует его вместе со строками, содержащими конфигурацию ЦС и запросом сертификата для отправки запроса в ЦС.
12. Проверяет состояние процесса регистрации и сохраняет установленный сертификат в файл. Функция Енкодетофилев определена в Енроллкоммон. cpp.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Запрос CMC](cmc-request.md)
</dt> <dt>

[\#Запрос PKCS 10](pkcs--10-request.md)
</dt> <dt>

[Использование прилагаемых примеров](using-the-included-samples.md)
</dt> </dl>

 

 
