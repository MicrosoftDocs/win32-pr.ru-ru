---
description: Создает объект запроса CMC из внутреннего вложенного запроса PKCS \# 10.
ms.assetid: 8a0dc078-22ca-4bff-9cc0-46823912d3da
title: креатекнгкустомкмк
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0494fdf2af9e4e96983ed1aff462b38e749516eafe87f645a3bf8ae1b342292d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119798274"
---
# <a name="createcngcustomcmc"></a>креатекнгкустомкмк

В примере Креатекнгкустомкмк создается объект запроса CMC из внутреннего вложенного запроса PKCS \# 10. Внутренний запрос создается с помощью асимметричного [*закрытого ключа*](/windows/desktop/SecGloss/p-gly). Закрытый ключ создается с помощью поставщика криптографии API шифрования: следующего поколения (CNG) и алгоритма, указанного в командной строке. Для закрытого ключа также устанавливаются настраиваемые параметры, такие как экспорт политики и уровень защиты ключей.

## <a name="location"></a>Расположение

при установке пакета microsoft Windows Software Development Kit (SDK) образец устанавливается по умолчанию в папке *% ProgramFiles%* \\ Microsoft sdk \\ Windows \\ v 7.0 \\ samples \\ Security ssl \\ Certificate \\ \\ креатекнгкустомкмк.

## <a name="discussion"></a>Разговор

Пример Креатекнгкустомкмк:

1.  Обрабатывает следующие аргументы командной строки:
    -   Имя [*поставщика служб шифрования*](/windows/desktop/SecGloss/c-gly) CNG (CSP).
    -   Имя алгоритма, используемого для создания асимметричного закрытого ключа.
    -   Имя алгоритма, используемого для [*хэширования*](/windows/desktop/SecGloss/h-gly) [*запроса сертификата*](/windows/desktop/SecGloss/c-gly).
    -   Выходной файл, в котором сохраняется запрос на сертификат.
    -   Необязательная строка (Алтернатесигнатуре), если она есть, указывает, что используется дискретный, а не Объединенный алгоритм подписи. Дополнительные сведения см. в описании свойства [**алтернатесигнатуреалгорисм**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_alternatesignaturealgorithm) .
2.  Создает объект [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) и задает следующие свойства:
    -   [**легациксп**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_legacycsp)
    -   [**ProviderName**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_providername)
    -   [**Алгоритм**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_algorithm)
    -   [**кэйпротектион**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_keyprotection)
    -   [**експортполици**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_exportpolicy)
3.  Создает асимметричный закрытый ключ.
4.  Создает объект [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) и инициализирует его с помощью закрытого ключа.
5.  Создает объект [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) и инициализирует его с помощью \# объекта запроса PKCS 10, созданного на шаге 4.
6.  Устанавливает для флага альтернативного алгоритма подписи значение **Variant \_ true** или **Variant \_ false** в зависимости от того, указана ли в командной строке альтернативная строка подписи. Дополнительные сведения см. в разделе [**алтернатесигнатуреалгорисм**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_alternatesignaturealgorithm).
7.  Создает [*идентификатор объекта*](/windows/desktop/SecGloss/o-gly) (OID) [*алгоритма хэширования*](/windows/desktop/SecGloss/h-gly) из имени алгоритма, указанного в командной строке, и задает идентификатор объекта для объекта запроса CMC.
8.  подписывает запрос на сертификат и кодирует его с помощью [*Distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (DER).
9.  Извлекает строку, содержащую закодированный запрос сертификата CMC, и сохраняет его в файл. Функция Енкодетофилев определена в Енроллкоммон. cpp.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Запрос CMC](cmc-request.md)
</dt> <dt>

[\#Запрос PKCS 10](pkcs--10-request.md)
</dt> <dt>

[Использование прилагаемых примеров](using-the-included-samples.md)
</dt> <dt>

[**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey)
</dt> </dl>

 

 
