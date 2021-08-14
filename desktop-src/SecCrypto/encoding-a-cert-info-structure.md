---
description: Процесс кодирования является обратным процессом декодирования, описанным в разделе Декодирование \_ структуры сведений о сертификате.
ms.assetid: 5d3311e5-a2fb-46f7-aa76-f232b39b34fd
title: Кодирование структуры CERT_INFO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b469ae0bdf02ffd8f30f8b0c2dd44051239a5702ff32704d58de8b60f1ca9701
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117766796"
---
# <a name="encoding-a-cert_info-structure"></a>Кодирование \_ структуры сведений о сертификате

Процесс кодирования является обратным процессом декодирования, описанным в разделе [декодирование \_ структуры сведений о сертификате](decoding-a-cert-info-structure.md). Например, следующая процедура добавляет закодированный **Издатель** в структуру [**\_ сведений о сертификате**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) . Также см. иллюстрацию, следующую за процедурой.

**Добавление закодированного издателя в \_ структуру сведений о сертификате**

1.  Создайте строку, содержащую имя используемого издателя.
2.  Создайте массив структур [**attr на \_ RDN \_ сертификата**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_rdn_attr) , который будет инициализирован для хранения нужных сведений о созданной строке имени издателя.
3.  Создайте массив структур [**\_ RDN сертификата**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_rdn) , один из которых содержит сведения о массиве только что инициализированных [**структур \_ \_ attr RDN сертификата**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_rdn_attr) .
4.  Создайте структуру [**\_ \_ сведений об имени сертификата**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_name_info) , которая содержит указатель на массив только что созданных структур [**\_ RDN сертификата**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_rdn) .
5.  Вызовите [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) , чтобы получить размер большого двоичного объекта, закодированного в результате, передав ему адрес только что созданной структуры [**\_ \_ сведений о имени сертификата**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_name_info) .
6.  Выделите память для выходного BLOB-объекта в формате.
7.  Снова вызовите [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) , передав ему ту же информацию, но передавая ей адрес только что выделенной памяти.
8.  Задайте для элемента **Issuer. cbData** структуры [**\_ сведений о сертификате**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) размер, возвращенный на шаге 5, и член **Issuer. pbData** на адрес, полученный на шаге 6. BLOB-объект закодированного **издателя** теперь находится там.

![Добавление закодированного издателя в \- структуру сведений о сертификате](images/encflow.png)

Для инициализации и кодирования некоторых сведений о расширении сертификата используйте следующую процедуру. Также см. иллюстрацию, следующую за процедурой.

**Добавление сведений о кодированном расширении в \_ структуру сведений о сертификате**

1.  Создание и инициализация структуры сведений о расширении. в этом примере это структура сведений [**\_ \_ \_ о базовых ограничениях сертификата**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_basic_constraints_info) .
2.  Вызовите [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject), передав ему адрес созданной структуры, чтобы получить размер BLOB-объекта, закодированного в результате.
3.  Выделите память для выходного BLOB-объекта в формате.
4.  Снова вызовите [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) , передав те же сведения, за исключением того, что теперь передает адрес выделенной памяти.
5.  Создайте массив структур [**\_ расширения сертификата**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_extension) .
6.  Инициализируйте одну из [**структур \_ расширения сертификата**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_extension) , чтобы **псзобжид** является правильной строкой для данных, содержащихся в **значении**, и это **значение** содержит зашифрованный большой двоичный объект данных, который был выведен из вызова [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject).
7.  Инициализируйте элемент **ржекстенсион** структуры [**\_ сведений о сертификате**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) , чтобы он указывал на массив [**структур \_ расширения сертификата**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_extension) .

![Добавление закодированных сведений о расширении в \- структуру сведений о сертификате](images/xtenflow.png)

 

 



