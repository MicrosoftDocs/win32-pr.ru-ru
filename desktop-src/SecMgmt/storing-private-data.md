---
description: Политика LSA предоставляет две функции, которые можно использовать для установки и получения закрытых данных.
ms.assetid: 7b6e63d4-ce8f-4279-85d9-da6b2b589afa
title: Хранение частных данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6281f77e66a4217bda534b34342d6cefd92bd7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423766"
---
# <a name="storing-private-data"></a>Хранение частных данных

Политика LSA предоставляет две функции, которые можно использовать для установки и получения закрытых данных. Эти данные хранятся в реестре в виде зашифрованной строки. Например, эти функции можно использовать для хранения паролей учетных записей сервера и других конфиденциальных данных.

Вызовите функцию [**лсастореприватедата**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsastoreprivatedata) для хранения и шифрования закрытых данных. Как описано в разделе [закрытый объект данных](private-data-object.md), закрытые объекты данных включают в себя три специализированных типа: локальный, глобальный и компьютер. Чтобы создать специализированный объект, добавьте префикс в имя ключа, передаваемое в **лсастореприватедата**: "L $" для локальных объектов, "G $" для глобальных объектов и "M $" для объектов-компьютеров. Если вы не создаете один из этих специализированных типов, не нужно указывать префикс имени ключа.

Чтобы получить и декодировать ранее сохраненные закрытые данные, вызовите [**лсаретриевеприватедата**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaretrieveprivatedata). Обратите внимание, что невозможно получить частные объекты данных компьютера; объекты компьютеров могут быть получены только операционной системой.

Прежде чем можно будет хранить или извлекать закрытые данные, приложение должно получить обработчик для объекта локальной [**политики**](policy-object.md) , как показано в примере [открытия объекта политики](opening-a-policy-object-handle.md).

В следующем примере создается локальный закрытый объект данных. Обратите внимание, что функция Инитлсастринг преобразует строку [*Юникода*](/windows/desktop/SecGloss/u-gly) в [**структуру \_ \_ строки Юникода LSA**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) . Код для этой функции показан в [использовании строк Юникода в формате LSA](using-lsa-unicode-strings.md).


```C++
#include <windows.h>
#include <stdio.h>

BOOL CreatePrivateDataObject(LSA_HANDLE PolicyHandle)
{
  NTSTATUS ntsResult;
  LSA_UNICODE_STRING lucKeyName;
  LSA_UNICODE_STRING lucPrivateData;
  // The L$ prefix specifies a local private data object
  WCHAR wszKeyName[] = L"L$MyPrivateKey";
  WCHAR wszPrivateData[] = L"Something secret.";

  // Initializing PLSA_UNICODE_STRING structures
  if (!InitLsaString(&lucKeyName, wszKeyName))
  {
         wprintf(L"Failed InitLsaString\n");
         return FALSE;
  }
  if (!InitLsaString(&lucPrivateData, wszPrivateData))
  {
         wprintf(L"Failed InitLsaString\n");
         return FALSE;
  }

  // Store the private data.
  ntsResult = LsaStorePrivateData(
    PolicyHandle,   // handle to a Policy object
    &lucKeyName,    // key to identify the data
    &lucPrivateData // the private data
  );
  if (ntsResult != STATUS_SUCCESS)
  {
    wprintf(L"Store private object failed %lu\n",
      LsaNtStatusToWinError(ntsResult));
    return FALSE;
  }
  return TRUE;
}
```



> [!Note]  
> Данные, хранящиеся в функции [**лсастореприватедата**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsastoreprivatedata) , не являются абсолютно защищенными. Раздел, однако, имеет [*список управления доступом на уровне пользователей*](/windows/desktop/SecGloss/d-gly) (DACL), позволяющий только создателю и администраторам считывать данные.

 

 

 
