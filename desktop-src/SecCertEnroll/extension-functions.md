---
description: Формат сертификата X. 509 версии 3 определяет несколько расширений, которые могут быть добавлены к сертификату для предоставления расширенной информации об использовании ключа, политиках сертификатов и ограничениях, других формах имен и т. д.
ms.assetid: d53107b7-a153-41cf-9876-1d28aaf99816
title: Функции расширения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da84fbe58e4b3cdb3bd510b8ec33bedd0ab7af29f3c0a592724f2711bb9bedd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117779867"
---
# <a name="extension-functions"></a>Функции расширения

Формат сертификата [*X. 509*](/windows/desktop/SecGloss/x-gly) версии 3 определяет несколько расширений, которые могут быть добавлены к сертификату для предоставления расширенной информации об использовании ключа, политиках сертификатов и ограничениях, других формах имен и т. д.

CertEnroll.dll реализует следующие интерфейсы для управления расширениями сертификатов:

-   [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)
-   [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions)
-   [**IX509ExtensionAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionalternativenames)
-   [**IX509ExtensionAuthorityKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionauthoritykeyidentifier)
-   [**IX509ExtensionBasicConstraints**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionbasicconstraints)
-   [**IX509ExtensionCertificatePolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensioncertificatepolicies)
-   [**IX509ExtensionEnhancedKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage)
-   [**IX509ExtensionKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionkeyusage)
-   [**IX509ExtensionMSApplicationPolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionmsapplicationpolicies)
-   [**IX509ExtensionSmimeCapabilities**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsmimecapabilities)
-   [**IX509ExtensionSubjectKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsubjectkeyidentifier)
-   [**IX509ExtensionTemplate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplate)
-   [**IX509ExtensionTemplateName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplatename)

В каждом из следующих разделов обсуждается функция, экспортируемая с помощью Xenroll.dll для управления расширениями сертификатов. В каждом разделе также обсуждается использование CertEnroll.dll для замены функции или указывает, что сопоставление между двумя библиотеками не существует:

