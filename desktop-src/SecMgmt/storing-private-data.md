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
# <a name="storing-private-data"></a><span data-ttu-id="82b1e-103">Хранение частных данных</span><span class="sxs-lookup"><span data-stu-id="82b1e-103">Storing Private Data</span></span>

<span data-ttu-id="82b1e-104">Политика LSA предоставляет две функции, которые можно использовать для установки и получения закрытых данных.</span><span class="sxs-lookup"><span data-stu-id="82b1e-104">LSA Policy provides two functions that you can use to set and retrieve private data.</span></span> <span data-ttu-id="82b1e-105">Эти данные хранятся в реестре в виде зашифрованной строки.</span><span class="sxs-lookup"><span data-stu-id="82b1e-105">This data is stored as an encrypted string in the registry.</span></span> <span data-ttu-id="82b1e-106">Например, эти функции можно использовать для хранения паролей учетных записей сервера и других конфиденциальных данных.</span><span class="sxs-lookup"><span data-stu-id="82b1e-106">For example, you can use these functions to store server account passwords and other sensitive information.</span></span>

<span data-ttu-id="82b1e-107">Вызовите функцию [**лсастореприватедата**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsastoreprivatedata) для хранения и шифрования закрытых данных.</span><span class="sxs-lookup"><span data-stu-id="82b1e-107">Call the [**LsaStorePrivateData**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsastoreprivatedata) function to store and encrypt private data.</span></span> <span data-ttu-id="82b1e-108">Как описано в разделе [закрытый объект данных](private-data-object.md), закрытые объекты данных включают в себя три специализированных типа: локальный, глобальный и компьютер.</span><span class="sxs-lookup"><span data-stu-id="82b1e-108">As described in [Private Data Object](private-data-object.md), private data objects include three specialized types: local, global, and machine.</span></span> <span data-ttu-id="82b1e-109">Чтобы создать специализированный объект, добавьте префикс в имя ключа, передаваемое в **лсастореприватедата**: "L $" для локальных объектов, "G $" для глобальных объектов и "M $" для объектов-компьютеров.</span><span class="sxs-lookup"><span data-stu-id="82b1e-109">To create a specialized object, add a prefix to the key name passed to **LsaStorePrivateData**: "L$" for local objects, "G$" for global objects, and "M$" for machine objects.</span></span> <span data-ttu-id="82b1e-110">Если вы не создаете один из этих специализированных типов, не нужно указывать префикс имени ключа.</span><span class="sxs-lookup"><span data-stu-id="82b1e-110">If you are not creating one of these specialized types, you do not need to specify a key name prefix.</span></span>

<span data-ttu-id="82b1e-111">Чтобы получить и декодировать ранее сохраненные закрытые данные, вызовите [**лсаретриевеприватедата**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaretrieveprivatedata).</span><span class="sxs-lookup"><span data-stu-id="82b1e-111">To retrieve and decode previously stored private data, call [**LsaRetrievePrivateData**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaretrieveprivatedata).</span></span> <span data-ttu-id="82b1e-112">Обратите внимание, что невозможно получить частные объекты данных компьютера; объекты компьютеров могут быть получены только операционной системой.</span><span class="sxs-lookup"><span data-stu-id="82b1e-112">Note that you cannot retrieve machine private data objects; machine objects can be retrieved only by the operating system.</span></span>

<span data-ttu-id="82b1e-113">Прежде чем можно будет хранить или извлекать закрытые данные, приложение должно получить обработчик для объекта локальной [**политики**](policy-object.md) , как показано в примере [открытия объекта политики](opening-a-policy-object-handle.md).</span><span class="sxs-lookup"><span data-stu-id="82b1e-113">Before you can store or retrieve private data, your application must get a handle to the local [**Policy**](policy-object.md) object, as demonstrated in [Opening a Policy Object Handle](opening-a-policy-object-handle.md).</span></span>

<span data-ttu-id="82b1e-114">В следующем примере создается локальный закрытый объект данных.</span><span class="sxs-lookup"><span data-stu-id="82b1e-114">The following example creates a local private data object.</span></span> <span data-ttu-id="82b1e-115">Обратите внимание, что функция Инитлсастринг преобразует строку [*Юникода*](/windows/desktop/SecGloss/u-gly) в [**структуру \_ \_ строки Юникода LSA**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) .</span><span class="sxs-lookup"><span data-stu-id="82b1e-115">Note that the function InitLsaString converts a [*Unicode*](/windows/desktop/SecGloss/u-gly) string to an [**LSA\_UNICODE\_STRING**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) structure.</span></span> <span data-ttu-id="82b1e-116">Код для этой функции показан в [использовании строк Юникода в формате LSA](using-lsa-unicode-strings.md).</span><span class="sxs-lookup"><span data-stu-id="82b1e-116">The code for this function is shown in [Using LSA Unicode Strings](using-lsa-unicode-strings.md).</span></span>


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
> <span data-ttu-id="82b1e-117">Данные, хранящиеся в функции [**лсастореприватедата**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsastoreprivatedata) , не являются абсолютно защищенными.</span><span class="sxs-lookup"><span data-stu-id="82b1e-117">The data stored by the [**LsaStorePrivateData**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsastoreprivatedata) function is not absolutely protected.</span></span> <span data-ttu-id="82b1e-118">Раздел, однако, имеет [*список управления доступом на уровне пользователей*](/windows/desktop/SecGloss/d-gly) (DACL), позволяющий только создателю и администраторам считывать данные.</span><span class="sxs-lookup"><span data-stu-id="82b1e-118">The key, however, has a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) that allows only the creator and administrators to read the data.</span></span>

 

 

 
