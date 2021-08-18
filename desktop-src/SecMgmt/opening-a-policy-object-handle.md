---
description: Большинство функций политики LSA требует наличия обработчика для объекта политики, чтобы система была запрашивать или изменять. Чтобы получить маркер объекта политики, вызовите Лсаопенполици и укажите имя системы, к которой необходимо получить доступ, а также необходимый набор разрешений на доступ.
ms.assetid: 66fdc878-d9c4-421c-b79f-9df08984611c
title: Открытие обработчика объектов политики
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16baf2cf7e722faca1f0441505ec325b8e64c8aad95522e697b4905f566985af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118894056"
---
# <a name="opening-a-policy-object-handle"></a>Открытие обработчика объектов политики

Большинство функций политики LSA требует наличия обработчика для объекта [**политики**](policy-object.md) , чтобы система была запрашивать или изменять. Чтобы получить маркер объекта **политики** , вызовите [**лсаопенполици**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy) и укажите имя системы, к которой необходимо получить доступ, а также необходимый набор разрешений на доступ.

Разрешения на доступ, необходимые для вашего приложения, зависят от выполняемых им действий. Дополнительные сведения о разрешениях, необходимых для каждой функции, см. в описании этой функции в разделе [функции политики LSA](management-functions.md).

Если вызов [**лсаопенполици**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy) успешно выполнен, он возвращает маркер объекта [**политики**](policy-object.md) для указанной системы. Затем приложение передает этот обработчик в последующие вызовы функции политики LSA. Когда приложению больше не требуется этот обработчик, он должен вызвать [**лсаклосе**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose) , чтобы освободить его.

В следующем примере показано, как открыть обработчик объекта [**политики**](policy-object.md) .


```C++
#include <windows.h>

#define TARGET_SYSTEM_NAME L"mysystem"

LSA_HANDLE GetPolicyHandle()
{
  LSA_OBJECT_ATTRIBUTES ObjectAttributes;
  WCHAR SystemName[] = TARGET_SYSTEM_NAME;
  USHORT SystemNameLength;
  LSA_UNICODE_STRING lusSystemName;
  NTSTATUS ntsResult;
  LSA_HANDLE lsahPolicyHandle;

  // Object attributes are reserved, so initialize to zeros.
  ZeroMemory(&ObjectAttributes, sizeof(ObjectAttributes));

  //Initialize an LSA_UNICODE_STRING to the server name.
  SystemNameLength = wcslen(SystemName);
  lusSystemName.Buffer = SystemName;
  lusSystemName.Length = SystemNameLength * sizeof(WCHAR);
  lusSystemName.MaximumLength = (SystemNameLength+1) * sizeof(WCHAR);

  // Get a handle to the Policy object.
  ntsResult = LsaOpenPolicy(
        &lusSystemName,    //Name of the target system.
        &ObjectAttributes, //Object attributes.
        POLICY_ALL_ACCESS, //Desired access permissions.
        &lsahPolicyHandle  //Receives the policy handle.
    );

  if (ntsResult != STATUS_SUCCESS)
  {
    // An error occurred. Display it as a win32 error code.
    wprintf(L"OpenPolicy returned %lu\n",
      LsaNtStatusToWinError(ntsResult));
    return NULL;
  } 
  return lsahPolicyHandle;
}
```



В предыдущем примере приложение запросило политику \_ все \_ [*права*](/windows/desktop/SecGloss/p-gly)доступа. Дополнительные сведения о том, какие разрешения приложение должно запрашивать при вызове [**лсаопенполици**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy), см. в описании функций, в которые приложение будет передавать дескриптор объекта [**политики**](policy-object.md) .

Чтобы открыть маркер для объекта [**политики**](policy-object.md) доверенного домена, вызовите [**лсакреатетрустеддомаинекс**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacreatetrusteddomainex) (для создания нового отношения доверия с доменом) или вызовите [**лсаопентрустеддомаинбинаме**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaopentrusteddomainbyname) (для доступа к существующему доверенному домену). Обе эти функции устанавливают указатель на [**\_ обработчик LSA**](lsa-handle.md), который затем можно указать в последующих вызовах функции политики LSA. Как и в случае с [**лсаопенполици**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy), приложение должно вызывать [**лсаклосе**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose) , когда больше не требуется обращаться к объекту **политики** доверенного домена.

 

 
