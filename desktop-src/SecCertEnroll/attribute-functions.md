---
description: В запрос на сертификат можно добавить атрибуты, чтобы предоставить центр сертификации (ЦС) с дополнительными сведениями, которые он может использовать при создании и выдаче сертификата.
ms.assetid: 3eba5a2f-eeac-4e38-8705-b12bc183b7eb
title: Функции атрибутов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6413da0d43c142373e6f3cabe3d8e31636b82ef2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264352"
---
# <a name="attribute-functions"></a>Функции атрибутов

В запрос на сертификат можно добавить атрибуты, чтобы предоставить [*центр сертификации*](/windows/desktop/SecGloss/c-gly) (ЦС) с дополнительными сведениями, которые он может использовать при создании и выдаче сертификата.

CertEnroll.dll реализует следующие интерфейсы для определения атрибутов и коллекций атрибутов:

-   [**икриптаттрибуте**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute)
-   [**икриптаттрибутес**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes)
-   [**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute)
-   [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes)
-   [**IX509AttributeClientId**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid)
-   [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions)
-   [**IX509AttributeArchiveKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekey)
-   [**IX509AttributeArchiveKeyHash**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekeyhash)
-   [**IX509AttributeCspProvider**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributecspprovider)
-   [**IX509AttributeOSVersion**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeosversion)
-   [**IX509AttributeRenewalCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributerenewalcertificate)

В следующих разделах указываются функции, экспортированные Xenroll.dll, чтобы связать криптографические атрибуты с запросами на сертификаты и обсудить использование CertEnroll.dll для замены функции или указания на отсутствие сопоставления между двумя библиотеками:

