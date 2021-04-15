---
description: Представляет один цифровой сертификат.
ms.assetid: da95312b-cc9f-44f0-9517-0b28c5fcfb61
title: Объект Certificate
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 1360b197f0d7f5e0579a5378a37047e6a117a9c9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688816"
---
# <a name="certificate-object"></a>Объект Certificate

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP. Вместо этого используйте [**класс X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

Объект **Certificate** представляет один [*цифровой сертификат*](../secgloss/d-gly.md).

Объект **сертификата** предоставляет следующие интерфейсы:

-   **Ицертификате** — представлено в CAPICOM 1,0.
-   **ICertificate2** — представлено в CAPICOM 2,0.

## <a name="when-to-use"></a>Назначение

Объект **Certificate** используется для выполнения следующих задач:

-   Загрузка данных сертификата, включая закрытый ключ, из файла.
-   Получение сведений из сертификата.
-   Возвращают базовые ограничения, EKU, расширенные свойства, расширения, использование ключей, Открытый ключ и объекты шаблонов, связанные с сертификатом.
-   Определите, является ли сертификат допустимым, и проверьте доступность доступа закрытого ключа субъекта сертификата.
-   Отображение сертификата.
-   Импортируйте и экспортируйте сертификат.
-   Сохраните сертификат в файл.
-   Получение или установка свойств, описывающих сертификат.

## <a name="members"></a>Элементы

Объект **сертификата** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Объект **сертификата** содержит следующие методы.



| Метод                                                       | Описание                                                                                                                                                                                                                                              |
|:-------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**басикконстраинтс**](certificate-basicconstraints.md)     | Возвращает объект [**басикконстраинтс**](basicconstraints.md) , представляющий расширение базовых ограничений сертификата.<br/> (Наследуется от **CertificateICertificate2ICertificate**)                                                   |
| [**Отображение**](certificate-display.md)                       | Отображает сертификат.<br/> (Наследуется от **CertificateICertificate2ICertificate**)                                                                                                                                                             |
| [**Экспорт**](certificate-export.md)                         | Копирует сертификат в зашифрованную строку. Закодированная строка может быть записана в файл или импортирована в новый объект **сертификата** .<br/> (Наследуется от **CertificateICertificate2ICertificate**)                                               |
| [**екстендедкэйусаже**](certificate-extendedkeyusage.md)     | Возвращает объект [**екстендедкэйусаже**](extendedkeyusage.md) , указывающий допустимое использование расширенного ключа сертификата.<br/> (Наследуется от **CertificateICertificate2ICertificate**)                                                       |
| [**ExtendedProperties**](certificate-extendedproperties.md) | Возвращает коллекцию расширенных свойств сертификата.<br/> (Наследуется от **CertificateICertificate2**)                                                                                                                             |
| [**Модули**](certificate-extensions.md)                 | Возвращает коллекцию расширений, связанных с сертификатом.<br/> (Наследуется от **CertificateICertificate2**)                                                                                                                         |
| [**GetInfo**](certificate-getinfo.md)                       | Извлекает сведения из сертификата.<br/> (Наследуется от **CertificateICertificate2ICertificate**)                                                                                                                                         |
| [**HasPrivateKey**](certificate-hasprivatekey.md)           | Определяет, связан ли сертификат с [*закрытым ключом*](../secgloss/p-gly.md) .<br/> (Наследуется от **CertificateICertificate2ICertificate**)                                    |
| [**Импорт**](certificate-import.md)                         | Импортирует ранее закодированный сертификат из строки в объект **сертификата** .<br/> (Наследуется от **CertificateICertificate2ICertificate**)                                                                                             |
| [**IsValid**](certificate-isvalid.md)                       | Создает цепочку проверки сертификатов для сертификата и возвращает объект [**цертификатестатус**](certificatestatus.md) , который содержит состояние действия сертификата.<br/> (Наследуется от **CertificateICertificate2ICertificate**) |
| [**кэйусаже**](certificate-keyusage.md)                     | Возвращает объект [**кэйусаже**](keyusage.md) , указывающий допустимое использование ключа сертификата.<br/> (Наследуется от **CertificateICertificate2ICertificate**)                                                                                |
| [**Загрузить**](certificate-load.md)                             | Импортирует сертификат из файла.<br/> (Наследуется от **CertificateICertificate2**)                                                                                                                                                              |
| [**PublicKey**](certificate-publickey.md)                   | Возвращает объект [**PublicKey**](publickey.md) .<br/> (Наследуется от **CertificateICertificate2**)                                                                                                                                                |
| [**Сохранить**](certificate-save.md)                             | Сохраняет сертификат в файл.<br/> (Наследуется от **CertificateICertificate2**)                                                                                                                                                                |
| [**Шаблон**](certificate-template.md)                     | Возвращает шаблон, связанный с сертификатом.<br/> (Наследуется от **CertificateICertificate2**)                                                                                                                                           |



 

