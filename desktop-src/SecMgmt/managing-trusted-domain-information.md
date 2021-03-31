---
description: Политика LSA предоставляет несколько функций, которые можно использовать для создания, перечисления и удаления доверенных доменов, а также для установки и получения сведений о доверенном домене.
ms.assetid: 0c7534d7-3372-49c4-992c-9b519279982d
title: Управление сведениями о доверенном домене
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b7df297b8c83ebe9054ca6f04b657905c21fae6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104266095"
---
# <a name="managing-trusted-domain-information"></a>Управление сведениями о доверенном домене

Политика LSA предоставляет несколько функций, которые можно использовать для создания, перечисления и удаления доверенных доменов, а также для установки и получения сведений о доверенном домене.

Прежде чем можно будет управлять сведениями о доверенном домене, приложение должно получить обработчик для объекта [**политики**](policy-object.md) , как описано в разделах [Открытие обработчика объектов политики](opening-a-policy-object-handle.md).

Вы можете перечислить доверенные домены, вызвав [**лсаенумератетрустеддомаинсекс**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomainsex).

Чтобы получить сведения о доверенном домене, вызовите либо [**лсакуеритрустеддомаининфо**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaquerytrusteddomaininfo) , либо [**LsaQueryTrustedDomainInfoByName**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaquerytrusteddomaininfobyname). Обе функции возвращают одну и ту же информацию; Однако **лсакуеритрустеддомаининфо** идентифицирует доверенный домен по идентификатору безопасности, а **LsaQueryTrustedDomainInfoByName** определяет доверенный домен по имени.

Чтобы задать сведения для доверенного домена, вызовите либо [**лсасеттрустеддомаининформатион**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsasettrusteddomaininformation) , либо [**лсасеттрустеддомаининфобинаме**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsasettrusteddomaininfobyname). Как и в случае с функциями запросов, **лсасеттрустеддомаининформатион** идентифицирует доверенный домен по идентификатору безопасности, а **лсасеттрустеддомаининфобинаме** определяет доверенный домен по имени.

Приложение может отозвать отношение доверия для доверенного домена, вызвав [**лсаделететрустеддомаин**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsadeletetrusteddomain).

В следующем примере перечисляются доверенные домены для локальной системы.


```C++
#include <windows.h>

void EnumerateTrusts(LSA_HANDLE PolicyHandle)
{
  LSA_ENUMERATION_HANDLE hEnum=0; 
  PLSA_TRUST_INFORMATION TrustInfo = NULL;
  ULONG ulReturned = 0;               
  NTSTATUS Status = 0;
  ULONG i;
  WCHAR StringBuffer[256];

  // Enumerate the trusted domains until there are no more to return.
  do 
  {
    Status = LsaEnumerateTrustedDomains(
       PolicyHandle,         // an open policy handle
       &hEnum,               // enumeration tracker
       (PVOID*)&TrustInfo,   // buffer to receive data
       32000,                // recommended buffer size
       &ulReturned           // number of items returned in TrustInfo
    );

    // Check the return status for errors.
    if((Status != STATUS_SUCCESS) &&
       (Status != STATUS_MORE_ENTRIES) &&
     (Status != STATUS_NO_MORE_ENTRIES))
      {
        // Handle the error.
        wprintf(L"Error occurred enumerating domains %lu\n",
        LsaNtStatusToWinError(Status));
        return;
      } 

      wprintf(L"Status %lu\n", LsaNtStatusToWinError(Status));
      // Process the trusted domain information.
      for (i=0;i<ulReturned; i++) 
      {
        // LSA_Unicode strings might not be null-terminated.
        if(TrustInfo[i].Name.Length < 256)
        {
            wcsncpy_s(StringBuffer,
                256,
                TrustInfo[i].Name.Buffer,
                TrustInfo[i].Name.Length
            );
            // Guarantee that StringBuffer is null-terminated.
            StringBuffer[TrustInfo[i].Name.Length] = NULL; 
        }
        else
        {
            fprintf(stderr, "Name too long for string buffer.\n");
            exit(1);
        }
        
        wprintf(L"Enum Trusted Domain - %ws ", StringBuffer);
      }
      // Free the buffer.
      if (TrustInfo != NULL) 
      {
        LsaFreeMemory(TrustInfo);
        TrustInfo = NULL;
      }
    } while (Status != STATUS_NO_MORE_ENTRIES);
    return;
}
```



 

 



