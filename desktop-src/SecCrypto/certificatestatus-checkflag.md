---
description: Задает или получает флаги проверки достоверности для сертификата.
ms.assetid: c80c95a0-8a9b-441d-b243-7ee0552731e4
title: Цертификатестатус. Чеккфлаг, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.CheckFlag
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 1c47d7f1c59ecd629db1d6fc735f61b8d1fe59c864ffa8a5a9f013c86bd30faa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877454"
---
# <a name="certificatestatuscheckflag-property"></a>Цертификатестатус. Чеккфлаг, свойство

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP. Вместо этого используйте [**структуру X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

Свойство **чеккфлаг** задает или получает флаги проверки достоверности для сертификата.

## <a name="syntax"></a>Синтаксис


```VB
CertificateStatus.CheckFlag As CAPICOM_CHECK_FLAG
```



## <a name="property-value"></a>Значение свойства

Значение перечисления " [**CAPICOM \_ Check \_ Flag**](capicom-check-flag.md) ", которое описывает проверки достоверности сертификата. Значение по умолчанию — **CAPICOM \_ Check on \_ Online \_**.

**CAPICOM 2.0.0.3/2.0.0.2/2.0.0.1:** Значение по умолчанию — " [**\_ Проверка \_ \_ достоверности подписи" CAPICOM**](capicom-check-flag.md), " [**\_ \_ \_ допустимость времени проверки достоверности**](capicom-check-flag.md)", " [**CAPICOM \_ Check \_ Trusted \_ root**](capicom-check-flag.md)" и " [**CAPICOM- \_ Проверка \_ завершена \_**](capicom-check-flag.md)".

**CAPICOM 2,0 и более ранних версий:** Значение по умолчанию [**— \_ Проверка \_ \_ достоверности сигнатуры CAPICOM**](capicom-check-flag.md), [**\_ \_ \_ допустимость времени проверки CAPICOM**](capicom-check-flag.md)и [**CAPICOM \_ Проверка \_ доверенного \_ корня**](capicom-check-flag.md).

В следующей таблице приводятся возможные значения.



| Значение                                                                                                                                                                                                                                          | Значение                                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_CHECK_BASIC_CONSTRAINTS"></span><span id="capicom_check_basic_constraints"></span><dl> <dt>**CAPICOM \_ Check, \_ основные \_ ограничения**</dt> </dl>                          | Проверяет основные ограничения. Представлено в CAPICOM 2,0.<br/>                                                                                                                                                                                                                                                                                                                                    |
| <span id="CAPICOM_CHECK_COMPLETE_CHAIN"></span><span id="capicom_check_complete_chain"></span><dl> <dt>**\_ \_ цепочка завершения проверки CAPICOM \_**</dt> </dl>                                   | Проверяет всю цепь. Представлено в CAPICOM 2,0.<br/>                                                                                                                                                                                                                                                                                                                                   |
| <span id="CAPICOM_CHECK_NAME_CONSTRAINTS"></span><span id="capicom_check_name_constraints"></span><dl> <dt>**\_ \_ ограничения имени CAPICOM \_ Check**</dt> </dl>                             | Проверяет ограничения имен. Представлено в CAPICOM 2,0.<br/>                                                                                                                                                                                                                                                                                                                                     |
| <span id="CAPICOM_CHECK_NESTED_VALIDITY_PERIOD"></span><span id="capicom_check_nested_validity_period"></span><dl> <dt>**\_флажок CAPICOM проверить \_ вложенный \_ \_ период действия**</dt> </dl>          | Проверяет вложенное допустимость. Представлено в CAPICOM 2,0.<br/>                                                                                                                                                                                                                                                                                                                                      |
| <span id="CAPICOM_CHECK_NONE"></span><span id="capicom_check_none"></span><dl> <dt>**CAPICOM \_ Check \_ None**</dt> </dl>                                                                  | Проверка действительности не выполняется.<br/>                                                                                                                                                                                                                                                                                                                                                           |
| <span id="CAPICOM_CHECK_OFFLINE_ALL"></span><span id="capicom_check_offline_all"></span><dl> <dt>**\_неавтономная проверка CAPICOM \_ \_**</dt> </dl>                                            | Все автономные проверки. Проверки отзыва выполняются для всех сертификатов в цепочке, за исключением корневого сертификата. Представлено в CAPICOM 2,0.<br/>                                                                                                                                                                                                                                        |
| <span id="CAPICOM_CHECK_ONLINE_ALL"></span><span id="capicom_check_online_all"></span><dl> <dt>**CAPICOM \_ \_ -проверить \_ все**</dt> </dl>                                               | Проверяет все в сети. Проверки отзыва выполняются для всех сертификатов в цепочке, за исключением корневого сертификата. Представлено в CAPICOM 2,0.<br/>                                                                                                                                                                                                                                         |
| <span id="CAPICOM_CHECK_OFFLINE_REVOCATION_STATUS"></span><span id="capicom_check_offline_revocation_status"></span><dl> <dt>**\_ \_ состояние неавтономного \_ отзыва проверки CAPICOM \_**</dt> </dl> | Проверяет состояние отзыва всех сертификатов в цепочке, используя только автономные списки отзыва сертификатов.<br/>                                                                                                                                                                                                                                                                                                  |
| <span id="CAPICOM_CHECK_ONLINE_REVOCATION_STATUS"></span><span id="capicom_check_online_revocation_status"></span><dl> <dt>**\_запись CAPICOM \_ Проверка \_ состояния отзыва в сети \_**</dt> </dl>    | Проверяет состояние отзыва всех сертификатов в цепочке с помощью списков отзыва сертификатов, доступных в сети. Списки отзыва сертификатов загружаются с помощью расширения CDP в сертификате.<br/> Если список отзыва сертификатов был скачан и срок его действия не истек, CAPICOM использует его и не переходит в режим «в сети».<br/> Если список отзыва сертификатов не был загружен или устарел, то CAPICOM перейдет в режим «в сети», чтобы попытаться загрузить список отзыва сертификатов.<br/> |
| <span id="CAPICOM_CHECK_SIGNATURE_VALIDITY"></span><span id="capicom_check_signature_validity"></span><dl> <dt>**\_Проверка \_ достоверности подписи \_ CAPICOM**</dt> </dl>                       | Проверяет наличие допустимых подписей для всех сертификатов в цепочке.<br/>                                                                                                                                                                                                                                                                                                                           |
| <span id="CAPICOM_CHECK_TIME_VALIDITY"></span><span id="capicom_check_time_validity"></span><dl> <dt>**\_ \_ допустимость времени проверки CAPICOM \_**</dt> </dl>                                      | Проверяет допустимость времени для всех сертификатов в цепочке.<br/>                                                                                                                                                                                                                                                                                                                              |
| <span id="CAPICOM_CHECK_TRUSTED_ROOT"></span><span id="capicom_check_trusted_root"></span><dl> <dt>**CAPICOM \_ проверить \_ доверенный \_ корень**</dt> </dl>                                         | Проверяет наличие доверенного корня цепочки сертификатов.<br/>                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------------------------|----------------------------------------------------------------------------------------|
| Окончание поддержки клиента<br/> | Windows Vista<br/>                                                               |
| Поддержка конца сервера<br/> | Windows Server 2008<br/>                                                         |
| Распространяемые компоненты<br/>       | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
