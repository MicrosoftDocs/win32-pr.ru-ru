---
description: Библиотека CertEnroll.dll реализует пять интерфейсов, которые можно использовать для создания запроса сертификата и управления им.
ms.assetid: f4630095-6ba2-46f7-8825-e7a5b1cb185a
title: Функции запроса сертификата
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e07fb348b335562863f04226a2fb729bfbcbdaba27cb574a04c87075a64653a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118902573"
---
# <a name="certificate-request-functions"></a>Функции запроса сертификата

Библиотека CertEnroll.dll реализует пять интерфейсов, которые можно использовать для создания запроса сертификата и управления им. Из них интерфейс [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) представляет абстрактный базовый объект, определяющий сигнатуры методов, наследуемые следующими четырьмя интерфейсами.

| Интерфейс                                                                        | Описание                                                                                                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IX509CertificateRequestCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate) | Позволяет создавать сертификаты напрямую без применения к [*центру сертификации*](/windows/desktop/SecGloss/c-gly) (ЦС).<br/>                                                                                                            |
| [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)                 | Представляет [*Управление сертификатами через CMS*](/windows/desktop/SecGloss/c-gly) (CMC) (сообщение управления сертификатами через CMS), которое может содержать вложенный \# запрос PKCS 10 или другой объект запроса CMC.<br/> |
| [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7)             | Представляет объект запроса синтаксиса сообщения [*PKCS \# 7*](/windows/desktop/SecGloss/p-gly) (CMS), который должен содержать вложенный \# запрос PKCS 10.<br/>                                                                                                         |
| [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)           | Представляет \# запрос сертификата PKCS 10. Запрос PKCS \# 10 может быть отправлен непосредственно в центр сертификации или может быть заключен в \# запрос PKCS 7 или CMC.<br/>                                                                                                                                                            |



 

Объект запроса сертификата можно использовать для инициализации объекта [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) для регистрации клиента в иерархии сертификатов и установки ответа сертификата, возвращенного ЦС.

В каждом из следующих разделов указывается функция, экспортируемая с помощью Xenroll.dll для создания, перечисления или удаления запросов сертификатов. В каждом разделе также обсуждается использование CertEnroll.dll для замены функции или указывает, что сопоставление между двумя библиотеками не существует:

-   [createFilePKCS10WStr](#createfilepkcs10wstr)
-   [креатефилерекуествстр](#createfilerequestwstr)
-   [createPKCS10WStr](#createpkcs10wstr)
-   [CreatePKCS7RequestFromRequest](#createpkcs7requestfromrequest)
-   [креатерекуествстр](#createrequestwstr)
-   [делетерекуестцерт](#deleterequestcert)
-   [енумпендингрекуествстр](#enumpendingrequestwstr)
-   [ремовепендингрекуествстр](#removependingrequestwstr)
-   [Сброс](#reset)
-   [сетпендингрекуестинфовстр](#setpendingrequestinfowstr)
-   [Связанные темы](#related-topics)

## <a name="createfilepkcs10wstr"></a>createFilePKCS10WStr

Функция [**createFilePKCS10WStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-createfilepkcs10wstr) в Xenroll.dll создает запрос сертификата PKCS 10 в кодировке Base64 \# и сохраняет его в файле.

Библиотека CertEnroll.dll не реализует напрямую функции для записи запроса в файл. Однако можно получить запрос на сертификат, вызвав свойство [**rawData**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_rawdata) объекта [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) и создав пользовательскую функцию для копирования значения в файл.

## <a name="createfilerequestwstr"></a>креатефилерекуествстр

Функция [**креатефилерекуествстр**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createfilerequestwstr) в Xenroll.dll создает \# запрос сертификата PKCS 7, PKCS \# 10 или CMC и сохраняет его в файле.

Библиотека CertEnroll.dll не реализует напрямую функции для записи запроса в файл. Однако можно получить запрос на сертификат, вызвав свойство [**rawData**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_rawdata) объекта [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) и создав пользовательскую функцию для копирования значения в файл.

## <a name="createpkcs10wstr"></a>createPKCS10WStr

Функция [**createPKCS10WStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-createpkcs10wstr) в Xenroll.dll создает \# запрос сертификата PKCS 10 и копирует его в массив байтов.

Вы можете использовать объект [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) для инициализации \# запроса PKCS 10 из существующего запроса, существующего сертификата, [*закрытого ключа*](/windows/desktop/SecGloss/p-gly), [*открытого ключа*](/windows/desktop/SecGloss/p-gly)или шаблона.

## <a name="createpkcs7requestfromrequest"></a>CreatePKCS7RequestFromRequest

Функция [**CreatePKCS7RequestFromRequest**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-createpkcs7requestfromrequest) в Xenroll.dll создает \# запрос сертификата PKCS 7 и копирует его в массив байтов.

Вы можете использовать объект [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) для инициализации \# запроса PKCS 7 из существующего запроса, существующего сертификата, объекта внутреннего запроса или шаблона.

## <a name="createrequestwstr"></a>креатерекуествстр

Функция [**креатерекуествстр**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createrequestwstr) в Xenroll.dll создает \# запрос сертификата PKCS 7, PKCS \# 10 или CMC и копирует его в массив байтов.

Чтобы использовать библиотеку CertEnroll.dll для создания запросов PKCS \# 7, PKCS \# 10 или CMC, можно создать и инициализировать экземпляры объектов [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7), [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)или [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) .

## <a name="deleterequestcert"></a>делетерекуестцерт

Функция [**делетерекуестцерт**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_deleterequestcert) в Xenroll.dll указывает или получает логическое значение, указывающее, удаляется ли фиктивный сертификат после установки ответа на сертификат.

Объект [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) в CertEnroll.dll автоматически создает фиктивные сертификаты в хранилище запросов для временного сохранения различных свойств сертификата, которые инициализируются во время процесса регистрации. После выдачи сертификата центром сертификации свойства копируются в новый сертификат и удаляется фиктивный сертификат. Библиотека CertEnroll.dll не позволяет принудительно оставаться фиктивным сертификатом после установки ответа на сертификат.

## <a name="enumpendingrequestwstr"></a>енумпендингрекуествстр

Функция [**енумпендингрекуествстр**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-enumpendingrequestwstr) в Xenroll.dll извлекает указанное значение свойства для ожидающего запроса.

Библиотека CertEnroll.dll напрямую не реализует функции для удаления ожидающего запроса на сертификат.

## <a name="removependingrequestwstr"></a>ремовепендингрекуествстр

Функция [**ремовепендингрекуествстр**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-removependingrequestwstr) в Xenroll.dll Удаляет ожидающий запрос из хранилища запросов.

Библиотека CertEnroll.dll напрямую не реализует функции для удаления ожидающего запроса на сертификат.

## <a name="reset"></a>Reset

Функция [**Reset**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-reset) в Xenroll.dll возвращает управление регистрацией сертификата в исходное состояние.

Тот же результат можно получить с помощью Certenroll.dll, чтобы создать новый объект запроса для требуемого типа.

## <a name="setpendingrequestinfowstr"></a>сетпендингрекуестинфовстр

Функция [**сетпендингрекуестинфовстр**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-setpendingrequestinfowstr) в Xenroll.dll задает свойства ожидающего запроса.

Библиотека CertEnroll.dll напрямую не реализует функции для удаления ожидающего запроса на сертификат. Можно вызвать свойство [**каконфигстринг**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_caconfigstring) объекта [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) , чтобы получить строку конфигурации, но только для активного объекта регистрации.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Сопоставление Xenroll.dll CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> <dt>

[**исигнерцертификате**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate)
</dt> <dt>

[**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest)
</dt> <dt>

[**IX509CertificateRequestCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate)
</dt> <dt>

[**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)
</dt> <dt>

[**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7)
</dt> <dt>

[**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)
</dt> <dt>

[**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)
</dt> </dl>

 

