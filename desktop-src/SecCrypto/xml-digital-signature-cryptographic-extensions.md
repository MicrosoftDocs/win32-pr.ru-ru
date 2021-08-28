---
description: Криптксмл позволяет разработчикам расширять встроенные криптографические алгоритмы путем регистрации общесистемной библиотеки DLL расширения шифрования.
ms.assetid: b0625481-660a-4fd5-ba15-d532998f95a6
title: Криптографические расширения цифровых подписей XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41bf0f2d99b34d59e9817f8568b03be20e72dda1
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474940"
---
# <a name="xml-digital-signature-cryptographic-extensions"></a>Криптографические расширения цифровых подписей XML

Криптксмл позволяет разработчикам расширять встроенные криптографические алгоритмы путем регистрации общесистемной библиотеки DLL расширения шифрования. Библиотеки DLL расширения расширяют алгоритмы, поддерживаемые XML-элементами **SignatureMethod** и **дижестмесод** . Библиотеки DLL расширения могут поддерживать алгоритмы, которые закодируются дополнительные параметры в цифровой подписи XML.

Все библиотеки DLL расширений должны поддерживать функцию [**криптксмлдллжетинтерфаце**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllgetinterface) , которая возвращает указатель на [**понятную структуру \_ \_ \_ интерфейса шифрования XML**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_cryptographic_interface) . Эта структура предоставляет указатели на функции для реализованных функций криптографических расширений. Поддерживаемые функции зависят от типа поддерживаемого алгоритма шифрования и от того, должен ли алгоритм кодировать параметры в цифровой подписи XML.

К функциям расширений шифрования относятся следующие указатели функций:

<dl> <dt>

<span id="Required_functions"></span><span id="required_functions"></span><span id="REQUIRED_FUNCTIONS"></span>Обязательные функции
</dt> <dd>

-   [**криптксмлдллжетинтерфаце**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllgetinterface)
-   [**криптксмлдллжеталгорисминфо**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllgetalgorithminfo)

</dd> <dt>

<span id="Digest_Method_functions"></span><span id="digest_method_functions"></span><span id="DIGEST_METHOD_FUNCTIONS"></span>Функции метода дайджеста
</dt> <dd>

-   [**криптксмлдллклоседижест**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllclosedigest)
-   [**криптксмлдллкреатедижест**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllcreatedigest)
-   [**криптксмлдллдижестдата**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldlldigestdata)
-   [**криптксмлдллфинализедижест**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllfinalizedigest)

</dd> <dt>

<span id="Signature_Method_Functions"></span><span id="signature_method_functions"></span><span id="SIGNATURE_METHOD_FUNCTIONS"></span>Функции метода подписи
</dt> <dd>

-   [**криптксмлдллсигндата**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllsigndata)
-   [**криптксмлдллверифисигнатуре**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllverifysignature)
-   [**криптксмлдллкреатекэй**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllcreatekey)
-   [**криптксмлдлленкодекэйвалуе**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllencodekeyvalue)

</dd> <dt>

<span id="For_algorithms_with_default_encoded_parameters"></span><span id="for_algorithms_with_default_encoded_parameters"></span><span id="FOR_ALGORITHMS_WITH_DEFAULT_ENCODED_PARAMETERS"></span>Для алгоритмов с закодированными параметрами по умолчанию
</dt> <dd>

-   [**криптксмлдлленкодеалгорисм**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllencodealgorithm)

</dd> </dl>

Библиотеки DLL расширения шифрования регистрируются на уровне системы. Для регистрации библиотеки DLL расширения шифрования требуются права администратора.

Все криптографические расширения Криптксмл регистрируются значением URI, заданным в поле **SignatureMethod** или атрибутом Algorithm элемента **дижестмесод** .

Ниже приведены пути реестра для библиотек DLL расширения.

<dl> <dt>

<span id="32-bit"></span><span id="32-BIT"></span>32-разрядный
</dt> <dd>

**HKey \_ \_** \\ **Программное обеспечение** локального компьютера \\ (**Microsoft** \\ **Cryptography** \\ **криптксмл** \\ **URI)** \\ *{URI}*

</dd> <dt>

<span id="64-bit"></span><span id="64-BIT"></span>64-разрядный
</dt> <dd>

**HKey \_ \_** \\ **Программное обеспечение** локального компьютера \\ (**Microsoft** \\ **Cryptography** \\ **криптксмл** \\ **URI)** \\ *{URI}*

**HKey \_ \_** \\ **Программное обеспечение** локального компьютера \\ **WOW6432NODE** \\ **Microsoft** \\ **Cryptography** \\ **криптксмл** \\ **URI** \\ *{URI}*

</dd> </dl>

Каждый ключ содержит следующие параметры.




| Имя | Тип | Данные | 
|------|------|------|
| DLL<br /> | Расширяемая строка<br /> | Обязательный.<br />Абсолютный путь к библиотеке DLL поставщика служб шифрования XML.<blockquote><p><b>Примечание. </b> Рекомендуется размещать библиотеки DLL расширения шифрования в каталогах, которые могут быть записаны только приложениями с правами администратора.</p><p><a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya"><strong>LoadLibrary</strong></a> используется для загрузки библиотеки DLL расширения шифрования.<br /></p></blockquote><br /> | 
| Имя<br /> | <strong>String</strong> | Необязательный элемент.<br /> Отображаемое имя, связанное с этим URI.<br /> | 
| GroupId<br /> | <strong>DWORD</strong> | Обязательный.<br /> Идентификатор группы, связанный с этим алгоритмом шифрования. Возможные значения включают следующие:<strong>CRYPT_XML_GROUP_ID_HASH</strong> \<strong> </strong> = 1.<br /><strong></strong> \<strong> CRYPT_XML_GROUP_ID_SIGN </strong> = 2<br /> | 
| кнгалгид<br /> | <strong>String</strong> | Обязательный.<br /> Имя алгоритма CNG, которое будет передано функциям BCrypt или NCrypt.<br /> | 
| кнжекстраалгид<br /> | <strong>String</strong> | Необязательный элемент.<br /> Дополнительные строки алгоритма, отличные от строки в члене Кнгалгид, которые могут быть переданы в функции CNG.<br /> Для алгоритмов подписи (CRYPT_XML_GROUP_ID_SIGN) этот член является строкой алгоритма открытого ключа для передачи в функции CNG.<br /> Для других значений GroupId присвойте элементу <strong>пвсзкнжекстраалгид</strong> пустую строку L "". <br /> | 




 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>


</dt> <dt>

[Алгоритмы шифрования цифровых подписей XML](xml-digital-signature-cryptographic-algorithms.md)
</dt> </dl>

 

 