### <a name="properties"></a>Свойства

Объект **сертификата** имеет следующие свойства.



| Свойство                                                      | Тип доступа           | Описание                                                                                                                                          |
|:--------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Архивная**](certificate-archived.md)<br/>           | Чтение/запись<br/> | Задает или получает логическое значение, указывающее, архивируется ли сертификат.<br/> (Наследуется от **CertificateICertificate2**)       |
| [**IssuerName**](certificate-issuername.md)<br/>       | Только для чтения<br/>  | Извлекает строку, содержащую имя издателя сертификата.<br/> (Наследуется от **CertificateICertificate2ICertificate**)            |
| [**PrivateKey**](certificate-privatekey.md)<br/>       | Чтение/запись<br/> | Задает или получает закрытый ключ, связанный с сертификатом.<br/> (Наследуется от **CertificateICertificate2**)                          |
| [**Номер**](certificate-serialnumber.md)<br/>   | Только для чтения<br/>  | Извлекает строку, содержащую серийный номер сертификата.<br/> (Наследуется от **CertificateICertificate2ICertificate**)                 |
| [**SubjectName**](certificate-subjectname.md)<br/>     | Только для чтения<br/>  | Извлекает строку, содержащую имя субъекта сертификата.<br/> (Наследуется от **CertificateICertificate2ICertificate**)           |
| [**Отпечаток**](certificate-thumbprint.md)<br/>       | Только для чтения<br/>  | Извлекает шестнадцатеричную строку, содержащую хэш SHA-1 сертификата.<br/> (Наследуется от **CertificateICertificate2ICertificate**) |
| [**валидфромдате**](certificate-validfromdate.md)<br/> | Только для чтения<br/>  | Возвращает начальную дату срока действия сертификата.<br/> (Наследуется от **CertificateICertificate2ICertificate**)               |
| [**валидтодате**](certificate-validtodate.md)<br/>     | Только для чтения<br/>  | Возвращает дату окончания срока действия сертификата.<br/> (Наследуется от **CertificateICertificate2ICertificate**)                  |
| [**Версия**](certificate-version.md)<br/>             | Только для чтения<br/>  | Возвращает номер версии сертификата.<br/> (Наследуется от **CertificateICertificate2ICertificate**)                                |



 

## <a name="remarks"></a>Комментарии

Объект **сертификата** может быть создан и защищен для создания скриптов. ProgID для объекта **сертификата** — CAPICOM. Certificate. 2.

**CAPICOM 1. *x*:** ProgID для объекта **сертификата** — CAPICOM. Certificate. 1 ".

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------------|----------------------------------------------------------------------------------------|
| Окончание поддержки клиента<br/> | Windows Vista<br/>                                                               |
| Поддержка конца сервера<br/> | Windows Server 2008<br/>                                                         |
| Распространяемые компоненты<br/>       | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
