---
description: Описание процедур создания, извлечения, проверки и экспорта ключей и подписей DSS.
ms.assetid: d28fe531-af4b-4b5e-ab67-47ef70f8fa5b
title: Ключи DSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5497a2a02ac5614c056f819a3999ee3cca6c5da78229f92e57002ae6a9e401ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119875314"
---
# <a name="dss-keys"></a>Ключи DSS

-   [Создание и получение ключей DSS](#generating-and-retrieving-dss-keys)
-   [Создание подписей DSS](#generating-dss-signatures)
-   [Проверка подписи DSS](#verifying-a-dss-signature)
-   [Экспорт ключей DSS](#exporting-dss-keys)

## <a name="generating-and-retrieving-dss-keys"></a>Создание и получение ключей DSS

Ключи DSS можно создавать с помощью вызова функции [**криптженкэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) . Вызов **криптженкэй** требует, чтобы в \_ \_ \_ аргументе *алгид* был передан либо сигнатура, либо калг DSS. Этот вызов создаст значения P (основной модуль), Q (простой), G (генератор), X (секретный показатель) и Y (открытый ключ) с нуля и сохранит их в [*двоичном объекте ключа*](../secgloss/k-gly.md) в локальном хранилище.

**Создание пары ключей подписи DSS**

1.  Вызовите функцию [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) , чтобы получить маркер поставщика служб шифрования Microsoft DSS.
2.  Вызовите [**криптженкэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) , чтобы создать ключи. \_ \_ Для аргумента алгид необходимо передать либо сигнатуру, либо калг DSS \_ Sign, а старшие 16 разрядов аргумента *dwFlags* должны быть заданы с требуемым размером ключа.  Если 16 верхних разрядов равны нулю, будет использоваться размер ключа по умолчанию (1 024 бит). В аргументе *hKey* возвращается [**хкрипткэй**](hcryptkey.md) -маркер.

**Получение указателя на ранее созданные ключи подписи**

1.  Вызовите [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) , чтобы получить маркер поставщика служб шифрования Microsoft DSS.
2.  Вызовите функцию [**криптжетусеркэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) с аргументом *двкэйспек* , для которого задано значение в \_ сигнатуре или калге \_ DSS \_ .

**Получение значений P, Q и G**

1.  Вызовите [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) , чтобы получить маркер поставщика служб шифрования Microsoft DSS.
2.  Вызовите [**криптжетусеркэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) , указав для аргумента *двкэйспек* значение at \_ или калг \_ \_ Sign.
3.  Вызовите [**криптжеткэйпарам**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetkeyparam) , указав в качестве аргумента *hKey* указатель, полученный на предыдущем шаге. Для аргумента *двпарам* должен быть задан нужный флаг; КЛЮЧЕВОЙ \_ P, ключевой \_ вопрос Q или ключевой \_ номер G. Значение возвращается в аргументе *pbData* , а длина данных возвращается в аргументе *пдвдатален* . Значение возвращается без сведений о заголовке и в формате с [*прямым порядком байтов*](../secgloss/l-gly.md) .

## <a name="generating-dss-signatures"></a>Создание подписей DSS

Данные для подписи должны быть сначала [*хэшированы*](../secgloss/h-gly.md) с помощью алгоритма [*SHA*](../secgloss/s-gly.md) . После хэширования данных создается подпись [*DSS*](../secgloss/d-gly.md) путем вызова функции [**криптсигнхаш**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignhasha) .

**Создание подписи DSS**

1.  Вызовите [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) , чтобы получить маркер поставщика служб шифрования Microsoft DSS.
2.  Вызовите [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) , указав для аргумента *алгид* значение калг \_ SHA, чтобы получить маркер для хэш-объекта SHA.
3.  Вызовите [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) с аргументом *ххаш* , для которого задан маркер, полученный на предыдущем шаге. При этом создается хэш данных и возвращается маркер для хеша в аргументе *фхаш* вызова функции [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) .
4.  Вызовите [**криптсигнхаш**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignhasha) с аргументом *ххаш* , для которого задан маркер, полученный на предыдущем шаге. В \_ \_ \_ параметре *двкэйспек* может быть передан либо подпись at, либо калг DSS Sign. Сигнатура возвращается к адресу, указанному в аргументе *пбсигнатуре* , и длина подписи возвращается к адресу, указанному в аргументе *пдвсиглен* . Указатель **null** может быть передан в аргумент *пбсигнатуре* , и в данном случае сигнатура не создается, но длина сигнатуры возвращается к адресу, указанному в параметре *пдвсиглен* .

## <a name="verifying-a-dss-signature"></a>Проверка подписи DSS

Чтобы проверить подпись DSS, необходимо импортировать открытый ключ DSS, [*подписанные данные*](../secgloss/s-gly.md) должны быть хэшированы, после чего подпись может быть проверена.

**Проверка подписи DSS**

1.  Вызовите [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) , чтобы получить маркер поставщика служб шифрования Microsoft DSS.
2.  Вызовите [**криптимпорткэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) , чтобы импортировать открытый ключ DSS подписавший.
3.  Вызовите [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) , указав для аргумента *алгид* значение калг \_ SHA, чтобы получить маркер для хэш-объекта SHA.
4.  Вызовите [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) с аргументом *ххаш* , для которого задан маркер, полученный на предыдущем шаге, а *pbData* указывает на подписанные данные. При этом создается хэш данных и возвращается маркер для хеша в аргументе *фхаш* вызова функции [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) .
5.  Вызовите [**криптверифисигнатуре**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifysignaturea) со следующими параметрами:

    *ххаш* задается в качестве маркера для хэша, выполненного на предыдущем шаге.

    *пбсигнатуре* указывает на проверяемую подпись.

    *двсиглен* задает длину подписи.

    для *хпубкэй* задается маркер открытого ключа, импортированного на шаге 2.

    *dwFlags* имеет значение 0.

## <a name="exporting-dss-keys"></a>Экспорт ключей DSS

При отправке [*подписанных данных*](../secgloss/s-gly.md) пользователю, где подпись должна быть проверена получателем, Открытый ключ подписавшего должен быть предоставлен получателю и обычно отправляется вместе с подписанными данными. Поэтому необходимо иметь возможность экспортировать ключи [*DSS*](../secgloss/d-gly.md) в формате [*большого двоичного объекта ключа*](../secgloss/k-gly.md) .

**Экспорт открытого ключа DSS**

1.  Вызовите [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) , чтобы получить маркер поставщика служб шифрования Microsoft DSS.
2.  Вызовите [**криптжетусеркэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) , указав для аргумента *двкэйспек* значение at \_ или калг \_ \_ Sign.
3.  Вызовите [**криптекспорткэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) с помощью *hKey* , полученного на предыдущем шаге, *двблобтипе* , для которого задано значение публиккэйблоб, а *dwFlags* — нулевое значение. [*Большой двоичный объект открытого ключа*](../secgloss/p-gly.md) DSS возвращается в *pbData*, а длина [*большого двоичного объекта ключа*](../secgloss/k-gly.md) возвращается в *пдвдатален*. Указатель **null** можно передать в *pbData*, и в этом случае будет возвращена только длина большого двоичного объекта DSS Key. Большой двоичный объект, возвращаемый при вызове **криптекспорткэй** , имеет формат, описанный в [разделе BLOB-объекты поставщика DSS](dss-provider-key-blobs.md).

**Экспорт закрытого ключа DSS**

-   Выполните ту же процедуру, что и для экспорта открытого ключа DSS, за исключением того, что при вызове [**криптекспорткэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) *ДВБЛОБТИПЕ* имеет значение приватекэйблоб. Большой двоичный объект, возвращаемый при вызове **криптекспорткэй** , имеет формат, описанный в [разделе BLOB-объекты поставщика DSS](dss-provider-key-blobs.md).

 

 