-   [аддаттрибутеторекуествстр](#addattributetorequestwstr)
-   [AddAuthenticatedAttributesToPKCS7Request](#addauthenticatedattributestopkcs7request)
-   [адднамевалуепаирторекуествстр](#addnamevaluepairtorequestwstr)
-   [адднамевалуепаиртосигнатуревстр](#addnamevaluepairtosignaturewstr)
-   [ClientId](#clientid)
-   [реневалцертификате](#renewalcertificate)
-   [ресетаттрибутес](#resetattributes)
-   [См. также](#related-topics)

## <a name="addattributetorequestwstr"></a>аддаттрибутеторекуествстр

Функция [**аддаттрибутеторекуествстр**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-addattributetorequestwstr) в Xenroll.dll добавляет атрибут к запросу на сертификат.

Как правило, чтобы добавить атрибут к запросу с помощью объектов, реализованных в CertEnroll.dll, можно выполнить следующие действия.

1.  Создайте объект коллекции [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) .
2.  Создайте объект [**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute) и вызовите метод [**Initialize**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509attribute-initialize) , чтобы создать атрибут из идентификатора объекта и значения атрибута или использовать любой из перечисленных выше интерфейсов, чтобы определить один из более общих атрибутов.
3.  Добавьте каждый новый атрибут, созданный на предыдущем шаге, в коллекцию [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) с помощью метода [**Add**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509attributes-add) .
4.  Создайте объект [**икриптаттрибуте**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) и инициализируйте его, вызвав метод [**инитиализефромвалуес**](/windows/desktop/api/CertEnroll/nf-certenroll-icryptattribute-initializefromvalues) и указав коллекцию [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) во входных данных.
5.  Получите объект коллекции [**икриптаттрибутес**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) , вызвав свойство [**криптаттрибутес**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_cryptattributes) для существующего объекта запроса [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) или [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) .
6.  Добавьте объект [**икриптаттрибуте**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) в коллекцию [**икриптаттрибутес**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) .

## <a name="addauthenticatedattributestopkcs7request"></a>AddAuthenticatedAttributesToPKCS7Request

Прошедшие проверку атрибуты — это пары "имя-значение", которые подписываются и добавляются в сигнатуру. Функция [**AddAuthenticatedAttributesToPKCS7Request**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-addauthenticatedattributestopkcs7request) в Xenroll.dll Добавляет массив атрибутов, прошедших проверку подлинности, к запросу [*PKCS \# 7*](/windows/desktop/SecGloss/p-gly) .

Как обсуждалось выше для функции [**аддаттрибутеторекуествстр**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-addattributetorequestwstr) , можно использовать CertEnroll.dll, чтобы легко определить и добавить коллекцию атрибутов в запрос на сертификат. Однако нельзя выбрать, прошел ли атрибут проверку подлинности. Процесс регистрации автоматически принимает это решение.

## <a name="addnamevaluepairtorequestwstr"></a>адднамевалуепаирторекуествстр

Функция [**адднамевалуепаирторекуествстр**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-addnamevaluepairtorequestwstr) в Xenroll.dll добавляет в запрос пару "имя-значение", не прошедшее проверку подлинности.

Вы можете использовать интерфейс [**IX509NameValuePair**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) в CertEnroll.dll для определения пары "имя-значение", а также добавить коллекцию пар "имя-значение" в объект запроса CMC, выполнив следующие действия:

1.  Создание и инициализация объекта [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) . Процесс инициализации создает пустую коллекцию [**IX509NameValuePairs**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepairs) .
2.  Вызовите свойство [**намевалуепаирс**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_namevaluepairs) для существующего объекта запроса CMC, чтобы получить коллекцию.
3.  Создание и инициализация объекта [**IX509NameValuePair**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) .
4.  Добавьте каждую новую пару "имя-значение" в коллекцию [**IX509NameValuePairs**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepairs) , вызвав метод [**Add**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509namevaluepairs-add) .

Процесс регистрации помещает коллекцию пар "имя-значение" в структуру **тагжедаттрибуте** запроса CMC.

## <a name="addnamevaluepairtosignaturewstr"></a>адднамевалуепаиртосигнатуревстр

Функция [**адднамевалуепаиртосигнатуревстр**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-addnamevaluepairtosignaturewstr) в Xenroll.dll добавляет к запросу пару "имя-значение", прошедшее проверку подлинности. Обычно это используется для указания имени инициатора запроса в запросе на регистрацию (ЕОБО).

В CertEnroll.dll используйте свойство [**рекуестернаме**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-get_requestername) , чтобы указать имя в запросе еобо.

## <a name="clientid"></a>ClientId

Функция [**ClientID**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-get_clientid) в Xenroll.dll указывает или получает атрибут **ClientID** .

Используйте свойство [**ClientID**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_clientid) в CertEnroll.dll, чтобы добавить этот атрибут в запрос CMC или PKCS \# 10.

## <a name="renewalcertificate"></a>реневалцертификате

Функция [**реневалцертификате**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_renewalcertificate) в Xenroll.dll указывает или получает атрибут **реневалцертификате** .

В CertEnroll.dll при вызове [**инитиализефромцертификате**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-initializefromcertificate) для \# объекта PKCS 7 или PKCS) автоматически создается.

## <a name="resetattributes"></a>ресетаттрибутес

Функция [**ресетаттрибутес**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-resetattributes) в Xenroll.dll удаляет коллекцию атрибутов из запроса.

Чтобы удалить атрибут из запроса по индексу с помощью CertEnroll.dll, вызовите метод [**Remove**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509attributes-remove) в коллекции [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) . Чтобы удалить все атрибуты из запроса, вызовите метод [**clear**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509attributes-clear) .

## <a name="related-topics"></a>См. также

<dl> <dt>

[Сопоставление Xenroll.dll CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> <dt>

[**икриптаттрибуте**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute)
</dt> <dt>

[**икриптаттрибутес**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes)
</dt> <dt>

[**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute)
</dt> <dt>

[**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes)
</dt> <dt>

[**IX509NameValuePair**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair)
</dt> <dt>

[**IX509NameValuePairs**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepairs)
</dt> </dl>

 

 
