---
description: В этом разделе приведены рекомендации по использованию API цифровой подписи XPS для добавления цифровых подписей в документ XPS.
ms.assetid: 27c28313-d8db-4c40-9972-cb03bdaa125c
title: Использование API цифровых подписей XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84ea6e38704efa2a348a90fec247f37b9722857a3838b10233937e63dc37fdbd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118469356"
---
# <a name="using-xps-digital-signature-api"></a>Использование API цифровых подписей XPS

В этом разделе приведены рекомендации по использованию API цифровой подписи XPS для добавления цифровых подписей в документ XPS.

API цифровой подписи XPS позволяет приложениям запрашивать у пользователей подписывать XPS-документы и проверять подписи, найденные в документах XPS. API цифровой подписи XPS можно применить к документу XPS, не загружая его в модель XPS, и его можно использовать в потоках документов XPS, сериализуемых из OM-объекта XPS.

В разделе [задачи программирования API цифровых подписей XPS](#xps-digital-signature-api-programming-tasks) содержатся разделы, в которых описывается программирование с помощью API цифровой подписи XPS. В этом разделе приведены рекомендации по использованию API цифровой подписи XPS при добавлении поддержки цифровых подписей в приложение.

-   [Задачи программирования API цифровых подписей XPS](#xps-digital-signature-api-programming-tasks)
-   [Специальные примечания о программировании API цифровых подписей XPS](#special-notes-about-xps-digital-signature-api-programming)
    -   [Проверка цифровых подписей в документе XPS](#verifying-digital-signatures-in-an-xps-document)
    -   [Политика подписи цифровых подписей](#digital-signature-signing-policy)
    -   [Внедрение цепочки сертификатов](#embedding-a-certificate-chain)
    -   [Использование \_ структуры контекста CERT](#using-the-cert\_context-structure)
-   [Связанные темы](#related-topics)

## <a name="xps-digital-signature-api-programming-tasks"></a>Задачи программирования API цифровых подписей XPS

В этом разделе содержатся разделы, в которых описывается выполнение задач по программированию с помощью API цифровой подписи XPS.

-   [Распространенные задачи по программированию цифровых подписей](basic-digital-signature-programming-tasks.md)<dl>

[Инициализация диспетчера сигнатур](initialize-the-signature-manager.md)  
    [Подписать документ](sign-a-document.md)  
    [Добавление запроса подписи в документ XPS](add-a-signature-request-to-a-document.md)  
    [Проверка подписей документов](verify-document-signatures.md)  
    </dl>
-   [Дополнительные задачи по программированию цифровых подписей](advanced-digital-signature-programming-tasks.md)<dl>

[Загрузка сертификата из файла](load-a-certificate-from-a-file.md)  
    [Убедитесь, что сертификат поддерживает метод подписи.](verify-a-certificate-supports-a-signature-method.md)  
    [Проверка того, что система поддерживает метод дайджеста](verify-a-certificate-supports-a-digest-method.md)  
    [Внедрение цепочек сертификатов в документ](embedding-certificate-trust-chains-in-a-document.md)  
    </dl>

## <a name="special-notes-about-xps-digital-signature-api-programming"></a>Специальные примечания о программировании API цифровых подписей XPS

В следующих разделах при использовании API цифровых подписей XPS необходимо учитывать некоторые особенности.

-   [Проверка цифровых подписей в документе XPS](#verifying-digital-signatures-in-an-xps-document)
-   [Политика подписи цифровых подписей](#digital-signature-signing-policy)
-   [Внедрение цепочки сертификатов](#embedding-a-certificate-chain)
-   [Использование \_ структуры контекста CERT](#using-the-cert\_context-structure)

### <a name="verifying-digital-signatures-in-an-xps-document"></a>Проверка цифровых подписей в документе XPS

[**Икспссигнатуре:: Verify**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignature-verify) проверяет только подписанное содержимое, чтобы определить, что оно не изменилось с момента подписания. **Икспссигнатуре:: Verify** не проверяет сертификаты, которые использовались для подписания содержимого документа.

Дополнительные сведения о сертификатах и криптографии см. в статье [о шифровании](/windows/desktop/SecCrypto/about-cryptography).

Пример проверки подписей документов в программе см. в разделе [Проверка подписей документов и сертификатов](verify-document-signatures.md).

### <a name="digital-signature-signing-policy"></a>Политика подписи цифровых подписей

Политика подписи цифровых подписей определяет, какие части документа XPS подписаны. Одним из политик подписывания является подписывание связей подписей, начинающихся с части источника подписи. Так как связи сигнатур меняются при каждой добавляемой подписи, при добавлении новых подписей подписи, сделанные в этой политике, будут нарушены. Убедитесь, что вы четко понимаете последствия и последствия установки этой политики. в противном случае может возникнуть непредвиденное или нежелательное поведение.

Дополнительные сведения о политиках подписывания см. в статье о [**\_ \_ политике подписания XPS**](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_policy).

### <a name="embedding-a-certificate-chain"></a>Внедрение цепочки сертификатов

Сертификаты, составляющие цепочку доверия определенного сертификата, можно добавить в документ XPS. Внедрение этих сертификатов упрощает работу в автономных сценариях, чтобы приложение проверяло сертификаты, используемые цифровой подписью.

Дополнительные сведения о внедрении сертификатов в документ XPS см. [в разделе внедрение цепочек сертификатов в документ](embedding-certificate-trust-chains-in-a-document.md).

### <a name="using-the-cert_context-structure"></a>Использование \_ структуры контекста CERT

[**\_ Контекст сертификата**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) и структуры [**\_ сведений о**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_info) сертификатах являются основными структурами данных, которые содержат сведения о сертификате. Дополнительные сведения об использовании этих структур см. в разделе [использование \_ структуры данных о сертификатах](/windows/desktop/SecCrypto/using-a-cert-info-data-structure).

[**Сертификат \_ Структуры контекста**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) , возвращаемые ФУНКЦИЯМИ API шифрования, должны освобождаться, если они больше не нужны. Чтобы освободить структуру **\_ контекста сертификата** , вызовите функцию [**цертфрицертификатеконтекст**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) .

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Распространенные задачи по программированию цифровых подписей](basic-digital-signature-programming-tasks.md)
</dt> <dt>

[Дополнительные задачи по программированию цифровых подписей](advanced-digital-signature-programming-tasks.md)
</dt> <dt>

[**\_контекст сертификата**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context)
</dt> <dt>

[**\_сведения о сертификате**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_info)
</dt> <dt>

[**цертфрицертификатеконтекст**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext)
</dt> <dt>

[**\_Политика подписывания XPS \_**](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_policy)
</dt> <dt>

[XPS](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