-   [аддцерттипеторекуествстр](#addcerttypetorequestwstr)
-   [аддцерттипеторекуествстрекс](#addcerttypetorequestwstrex)
-   [аддекстенсионсторекуест](#addextensionstorequest)
-   [аддекстенсионторекуествстр](#addextensiontorequestwstr)
-   [енаблесмимекапабилитиес](#enablesmimecapabilities)
-   [инклудесубжекткэйид](#includesubjectkeyid)
-   [ресетекстенсионс](#resetextensions)
-   [Связанные темы](#related-topics)

## <a name="addcerttypetorequestwstr"></a>аддцерттипеторекуествстр

Функция [**аддцерттипеторекуествстр**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-addcerttypetorequestwstr) в Xenroll.dll добавляет к запросу шаблон сертификата по имени.

С помощью CertEnroll.dll предпочтительным методом включения шаблона в запрос на сертификат является использование метода [**инитиализефромтемплатенаме**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-initializefromtemplatename) для \# объекта запроса PKCS 10 или [* PKCS) или метода [**инитиализефроминнеррекуесттемплатенаме**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-initializefrominnerrequesttemplatename) в запросе CMC.

Если конкретный шаблон недоступен на клиенте, но должен быть понят [*центром сертификации*](/windows/desktop/SecGloss/c-gly) (ЦС), можно использовать интерфейс [**IX509ExtensionTemplateName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplatename) для добавления шаблона версии 1 или использовать интерфейс [**IX509ExtensionTemplate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplate) для добавления шаблона версии 2 к запросу на сертификат. Например, чтобы добавить шаблон версии 1, выполните следующие действия.

1.  Создайте объект [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) .
2.  Создайте объект [**IX509ExtensionTemplateName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplatename) и вызовите метод [**инитиализинкоде**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509extensiontemplatename-initializeencode) , указав имя шаблона.
3.  Добавьте расширение, созданное в коллекцию [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) , вызвав метод [**Add**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509extensions-add) .
4.  Создайте объект [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) и вызовите метод [**инитиализинкоде**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509attributeextensions-initializeencode) , указав коллекцию [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) во входных данных.
5.  Получите объект коллекции [**икриптаттрибутес**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) , вызвав свойство [**криптаттрибутес**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_cryptattributes) для существующего объекта запроса [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) или [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) .

## <a name="addcerttypetorequestwstrex"></a>аддцерттипеторекуествстрекс

Функция [**аддцерттипеторекуествстрекс**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-addcerttypetorequestwstrex) в Xenroll.dll добавляет шаблон сертификата к запросу по имени, идентификатору объекта и версии.

Сведения об использовании CertEnroll.dll для включения сведений о шаблоне в запрос см. в разделе Аддцерттипеторекуествстр.

## <a name="addextensionstorequest"></a>аддекстенсионсторекуест

Функция [**аддекстенсионсторекуест**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-addextensionstorequest) в Xenroll.dll Добавляет коллекцию расширений в запрос.

В CertEnroll.dll расширения добавляются в коллекцию Attributes запроса CMC или PKCS \# 10. Чтобы добавить расширения, выполните следующие действия.

1.  Создайте объект [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) .
2.  Создайте объект [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) и вызовите метод [**Initialize**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509extension-initialize) , чтобы создать расширение на основе идентификатора объекта и значения расширения или использовать любой из перечисленных выше интерфейсов, чтобы определить одно из более распространенных расширений.
3.  Добавьте каждое новое расширение, созданное на предыдущем шаге, в коллекцию [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) , вызвав метод [**Add**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509extensions-add) .

## <a name="addextensiontorequestwstr"></a>аддекстенсионторекуествстр

Функция [**аддекстенсионторекуествстр**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-addextensiontorequestwstr) в Xenroll.dll добавляет к запросу определенное расширение.

В CertEnroll.dll конкретное расширение должно быть определено и Добавлено в коллекцию Extensions перед добавлением коллекции Extensions в коллекцию Attributes запроса CMC или PKCS \# 10. Дополнительные сведения см. в обсуждении Аддекстенсионсторекуест выше.

## <a name="enablesmimecapabilities"></a>енаблесмимекапабилитиес

Функция [**енаблесмимекапабилитиес**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-get_enablesmimecapabilities) в Xenroll.dll указывает или получает логическое значение, указывающее, следует ли добавить расширение **смимекапабилитиес** в запрос.

Можно вызвать свойство [**смимекапабилитиес**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_smimecapabilities) объекта [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) , чтобы автоматически добавить объект [**IX509ExtensionSmimeCapabilities**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsmimecapabilities) в запрос перед кодированием.

## <a name="includesubjectkeyid"></a>инклудесубжекткэйид

Функция [**инклудесубжекткэйид**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-get_includesubjectkeyid) в Xenroll.dll указывает или получает логическое значение, указывающее, следует ли добавить расширение **субжекткэйидентифиер** в запрос.

По умолчанию расширение **субжекткэйидентифиер** создается при инициализации объекта запроса [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) . Это поведение можно переопределить, вызвав свойство [**суппрессоидс**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_suppressoids) .

Если у вас есть [*пара из открытого и закрытого ключей*](/windows/desktop/SecGloss/p-gly), можно также использовать интерфейс [**IX509ExtensionSubjectKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsubjectkeyidentifier) в CertEnroll.dll, чтобы добавить расширение **субжекткэйидентифиер** к запросу сертификата, выполнив следующие действия.

1.  Создайте объект [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) .
2.  Создайте объект [**IX509ExtensionSubjectKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsubjectkeyidentifier) и вызовите метод [**инитиализинкоде**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509extensionsubjectkeyidentifier-initializeencode) , указав строку, содержащую идентификатор. Как правило, это 20-байтовый хэш SHA-1 [*открытого ключа*](/windows/desktop/SecGloss/p-gly) , содержащегося в сертификате подписи ЦС.
3.  Добавьте расширение, созданное в коллекцию [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) , вызвав метод [**Add**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509extensions-add) .
4.  Создайте объект [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) и вызовите метод [**инитиализинкоде**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509attributeextensions-initializeencode) , указав коллекцию [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) во входных данных.
5.  Получите объект коллекции [**икриптаттрибутес**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) , вызвав свойство [**криптаттрибутес**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_cryptattributes) для существующего объекта запроса [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) или [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) .

## <a name="resetextensions"></a>ресетекстенсионс

Функция [**ресетекстенсионс**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-resetextensions) в Xenroll.dll удаляет коллекцию расширений из запроса.

Чтобы удалить расширение из запроса по номеру индекса с помощью CertEnroll.dll, вызовите метод [**Remove**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509extensions-remove) в коллекции [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) . Чтобы удалить все атрибуты из запроса, вызовите метод [**clear**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509extensions-clear) .

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Сопоставление Xenroll.dll CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> <dt>

[**икриптаттрибутес**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes)
</dt> <dt>

[**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)
</dt> <dt>

[**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions)
</dt> </dl>

 

 
