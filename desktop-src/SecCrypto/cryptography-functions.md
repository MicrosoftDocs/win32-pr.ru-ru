---
description: Перечисляет функции, предоставляемые интерфейсом CryptoAPI.
ms.assetid: 9a65f73d-6f8c-4271-a2d0-d91ad952f9c6
title: 'Функции шифрования '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b65c04d3cb1ff619d03d7f0340fc4f94826722f8ed6c0457987b8ec432a66128
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117768346"
---
# <a name="cryptography-functions"></a>Функции шифрования 

Функции шифрования делятся на категории по использованию следующим образом.

-   [Функции Криптксмл](#cryptxml-functions)
-   [Функции подписывающих](#signer-functions)
-   [Базовые криптографические функции](#base-cryptography-functions)
    -   [Функции поставщика услуг](#service-provider-functions)
    -   [создание ключей и функции Exchange](#key-generation-and-exchange-functions)
    -   [Функции кодирования и декодирования объектов](#object-encoding-and-decoding-functions)
    -   [Функции шифрования и расшифровки данных](#data-encryption-and-decryption-functions)
    -   [Функции хэширования и цифровой подписи](#hash-and-digital-signature-functions)
-   [Функции сертификатов и хранилища сертификатов](#certificate-and-certificate-store-functions)
    -   [Функции хранилища сертификатов](#certificate-and-certificate-store-functions)
    -   [Функции обслуживания сертификатов и хранилища сертификатов](#certificate-and-certificate-store-maintenance-functions)
    -   [Функции сертификата](#certificate-functions)
    -   [Функции списка отзыва сертификатов](#certificate-revocation-list-functions)
    -   [Функции списка доверия сертификатов](#certificate-trust-list-functions)
    -   [Функции расширенных свойств](#extended-property-functions)
-   [Функции MakeCert](#makecert-functions)
-   [Функции проверки сертификатов](#certificate-verification-functions)
    -   [Функции проверки с использованием списков CTL](#verification-functions-using-ctls)
    -   [Функции проверки цепочки сертификатов](#certificate-chain-verification-functions)
-   [Функции сообщений](#message-functions)
    -   [Низкоуровневые функции сообщений](#low-level-message-functions)
    -   [Упрощенные функции сообщений](#simplified-message-functions)
-   [Вспомогательные функции](#auxiliary-functions)
    -   [Функции Управление данными](#data-management-functions)
    -   [Функции преобразования данных](#data-conversion-functions)
    -   [Функции расширенного использования ключа](#enhanced-key-usage-functions)
    -   [Функции идентификатора ключа](#key-identifier-functions)
    -   [Функции поддержки OID](#oid-support-functions)
    -   [Функции извлечения удаленных объектов](#remote-object-retrieval-functions)
    -   [Функции PFX](#pfx-functions)
-   [Функции резервного копирования и восстановления служб сертификатов](#certificate-services-backup-and-restore-functions)
-   [Функции обратного вызова](#callback-functions)
-   [Функции определения каталога](#catalog-definition-functions)
-   [Функции работы с каталогами](#catalog-functions)
-   [Функции Винтруст](#wintrust-functions)
-   [Функции локатора объектов](#object-locator-functions)

## <a name="cryptxml-functions"></a>Функции Криптксмл

Криптографические XML-функции предоставляют API для создания и представления цифровых подписей с помощью данных в формате XML. Дополнительные сведения о сигнатурах в формате XML см. в разделе синтаксис и спецификация обработки XML-Signature по адресу <https://go.microsoft.com/fwlink/p/?linkid=139649> .



| Функция                                                                          | Описание                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_Шафинал**](a-shafinal.md)                                                 | Выполняет вычисление конечного хэша данных, вводимых функцией MD5Update.                                                                                                                                                                                                                                           |
| [**\_Шаинит**](a-shainit.md)                                                   | Инициирует хэширование потока данных.                                                                                                                                                                                                                                                                       |
| [**\_Шаупдате**](a-shaupdate.md)                                               | Добавляет данные в указанный хэш-объект.                                                                                                                                                                                                                                                                            |
| [**криптксмлкреатереференце**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlcreatereference)                        | Создает ссылку на XML-подпись.                                                                                                                                                                                                                                                                         |
| [**криптксмладдобжект**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmladdobject)                                    | Добавляет элемент **Object** в сигнатуру в контексте документа, открытого для кодирования.                                                                                                                                                                                                                        |
| [**криптксмлклосе**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlclose)                                            | Закрывает обработчик зашифрованного XML-объекта.                                                                                                                                                                                                                                                                        |
| [**криптксмлдижестреференце**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmldigestreference)                        | Используется приложением для дайджеста разрешенной ссылки. Эта функция применяет преобразования перед обновлением дайджеста.                                                                                                                                                                                            |
| [**криптксмлдллклоседижест**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllclosedigest)                          | Освобождает ЗАШИФРОВАНный \_ XML- \_ дайджест, выделенный функцией [**криптксмлдллкреатедижест**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllcreatedigest) .                                                                                                                                                                                               |
| [**криптксмлдллкреатедижест**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllcreatedigest)                        | Создает объект дайджеста для указанного метода.                                                                                                                                                                                                                                                                |
| [**криптксмлдллкреатекэй**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllcreatekey)                              | Выполняет синтаксический анализ элемента **KeyValue** и создает API-интерфейс шифрования: следующего поколения (CNG) BCrypt для проверки подписи.                                                                                                                                                                                   |
| [**криптксмлдллдижестдата**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldlldigestdata)                            | Помещает данные в дайджест.                                                                                                                                                                                                                                                                                       |
| [**криптксмлдлленкодеалгорисм**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllencodealgorithm)                  | Кодирует элементы **SignatureMethod** или **дижестмесод** для алгоритмов Agile с параметрами по умолчанию.                                                                                                                                                                                                           |
| [**криптксмлдлленкодекэйвалуе**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllencodekeyvalue)                    | Кодирует элемент **KeyValue** .                                                                                                                                                                                                                                                                                  |
| [**криптксмлдллфинализедижест**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllfinalizedigest)                    | Извлекает значение дайджеста.                                                                                                                                                                                                                                                                                      |
| [**криптксмлдллжеталгорисминфо**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllgetalgorithminfo)                | Декодирует XML-алгоритм и возвращает сведения о алгоритме.                                                                                                                                                                                                                                           |
| [**криптксмлдллжетинтерфаце**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllgetinterface)                        | Получает указатель на функции расширения шифрования для указанного алгоритма.                                                                                                                                                                                                                        |
| [**криптксмлдллсигндата**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllsigndata)                                | Подписывает данные.                                                                                                                                                                                                                                                                                                      |
| [**криптксмлдллверифисигнатуре**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllverifysignature)                  | Проверяет сигнатуру.                                                                                                                                                                                                                                                                                            |
| [**криптксмленкоде**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlencode)                                          | Кодирует данные сигнатуры с помощью предоставленной функции обратного вызова модуля записи XML.                                                                                                                                                                                                                                       |
| [**криптксмлжеталгорисминфо**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlgetalgorithminfo)                      | Декодирует \_ \_ структуру алгоритма шифрования XML и возвращает сведения о алгоритме.                                                                                                                                                                                                                         |
| [**криптксмлжетдокконтекст**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlgetdoccontext)                            | Возвращает контекст документа, заданный предоставленным обработчиком.                                                                                                                                                                                                                                                   |
| [**криптксмлжетреференце**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlgetreference)                              | Возвращает элемент **Reference** , заданный предоставленным обработчиком.                                                                                                                                                                                                                                              |
| [**криптксмлжетсигнатуре**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlgetsignature)                              | Возвращает XML-элемент **подписи** .                                                                                                                                                                                                                                                                            |
| [**криптксмлжетстатус**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlgetstatus)                                    | Возвращает структуру [**\_ \_ состояния незашифрованного XML**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_status) , которая содержит сведения о состоянии объекта, указанного предоставленным обработчиком.                                                                                                                                                           |
| [**криптксмлжеттрансформс**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlgettransforms)                            | Возвращает сведения о механизме цепочки преобразований по умолчанию.                                                                                                                                                                                                                                                    |
| [**криптксмлимпортпубликкэй**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlimportpublickey)                        | Импортирует открытый ключ, заданный предоставленным обработчиком.                                                                                                                                                                                                                                                         |
| [**криптксмлопентоенкоде**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlopentoencode)                              | Открывает цифровую подпись XML для кодирования и возвращает маркер открытого элемента **сигнатуры** . Этот обработчик инкапсулирует контекст документа с одной [**понятной структурой \_ \_ подписи XML**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_signature) и остается открытым до тех пор, пока не будет вызвана функция [**криптксмлклосе**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlclose) . |
| [**криптксмлопентодекоде**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlopentodecode)                              | Открывает цифровую подпись XML для декодирования и возвращает маркер контекста документа, который инкапсулирует структуру [**зашифрованной \_ XML- \_ подписи**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_signature) . Контекст документа может включать один или несколько элементов **сигнатуры** .                                                                 |
| [**криптксмлсесмаксекрет**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlsethmacsecret)                            | Задает секрет HMAC для данного обработчика перед вызовом функции [**криптксмлсигн**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlsign) или [**криптксмлверифи**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlverifysignature) .                                                                                                                                                        |
| [**криптксмлсигн**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlsign)                                              | Создает криптографическую подпись элемента **SignedInfo** .                                                                                                                                                                                                                                                   |
| [**криптксмлверифисигнатуре**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlverifysignature)                        | Выполняет проверку криптографической подписи элемента **SignedInfo** .                                                                                                                                                                                                                                       |
| [*\_ \_ \_ обратный вызов PFN для шифрования XML \_*](/windows/desktop/api/Cryptxml/nc-cryptxml-pfn_crypt_xml_write_callback)            | Создает преобразование для указанного поставщика данных.                                                                                                                                                                                                                                                               |
| [*PFN \_ шифрования \_ \_ Создание \_ преобразования XML*](/windows/desktop/api/Cryptxml/nc-cryptxml-pfn_crypt_xml_create_transform)        | Записывает криптографические XML-данные.                                                                                                                                                                                                                                                                                   |
| [*\_ \_ \_ \_ Чтение поставщика XML-данных \_ PFN*](/windows/desktop/api/Cryptxml/nc-cryptxml-pfn_crypt_xml_data_provider_read)   | Считывает зашифрованные XML-данные.                                                                                                                                                                                                                                                                                    |
| [*PFN \_ при \_ \_ \_ закрытии поставщика XML-данных \_*](/windows/desktop/api/Cryptxml/nc-cryptxml-pfn_crypt_xml_data_provider_close) | Освобождает поставщик криптографических XML-данных.                                                                                                                                                                                                                                                                    |
| [*PFN \_ шифрования \_ XML-данных \_ \_ о алгоритме перечислений \_*](/windows/desktop/api/Cryptxml/nc-cryptxml-pfn_crypt_xml_enum_alg_info)             | Перечисляет стандартные и зарегистрированные [**записи \_ \_ \_ сведений о XML-алгоритме шифрования**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_algorithm_info) .                                                                                                                                                                                                    |



 

## <a name="signer-functions"></a>Функции подписывающих

Предоставляет функции для подписи и данных метки времени.



| Функция                                                   | Описание                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**сигнерфрисигнерконтекст**](signerfreesignercontext.md) | Освобождает структуру [**\_ контекста подписи**](signer-context.md) , выделенную предыдущим вызовом функции [**сигнерсигнекс**](signersignex.md) .                                                                                                                                                                                                                                                                      |
| [**сигнеррор**](signerror.md)                             | Вызывает функцию [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) и преобразует код возврата в **значение HRESULT**.                                                                                                                                                                                                                                                                                                            |
| [**сигнерсигн**](signersign.md)                           | Подписывает указанный файл.                                                                                                                                                                                                                                                                                                                                                                                           |
| [**сигнерсигнекс**](signersignex.md)                       | Подписывает указанный файл и возвращает указатель на подписанные данные.                                                                                                                                                                                                                                                                                                                                                  |
| [**SignerSignEx2**](signersignex2.md)                     | Метки и отметки времени задаются в указанном файле, что позволяет использовать несколько вложенных подписей.                                                                                                                                                                                                                                                                                                                                      |
| [**сигнертиместамп**](signertimestamp.md)                 | Помечает время указанной темой. Эта функция поддерживает отметку времени Authenticode. Чтобы выполнить отметку времени X. 509 для инфраструктуры открытых ключей (RFC 3161), используйте функцию [**SignerTimeStampEx2**](signertimestampex2.md) .                                                                                                                                                                                       |
| [**сигнертиместампекс**](signertimestampex.md)             | Время помечает указанную тему и при необходимости возвращает указатель на структуру [**\_ контекста подписи**](signer-context.md) , содержащую указатель на [*большой двоичный объект*](../secgloss/b-gly.md). Эта функция поддерживает отметку времени Authenticode. Чтобы выполнить отметку времени X. 509 для инфраструктуры открытых ключей (RFC 3161), используйте функцию [**SignerTimeStampEx2**](signertimestampex2.md) . |
| [**SignerTimeStampEx2**](signertimestampex2.md)           | Время помечает указанную тему и при необходимости возвращает указатель на структуру [**\_ контекста подписи**](signer-context.md) , содержащую указатель на [*большой двоичный объект*](../secgloss/b-gly.md). Эта функция может использоваться для выполнения 509 инфраструктуры открытого ключа X., совместимой с RFC 3161, меток времени.                                                                                     |
| [**SignerTimeStampEx3**](signertimestampex3.md)           | Помечает время указанной темой и поддерживает задание меток времени для нескольких подписей.                                                                                                                                                                                                                                                                                                                          |



 

## <a name="base-cryptography-functions"></a>Базовые криптографические функции

Базовые криптографические функции обеспечивают наиболее гибкие средства разработки криптографических приложений. Все взаимодействия с [*поставщиком служб шифрования*](../secgloss/c-gly.md) (CSP) выполняются с помощью этих функций.

CSP — это независимый модуль, выполняющий все криптографические операции. Для каждого приложения, использующего криптографические функции, требуется по крайней мере один CSP. В одном приложении иногда может использоваться более одного CSP.

Если используется более одного CSP, то один из них можно указать в вызовах криптографических функций CryptoAPI. Один CSP, базовый поставщик служб шифрования Майкрософт, объединяется с интерфейсом [*CryptoAPI*](../secgloss/c-gly.md). Этот CSP используется в качестве поставщика по умолчанию многими функциями CryptoAPI, если не указан другой CSP.

Каждый CSP предоставляет различные реализации криптографической поддержки, предоставляемой интерфейсу CryptoAPI. Некоторые предоставляют более надежные алгоритмы шифрования; другие содержат компоненты оборудования, например [*смарт-карты*](../secgloss/s-gly.md). Кроме того, некоторые поставщики служб шифрования иногда могут напрямую взаимодействовать с пользователями, например при выполнении [*цифровых подписей*](../secgloss/d-gly.md) с помощью [*закрытого ключа подписи*](../secgloss/s-gly.md)пользователя.

Базовые криптографические функции находятся в следующих обширных группах:

-   Функции поставщика услуг
-   создание ключей и функции Exchange
-   Функции кодирования и декодирования объектов
-   Функции шифрования и расшифровки данных
-   Функции хэширования и цифровой подписи

### <a name="service-provider-functions"></a>Функции поставщика услуг

Приложения используют следующие функции службы для подключения и отключения [*поставщика служб шифрования*](../secgloss/c-gly.md) (CSP).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Функция</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta"><strong>CryptAcquireContext</strong></a></td>
<td><blockquote>
[!Important]<br />
Это нерекомендуемый API. Новое и существующее программное обеспечение должно начинаться с использования <a href="/windows/desktop/SecCNG/cng-portal">API-интерфейсов следующего поколения шифрования.</a> Корпорация Майкрософт может удалить этот API в будущих выпусках.
</blockquote>
<br/> Получает маркер для <a href="/windows/desktop/SecGloss/k-gly"><em>контейнера ключей</em></a> текущего пользователя в пределах определенного CSP.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcontextaddref"><strong>криптконтекстаддреф</strong></a></td>
<td><blockquote>
[!Important]<br />
Это нерекомендуемый API. Новое и существующее программное обеспечение должно начинаться с использования <a href="/windows/desktop/SecCNG/cng-portal">API-интерфейсов следующего поколения шифрования.</a> Корпорация Майкрософт может удалить этот API в будущих выпусках.
</blockquote>
<br/> Увеличивает значение <a href="/windows/desktop/SecGloss/r-gly"><em>счетчика ссылок</em></a> для маркера <a href="hcryptprov.md"><strong>хкриптпров</strong></a> .</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptenumprovidersa"><strong>криптенумпровидерс</strong></a></td>
<td><blockquote>
[!Important]<br />
Это нерекомендуемый API. Новое и существующее программное обеспечение должно начинаться с использования <a href="/windows/desktop/SecCNG/cng-portal">API-интерфейсов следующего поколения шифрования.</a> Корпорация Майкрософт может удалить этот API в будущих выпусках.
</blockquote>
<br/> Перечисление поставщиков на компьютере.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptenumprovidertypesa"><strong>криптенумпровидертипес</strong></a></td>
<td><blockquote>
[!Important]<br />
Это нерекомендуемый API. Новое и существующее программное обеспечение должно начинаться с использования <a href="/windows/desktop/SecCNG/cng-portal">API-интерфейсов следующего поколения шифрования.</a> Корпорация Майкрософт может удалить этот API в будущих выпусках.
</blockquote>
<br/> Перечисляет типы поставщиков, поддерживаемых на компьютере.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetdefaultprovidera"><strong>криптжетдефаултпровидер</strong></a></td>
<td><blockquote>
[!Important]<br />
Это нерекомендуемый API. Новое и существующее программное обеспечение должно начинаться с использования <a href="/windows/desktop/SecCNG/cng-portal">API-интерфейсов следующего поколения шифрования.</a> Корпорация Майкрософт может удалить этот API в будущих выпусках.
</blockquote>
<br/> Определяет CSP по умолчанию для текущего пользователя или для компьютера указанного типа поставщика.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam"><strong>криптжетпровпарам</strong></a></td>
<td><blockquote>
[!Important]<br />
Это нерекомендуемый API. Новое и существующее программное обеспечение должно начинаться с использования <a href="/windows/desktop/SecCNG/cng-portal">API-интерфейсов следующего поколения шифрования.</a> Корпорация Майкрософт может удалить этот API в будущих выпусках.
</blockquote>
<br/> Извлекает параметры, управляющие операциями CSP.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinstalldefaultcontext"><strong>криптинсталлдефаултконтекст</strong></a></td>
<td><blockquote>
[!Important]<br />
Это нерекомендуемый API. Новое и существующее программное обеспечение должно начинаться с использования <a href="/windows/desktop/SecCNG/cng-portal">API-интерфейсов следующего поколения шифрования.</a> Корпорация Майкрософт может удалить этот API в будущих выпусках.
</blockquote>
<br/> Устанавливает ранее полученный контекст <a href="hcryptprov.md"><strong>хкриптпров</strong></a> для использования в качестве контекста по умолчанию.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptreleasecontext"><strong>криптрелеасеконтекст</strong></a></td>
<td><blockquote>
[!Important]<br />
Это нерекомендуемый API. Новое и существующее программное обеспечение должно начинаться с использования <a href="/windows/desktop/SecCNG/cng-portal">API-интерфейсов следующего поколения шифрования.</a> Корпорация Майкрософт может удалить этот API в будущих выпусках.
</blockquote>
<br/> Освобождает дескриптор, полученный функцией <a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta"><strong>CryptAcquireContext</strong></a> .</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetprovidera"><strong>Криптсетпровидер</strong></a> и <a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetproviderexa"> <strong>криптсетпровидерекс</strong></a></td>
<td><blockquote>
[!Important]<br />
Это нерекомендуемый API. Новое и существующее программное обеспечение должно начинаться с использования <a href="/windows/desktop/SecCNG/cng-portal">API-интерфейсов следующего поколения шифрования.</a> Корпорация Майкрософт может удалить этот API в будущих выпусках.
</blockquote>
<br/> Указывает CSP пользователя по умолчанию для конкретного типа CSP.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetprovparam"><strong>криптсетпровпарам</strong></a></td>
<td><blockquote>
[!Important]<br />
Это нерекомендуемый API. Новое и существующее программное обеспечение должно начинаться с использования <a href="/windows/desktop/SecCNG/cng-portal">API-интерфейсов следующего поколения шифрования.</a> Корпорация Майкрософт может удалить этот API в будущих выпусках.
</blockquote>
<br/> Задает атрибуты CSP.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptuninstalldefaultcontext"><strong>криптунинсталлдефаултконтекст</strong></a></td>
<td><blockquote>
[!Important]<br />
Это нерекомендуемый API. Новое и существующее программное обеспечение должно начинаться с использования <a href="/windows/desktop/SecCNG/cng-portal">API-интерфейсов следующего поколения шифрования.</a> Корпорация Майкрософт может удалить этот API в будущих выпусках.
</blockquote>
<br/> Удаляет контекст по умолчанию, установленный ранее <a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinstalldefaultcontext"><strong>криптинсталлдефаултконтекст</strong></a>.</td>
</tr>
<tr class="even">
<td><a href="freecryptprovfromcertex.md"><strong>фрикриптпровфромцертекс</strong></a></td>
<td>Освобождает дескриптор от <a href="/windows/desktop/SecGloss/c-gly"><em>поставщика служб шифрования</em></a> (CSP) или ключа API шифрования: следующего поколения (CNG).</td>
</tr>
</tbody>
</table>



 

### <a name="key-generation-and-exchange-functions"></a>создание ключей и функции Exchange

Функции создания ключей и обмена ключами [*обмениваются*](../secgloss/e-gly.md) данными с другими пользователями, а также создают, настраивают и удаляют [*криптографические ключи*](../secgloss/c-gly.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Функция</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey"><strong>криптдеривекэй</strong></a></td>
<td><blockquote>
[!Important]<br />
Это нерекомендуемый API. Новое и существующее программное обеспечение должно начинаться с использования <a href="/windows/desktop/SecCNG/cng-portal">API-интерфейсов следующего поколения шифрования.</a> Корпорация Майкрософт может удалить этот API в будущих выпусках.
</blockquote>
<br/> Создает ключ, полученный на основе пароля.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey"><strong>криптдестройкэй</strong></a></td>
<td><blockquote>
[!Important]<br />
Это нерекомендуемый API. Новое и существующее программное обеспечение должно начинаться с использования <a href="/windows/desktop/SecCNG/cng-portal">API-интерфейсов следующего поколения шифрования.</a> Корпорация Майкрософт может удалить этот API в будущих выпусках.
</blockquote>
<br/> Уничтожает ключ.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptduplicatekey"><strong>криптдупликатекэй</strong></a></td>
<td><blockquote>
[!Important]<br />
Это нерекомендуемый API. Новое и существующее программное обеспечение должно начинаться с использования <a href="/windows/desktop/SecCNG/cng-portal">API-интерфейсов следующего поколения шифрования.</a> Корпорация Майкрософт может удалить этот API в будущих выпусках.
</blockquote>
<br/> Создает точную копию ключа, включая <a href="/windows/desktop/SecGloss/s-gly"><em>состояние</em></a> ключа.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey"><strong>криптекспорткэй</strong></a></td>
<td><blockquote>
[!Important]<br />
Это нерекомендуемый API. Новое и существующее программное обеспечение должно начинаться с использования <a href="/windows/desktop/SecCNG/cng-portal">API-интерфейсов следующего поколения шифрования.</a> Корпорация Майкрософт может удалить этот API в будущих выпусках.
</blockquote>
<br/> Передает ключ из CSP в <a href="/windows/desktop/SecGloss/k-gly"><em>ключевой BLOB-объект</em></a> в пространстве памяти приложения.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey"><strong>криптженкэй</strong></a></td>
<td><blockquote>
[!Important]<br />
Это нерекомендуемый API. Новое и существующее программное обеспечение должно начинаться с использования <a href="/windows/desktop/SecCNG/cng-portal">API-интерфейсов следующего поколения шифрования.</a> Корпорация Майкрософт может удалить этот API в будущих выпусках.
</blockquote>
<br/> Создает случайный ключ.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenrandom"><strong>CryptGenRandom</strong></a></td>
<td><blockquote>
[!Important]<br />
Это нерекомендуемый API. Новое и существующее программное обеспечение должно начинаться с использования <a href="/windows/desktop/SecCNG/cng-portal">API-интерфейсов следующего поколения шифрования.</a> Корпорация Майкрософт может удалить этот API в будущих выпусках.
</blockquote>
<br/> Создает случайные данные.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetkeyparam"><strong>криптжеткэйпарам</strong></a></td>
<td><blockquote>
[!Important]<br />
Это нерекомендуемый API. Новое и существующее программное обеспечение должно начинаться с использования <a href="/windows/desktop/SecCNG/cng-portal">API-интерфейсов следующего поколения шифрования.</a> Корпорация Майкрософт может удалить этот API в будущих выпусках.
</blockquote>
<br/> Извлекает параметры ключа.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey"><strong>криптжетусеркэй</strong></a></td>
<td><blockquote>
[!Important]<br />
Это нерекомендуемый API. Новое и существующее программное обеспечение должно начинаться с использования <a href="/windows/desktop/SecCNG/cng-portal">API-интерфейсов следующего поколения шифрования.</a> Корпорация Майкрософт может удалить этот API в будущих выпусках.
</blockquote>
<br/> Возвращает маркер обмена ключами или ключа подписи.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey"><strong>криптимпорткэй</strong></a></td>
<td><blockquote>
[!Important]<br />
Это нерекомендуемый API. Новое и существующее программное обеспечение должно начинаться с использования <a href="/windows/desktop/SecCNG/cng-portal">API-интерфейсов следующего поколения шифрования.</a> Корпорация Майкрософт может удалить этот API в будущих выпусках.
</blockquote>
<br/> Передает ключ из BLOB- <a href="/windows/desktop/SecGloss/k-gly"><em>объекта ключа</em></a> в CSP.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam"><strong>криптсеткэйпарам</strong></a></td>
<td><blockquote>
[!Important]<br />
Это нерекомендуемый API. Новое и существующее программное обеспечение должно начинаться с использования <a href="/windows/desktop/SecCNG/cng-portal">API-интерфейсов следующего поколения шифрования.</a> Корпорация Майкрософт может удалить этот API в будущих выпусках.
</blockquote>
<br/> Задает параметры ключа.</td>
</tr>
</tbody>
</table>



 

### <a name="object-encoding-and-decoding-functions"></a>Функции кодирования и декодирования объектов

Это обобщенные функции кодирования и декодирования. Они используются для кодирования и декодирования [*сертификатов*](../secgloss/c-gly.md), [*списков отзыва сертификатов*](../secgloss/c-gly.md) (CRL), [*запросов сертификатов*](../secgloss/c-gly.md)и расширений сертификатов.

| Функция                                           | Описание                                                                                                                                      |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**криптдекодеобжект**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject)     | Декодирует структуру типа *лпсзструкттипе*.                                                                                                    |
| [**криптдекодеобжектекс**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobjectex) | Декодирует структуру типа *лпсзструкттипе*. [**Криптдекодеобжектекс**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobjectex) поддерживает параметр выделения памяти с одним проходом. |
| [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject)     | Кодирует структуру типа *лпсзструкттипе*.                                                                                                    |
| [**криптенкодеобжектекс**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobjectex) | Кодирует структуру типа *лпсзструкттипе*. [**Криптенкодеобжектекс**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobjectex) поддерживает параметр выделения памяти с одним проходом. |



 

### <a name="data-encryption-and-decryption-functions"></a>Функции шифрования и расшифровки данных

Следующие функции поддерживают операции шифрования и расшифровки. Перед вызовом [**криптенкрипт**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt) и [**криптдекрипт**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecrypt) требуется [*криптографический ключ*](../secgloss/c-gly.md) . Это делается с помощью функции [**криптженкэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey), [**криптдеривекэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey)или [**криптимпорткэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) . Алгоритм шифрования указывается при создании ключа. [**Криптсеткэйпарам**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) может задавать дополнительные параметры шифрования.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Функция</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecrypt"><strong>криптдекрипт</strong></a></td>
<td><blockquote>
[!Important]<br />
Это нерекомендуемый API. Новое и существующее программное обеспечение должно начинаться с использования <a href="/windows/desktop/SecCNG/cng-portal">API-интерфейсов следующего поколения шифрования.</a> Корпорация Майкрософт может удалить этот API в будущих выпусках.
</blockquote>
<br/> Расшифровывает фрагмент <a href="/windows/desktop/SecGloss/c-gly"><em>зашифрованного текста</em></a> с помощью указанного ключа шифрования.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt"><strong>криптенкрипт</strong></a></td>
<td><blockquote>
[!Important]<br />
Это нерекомендуемый API. Новое и существующее программное обеспечение должно начинаться с использования <a href="/windows/desktop/SecCNG/cng-portal">API-интерфейсов следующего поколения шифрования.</a> Корпорация Майкрософт может удалить этот API в будущих выпусках.
</blockquote>
<br/> Шифрует раздел <a href="/windows/desktop/SecGloss/p-gly"><em>открытого текста</em></a> с помощью указанного ключа шифрования.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dpapi/nf-dpapi-cryptprotectdata"><strong>CryptProtectData</strong></a></td>
<td>Выполняет шифрование данных в структуре <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)"><strong>DATA_BLOB</strong></a> .</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dpapi/nf-dpapi-cryptprotectmemory"><strong>CryptProtectMemory</strong></a></td>
<td>Шифрует память для защиты конфиденциальных данных.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dpapi/nf-dpapi-cryptunprotectdata"><strong>CryptUnprotectData</strong></a></td>
<td>Выполняет расшифровку и проверку целостности данных в <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)"><strong>DATA_BLOB</strong></a>.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dpapi/nf-dpapi-cryptunprotectmemory"><strong>CryptUnprotectMemory</strong></a></td>
<td>Расшифровывает память, зашифрованную с помощью <a href="/windows/desktop/api/Dpapi/nf-dpapi-cryptprotectmemory"><strong>криптпротектмемори</strong></a>.</td>
</tr>
</tbody>
</table>



 

### <a name="hash-and-digital-signature-functions"></a>Функции хэширования и цифровой подписи

Эти функции вычисляют [*хэши*](../secgloss/h-gly.md) данных, а также создают и проверяют [*цифровые подписи*](../secgloss/d-gly.md). Хэши также называются дайджестами сообщений.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Функция</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash"><strong>CryptCreateHash</strong></a></td>
<td><blockquote>
[!Important]<br />
Это нерекомендуемый API. Новое и существующее программное обеспечение должно начинаться с использования <a href="/windows/desktop/SecCNG/cng-portal">API-интерфейсов следующего поколения шифрования.</a> Корпорация Майкрософт может удалить этот API в будущих выпусках.
</blockquote>
<br/> Создает пустой хэш-объект.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroyhash"><strong>криптдестройхаш</strong></a></td>
<td><blockquote>
[!Important]<br />
Это нерекомендуемый API. Новое и существующее программное обеспечение должно начинаться с использования <a href="/windows/desktop/SecCNG/cng-portal">API-интерфейсов следующего поколения шифрования.</a> Корпорация Майкрософт может удалить этот API в будущих выпусках.
</blockquote>
<br/> Уничтожает хэш-объект.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptduplicatehash"><strong>криптдупликатехаш</strong></a></td>
<td>Дублирует хэш-объект.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgethashparam"><strong>CryptGetHashParam</strong></a></td>
<td>Извлекает параметр хэш-объекта.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata"><strong>CryptHashData</strong></a></td>
<td><blockquote>
[!Important]<br />
Это нерекомендуемый API. Новое и существующее программное обеспечение должно начинаться с использования <a href="/windows/desktop/SecCNG/cng-portal">API-интерфейсов следующего поколения шифрования.</a> Корпорация Майкрософт может удалить этот API в будущих выпусках.
</blockquote>
<br/> Хэширует блок данных, добавляя его в указанный хэш-объект.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashsessionkey"><strong>крипсашсессионкэй</strong></a></td>
<td><blockquote>
[!Important]<br />
Это нерекомендуемый API. Новое и существующее программное обеспечение должно начинаться с использования <a href="/windows/desktop/SecCNG/cng-portal">API-интерфейсов следующего поколения шифрования.</a> Корпорация Майкрософт может удалить этот API в будущих выпусках.
</blockquote>
<br/> Хэширует ключ сеанса, добавляя его в указанный хэш-объект.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsethashparam"><strong>криптсесашпарам</strong></a></td>
<td><blockquote>
[!Important]<br />
Это нерекомендуемый API. Новое и существующее программное обеспечение должно начинаться с использования <a href="/windows/desktop/SecCNG/cng-portal">API-интерфейсов следующего поколения шифрования.</a> Корпорация Майкрософт может удалить этот API в будущих выпусках.
</blockquote>
<br/> Задает параметр хэш-объекта.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignhasha"><strong>криптсигнхаш</strong></a></td>
<td><blockquote>
[!Important]<br />
Это нерекомендуемый API. Новое и существующее программное обеспечение должно начинаться с использования <a href="/windows/desktop/SecCNG/cng-portal">API-интерфейсов следующего поколения шифрования.</a> Корпорация Майкрософт может удалить этот API в будущих выпусках.
</blockquote>
<br/> Подписывает указанный хэш-объект.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cryptuiapi/nf-cryptuiapi-cryptuiwizdigitalsign"><strong>криптуивиздигиталсигн</strong></a></td>
<td>Отображает мастер, который выполняет цифровую подпись документа или <a href="/windows/desktop/SecGloss/b-gly"><em>большого двоичного объекта</em></a>.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cryptuiapi/nf-cryptuiapi-cryptuiwizfreedigitalsigncontext"><strong>криптуивизфридигиталсигнконтекст</strong></a></td>
<td>Освобождает указатель на структуру <a href="/windows/desktop/api/Cryptuiapi/ns-cryptuiapi-cryptui_wiz_digital_sign_context"><strong>CRYPTUI_WIZ_DIGITAL_SIGN_CONTEXT</strong></a> .</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifysignaturea"><strong>криптверифисигнатуре</strong></a></td>
<td><blockquote>
[!Important]<br />
Это нерекомендуемый API. Новое и существующее программное обеспечение должно начинаться с использования <a href="/windows/desktop/SecCNG/cng-portal">API-интерфейсов следующего поколения шифрования.</a> Корпорация Майкрософт может удалить этот API в будущих выпусках.
</blockquote>
<br/> Проверяет цифровую подпись при наличии маркера для хэш-объекта.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cryptuiapi/nc-cryptuiapi-pfncfilterproc"><strong>пфнкфилтерпрок</strong></a></td>
<td>Фильтрует сертификаты, которые отображаются в мастере цифровых подписей, отображаемом функцией <a href="/windows/desktop/api/Cryptuiapi/nf-cryptuiapi-cryptuiwizdigitalsign"><strong>криптуивиздигиталсигн</strong></a> .</td>
</tr>
</tbody>
</table>



 

## <a name="certificate-and-certificate-store-functions"></a>Функции сертификатов и хранилища сертификатов

Функции сертификатов и хранилища сертификатов управляют использованием, хранением и извлечением [*сертификатов*](../secgloss/c-gly.md), [*списков отзыва сертификатов*](../secgloss/c-gly.md) (CRL) и [*списков доверия сертификатов*](../secgloss/c-gly.md) (CTL). Эти функции делятся на следующие группы:

-   Функции хранилища сертификатов
-   Функции обслуживания сертификатов и хранилища сертификатов
-   Функции сертификата
-   Функции списка отзыва сертификатов
-   Функции списка доверия сертификатов
-   Функции расширенных свойств
-   Функции MakeCert

### <a name="certificate-store-functions"></a>Функции хранилища сертификатов

С течением времени сайт пользователя может получить много сертификатов. Как правило, сайт имеет сертификаты для пользователя сайта, а также другие сертификаты, описывающие этих пользователей и сущности, с которыми взаимодействует пользователь. Для каждой сущности может существовать более одного сертификата. Для каждого отдельного сертификата должна существовать цепочка проверки сертификатов, которая обеспечивает обратный доступ к доверенному [*корневому сертификату*](../secgloss/r-gly.md). [*Хранилища сертификатов*](../secgloss/c-gly.md) и связанные с ними функции предоставляют функциональные возможности для хранения, извлечения, перечисления, проверки и использования сведений, хранящихся в сертификатах.

| Функция                                                               | Описание                                                                                                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**цертаддсторетоколлектион**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddstoretocollection)           | Добавляет хранилище сертификатов одного уровня в хранилище сертификатов коллекции.                                                                                                                                                                                                                                                                       |
| [**цертклосесторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore)                               | Закрывает обработчик хранилища сертификатов.                                                                                                                                                                                                                                                                                                        |
| [**цертконтролсторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcontrolstore)                           | Позволяет приложению получать уведомления о различиях между содержимым кэшированного хранилища и содержимым хранилища, которое сохраняется в хранилище. Он также обеспечивает отработку несинхронизированного кэшированного хранилища, если это необходимо, и предоставляет средства для фиксации изменений, внесенных в кэшированное хранилище, в постоянное хранилище.<br/> |
| [**цертдупликатесторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certduplicatestore)                       | Дублирует маркер хранилища, увеличивая [*число ссылок*](../secgloss/r-gly.md).                                                                                                                                                                                            |
| [**цертенумфисикалсторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumphysicalstore)                 | Перечисляет физические хранилища для указанного системного хранилища.                                                                                                                                                                                                                                                                              |
| [**цертенумсистемсторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumsystemstore)                     | Перечисляет все доступные системные хранилища.                                                                                                                                                                                                                                                                                                   |
| [**цертенумсистемсторелокатион**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumsystemstorelocation)     | Перечисляет все расположения, имеющие доступное системное хранилище.                                                                                                                                                                                                                                                                      |
| [**цертжетсторепроперти**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetstoreproperty)                   | Возвращает свойство хранилища.                                                                                                                                                                                                                                                                                                                    |
| [**цертопенсторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore)                                 | Открывает хранилище сертификатов с использованием указанного типа поставщика хранилища.                                                                                                                                                                                                                                                                          |
| [**цертопенсистемсторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopensystemstorea)                     | Открывает системное хранилище сертификатов на основе протокола подсистемы.                                                                                                                                                                                                                                                                           |
| [**цертрегистерфисикалсторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certregisterphysicalstore)         | Добавляет физическое хранилище в коллекцию системных хранилищ реестра.                                                                                                                                                                                                                                                                              |
| [**цертрегистерсистемсторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certregistersystemstore)             | Регистрирует системное хранилище.                                                                                                                                                                                                                                                                                                                 |
| [**цертремовесторефромколлектион**](/windows/desktop/api/Wincrypt/nf-wincrypt-certremovestorefromcollection) | Удаляет одноуровневый хранилище сертификатов из хранилища коллекции.                                                                                                                                                                                                                                                                              |
| [**цертсавесторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsavestore)                                 | Сохраняет хранилище сертификатов.                                                                                                                                                                                                                                                                                                              |
| [**цертсетсторепроперти**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetstoreproperty)                   | Задает свойство хранилища.                                                                                                                                                                                                                                                                                                                    |
| [**цертунрегистерфисикалсторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certunregisterphysicalstore)     | Удаляет физическое хранилище из указанной коллекции системных хранилищ.                                                                                                                                                                                                                                                                        |
| [**цертунрегистерсистемсторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certunregistersystemstore)         | Отменяет регистрацию указанного системного хранилища.                                                                                                                                                                                                                                                                                                     |
| [**криптуивизекспорт**](/windows/desktop/api/Cryptuiapi/nf-cryptuiapi-cryptuiwizexport)                           | Содержит мастер, который экспортирует сертификат, список доверия сертификатов (CTL), список отзыва сертификатов (CRL) или хранилище сертификатов.                                                                                                                                                                                                      |
| [**криптуивизимпорт**](/windows/desktop/api/Cryptuiapi/nf-cryptuiapi-cryptuiwizimport)                           | Содержит мастер, который импортирует сертификат, список доверия сертификатов (CTL), список отзыва сертификатов (CRL) или хранилище сертификатов.                                                                                                                                                                                                      |



 

### <a name="certificate-and-certificate-store-maintenance-functions"></a>Функции обслуживания сертификатов и хранилища сертификатов

Интерфейс CryptoAPI предоставляет набор общих функций обслуживания сертификатов и хранилища сертификатов.

| Функция                                                                                                                              | Описание                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**цертаддсериализеделементтосторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddserializedelementtostore)                                                            | Добавляет сериализованный сертификат или элемент списка отзыва сертификатов в хранилище.                                   |
| [**церткреатеконтекст**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatecontext)                                                                                        | Создает указанный контекст из закодированных байтов. Новый контекст не помещается в хранилище. |
| [**цертенумсубжектинсортедктл**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumsubjectinsortedctl)                                                                      | Перечисляет Трустедсубжектс в отсортированном контексте CTL.                                        |
| [**цертфиндсубжектинктл**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindsubjectinctl)                                                                                  | Находит указанную тему в списке доверия сертификатов.                                                          |
| [**цертфиндсубжектинсортедктл**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindsubjectinsortedctl)                                                                      | Находит указанную тему в отсортированном списке доверия сертификатов.                                                   |
| [**Опенперсоналтрустдбдиалог**](/windows/desktop/api/wintrust/nf-wintrust-openpersonaltrustdbdialog) и [ **опенперсоналтрустдбдиаложекс**](/windows/desktop/api/wintrust/nf-wintrust-openpersonaltrustdbdialogex) | Отображает диалоговое окно **Сертификаты** .                                                      |



 

### <a name="certificate-functions"></a>Функции сертификата

Большинство функций [*сертификатов*](../secgloss/c-gly.md) имеют связанные функции для работы с списками [*отзыва сертификатов*](../secgloss/c-gly.md) и [*CTL*](../secgloss/c-gly.md). Дополнительные сведения о связанных функциях CRL и CTL см. в разделе функции списка отзыва сертификатов и функции списков доверия сертификатов.

| Функция                                                                             | Описание                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**цертаддцертификатеконтексттосторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatecontexttostore)         | Добавляет контекст сертификата в хранилище сертификатов.                                                                                                                                                                                            |
| [**цертаддцертификателинктосторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatelinktostore)               | Добавляет ссылку в хранилище сертификатов в контекст сертификата в другом хранилище.                                                                                                                                                               |
| [**CertAddEncodedCertificateToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedcertificatetostore)         | Преобразует закодированный сертификат в контекст сертификата, а затем добавляет контекст в хранилище сертификатов.                                                                                                                                  |
| [**цертаддрефсерверокспреспонсе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddrefserverocspresponse)                 | Увеличивает значение счетчика ссылок для обработчика **\_ \_ \_ ответов OCSP сервера хцерт** .                                                                                                                                                                 |
| [**цертаддрефсерверокспреспонсеконтекст**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddrefserverocspresponsecontext)   | Увеличивает значение счетчика ссылок для структуры [**\_ \_ \_ \_ контекста ответа OCSP сервера сертификатов**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_server_ocsp_response_context) .                                                                                                              |
| [**цертклосесерверокспреспонсе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcloseserverocspresponse)                   | Закрывается маркер ответа сервера [*протокола*](../secgloss/o-gly.md) OCSP.                                               |
| [**церткреатецертификатеконтекст**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatecertificatecontext)                 | Создает контекст сертификата из закодированного сертификата. Созданный контекст не помещается в хранилище сертификатов.                                                                                                                               |
| [**церткреатеселфсигнцертификате**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreateselfsigncertificate)               | создает самозаверяющий сертификат;                                                                                                                                                                                                              |
| [**цертделетецертификатефромсторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletecertificatefromstore)             | Удаляет сертификат из хранилища сертификатов.                                                                                                                                                                                               |
| [**цертдупликатецертификатеконтекст**](/windows/desktop/api/Wincrypt/nf-wincrypt-certduplicatecertificatecontext)           | Дублирует контекст сертификата, увеличивая его [*число ссылок*](../secgloss/r-gly.md).                                                                                           |
| [**цертенумцертификатесинсторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumcertificatesinstore)                   | Перечисляет контексты сертификатов в хранилище сертификатов.                                                                                                                                                                                   |
| [**цертфиндцертификатеинсторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateinstore)                     | Находит первый (или следующий) контекст сертификата в хранилище сертификатов, соответствующий критерию поиска.                                                                                                                                           |
| [**цертфрицертификатеконтекст**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatecontext)                     | Освобождает контекст сертификата.                                                                                                                                                                                                                    |
| [**цертжетиссуерцертификатефромсторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetissuercertificatefromstore)       | Возвращает контекст сертификата из хранилища сертификатов для первого или следующего издателя указанного сертификата субъекта.                                                                                                                      |
| [**цертжетсерверокспреспонсеконтекст**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetserverocspresponsecontext)         | Извлекает неблокирующий времени допустимый контекст ответа [*протокола*](../secgloss/o-gly.md) OCSP для указанного маркера. |
| [**цертжетсубжектцертификатефромсторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetsubjectcertificatefromstore)     | Получает из хранилища сертификатов контекст сертификата субъекта, который однозначно идентифицируется его издателем и серийным номером.                                                                                                                  |
| [**цертжетвалидусажес**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetvalidusages)                                     | Возвращает массив использования, состоящий из пересечения допустимых использований для всех сертификатов в массиве сертификатов.                                                                                                               |
| [**цертопенсерверокспреспонсе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenserverocspresponse)                     | Открывает обработчик для ответа [*протокола*](../secgloss/o-gly.md) OCSP, связанного с цепочкой сертификатов сервера.       |
| [**цертретриевелогурбиометриЦинфо**](/windows/desktop/api/Wincrypt/nf-wincrypt-certretrievelogoorbiometricinfo)           | Выполняет получение URL-адреса эмблемы или биометрических данных, указанных в расширении сертификата **\_ биометрического \_** **сзоид \_ LOGOTYPE \_ ext** или сзоид.                                                                                  |
| [**цертселектцертификате**](/windows/win32/api/cryptdlg/nf-cryptdlg-certselectcertificatea)                               | Представляет диалоговое окно, позволяющее пользователю выбирать сертификаты из набора сертификатов, соответствующих заданным критериям.                                                                                                                       |
| [**цертселектцертификатечаинс**](/windows/desktop/api/Wincrypt/nf-wincrypt-certselectcertificatechains)                   | Извлекает цепочки сертификатов на основе указанных критериев выбора.                                                                                                                                                                             |
| [**цертселектионжетсериализедблоб**](/windows/desktop/api/Cryptuiapi/nf-cryptuiapi-certselectiongetserializedblob)             | Вспомогательная функция, используемая для получения сериализованного [*BLOB-объекта*](../secgloss/b-gly.md) сертификата из структуры [**\_ \_ ввода сертификата селектуи**](/windows/desktop/api/Cryptuiapi/ns-cryptuiapi-cert_selectui_input) .                                               |
| [**цертсериализецертификатесторилемент**](/windows/desktop/api/Wincrypt/nf-wincrypt-certserializecertificatestoreelement) | Сериализует закодированный сертификат контекста сертификата и закодированное представление его свойств.                                                                                                                                         |
| [**CertVerifySubjectCertificateContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certverifysubjectcertificatecontext)   | Выполняет включенные проверки сертификата субъекта с помощью издателя.                                                                                                                                                           |
| [**криптуидлгцертмгр**](/windows/desktop/api/Cryptuiapi/nf-cryptuiapi-cryptuidlgcertmgr)                                       | Отображает диалоговое окно, позволяющее пользователю управлять сертификатами.                                                                                                                                                                              |
| [**криптуидлгселектцертификате**](cryptuidlgselectcertificate.md)                   | Отображает диалоговое окно, позволяющее пользователю выбрать сертификат.                                                                                                                                                                               |
| [**криптуидлгселектцертификатефромсторе**](/windows/desktop/api/Cryptuiapi/nf-cryptuiapi-cryptuidlgselectcertificatefromstore) | Отображает диалоговое окно, позволяющее выбрать сертификат из указанного хранилища.                                                                                                                                                        |
| [**криптуидлгвиевцертификате**](/windows/desktop/api/Cryptuiapi/nf-cryptuiapi-cryptuidlgviewcertificatea)                       | Представляет диалоговое окно, в котором отображается указанный сертификат.                                                                                                                                                                                    |
| [**криптуидлгвиевконтекст**](/windows/desktop/api/Cryptuiapi/nf-cryptuiapi-cryptuidlgviewcontext)                               | Отображает сертификат, список отзыва сертификатов или список доверия сертификатов.                                                                                                                                                                                                            |
| [**криптуидлгвиевсигнеринфо**](cryptuidlgviewsignerinfo.md)                         | Отображает диалоговое окно, содержащее сведения о подписавшем для подписанного сообщения.                                                                                                                                                                |
| [**жетфриендлинамеофцерт**](/windows/desktop/api/CryptDlg/nf-cryptdlg-getfriendlynameofcerta)                               | Извлекает отображаемое имя для сертификата.                                                                                                                                                                                                   |
| [**ркэйклосекэйсервице**](rkeyclosekeyservice.md)                                   | Закрывает маркер службы ключей.                                                                                                                                                                                                                    |
| [**ркэйопенкэйсервице**](rkeyopenkeyservice.md)                                     | Открывает маркер службы ключей на удаленном компьютере.                                                                                                                                                                                                |
| [**ркэйпфксинсталл**](rkeypfxinstall.md)                                             | Устанавливает сертификат на удаленном компьютере.                                                                                                                                                                                                    |



 

### <a name="certificate-revocation-list-functions"></a>Функции списка отзыва сертификатов

Эти функции управляют хранением и извлечением [*списков отзыва сертификатов*](../secgloss/c-gly.md) (CRL).

| Функция                                                             | Описание                                                                                                                                                                           |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**цертаддкрлконтексттосторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcrlcontexttostore)         | Добавляет контекст списка отзыва сертификатов в хранилище сертификатов.                                                                                                                                          |
| [**цертаддкрллинктосторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcrllinktostore)               | Добавляет ссылку в хранилище в контекст списка отзыва сертификатов в другом хранилище.                                                                                                                         |
| [**цертадденкодедкрлтосторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedcrltostore)         | Преобразует закодированный CRL в контекст списка отзыва сертификатов, а затем добавляет контекст в хранилище сертификатов.                                                                                        |
| [**церткреатекрлконтекст**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatecrlcontext)                 | Создает контекст списка отзыва сертификатов из закодированного списка отзыва сертификатов. Созданный контекст не помещается в хранилище сертификатов.                                                                                     |
| [**цертделетекрлфромсторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletecrlfromstore)             | Удаляет список отзыва сертификатов из хранилища сертификатов.                                                                                                                                             |
| [**цертдупликатекрлконтекст**](/windows/desktop/api/Wincrypt/nf-wincrypt-certduplicatecrlcontext)           | Дублирует контекст списка отзыва сертификатов, увеличивая [*число ссылок*](../secgloss/r-gly.md).                                         |
| [**цертенумкрлсинсторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumcrlsinstore)                   | Перечисляет контексты CRL в хранилище.                                                                                                                                               |
| [**цертфиндцертификатеинкрл**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateincrl)         | Поиск указанного сертификата в [*списке отзыва сертификатов*](../secgloss/c-gly.md) (CRL). |
| [**цертфиндкрлинсторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcrlinstore)                     | Поиск первого или следующего контекста списка отзыва сертификатов в хранилище сертификатов, соответствующего определенному условию.                                                                                     |
| [**цертфрикрлконтекст**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecrlcontext)                     | Освобождает контекст списка отзыва сертификатов.                                                                                                                                                                  |
| [**цертжеткрлфромсторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcrlfromstore)                   | Возвращает первый или следующий контекст списка отзыва сертификатов из хранилища сертификатов для указанного сертификата издателя.                                                                                 |
| [**цертсериализекрлсторилемент**](/windows/desktop/api/Wincrypt/nf-wincrypt-certserializecrlstoreelement) | Сериализует закодированный список CRL контекста списка отзыва сертификатов и его свойства.                                                                                                                          |



 

### <a name="certificate-trust-list-functions"></a>Функции списка доверия сертификатов

Эти функции управляют хранением и извлечением [*списков доверия сертификатов*](../secgloss/c-gly.md) (CTL).

| Функция                                                               | Описание                                                                                                          |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**цертаддктлконтексттосторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddctlcontexttostore)           | Добавляет контекст CTL в хранилище сертификатов.                                                                         |
| [**цертаддктллинктосторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddctllinktostore)                 | Добавляет ссылку в хранилище в контекст списка отзыва сертификатов в другом хранилище.                                                        |
| [**цертадденкодедктлтосторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedctltostore)           | Преобразует закодированный список доверия сертификатов в контекст CTL, а затем добавляет контекст в хранилище сертификатов.                       |
| [**церткреатектлконтекст**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatectlcontext)                   | Создает контекст CTL из списка доверия закодированного сертификата. Созданный контекст не помещается в хранилище сертификатов. |
| [**цертделетектлфромсторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletectlfromstore)               | Удаляет список доверия сертификатов из хранилища сертификатов.                                                                            |
| [**цертдупликатектлконтекст**](/windows/desktop/api/Wincrypt/nf-wincrypt-certduplicatectlcontext)             | Дублирует контекст CTL, увеличивая счетчик ссылок.                                                        |
| [**цертенумктлсинсторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumctlsinstore)                     | Перечисляет контексты CTL в хранилище сертификатов.                                                                |
| [**цертфиндктлинсторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore)                       | Находит первый (или следующий) контекст CTL в хранилище сертификатов, соответствующий указанным критериям.                     |
| [**цертфриктлконтекст**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreectlcontext)                       | Освобождает контекст CTL.                                                                                                 |
| [**цертмодифицертификатестотруст**](/windows/desktop/api/CryptDlg/nf-cryptdlg-certmodifycertificatestotrust) | Изменяет набор сертификатов в списке доверия (CTL) для данной цели.                                                       |
| [**цертсериализектлсторилемент**](/windows/desktop/api/Wincrypt/nf-wincrypt-certserializectlstoreelement)   | Сериализует закодированный CTL контекста CTL и его свойства.                                                         |



 

### <a name="extended-property-functions"></a>Функции расширенных свойств

Следующие функции работают с расширенными свойствами сертификатов, списков отзыва сертификатов и списков CTL.

| Функция                                                                             | Описание                                                      |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [**цертенумцертификатеконтекстпропертиес**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumcertificatecontextproperties) | Перечисляет свойства для указанного контекста сертификата. |
| [**цертенумкрлконтекстпропертиес**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumcrlcontextproperties)                 | Перечисляет свойства для указанного контекста списка отзыва сертификатов.         |
| [**цертенумктлконтекстпропертиес**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumctlcontextproperties)                 | Перечисляет свойства для указанного контекста CTL.         |
| [**цертжетцертификатеконтекстпроперти**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty)       | Извлекает свойства сертификата.                                |
| [**цертжеткрлконтекстпроперти**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcrlcontextproperty)                       | Получает свойства списка отзыва сертификатов.                                        |
| [**цертжетктлконтекстпроперти**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetctlcontextproperty)                       | Извлекает свойства CTL.                                        |
| [**цертсетцертификатеконтекстпроперти**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetcertificatecontextproperty)       | Задает свойства сертификата.                                     |
| [**цертсеткрлконтекстпроперти**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetcrlcontextproperty)                       | Задает свойства списка отзыва сертификатов.                                             |
| [**цертсетктлконтекстпроперти**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetctlcontextproperty)                       | Задает свойства CTL.                                             |



 

## <a name="makecert-functions"></a>Функции MakeCert

Следующие функции поддерживают средство [MakeCert](makecert.md) .



| Функция                                                                               | Описание                                                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**фрикриптпровфромцерт**](freecryptprovfromcert.md)                                 | Освобождает дескриптор [*поставщика служб шифрования*](../secgloss/c-gly.md) (CSP) и при необходимости удаляет временный контейнер, созданный функцией [**жеткриптпровфромцерт**](getcryptprovfromcert.md) . |
| [**жеткриптпровфромцерт**](getcryptprovfromcert.md)                                   | Возвращает маркер CSP и ключевую спецификацию для контекста сертификата.                                                                                                                                                                                                                                |
| [**пвкфрикриптпров**](pvkfreecryptprov.md)                                           | Освобождает дескриптор CSP и при необходимости удаляет временный контейнер, созданный функцией [**пвкжеткриптпров**](pvkgetcryptprov.md) .                                                                                                                                                          |
| [**пвкжеткриптпров**](pvkgetcryptprov.md)                                             | Возвращает маркер CSP на основе имени файла [*закрытого ключа*](../secgloss/p-gly.md) или имени контейнера ключей.                                                                                                                                          |
| [**пвкприватекэйаккуиреконтекстфроммемори**](pvkprivatekeyacquirecontextfrommemory.md) | Создает временный контейнер в CSP и загружает закрытый ключ из памяти в контейнер.                                                                                                                                                                                                         |
| [**пвкприватекэйсаве**](pvkprivatekeysave.md)                                         | Сохраняет закрытый ключ и соответствующий [*открытый ключ*](../secgloss/p-gly.md) в указанном файле.                                                                                                                                                          |
| [**сигнеррор**](signerror.md)                                                         | Вызывает [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) и преобразует код возврата в **значение HRESULT**.                                                                                                                                                                                                              |



 

## <a name="certificate-verification-functions"></a>Функции проверки сертификатов

Сертификаты проверяются с помощью [*списков CTL*](../secgloss/c-gly.md) или цепочек сертификатов. Функции предоставляются для обоих типов:

-   Функции проверки с использованием списков CTL
-   Функции проверки цепочки сертификатов

### <a name="verification-functions-using-ctls"></a>Функции проверки с использованием списков CTL

Эти функции используют списки CTL в процессе проверки. Дополнительные функции для работы с CTL можно найти в функциях списков доверия сертификатов и функциях расширенных свойств.

Следующие функции используют списки CTL непосредственно для проверки.

| Функция                                                         | Описание                                  |
|------------------------------------------------------------------|----------------------------------------------|
| [**цертверификтлусаже**](/windows/desktop/api/Wincrypt/nf-wincrypt-certverifyctlusage)                 | Проверяет использование списка доверия сертификатов.                 |
| [**криптмсженкодеандсигнктл**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgencodeandsignctl)     | Кодирует и подписывает список доверия сертификатов как сообщение.        |
| [**криптмсгжетандверифисигнер**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetandverifysigner) | Извлекает и проверяет список доверия сертификатов из сообщения. |
| [**криптмсгсигнктл**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgsignctl)                       | Подписывает сообщение, содержащее список доверия сертификатов.         |



 

### <a name="certificate-chain-verification-functions"></a>Функции проверки цепочки сертификатов

Цепочки сертификатов создаются для предоставления доверенных сведений о отдельных сертификатах.

| Имя функции                                                                                                    | Описание                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**церткреатецертификатечаиненгине**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatecertificatechainengine)                                     | Создает новый, не используемый по умолчанию механизм цепочки для приложения.                                                                                                                                                          |
| [**церткреатектлентрифромцертификатеконтекстпропертиес**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatectlentryfromcertificatecontextproperties) | Создает запись CTL, атрибуты которой являются свойствами контекста сертификата.                                                                                                                                      |
| [**цертдупликатецертификатечаин**](/windows/desktop/api/Wincrypt/nf-wincrypt-certduplicatecertificatechain)                                           | Дублирует цепочку сертификатов, увеличивая [*счетчик ссылок*](../secgloss/r-gly.md) цепочки и возвращая указатель на цепочку.                    |
| [**цертфиндчаининсторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindchaininstore)                                                             | Находит первый (или следующий) контекст цепочки сертификатов в хранилище.                                                                                                                                                     |
| [**цертфрицертификатечаин**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatechain)                                                     | Освобождает цепочку сертификатов, уменьшая ее число ссылок.                                                                                                                                                          |
| [**цертфрицертификатечаиненгине**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatechainengine)                                         | Освобождает механизм цепочки сертификатов, отличный от используемого по умолчанию.                                                                                                                                                                        |
| [**цертфрицертификатечаинлист**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatechainlist)                                             | Освобождает массив указателей на контексты цепочки.                                                                                                                                                                      |
| [**CertGetCertificateChain**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatechain)                                                       | Создает контекст цепочки, начиная с конечного сертификата, и возвращается к доверенному [*корневому сертификату*](../secgloss/r-gly.md), если это возможно.                |
| [**цертисвалидкрлфорцертификате**](/windows/desktop/api/Wincrypt/nf-wincrypt-certisvalidcrlforcertificate)                                             | Проверяет [*список отзыва сертификатов*](../secgloss/c-gly.md) , чтобы определить, будет ли он включать определенный сертификат, если сертификат был отозван. |
| [**цертсетцертификатеконтекстпропертиесфромктлентри**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetcertificatecontextpropertiesfromctlentry)       | Задает свойства контекста сертификата с помощью атрибутов в записи CTL.                                                                                                                                   |
| [**цертверифицертификатечаинполици**](/windows/desktop/api/Wincrypt/nf-wincrypt-certverifycertificatechainpolicy)                                     | Проверяет цепочку сертификатов, чтобы проверить ее допустимость, включая ее соответствие с любыми указанными условиями политики срока действия.                                                                                            |



 

## <a name="message-functions"></a>Функции сообщений

Функции сообщений [*CryptoAPI*](../secgloss/c-gly.md) состоят из двух групп функций: низкоуровневых функций сообщений и [*упрощенных функций сообщений*](../secgloss/s-gly.md).

Функции сообщений низкого уровня создают и работают непосредственно с \# сообщениями PKCS 7. Эти функции кодируют \# данные PKCS 7 для передачи и декодирования \# полученных данных PKCS 7. Они также расшифровываются и проверяют подписи полученных сообщений. Общие сведения о \# стандартных и обычных сообщениях PKCS 7 см. в разделе [сообщения низкого уровня](low-level-messages.md).

Упрощенные функции сообщений находятся на более высоком уровне и заключают несколько низкоуровневых функций обработки сообщений и функций сертификатов в отдельные функции, выполняющие определенную задачу особым образом. Эти функции уменьшают число вызовов функций, необходимых для выполнения задачи, тем самым упрощая использование CryptoAPI. Общие сведения об упрощенных сообщениях см. в разделе [упрощенные сообщения](simplified-messages.md).

-   Низкоуровневые функции сообщений
-   Упрощенные функции сообщений

### <a name="low-level-message-functions"></a>Низкоуровневые функции сообщений

Низкоуровневые функции сообщений предоставляют функции, необходимые для кодирования данных для передачи и расшифровки \# полученных сообщений PKCS 7. Также предоставляется функциональность для расшифровки и проверки сигнатур полученных сообщений. Использовать эти низкоуровневые функции сообщений в большинстве приложений не рекомендуется. Для большинства приложений предпочтительнее использовать упрощенные функции сообщений, которые заключают несколько низкоуровневых функций сообщений в один вызов функции.

| Функция                                                                                   | Описание                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**криптмсгкалкулатинкодедленгс**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcalculateencodedlength)                   | Вычисляет длину закодированного криптографического сообщения.                                                                                                                                                                     |
| [**криптмсгклосе**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose)                                                     | Закрывает маркер криптографического сообщения.                                                                                                                                                                                    |
| [**криптмсгконтрол**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol)                                                 | Выполняет специальную функцию управления после окончательного [**криптмсгупдате**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) закодированного или декодированного криптографического сообщения.                                                                                   |
| [**криптмсгкаунтерсигн**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcountersign)                                         | Каунтерсигнс уже существующую подпись в сообщении.                                                                                                                                                                       |
| [**криптмсгкаунтерсигненкодед**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcountersignencoded)                           | Каунтерсигнс уже существующую сигнатуру (закодированную SignerInfo, как определено в PKCS \# 7).                                                                                                                                       |
| [**криптмсгдупликате**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgduplicate)                                             | Дублирует криптографический обработчик сообщений, увеличивая [*число ссылок*](../secgloss/r-gly.md). Счетчик ссылок отслеживает время существования сообщения. |
| [**криптмсгжетпарам**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam)                                               | Получает параметр после кодирования или декодирования криптографического сообщения.                                                                                                                                                       |
| [**криптмсгопентодекоде**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode)                                       | Открывает криптографическое сообщение для декодирования.                                                                                                                                                                                    |
| [**криптмсгопентоенкоде**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentoencode)                                       | Открывает криптографическое сообщение для кодирования.                                                                                                                                                                                    |
| [**криптмсгупдате**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate)                                                   | Обновляет содержимое криптографического сообщения.                                                                                                                                                                               |
| [**криптмсгверификаунтерсигнатуринкодед**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgverifycountersignatureencoded)     | Проверяет [*подпись другой стороны*](../secgloss/c-gly.md) в терминах структуры SignerInfo (как определено в PKCS \# 7).                                                   |
| [**криптмсгверификаунтерсигнатуринкодедекс**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgverifycountersignatureencodedex) | Проверяет, содержит ли параметр *пбсигнеринфокаунтерсигнатуре* зашифрованный [*хэш-код*](../secgloss/h-gly.md) поля **енкриптеддижест** структуры параметра *пбсигнеринфо* .   |



 

### <a name="simplified-message-functions"></a>Упрощенные функции сообщений

[*упрощенные функции сообщений*](../secgloss/s-gly.md) заключают низкоуровневые функции сообщений в одну функцию для выполнения указанной задачи.

| Функция                                                                               | Описание                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**криптдекодемессаже**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodemessage)                                       | Декодирует криптографическое сообщение.                                                                                                                                                                                                                                             |
| [**криптдекриптандверифимессажесигнатуре**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptandverifymessagesignature) | Расшифровывает указанное сообщение и проверяет подпись.                                                                                                                                                                                                                     |
| [**криптдекриптмессаже**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage)                                     | Расшифровывает указанное сообщение.                                                                                                                                                                                                                                              |
| [**криптенкриптмессаже**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage)                                     | Шифрует сообщение для получателя или получателей.                                                                                                                                                                                                                        |
| [**криптжетмессажецертификатес**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetmessagecertificates)                     | Возвращает [*хранилище сертификатов*](../secgloss/c-gly.md) , которое содержит сертификаты и [*CRL*](../secgloss/c-gly.md)сообщения. |
| [**криптжетмессажесигнеркаунт**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetmessagesignercount)                       | Возвращает число подписывающих подписей в подписанном сообщении.                                                                                                                                                                                                                          |
| [**крипсашмессаже**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashmessage)                                           | Создает хэш сообщения.                                                                                                                                                                                                                                               |
| [**криптсигнанденкриптмессаже**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignandencryptmessage)                       | Подписывает сообщение, а затем шифрует его для получателя или получателей.                                                                                                                                                                                                     |
| [**криптсигнмессажевискэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignmessagewithkey)                             | Подписывает сообщение с помощью закрытого ключа CSP, указанного в параметрах функции.                                                                                                                                                                                       |
| [**криптсигнмессаже**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignmessage)                                           | Подписывает сообщение.                                                                                                                                                                                                                                                           |
| [**криптверифидетачедмессажехаш**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifydetachedmessagehash)               | Проверяет хэшированное сообщение, содержащее отсоединенный хэш.                                                                                                                                                                                                                     |
| [**криптверифидетачедмессажесигнатуре**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifydetachedmessagesignature)     | Проверяет подписанное сообщение, содержащее отсоединенную подпись или подписи.                                                                                                                                                                                                  |
| [**криптверифимессажехаш**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifymessagehash)                               | Проверяет хэшированное сообщение.                                                                                                                                                                                                                                                   |
| [**криптверифимессажесигнатуре**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifymessagesignature)                     | Проверяет подписанное сообщение.                                                                                                                                                                                                                                                   |
| [**криптверифимессажесигнатуревискэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifymessagesignaturewithkey)       | Проверяет подпись подписанного сообщения с помощью указанных сведений об открытом ключе.                                                                                                                                                                                             |



 

## <a name="auxiliary-functions"></a>Вспомогательные функции

Вспомогательные функции группируются следующим образом:

-   Функции Управление данными
-   Функции преобразования данных
-   Функции расширенного использования ключа
-   Функции идентификатора ключа
-   Функции поддержки OID
-   Функции извлечения удаленных объектов
-   Функции PFX

### <a name="data-management-functions"></a>Функции Управление данными

Следующие функции CryptoAPI управляют данными и сертификатами.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Функция</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certcomparecertificate"><strong>церткомпарецертификате</strong></a></td>
<td>Сравнивает два сертификата, чтобы определить, идентичны ли они.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certcomparecertificatename"><strong>церткомпарецертификатенаме</strong></a></td>
<td>Сравнивает два имени сертификата, чтобы определить, идентичны ли они.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certcompareintegerblob"><strong>церткомпареинтежерблоб</strong></a></td>
<td>Сравнивает два целочисленных <a href="/windows/desktop/SecGloss/b-gly"><em>больших двоичных объектов</em></a>.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certcomparepublickeyinfo"><strong>церткомпарепубликкэйинфо</strong></a></td>
<td>Сравнивает два <a href="/windows/desktop/SecGloss/p-gly"><em>открытых ключа</em></a> , чтобы определить, идентичны ли они.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certfindattribute"><strong>цертфиндаттрибуте</strong></a></td>
<td>Находит первый атрибут, идентифицируемый его <a href="/windows/desktop/SecGloss/o-gly"><em>идентификатором объекта</em></a> (OID).</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certfindextension"><strong>цертфиндекстенсион</strong></a></td>
<td>Находит первое расширение, определяемое его идентификатором OID.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certfindrdnattr"><strong>цертфиндрднаттр</strong></a></td>
<td>Находит первый атрибут <a href="/windows/desktop/SecGloss/r-gly"><em>RDN</em></a> , идентифицируемый его ИДЕНТИФИКАТОРом OID, в списке имен <em>относительного различающегося имени</em>.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certgetintendedkeyusage"><strong>цертжетинтендедкэйусаже</strong></a></td>
<td>Получает из сертификата предполагаемые байты использования ключа.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certgetpublickeylength"><strong>цертжетпубликкэйленгс</strong></a></td>
<td>Получает длину битов открытого и закрытого ключей из <a href="/windows/desktop/SecGloss/p-gly"><em>большого двоичного объекта открытого ключа</em></a>.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certisrdnattrsincertificatename"><strong>цертисрднаттрсинцертификатенаме</strong></a></td>
<td>Сравнивает атрибуты в <a href="/windows/desktop/SecGloss/c-gly"><em>имени сертификата</em></a> с заданным <a href="/windows/desktop/api/Wincrypt/ns-wincrypt-cert_rdn"><strong>CERT_RDN</strong></a> , чтобы определить, включены ли там все атрибуты.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certisstronghashtosign"><strong>цертисстронгхаштосигн</strong></a></td>
<td>Определяет, можно ли использовать заданный хэш-алгоритм и открытый ключ в сертификате для подписи для выполнения строгого подписывания.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certverifycrlrevocation"><strong>цертверификрлревокатион</strong></a></td>
<td>Проверяет, что сертификат субъекта не находится в <a href="/windows/desktop/SecGloss/c-gly"><em>списке отзыва сертификатов</em></a> (CRL).</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certverifycrltimevalidity"><strong>цертверификрлтимевалидити</strong></a></td>
<td>Проверка допустимости времени CRL.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certverifyrevocation"><strong>цертверифиревокатион</strong></a></td>
<td>Проверяет, что сертификат субъекта не находится в списке ОТЗЫВА сертификатов.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certverifytimevalidity"><strong>цертверифитимевалидити</strong></a></td>
<td>Проверяет допустимость времени сертификата.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certverifyvaliditynesting"><strong>цертверифивалидитинестинг</strong></a></td>
<td>Проверяет правильность вложений времени субъекта во время действия издателя.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportpkcs8"><strong>CryptExportPKCS8</strong></a></td>
<td>Эта функция заменяется функцией <a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportpkcs8ex"><strong>CryptExportPKCS8Ex</strong></a> .</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportpkcs8ex"><strong>CryptExportPKCS8Ex</strong></a></td>
<td>Экспортирует закрытый ключ в формате PKCS #8.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportpublickeyinfo"><strong>CryptExportPublicKeyInfo</strong></a></td>
<td>Экспортирует сведения об открытом ключе, связанные с соответствующим закрытым ключом поставщика.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportpublickeyinfoex"><strong>криптекспортпубликкэйинфоекс</strong></a></td>
<td>Экспортирует сведения об открытом ключе, связанные с соответствующим закрытым ключом поставщика. Эта функция отличается от <a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportpublickeyinfo"><strong>CryptExportPublicKeyInfo</strong></a> тем, что пользователь может указать алгоритм открытого ключа, тем самым переопределяя значение по умолчанию, предоставляемое CSP.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportpublickeyinfofrombcryptkeyhandle"><strong>криптекспортпубликкэйинфофромбкрипткэйхандле</strong></a></td>
<td>Экспортирует сведения об открытом ключе, связанные с соответствующим закрытым ключом поставщика.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfindcertificatekeyprovinfo"><strong>криптфиндцертификатекэйпровинфо</strong></a></td>
<td>Перечисляет поставщики служб шифрования и их <a href="/windows/desktop/SecGloss/k-gly"><em>контейнеры ключей</em></a> , чтобы найти закрытый ключ, соответствующий открытому ключу сертификата.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfindlocalizedname"><strong>криптфиндлокализеднаме</strong></a></td>
<td>Находит локализованное имя для указанного имени, например, находит локализованное имя для имени хранилища корневой системы.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashcertificate"><strong>крипсашцертификате</strong></a></td>
<td><blockquote>
[!Important]<br />
Это нерекомендуемый API. Новое и существующее программное обеспечение должно начинаться с использования <a href="/windows/desktop/SecCNG/cng-portal">API-интерфейсов следующего поколения шифрования.</a> Корпорация Майкрософт может удалить этот API в будущих выпусках.
</blockquote>
<br/> Хэширует закодированное содержимое.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashcertificate2"><strong>CryptHashCertificate2</strong></a></td>
<td>Хэширует блок данных с помощью поставщика хэша криптографического API: следующего поколения (CNG).</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashpublickeyinfo"><strong>крипсашпубликкэйинфо</strong></a></td>
<td><blockquote>
[!Important]<br />
Это нерекомендуемый API. Новое и существующее программное обеспечение должно начинаться с использования <a href="/windows/desktop/SecCNG/cng-portal">API-интерфейсов следующего поколения шифрования.</a> Корпорация Майкрософт может удалить этот API в будущих выпусках.
</blockquote>
<br/> Вычисление хэша сведений о кодированном открытом ключе.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashtobesigned"><strong>крипсаштобесигнед</strong></a></td>
<td><blockquote>
[!Important]<br />
Это нерекомендуемый API. Новое и существующее программное обеспечение должно начинаться с использования <a href="/windows/desktop/SecCNG/cng-portal">API-интерфейсов следующего поколения шифрования.</a> Корпорация Майкрософт может удалить этот API в будущих выпусках.
</blockquote>
<br/> Вычисление хэша &quot; для подписи &quot; данных в кодированном подписанном содержимом (<a href="/windows/desktop/api/Wincrypt/ns-wincrypt-cert_signed_content_info"><strong>CERT_SIGNED_CONTENT_INFO</strong></a>).</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportpkcs8"><strong>CryptImportPKCS8</strong></a></td>
<td><blockquote>
[!Important]<br />
Это нерекомендуемый API. Новое и существующее программное обеспечение должно начинаться с использования <a href="/windows/desktop/SecCNG/cng-portal">API-интерфейсов следующего поколения шифрования.</a> Корпорация Майкрософт может удалить этот API в будущих выпусках.
</blockquote>
<br/> Импортирует <a href="/windows/desktop/SecGloss/p-gly"><em>закрытый ключ</em></a> в формате PKCS #8 в <a href="/windows/desktop/SecGloss/c-gly"><em>поставщик служб шифрования</em></a> (CSP).</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportpublickeyinfo"><strong>криптимпортпубликкэйинфо</strong></a></td>
<td><blockquote>
[!Important]<br />
Это нерекомендуемый API. Новое и существующее программное обеспечение должно начинаться с использования <a href="/windows/desktop/SecCNG/cng-portal">API-интерфейсов следующего поколения шифрования.</a> Корпорация Майкрософт может удалить этот API в будущих выпусках.
</blockquote>
<br/> Преобразует и импортирует сведения об открытом ключе в поставщик и возвращает маркер открытого ключа.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportpublickeyinfoex"><strong>криптимпортпубликкэйинфоекс</strong></a></td>
<td><blockquote>
[!Important]<br />
Это нерекомендуемый API. Новое и существующее программное обеспечение должно начинаться с использования <a href="/windows/desktop/SecCNG/cng-portal">API-интерфейсов следующего поколения шифрования.</a> Корпорация Майкрософт может удалить этот API в будущих выпусках.
</blockquote>
<br/> Преобразует и импортирует сведения об открытом ключе в поставщик и возвращает маркер открытого ключа. Дополнительные параметры (для заданных <a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportpublickeyinfo"><strong>криптимпортпубликкэйинфо</strong></a>), которые можно использовать для переопределения значений по умолчанию, предоставляются в дополнение <a href="/windows/desktop/api/Wincrypt/ns-wincrypt-cert_public_key_info"><strong>CERT_PUBLIC_KEY_INFO</strong></a>.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportpublickeyinfoex2"><strong>CryptImportPublicKeyInfoEx2</strong></a></td>
<td>Импортирует открытый ключ в поставщик асимметричных CNG.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmemalloc"><strong>криптмемаллок</strong></a></td>
<td>Выделяет память для буфера. Эта память используется всеми функциями Crypt32. lib, которые возвращают выделенные буферы.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmemfree"><strong>криптмемфри</strong></a></td>
<td>Освобождает память, выделенную <a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmemalloc"><strong>криптмемаллок</strong></a> или <a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmemrealloc"><strong>криптмемреаллок</strong></a>.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmemrealloc"><strong>криптмемреаллок</strong></a></td>
<td>Освобождает память, выделенную для буфера, и выделяет память для нового буфера.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptqueryobject"><strong>крипткуерйобжект</strong></a></td>
<td><blockquote>
[!Important]<br />
Это нерекомендуемый API. Новое и существующее программное обеспечение должно начинаться с использования <a href="/windows/desktop/SecCNG/cng-portal">API-интерфейсов следующего поколения шифрования.</a> Корпорация Майкрософт может удалить этот API в будущих выпусках.
</blockquote>
<br/> Извлекает сведения о содержимом большого двоичного объекта или файла.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignandencodecertificate"><strong>CryptSignAndEncodeCertificate</strong></a></td>
<td>Кодирует данные в &quot; со знаком &quot; , подписывает эти закодированные сведения и кодирует полученные зашифрованные сведения.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsigncertificate"><strong>криптсигнцертификате</strong></a></td>
<td>Подписывает в &quot; &quot; зашифрованное содержимое со знаком.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipaddprovider"><strong>криптсипаддпровидер</strong></a></td>
<td>Добавляет пакет интерфейса субъекта (SIP).</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipcreateindirectdata"><strong>криптсипкреатеиндиректдата</strong></a></td>
<td>Возвращает структуру <a href="/windows/win32/api/mssip/ns-mssip-sip_indirect_data"><strong>SIP_INDIRECT_DATA</strong></a> , содержащую <a href="/windows/desktop/SecGloss/h-gly"><em>хэш-код</em></a> указанной структуры <a href="/windows/win32/api/mssip/ns-mssip-sip_subjectinfo"><strong>SIP_SUBJECTINFO</strong></a> , алгоритм дайджеста и атрибут Encoding. Хэш можно использовать как косвенную ссылку на данные.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipgetcaps"><strong>криптсипжеткапс</strong></a></td>
<td>Получает возможности модуля SIP.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipgetsigneddatamsg"><strong>криптсипжетсигнеддатамсг</strong></a></td>
<td>Извлекает подпись Authenticode из файла.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipload"><strong>криптсиплоад</strong></a></td>
<td>Загружает библиотеку динамической компоновки, которая реализует пакет интерфейса субъекта, и назначает соответствующие функции экспорта библиотеки структуре <a href="/windows/win32/api/mssip/ns-mssip-sip_dispatch_info"><strong>SIP_DISPATCH_INFO</strong></a> .</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipputsigneddatamsg"><strong>криптсиппутсигнеддатамсг</strong></a></td>
<td>Сохраняет подпись Authenticode в целевом файле.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipremoveprovider"><strong>криптсипремовепровидер</strong></a></td>
<td>Удаляет модуль SIP, добавленный предыдущим вызовом функции <a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipaddprovider"><strong>криптсипаддпровидер</strong></a> .</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipremovesigneddatamsg"><strong>криптсипремовесигнеддатамсг</strong></a></td>
<td>Удаляет указанную подпись Authenticode.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipretrievesubjectguid"><strong>криптсипретриевесубжектгуид</strong></a></td>
<td>Извлекает идентификатор GUID на основе сведений о заголовке в указанном файле.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipretrievesubjectguidforcatalogfile"><strong>криптсипретриевесубжектгуидфоркаталогфиле</strong></a></td>
<td>Извлекает идентификатор GUID темы, связанный с указанным файлом.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipverifyindirectdata"><strong>криптсипверифиндиректдата</strong></a></td>
<td>Проверяет непрямые хэшированные данные по указанной теме.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dpapi/nf-dpapi-cryptupdateprotectedstate"><strong>криптупдатепротектедстате</strong></a></td>
<td>Переносит главные ключи текущего пользователя после изменения <a href="/windows/desktop/SecGloss/s-gly"><em>идентификатора безопасности</em></a> (SID) пользователя.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifycertificatesignature"><strong>криптверифицертификатесигнатуре</strong></a></td>
<td>Проверяет подпись сертификата субъекта или <a href="/windows/desktop/SecGloss/c-gly"><em>списка отзыва</em></a> сертификатов с помощью сведений об открытом ключе.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifycertificatesignatureex"><strong>криптверифицертификатесигнатурикс</strong></a></td>
<td>Расширенная версия <a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifycertificatesignature"><strong>криптверифицертификатесигнатуре</strong></a>.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-getencschannel"><strong>жетенксчаннел</strong></a></td>
<td>Сохраняет зашифрованное содержимое DLL-библиотеки Schannel в памяти.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Mssip/nc-mssip-pcryptsipgetcaps"><strong>пкриптсипжеткапс</strong></a></td>
<td>Реализуется модулем SIP для передачи отчетов о возможностях.</td>
</tr>
</tbody>
</table>



 

### <a name="data-conversion-functions"></a>Функции преобразования данных

Следующие функции CryptoAPI преобразуют члены структуры сертификатов в разные формы.

| Функция                                           | Описание                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**церталгидтуид**](/windows/desktop/api/Wincrypt/nf-wincrypt-certalgidtooid)           | Преобразует идентификатор алгоритма CryptoAPI ( \_ ID) в [*абстрактную нотацию синтаксиса*](../secgloss/a-gly.md) (ASN. 1) строка [*идентификатора объекта*](../secgloss/o-gly.md) (OID). |
| [**цертжетнаместринг**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa)     | Получает имя субъекта или издателя из сертификата и преобразует его в строку символов, завершающуюся нулем.                                                                                                                                                                                                               |
| [**цертнаметостр**](/windows/desktop/api/Wincrypt/nf-wincrypt-certnametostra)             | Преобразует [*большой двоичный объект*](../secgloss/b-gly.md) с именем сертификата в строку, заканчивающуюся нулем.                                                                                                                                                                                                      |
| [**цертоидтоалгид**](/windows/desktop/api/Wincrypt/nf-wincrypt-certoidtoalgid)           | Преобразует строку идентификатора объекта ASN. 1 в идентификатор алгоритма CSP.                                                                                                                                                                                                                                                 |
| [**цертрднвалуетостр**](/windows/desktop/api/Wincrypt/nf-wincrypt-certrdnvaluetostra)     | Преобразует значение имени в строку, завершающуюся нулем.                                                                                                                                                                                                                                                                           |
| [**CertStrToName**](/windows/desktop/api/Wincrypt/nf-wincrypt-certstrtonamea)             | Преобразует строку [*X. 500*](../secgloss/x-gly.md) , заканчивающуюся нулем, в закодированное имя сертификата.                                                                                                                                                                                          |
| [**криптбинаритостринг**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptbinarytostringa) | Преобразует двоичную последовательность в отформатированную строку.                                                                                                                                                                                                                                                                          |
| [**криптформатобжект**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptformatobject)     | Форматирует закодированные данные и возвращает строку в Юникоде.                                                                                                                                                                                                                                                                          |
| [**криптстрингтобинари**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptstringtobinarya) | Преобразует отформатированную строку в двоичную последовательность.                                                                                                                                                                                                                                                                            |



 

### <a name="enhanced-key-usage-functions"></a>Функции расширенного использования ключа

Следующие функции имеют дело с расширением расширенного [*использования ключа*](../secgloss/e-gly.md) (EKU) и расширенным свойством EKU для сертификатов. Расширение EKU и расширенное свойство указывают и ограничивают допустимые варианты использования сертификата. Расширения являются частью самого сертификата. Они задаются издателем сертификата и доступны только для чтения. Расширенные свойства сертификата — это значения, связанные с сертификатом, который можно задать в приложении.

| Функция                                                                             | Описание                                                                    |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**цертадденханцедкэйусажеидентифиер**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddenhancedkeyusageidentifier)       | Добавляет идентификатор использования в свойство EKU сертификата.                       |
| [**цертжетенханцедкэйусаже**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetenhancedkeyusage)                           | Получает от сертификата сведения о расширении EKU или свойстве. |
| [**цертремовинханцедкэйусажеидентифиер**](/windows/desktop/api/Wincrypt/nf-wincrypt-certremoveenhancedkeyusageidentifier) | Удаляет идентификатор использования из расширенного свойства EKU сертификата.       |
| [**цертсетенханцедкэйусаже**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetenhancedkeyusage)                           | Задает свойство EKU для сертификата.                                       |



 

### <a name="key-identifier-functions"></a>Функции идентификатора ключа

Функции идентификатора ключа позволяют пользователю создавать, задавать, извлекать или искать идентификатор ключа или его свойства.

Идентификатор ключа — это уникальный идентификатор [*пары открытого и закрытого ключей*](../secgloss/p-gly.md). Это может быть любой уникальный идентификатор, но обычно это 20-байтовый хэш SHA1 структуры зашифрованного [**сертификата \_ с \_ открытым \_ ключом**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_public_key_info) . Идентификатор ключа можно получить с помощью \_ идентификатора свойства идентификатора ключа сертификата \_ \_ \_ . Идентификатор ключа позволяет использовать эту [*пару ключей*](../secgloss/k-gly.md) для шифрования и расшифровки сообщений без использования сертификата.

Идентификаторы ключей не связаны с списками [*отзыва сертификатов*](../secgloss/c-gly.md) или [*CTL*](../secgloss/c-gly.md).

Идентификатор ключа может иметь те же свойства, что и контекст сертификата. Дополнительные сведения см. в разделе [**церткреатеконтекст**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatecontext).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Функция</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatekeyidentifierfromcsp"><strong>крипткреатекэйидентифиерфромксп</strong></a></td>
<td><blockquote>
[!Important]<br />
Это нерекомендуемый API. Новое и существующее программное обеспечение должно начинаться с использования <a href="/windows/desktop/SecCNG/cng-portal">API-интерфейсов следующего поколения шифрования.</a> Корпорация Майкрософт может удалить этот API в будущих выпусках.
</blockquote>
<br/> Создает идентификатор ключа из <a href="/windows/desktop/SecGloss/p-gly"><em>BLOB-объекта открытого ключа</em></a>CSP.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptenumkeyidentifierproperties"><strong>криптенумкэйидентифиерпропертиес</strong></a></td>
<td>Перечисляет идентификаторы ключей и их свойства.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetkeyidentifierproperty"><strong>криптжеткэйидентифиерпроперти</strong></a></td>
<td><blockquote>
[!Important]<br />
Это нерекомендуемый API. Новое и существующее программное обеспечение должно начинаться с использования <a href="/windows/desktop/SecCNG/cng-portal">API-интерфейсов следующего поколения шифрования.</a> Корпорация Майкрософт может удалить этот API в будущих выпусках.
</blockquote>
<br/> Получает определенное свойство из указанного идентификатора ключа.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyidentifierproperty"><strong>криптсеткэйидентифиерпроперти</strong></a></td>
<td><blockquote>
[!Important]<br />
Это нерекомендуемый API. Новое и существующее программное обеспечение должно начинаться с использования <a href="/windows/desktop/SecCNG/cng-portal">API-интерфейсов следующего поколения шифрования.</a> Корпорация Майкрософт может удалить этот API в будущих выпусках.
</blockquote>
<br/> Задает свойство указанного идентификатора ключа.</td>
</tr>
</tbody>
</table>



 

### <a name="oid-support-functions"></a>Функции поддержки OID

Эти функции предоставляют поддержку [*идентификатора объекта*](../secgloss/o-gly.md) (OID). Эти функции устанавливают, регистрируют и отправляются в функции, зависящие от типа OID и кодирования.

Следующие функции CryptoAPI используют следующие функции поддержки OID:

-   [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject)
-   [**криптенкодеобжектекс**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobjectex)
-   [**криптдекодеобжект**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject)
-   [**криптдекодеобжектекс**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobjectex)
-   [**цертверифиревокатион**](/windows/desktop/api/Wincrypt/nf-wincrypt-certverifyrevocation)
-   [**цертопенсторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore)

Общие сведения об этом процессе см. в разделе [расширение функциональности CryptoAPI](extending-cryptoapi-functionality.md).

Следующие функции работают с OID.

| Функция                                                                       | Описание                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**криптенумоидфунктион**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptenumoidfunction)                           | Перечисляет зарегистрированные функции OID, идентифицируемые их типом кодирования, именем функции и OID.                                                                                                                 |
| [**криптенумоидинфо**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptenumoidinfo)                                   | Перечисляет зарегистрированные сведения о OID, определяемые их группой, и вызывает *пфненумоидинфо* для совпадений.                                                                                                       |
| [**криптфиндоидинфо**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfindoidinfo)                                   | Использует указанные ключ и группу для поиска сведений о OID.                                                                                                                                                          |
| [**криптфриоидфунктионаддресс**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfreeoidfunctionaddress)             | Освобождает число дескрипторов, которое было увеличено и возвращено [**криптжетоидфунктионаддресс**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetoidfunctionaddress) или [**криптжетдефаултоидфунктионаддресс**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetdefaultoidfunctionaddress). |
| [**криптжетдефаултоиддлллист**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetdefaultoiddlllist)                 | Получает список зарегистрированных записей DLL по умолчанию для указанного набора функций и типа кодировки.                                                                                                              |
| [**криптжетдефаултоидфунктионаддресс**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetdefaultoidfunctionaddress) | Либо получает первую или следующую установленную функцию по умолчанию, либо загружает библиотеку DLL, содержащую функцию по умолчанию.                                                                                                 |
| [**криптжетоидфунктионаддресс**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetoidfunctionaddress)               | Выполняет поиск в списке установленных функций для типа кодирования и сопоставления OID. Если совпадение не найдено, реестр ищет совпадение.                                                                  |
| [**криптжетоидфунктионвалуе**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetoidfunctionvalue)                   | Получает значение для указанного типа кодировки, имени функции, OID и имени значения.                                                                                                                            |
| [**криптинитоидфунктионсет**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinitoidfunctionset)                     | Инициализирует и возвращает маркер набора функций OID, идентифицируемого указанным именем функции.                                                                                                                 |
| [**криптинсталлоидфунктионаддресс**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinstalloidfunctionaddress)       | Устанавливает набор вызываемых адресов функций OID.                                                                                                                                                                 |
| [**криптрегистердефаултоидфунктион**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptregisterdefaultoidfunction)     | Регистрирует библиотеку DLL, содержащую функцию по умолчанию, которая будет вызываться для указанного типа кодировки и имени функции.                                                                                               |
| [**криптрегистероидфунктион**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptregisteroidfunction)                   | Регистрирует библиотеку DLL, содержащую функцию, вызываемую для указанного типа кодировки, имени функции и OID.                                                                                                 |
| [**криптрегистероидинфо**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptregisteroidinfo)                           | Регистрирует сведения OID, указанные в структуре [**" \_ \_ сведения о шифровании OID**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_oid_info) ", сохраняющую их в реестре.                                                                                |
| [**криптсетоидфунктионвалуе**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetoidfunctionvalue)                   | Задает значение для указанного типа кодировки, имени функции, OID и имени значения.                                                                                                                                |
| [**криптунрегистердефаултоидфунктион**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptunregisterdefaultoidfunction) | Удаляет регистрацию библиотеки DLL, содержащей функцию по умолчанию, вызываемую для указанного типа кодировки и имени функции.                                                                            |
| [**криптунрегистероидфунктион**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptunregisteroidfunction)               | Удаляет регистрацию библиотеки DLL, содержащей функцию, вызываемую для указанного типа кодировки, имени функции и OID.                                                                              |
| [**криптунрегистероидинфо**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptunregisteroidinfo)                       | Удаляет регистрацию для указанных сведений о OID.                                                                                                                                                        |



 

### <a name="remote-object-retrieval-functions"></a>Функции извлечения удаленных объектов

Следующие функции позволяют пользователю получить объект инфраструктуры открытых ключей (PKI), получить URL-адрес сертификата, CTL или списка отзыва сертификатов или извлечь URL-адрес из объекта.

| Функция                                                     | Описание                                                            |
|--------------------------------------------------------------|------------------------------------------------------------------------|
| [**криптжетобжектурл**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetobjecturl)               | Получает URL-адрес удаленного объекта из сертификата, CTL или списка отзыва сертификатов. |
| [**криптретриевеобжектбюрл**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptretrieveobjectbyurla) | Извлекает объект PKI из расположения, указанного URL-адресом.           |



 

### <a name="pfx-functions"></a>Функции PFX

следующие функции поддерживают личную информацию Exchange (PFX) в формате [*blob-объектов*](../secgloss/b-gly.md).

| Функция                                             | Описание                                                                                                                                                                                                                                                                  |
|------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**пфксекспортцертсторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-pfxexportcertstore)     | Экспорты из упоминаемого [*сертификата хранят*](../secgloss/c-gly.md) сертификаты и, если они доступны, связанные с ними [*закрытые ключи*](../secgloss/p-gly.md). |
| [**пфксекспортцертсторикс**](/windows/desktop/api/Wincrypt/nf-wincrypt-pfxexportcertstoreex) | Экспорты из упоминаемого сертификата хранят сертификаты и, если они доступны, связанные с ними закрытые ключи.                                                                                                                                                             |
| [**пфксимпортцертсторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-pfximportcertstore)     | Импортирует большой двоичный объект PFX и возвращает маркер хранилища, который содержит сертификаты и все связанные закрытые ключи.                                                                                                                                                            |
| [**пфксиспфксблоб**](/windows/desktop/api/Wincrypt/nf-wincrypt-pfxispfxblob)                 | Пытается декодировать внешний слой большого двоичного объекта как PFX-пакет.                                                                                                                                                                                                                |
| [**пфксверифипассворд**](/windows/desktop/api/Wincrypt/nf-wincrypt-pfxverifypassword)       | Пытается декодировать внешний слой большого двоичного объекта как PFX-пакет и расшифровать его с заданным паролем.                                                                                                                                                                      |



 

## <a name="certificate-services-backup-and-restore-functions"></a>Функции резервного копирования и восстановления служб сертификатов

Службы сертификатов включают функции резервного копирования и восстановления базы данных служб сертификатов. Эти функции резервного копирования и восстановления служб сертификации содержатся в Certadm.dll. В отличие от других элементов API, связанных со службами сертификации, эти функции не инкапсулированы в объект, который можно использовать для вызова методов класса. Вместо этого API-интерфейсы резервного копирования и восстановления вызываются путем первой загрузки библиотеки Certadm.dll в память путем вызова [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и последующего определения адреса функций путем вызова [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress). После завершения вызова функций резервного копирования и восстановления служб сертификации вызовите [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) для освобождения ресурсов Certadm.dll из памяти.

> [!Note]
> Функции резервного копирования и восстановления, предоставляемые Certadm.dll, не выполняют резервное копирование и восстановление [*закрытых ключей*](../secgloss/p-gly.md)службы сертификатов. Сведения о резервном копировании закрытых ключей служб сертификатов см. [в разделе Резервное копирование и восстановление закрытого ключа служб сертификатов](backing-up-and-restoring-the-certificate-services-private-key.md).
> 
> Для вызова функций резервного копирования и восстановления необходимы [*права*](../secgloss/p-gly.md)на резервное копирование и восстановление. Дополнительные сведения см. [в разделе Настройка привилегий резервного копирования и восстановления](setting-the-backup-and-restore-privileges.md).

 

> [!Note]  
> Если метод **CoInitializeEx** был ранее вызван в том же потоке, который использовался для вызова API-интерфейсов резервного копирования и восстановления служб сертификатов, то \_ флаг апартментсреадед должен быть передан в **CoInitializeEx**. То есть при использовании того же потока нельзя вызвать API резервного копирования и восстановления служб сертификатов, если поток ранее был передан в \_ МНОГОпотоковый флаг при вызове **CoInitializeEx**.

 

API-интерфейсы резервного копирования служб сертификатов определены в Цертбкли. h. Однако при создании программы используйте файл certsrv. h в качестве включаемого файла.

Следующие API экспортируются с помощью Certadm.dll.

| Функция                                                                         | Описание                                                                                                           |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [**цертсрвбаккупклосе**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupclose)                                 | Закрывает открытый файл.                                                                                                |
| [**цертсрвбаккупенд**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupend)                                     | Завершает сеанс резервного копирования.                                                                                                |
| [**цертсрвбаккупфри**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupfree)                                   | Освобождает буфер, выделенный API-интерфейсам резервного копирования и восстановления.                                                              |
| [**цертсрвбаккупжетбаккуплогс**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetbackuplogsw)                 | Возвращает список файлов журнала, для которых необходимо создать резервную копию.                                                                |
| [**цертсрвбаккупжетдатабасенамес**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetdatabasenamesw)           | Возвращает список файлов базы данных, для которых необходимо создать резервную копию.                                                           |
| [**цертсрвбаккупжетдинамикфилелист**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetdynamicfilelistw)       | Возвращает список динамических имен файлов служб сертификации, для которых необходимо создать резервную копию для данного контекста резервного копирования. |
| [**цертсрвбаккупопенфиле**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupopenfilew)                           | Открывает файл в процессе подготовки к его резервному копированию.                                                                        |
| [**цертсрвбаккуппрепаре**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackuppreparew)                             | Подготавливает базу данных к оперативному резервному копированию.                                                                          |
| [**цертсрвбаккупреад**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupread)                                   | Считывает содержимое открытого файла.                                                                                 |
| [**цертсрвбаккуптрункателогс**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackuptruncatelogs)                   | Усекает файлы журнала.                                                                                              |
| [**цертсрвиссерверонлине**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvisserveronlinew)                           | Определяет, работает ли сервер служб сертификации в сети (активно).                                        |
| [**цертсрвресторинд**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoreend)                                   | Завершает сеанс восстановления.                                                                                               |
| [**цертсрвресторежетдатабаселокатионс**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoregetdatabaselocationsw) | Извлекает расположения базы данных (используется как для сценариев резервного копирования, так и для восстановления).                                            |
| [**цертсрвресторепрепаре**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestorepreparew)                           | Начинает сеанс восстановления.                                                                                             |
| [**цертсрвресторерегистер**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoreregisterw)                         | Регистрирует операцию восстановления.                                                                                        |
| [**цертсрвресторерегистеркомплете**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoreregistercomplete)         | Завершает ранее зарегистрированную операцию восстановления.                                                                  |
| [**цертсрвресторерегистерсраугхфиле**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoreregisterthroughfile)   | Регистрирует операцию восстановления.                                                                                        |
| [**цертсрвсерверконтрол**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvservercontrolw)                             | Отправляет команду управления в экземпляр служб сертификатов.                                                         |



 

## <a name="callback-functions"></a>Функции обратного вызова

Функции обратного вызова в этом разделе используются для регистрации или установки определенных приложением поставщиков [*хранилища сертификатов*](../secgloss/c-gly.md) и для предоставления связанных функций посредством функций обратного вызова. Функции обратного вызова реализуются приложением и вызываются функциями [*CryptoAPI*](../secgloss/c-gly.md) . Функции обратного вызова позволяют приложению управлять, частично, таким образом, чтобы функции CryptoAPI работали с данными.

| Функция обратного вызова                                                                                                        | Использовать                                                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**цертчаинфиндбиссуеркаллбакк**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_chain_find_by_issuer_callback)                                                   | Определяемая приложением функция обратного вызова, позволяющая приложению фильтровать сертификаты, которые могут быть добавлены в цепочку сертификатов.                                                                                                                                                                                                     |
| [**цертдллопенсторепров**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_dll_open_store_prov_func)                                                                     | Определяет функцию Open поставщика хранилища.                                                                                                                                                                                                                                                                                                     |
| [**цертенумфисикалсторекаллбакк**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_enum_physical_store)                                                   | Функция обратного вызова, используемая функцией [**цертенумфисикалсторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumphysicalstore) для форматирования и представления сведений о каждом обнаруженном физическом хранилище.                                                                                                                                                                                 |
| [**цертенумсистемсторекаллбакк**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_enum_system_store)                                                       | Функция обратного вызова, используемая функцией [**цертенумсистемсторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumsystemstore) для форматирования и представления сведений о каждом обнаруженном физическом хранилище.                                                                                                                                                                                     |
| [**цертенумсистемсторелокатионкаллбакк**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_enum_system_store_location)                                       | Функция обратного вызова, используемая функцией [**цертенумсистемсторелокатион**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumsystemstorelocation) для форматирования и представления сведений о каждом обнаруженном физическом хранилище.                                                                                                                                                                     |
| [**цертсторепровклосекаллбакк**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_store_prov_close)                                                         | Определяет, что происходит, когда [*счетчик ссылок*](../secgloss/r-gly.md) открытого хранилища станет нулевым.                                                                                                                                                                                    |
| [**цертсторепровконтрол**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cert_store_prov_control)                                                                     | Позволяет приложению получать уведомления при наличии различий между содержимым кэшированного хранилища и содержимым хранилища в том виде, в котором оно сохраняется в хранилище.                                                                                                                                                                   |
| [**цертсторепровделетецерткаллбакк**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_store_prov_delete_cert)                                               | Определяет действия, выполняемые перед удалением сертификата из хранилища сертификатов.                                                                                                                                                                                                                                                      |
| [**цертсторепровделетекрлкаллбакк**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_store_prov_delete_crl)                                                 | Определяет действия, выполняемые перед удалением [*списка отзыва сертификатов*](../secgloss/c-gly.md) (CRL) из хранилища сертификатов.                                                                                                                        |
| [**цертсторепровделетектл**](certstoreprovdeletectl.md)                                                                 | Определяет, можно ли удалить список доверия сертификатов.                                                                                                                                                                                                                                                                                                      |
| [**цертсторепровфиндцерт**](certstoreprovfindcert.md)                                                                   | Находит первый (или следующий) сертификат в хранилище, соответствующий указанным критериям.                                                                                                                                                                                                                                                             |
| [**цертсторепровфиндкрл**](certstoreprovfindcrl.md)                                                                     | Находит первый (или следующий) список отзыва сертификатов в магазине, соответствующий указанным критериям.                                                                                                                                                                                                                                                                     |
| [**цертсторепровфиндктл**](certstoreprovfindctl.md)                                                                     | Находит первый (или следующий) список доверия сертификатов в магазине, соответствующий указанным критериям.                                                                                                                                                                                                                                                                     |
| [**цертсторепровфрифиндцерт**](certstoreprovfreefindcert.md)                                                           | Освобождает ранее найденный контекст сертификата.                                                                                                                                                                                                                                                                                                 |
| [**цертсторепровфрифиндкрл**](certstoreprovfreefindcrl.md)                                                             | Освобождает ранее найденный контекст списка отзыва сертификатов.                                                                                                                                                                                                                                                                                                         |
| [**цертсторепровфрифиндктл**](certstoreprovfreefindctl.md)                                                             | Освобождает ранее найденный контекст CTL.                                                                                                                                                                                                                                                                                                         |
| [**цертсторепровжетцертпроперти**](certstoreprovgetcertproperty.md)                                                     | Извлекает указанное свойство сертификата.                                                                                                                                                                                                                                                                                              |
| [**цертсторепровжеткрлпроперти**](certstoreprovgetcrlproperty.md)                                                       | Извлекает указанное свойство списка отзыва сертификатов.                                                                                                                                                                                                                                                                                                      |
| [**цертсторепровжетктлпроперти**](certstoreprovgetctlproperty.md)                                                       | Извлекает указанное свойство списка доверия сертификатов.                                                                                                                                                                                                                                                                                                      |
| [**цертсторепровреадцерткаллбакк**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_store_prov_read_cert)                                                   | Сейчас не используется, но может быть экспортировано в будущие CSP.                                                                                                                                                                                                                                                                                      |
| [**цертсторепровреадкрлкаллбакк**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_store_prov_read_crl)                                                     | Сейчас не используется, но может быть экспортировано в будущие CSP.                                                                                                                                                                                                                                                                                      |
| [**цертсторепровреадктл**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cert_store_prov_read_ctl)                                                                     | Прочитайте копию поставщика контекста CTL и, если он существует, создайте новый контекст списка доверия сертификатов.                                                                                                                                                                                                                                                     |
| [**цертсторепровсетцертпропертикаллбакк**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_store_prov_set_cert_property)                                     | Определяет действия, выполняемые перед вызовом [**цертсетцертификатеконтекстпроперти**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetcertificatecontextproperty) или [**цертжетцертификатеконтекстпроперти**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty).                                                                                                                             |
| [**цертсторепровсеткрлпропертикаллбакк**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_store_prov_set_crl_property)                                       | Определяет действия, выполняемые перед вызовом [**цертсеткрлконтекстпроперти**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetcrlcontextproperty) или [**цертжеткрлконтекстпроперти**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcrlcontextproperty).                                                                                                                                                             |
| [**цертсторепровсетктлпроперти**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_store_prov_set_ctl_property)                                                       | Определяет, можно ли задать свойство для списка доверия сертификатов.                                                                                                                                                                                                                                                                                            |
| [**цертсторепроввритецерткаллбакк**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_store_prov_write_cert)                                                 | Определяет действия, выполняемые перед добавлением сертификата в хранилище.                                                                                                                                                                                                                                                                        |
| [**цертсторепроввритекрлкаллбакк**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_store_prov_write_crl)                                                   | Определяет действия, выполняемые перед добавлением списка отзыва сертификатов в магазин.                                                                                                                                                                                                                                                                                |
| [**цертсторепроввритектл**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_store_prov_write_ctl)                                                                   | Определяет, можно ли добавить список доверия сертификатов в хранилище.                                                                                                                                                                                                                                                                                           |
| [**Понятное \_ Перечисление \_ KEYID \_ prop**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_crypt_enum_keyid_prop)                                                                | Функция обратного вызова, используемая функцией [**криптенумкэйидентифиерпропертиес**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptenumkeyidentifierproperties) .                                                                                                                                                                                                                          |
| [**сошифрованное \_ Перечисление \_ \_ функции OID**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_crypt_enum_oid_func)                                                            | Функция обратного вызова, используемая функцией [**криптенумоидфунктион**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptenumoidfunction) .                                                                                                                                                                                                                                                  |
| [**\_ \_ сведения о шифровании объекта Enum \_**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_crypt_enum_oid_info)                                                                    | Функция обратного вызова, используемая функцией [**криптенумоидинфо**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptenumoidinfo) .                                                                                                                                                                                                                                                          |
| [**криптжетсигнерцертификатекаллбакк**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_crypt_get_signer_certificate)                                           | Функция обратного вызова, используемая со структурой [**шифрования \_ \_ сообщения Verify \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_verify_message_para) , для получения и проверки сертификата подписи сообщения.                                                                                                                                                                                 |
| [**ПКРИПТ \_ расшифровать \_ закрытый \_ ключ \_ Func**](/windows/win32/api/wincrypt/nc-wincrypt-pcrypt_decrypt_private_key_func)                                           | Функция обратного вызова, используемая функцией [**CryptImportPKCS8**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportpkcs8) .                                                                                                                                                                                                                                                          |
| [**ПКРИПТ \_ Шифрование \_ закрытого \_ ключа \_ Func**](/windows/win32/api/wincrypt/nc-wincrypt-pcrypt_encrypt_private_key_func)                                           | Функция обратного вызова, используемая при создании структуры [**\_ шифрования \_ \_ \_ сведений о зашифрованном закрытом ключе**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_encrypted_private_key_info) .                                                                                                                                                                                                          |
| [**ПКРИПТ \_ Разрешить \_ хкриптпров \_ Func**](/windows/win32/api/wincrypt/nc-wincrypt-pcrypt_resolve_hcryptprov_func)                                              | Функция обратного вызова, используемая функцией [**CryptImportPKCS8**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportpkcs8) .                                                                                                                                                                                                                                                          |
| [**\_ \_ \_ обратный вызов ошибки синтаксического анализа PFN CDF \_**](/windows/win32/api/mscat/nc-mscat-pfn_cdf_parse_error_callback)                                                 | Определяемая пользователем функция, вызываемая для ошибок функции определения каталога при анализе файла определения каталога (CDF).                                                                                                                                                                                                                          |
| [**\_ \_ Создание контекста сортировки для PFN CERT \_ \_ \_ Func**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cert_create_context_sort_func)                                      | Вызывается для каждой записи отсортированного контекста при создании контекста.                                                                                                                                                                                                                                                                               |
| [**\_ \_ \_ ключ шифрования для импорта \_ содержимого \_ PFN КМСГ CNG \_**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cmsg_cng_import_content_encrypt_key)                         | Устанавливаемая функция [*идентификатора объекта*](../secgloss/o-gly.md) (OID) CNG для импорта уже расшифрованного ключа шифрования содержимого (CEK).                                                                                                                                       |
| [**\_согласие на \_ \_ Импорт \_ ключа импорта \_ CNG PFN КМСГ**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cmsg_cng_import_key_agree)                                              | Импортирует ключ шифрования содержимого для получателя транспортного сообщения.                                                                                                                                                                                                                                                       |
| [**PFN \_ КМСГ \_ \_ ключ импорта \_ CNG \_**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cmsg_cng_import_key_trans)                                              | Функция, устанавливаемая с помощью CNG OID, для импорта и [*расшифровки*](../secgloss/d-gly.md) ключа-Transport-получател, зашифрованного ключа [*шифрования*](../secgloss/e-gly.md) содержимого (CEK).                                                                   |
| [**\_согласие на \_ Экспорт \_ ключа PFN КМСГ \_**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cmsg_export_key_agree)                                                       | Шифрует и экспортирует ключ шифрования содержимого для получателя соглашения о запечатанном сообщении.                                                                                                                                                                                                                                        |
| [**PFN \_ КМСГ \_ Экспорт \_ ключа \_ транзакции**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cmsg_export_key_trans)                                                       | Шифрует и экспортирует ключ шифрования содержимого для получателя транспортного сообщения.                                                                                                                                                                                                                                        |
| [**\_список PFN КМСГ \_ экспорта \_ почты \_**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cmsg_export_mail_list)                                                       | Шифрует и экспортирует ключ шифрования содержимого для получателя списка рассылки сообщения с оболочкой.                                                                                                                                                                                                                                         |
| [**\_ключ шифрования PFN КМСГ \_ Gen \_ Content \_ \_**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cmsg_gen_content_encrypt_key)                                        | Создает [*симметричный ключ*](../secgloss/s-gly.md) , используемый для шифрования содержимого запечатанного сообщения.                                                                                                                                                                                     |
| [**\_согласие на \_ Импорт \_ ключа \_ импорта PFN КМСГ**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cmsg_import_key_agree)                                                       | Импортирует ключ шифрования содержимого для получателя транспортного сообщения.                                                                                                                                                                                                                                                       |
| [**PFN \_ КМСГ \_ Импорт \_ ключа \_**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cmsg_import_key_trans)                                                       | Импортирует ключ шифрования содержимого для получателя транспортного сообщения.                                                                                                                                                                                                                                                       |
| [**\_ \_ \_ список импорта почты \_ PFN КМСГ**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cmsg_import_mail_list)                                                       | Импортирует ключ шифрования содержимого для получателя транспортного сообщения.                                                                                                                                                                                                                                                       |
| [**PFN \_ шифрования \_ , \_ сведения об экспорте открытого \_ ключа \_ \_ EX2 \_ Func**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_crypt_export_public_key_info_ex2_func)                    | Вызывается [**криптекспортпубликкэйинфоекс**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportpublickeyinfoex) для экспорта большого двоичного объекта открытого ключа и его кодирования.                                                                                                                                                                                                                         |
| [**PFN \_ \_ шифрует извлечение \_ параметров закодированной \_ сигнатуры \_ \_ Func**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_crypt_extract_encoded_signature_parameters_func) | Вызывается для декодирования и возврата идентификатора хэш-алгоритма и, при необходимости, параметров сигнатуры.                                                                                                                                                                                                                                            |
| [**PFN \_ шифрования \_ \_ -знак \_ \_ Func и \_ кодирование**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_crypt_sign_and_encode_hash_func)                                 | Вызывается для подписывания и кодирования вычисленного хэша.                                                                                                                                                                                                                                                                                                    |
| [**PFNие \_ шифрования \_ Проверка \_ кодированной \_ подписи \_ Func**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_crypt_verify_encoded_signature_func)                          | Вызывается для расшифровки кодированной подписи и ее сравнения с вычисленным хэшем.                                                                                                                                                                                                                                                                     |
| [**PFN \_ Импорт \_ \_ сведений об открытом ключе \_ \_ EX2 \_ Func**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_import_public_key_info_ex2_func)                                 | Вызывается методом [**CryptImportPublicKeyInfoEx2**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportpublickeyinfoex2) для декодирования идентификатора [*алгоритма открытого ключа*](../secgloss/p-gly.md) , загрузки поставщика алгоритма и импорта [*пары ключей*](../secgloss/k-gly.md). |
| [**пфнкцертдисплайпрок**](pfnccertdisplayproc.md)                                                                       | Определяемая пользователем функция обратного вызова, позволяющая вызывающему объекту функции [**криптуидлгселектцертификате**](cryptuidlgselectcertificate.md) управлять отображением сертификатов, которые пользователь выбирает для просмотра.                                                                                                                               |
| [**пфнкмфилтерпрок**](/windows/desktop/api/CryptDlg/nc-cryptdlg-pfncmfilterproc)                                                                               | Фильтрует каждый сертификат, чтобы решить, будет ли он отображаться в диалоговом окне "Выбор сертификата", отображаемом функцией [**цертселектцертификате**](/windows/win32/api/cryptdlg/nf-cryptdlg-certselectcertificatea) .                                                                                                                                                                |
| [**пфнкмхукпрок**](/windows/desktop/api/CryptDlg/nc-cryptdlg-pfncmhookproc)                                                                                   | Вызывается до обработки сообщений диалоговым окном выбора сертификата, созданным функцией [**цертселектцертификате**](/windows/win32/api/cryptdlg/nf-cryptdlg-certselectcertificatea) .                                                                                                                                                                                 |



 

## <a name="catalog-definition-functions"></a>Функции определения каталога

Эти функции используются для создания каталога. Все эти функции вызываются методом [макекат](makecat.md).

| Функция                                                                           | Описание                                                                                                               |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**крипткаткдфклосе**](/windows/desktop/api/Mscat/nf-mscat-cryptcatcdfclose)                                       | Закрывает файл определения каталога и освобождает память для соответствующей структуры [**крипткаткдф**](/windows/win32/api/mscat/ns-mscat-cryptcatcdf) . |
| [**крипткаткдфенуматтрибутесвискдфтаг**](cryptcatcdfenumattributeswithcdftag.md) | Перечисляет атрибуты файлов элементов в разделе **КАТАЛОГФИЛЕС** CDF.                                       |
| [**крипткаткдфенумкататтрибутес**](/windows/desktop/api/Mscat/nf-mscat-cryptcatcdfenumcatattributes)               | Перечисляет атрибуты уровня каталога в разделе **КАТАЛОГХЕАДЕР** CDF.                                        |
| [**крипткаткдфенуммемберсбикдфтажекс**](cryptcatcdfenummembersbycdftagex.md)       | Перечисляет отдельные элементы файла в разделе **КАТАЛОГФИЛЕС** CDF.                                          |
| [**крипткаткдфопен**](/windows/desktop/api/Mscat/nf-mscat-cryptcatcdfopen)                                         | Открывает существующий CDF для чтения и инициализации структуры [**крипткаткдф**](/windows/win32/api/mscat/ns-mscat-cryptcatcdf) .                         |



 

## <a name="catalog-functions"></a>Функции работы с каталогами

Эти функции используются для управления каталогом.

| Функция                                                                             | Описание                                                                                                                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**крипткатадминаккуиреконтекст**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminacquirecontext)                   | Получает маркер контекста администратора каталога. Этот маркер может использоваться при последующих вызовах функций [**крипткатадминаддкаталог**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminaddcatalog), [**крипткатадминенумкаталогфромхаш**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminenumcatalogfromhash)и [**крипткатадминремовекаталог**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminremovecatalog) . |
| [**CryptCATAdminAcquireContext2**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminacquirecontext2)                 | Получает маркер контекста администратора каталога для заданного хэш-алгоритма и политики хеширования.                                                                                                                                                                                                                                   |
| [**крипткатадминаддкаталог**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminaddcatalog)                           | Добавляет каталог в базу данных каталога.                                                                                                                                                                                                                                                                                            |
| [**крипткатадминкалчашфромфилехандле**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadmincalchashfromfilehandle)   | Вычисляет хэш для файла.                                                                                                                                                                                                                                                                                                    |
| [**CryptCATAdminCalcHashFromFileHandle2**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadmincalchashfromfilehandle2) | Вычисляет хэш для файла с помощью указанного алгоритма.                                                                                                                                                                                                                                                                   |
| [**крипткатадминенумкаталогфромхаш**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminenumcatalogfromhash)         | Перечисляет каталоги, содержащие указанный хэш.                                                                                                                                                                                                                                                                             |
| [**крипткатадминрелеасекаталогконтекст**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminreleasecatalogcontext)     | Освобождает дескриптор контекста каталога, который ранее был возвращен функцией [**крипткатадминаддкаталог**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminaddcatalog) .                                                                                                                                                                                             |
| [**крипткатадминрелеасеконтекст**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminreleasecontext)                   | Освобождает дескриптор, ранее назначенный функцией [**крипткатадминаккуиреконтекст**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminacquirecontext) .                                                                                                                                                                                                        |
| [**крипткатадминремовекаталог**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminremovecatalog)                     | удаляет файл каталога и удаляет запись этого каталога из базы данных Windows каталога.                                                                                                                                                                                                                                         |
| [**крипткатадминресолвекаталогпас**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminresolvecatalogpath)           | Возвращает полный путь к указанному каталогу.                                                                                                                                                                                                                                                                       |
| [**крипткаткаталогинфофромконтекст**](/windows/desktop/api/Mscat/nf-mscat-cryptcatcataloginfofromcontext)             | Извлекает сведения о каталоге из указанного контекста каталога.                                                                                                                                                                                                                                                                    |
| [**крипткатклосе**](/windows/desktop/api/Mscat/nf-mscat-cryptcatclose)                                               | Закрывает открытый ранее обработчик каталога, который был открыт функцией [**крипткатопен**](/windows/desktop/api/Mscat/nf-mscat-cryptcatopen) .                                                                                                                                                                                                                                    |
| [**крипткатенумератеаттр**](/windows/desktop/api/Mscat/nf-mscat-cryptcatenumerateattr)                               | Перечисляет атрибуты, связанные с элементом каталога.                                                                                                                                                                                                                                                                   |
| [**крипткатенумератекататтр**](/windows/desktop/api/Mscat/nf-mscat-cryptcatenumeratecatattr)                         | Перечисляет атрибуты, связанные с каталогом.                                                                                                                                                                                                                                                                               |
| [**крипткатенумератемембер**](/windows/desktop/api/Mscat/nf-mscat-cryptcatenumeratemember)                           | Перечисляет элементы каталога.                                                                                                                                                                                                                                                                                               |
| [**крипткатжетаттринфо**](/windows/desktop/api/Mscat/nf-mscat-cryptcatgetattrinfo)                                   | Извлекает сведения об атрибуте элемента каталога.                                                                                                                                                                                                                                                                 |
| [**крипткатжетмемберинфо**](/windows/desktop/api/Mscat/nf-mscat-cryptcatgetmemberinfo)                               | Получает сведения о членах из каталога PKCS \# 7 в каталоге. Кроме получения сведений об элементе для указанного тега ссылки, эта функция открывает контекст элемента.                                                                                                                                                    |
| [**крипткатопен**](/windows/desktop/api/Mscat/nf-mscat-cryptcatopen)                                                 | Открывает каталог и возвращает маркер контекста в открытый каталог.                                                                                                                                                                                                                                                                 |
| [**искаталогфиле**](/windows/desktop/api/Mscat/nf-mscat-iscatalogfile)                                               | Получает логическое значение, указывающее, является ли указанный файл файлом каталога.                                                                                                                                                                                                                                             |



 

## <a name="wintrust-functions"></a>Функции Винтруст

Следующие функции используются для выполнения различных операций доверия.

| Функция                                                                               | Описание                                                                                                                                                          |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**винтрустаддактионид**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustaddactionid)                                     | Добавляет действие поставщика доверия в систему пользователя.                                                                                                                   |
| [**винтрустжетрегполицифлагс**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustgetregpolicyflags)                         | Возвращает флаги политики для поставщика политики.                                                                                                                        |
| [**винтрустадддефаултфорусаже**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustadddefaultforusage)                       | Указывает идентификатор использования по умолчанию и сведения о обратном вызове для поставщика                                                                                       |
| [**винтрустжетдефаултфорусаже**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustgetdefaultforusage)                       | Извлекает идентификатор использования по умолчанию и сведения о обратном вызове.                                                                                                     |
| [**винтрустлоадфунктионпоинтерс**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustloadfunctionpointers)                   | Загружает точки входа функции для указанного GUID действия.                                                                                                             |
| [**винтрустремовеактионид**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustremoveactionid)                               | Удаляет действие, добавленное функцией [**винтрустаддактионид**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustaddactionid) .                                                                          |
| [**винтрустсетдефаултинклудепепажехашес**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustsetdefaultincludepepagehashes) | Задает значение по умолчанию, определяющее, будут ли включены хэши страниц при создании косвенных данных пакета интерфейса субъекта (SIP) для переносимых исполняемых файлов. |
| [**винтрустсетрегполицифлагс**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustsetregpolicyflags)                         | Задает флаги политики для поставщика политики.                                                                                                                             |
| [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust)                                               | Выполняет действие проверки доверия для указанного объекта.                                                                                                          |
| [**винверифитрустекс**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrustex)                                           | Выполняет проверку доверия для указанного объекта и принимает указатель на \_ структуру данных винтруст.                                                        |
| [**вселперцертчекквалидсигнатуре**](/windows/desktop/api/Wintrust/nf-wintrust-wthelpercertcheckvalidsignature)             | Проверяет, является ли подпись допустимой.                                                                                                                                 |
| [**вселперцертфиндиссуерцертификате**](wthelpercertfindissuercertificate.md)         | Находит сертификат издателя из указанных хранилищ сертификатов, который соответствует указанному сертификату субъекта.                                                    |
| [**вселперцертисселфсигнед**](/windows/desktop/api/Wintrust/nf-wintrust-wthelpercertisselfsigned)                           | Проверяет, является ли сертификат самозаверяющим.                                                                                                                         |
| [**вселпержетфилехаш**](wthelpergetfilehash.md)                                     | Проверяет подпись подписанного файла и получает хэш-значение и идентификатор алгоритма для файла.                                                            |
| [**вселпержетпровцертфромчаин**](/windows/desktop/api/Wintrust/nf-wintrust-wthelpergetprovcertfromchain)                   | Извлекает сертификат поставщика доверия из цепочки сертификатов.                                                                                                   |
| [**вселпержетпровприватедатафромчаин**](/windows/desktop/api/Wintrust/nf-wintrust-wthelpergetprovprivatedatafromchain)     | Получает из цепочки структуру [**\_ \_ привдата поставщика шифрования**](/windows/desktop/api/Wintrust/ns-wintrust-crypt_provider_privdata) , используя идентификатор поставщика.                                           |
| [**вселпержетпровсигнерфромчаин**](/windows/desktop/api/Wintrust/nf-wintrust-wthelpergetprovsignerfromchain)               | Получает от цепочки подписывающий или каунтерсигнер по индексу.                                                                                                         |
| [**вселперпровдатафромстатедата**](/windows/desktop/api/Wintrust/nf-wintrust-wthelperprovdatafromstatedata)                 | Извлекает сведения о поставщике доверия из указанного маркера.                                                                                                        |



 

## <a name="object-locator-functions"></a>Функции локатора объектов

Следующие функции обратного вызова могут быть реализованы пользовательским поставщиком, который должен вызываться пакетом безопасности безопасного канала (Schannel) для получения сертификатов.



| Функция                                                                                                             | Описание                                             |
|----------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| [**\_ \_ \_ Очистка поставщика ЛОКАТОРа \_ объектов \_ PFN**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_flush)                      | Указывает, что объект изменился.                   |
| [**\_ \_ \_ \_ Получение поставщика указателя объекта \_ PFNного шифрования**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_get)                          | Извлекает объект.                                    |
| [**\_ \_ \_ Выпуск поставщика ЛОКАТОРа \_ объектов \_ PFN**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_release)                  | Освобождает поставщик.                                  |
| [**\_ \_ \_ \_ \_ бесплатный пароль поставщика локатора объекта \_ PFN**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_free_password)     | Освобождает пароль, используемый для шифрования массива байтов PFX. |
| [**\_ \_ \_ бесплатный поставщик ЛОКАТОРа \_ объектов \_ PFN**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_free)                        | Освобождает объект, возвращенный поставщиком.           |
| [**\_ \_ \_ \_ \_ бесплатный идентификатор поставщика локатора объектов \_ PFN**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_free_identifier) | Освобождает память для идентификатора объекта.               |
| [**\_ \_ \_ \_ Инициализация поставщика локатора \_ объектов PFN**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_initialize)            | Инициализирует этот поставщик.                               |



 

 

 
