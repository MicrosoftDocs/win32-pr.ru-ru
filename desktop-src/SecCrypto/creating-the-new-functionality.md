---
description: Следующие функции доступны для расширенных функций CryptoAPI.
ms.assetid: eb4c1352-1432-4f45-a309-fa17b694a35e
title: Создание новых функциональных возможностей
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d660c14e99247c7d17f57100858b104d1cbcc9ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541007"
---
# <a name="creating-the-new-functionality"></a>Создание новых функциональных возможностей

Следующие функции доступны для расширенных функций CryptoAPI.



| CryptoAPI, функция                                   | Определение имени функции OID                         | Строка имени функции OID  |
|------------------------------------------------------|--------------------------------------------------|---------------------------|
| [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject)       | \_Шифрование OID \_ шифрования \_ объекта \_ Func<br/>     | "Криптдлленкодеобжект"    |
| [**криптдекодеобжект**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject)       | \_ \_ расшифровка объекта шифрования OID \_ \_ Func<br/>     | "Криптдллдекодеобжект"    |
| [**цертопенсторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore)               | ШИФРОВАНИЯ \_ OID \_ Open \_ Store \_ Prov \_ Func<br/>  | "Цертдллопенсторепров"    |
| [**цертверификтлусаже**](/windows/desktop/api/Wincrypt/nf-wincrypt-certverifyctlusage)     | способ \_ шифрования \_ OID \_ проверки \_ использования CTL \_ Func<br/> | "Цертдллверификтлусаже"   |
| [**цертверифиревокатион**](/windows/desktop/api/Wincrypt/nf-wincrypt-certverifyrevocation) | \_ \_ подтвердить отзыв проверки \_ отзыва OID \_<br/> | "Цертдллверифиревокатион" |



 

При нормальном использовании с существующим идентификатором объекта и типом кодировки используется код самой функции CryptoAPI. Если одна из этих функций вызывается с идентификатором OID и типом кодировки, которую код в функции CryptoAPI не предназначал для обработки, то в библиотеке DLL должна быть создана новая функция, содержащая новые функциональные возможности. Эта библиотека DLL должна быть зарегистрирована в реестре или установлена в памяти.

Когда одна из перечисленных функций вызывается с вновь назначенным идентификатором OID и типом кодирования, используется код в новой библиотеке DLL, а не код, предоставленный как часть функции CryptoAPI.

Имя вновь разработанной функции может быть именем, указанным в разделе "строка имени функции OID" в предыдущей таблице, или может быть задано другое имя при регистрации нового кода функции.

Новая функция должна использовать соответствующий прототип. Во всех случаях, за исключением [**цертопенсторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore), этот прототип аналогичен функции CryptoAPI, которая вызывает новую функцию. В случае с **цертопенсторе** прототип выглядит следующим образом.


```C++
#include <windows.h>

BOOL WINAPI CertDllOpenStoreProv(
  IN LPCSTR lpszStoreProvider,
  IN DWORD dwEncodingType,
  IN HCRYPTPROV hCryptProv,
  IN DWORD dwFlags,
  IN const void *pvPara,
  IN HCERTSTORE hCertStore,
  IN OUT PCERT_STORE_PROV_INFO pStoreProvInfo
);
```



> [!Note]  
> Если прототипы не совпадают, системный стек будет поврежден.

 

Помимо предоставления кода для новой функции в библиотеке DLL, расширение функциональных возможностей [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) или [**криптдекодеобжект**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject) требует определения типа для новой структуры данных C, которая будет помещена в заголовочный файл, включенный при компиляции программы пользователя.

 

 




