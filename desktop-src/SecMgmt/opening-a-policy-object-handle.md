---
description: Большинство функций политики LSA требует наличия обработчика для объекта политики, чтобы система была запрашивать или изменять. Чтобы получить маркер объекта политики, вызовите Лсаопенполици и укажите имя системы, к которой необходимо получить доступ, а также необходимый набор разрешений на доступ.
ms.assetid: 66fdc878-d9c4-421c-b79f-9df08984611c
title: Открытие обработчика объектов политики
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c187720692db4937b6e1299dd2bb63fac647852
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684440"
---
# <a name="opening-a-policy-object-handle"></a><span data-ttu-id="6047c-104">Открытие обработчика объектов политики</span><span class="sxs-lookup"><span data-stu-id="6047c-104">Opening a Policy Object Handle</span></span>

<span data-ttu-id="6047c-105">Большинство функций политики LSA требует наличия обработчика для объекта [**политики**](policy-object.md) , чтобы система была запрашивать или изменять.</span><span class="sxs-lookup"><span data-stu-id="6047c-105">Most LSA Policy functions require a handle to the [**Policy**](policy-object.md) object for the system to query or modify.</span></span> <span data-ttu-id="6047c-106">Чтобы получить маркер объекта **политики** , вызовите [**лсаопенполици**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy) и укажите имя системы, к которой необходимо получить доступ, а также необходимый набор разрешений на доступ.</span><span class="sxs-lookup"><span data-stu-id="6047c-106">To obtain a handle to a **Policy** object, call [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy) and specify the name of the system you want to access and the set of access permissions required.</span></span>

<span data-ttu-id="6047c-107">Разрешения на доступ, необходимые для вашего приложения, зависят от выполняемых им действий.</span><span class="sxs-lookup"><span data-stu-id="6047c-107">The access permissions required for your application depend on the actions it performs.</span></span> <span data-ttu-id="6047c-108">Дополнительные сведения о разрешениях, необходимых для каждой функции, см. в описании этой функции в разделе [функции политики LSA](management-functions.md).</span><span class="sxs-lookup"><span data-stu-id="6047c-108">For details about the permissions required for each function, see the description of that function in [LSA Policy Functions](management-functions.md).</span></span>

<span data-ttu-id="6047c-109">Если вызов [**лсаопенполици**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy) успешно выполнен, он возвращает маркер объекта [**политики**](policy-object.md) для указанной системы.</span><span class="sxs-lookup"><span data-stu-id="6047c-109">If the call to [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy) is successful, it returns a handle to the [**Policy**](policy-object.md) object for the specified system.</span></span> <span data-ttu-id="6047c-110">Затем приложение передает этот обработчик в последующие вызовы функции политики LSA.</span><span class="sxs-lookup"><span data-stu-id="6047c-110">Your application then passes this handle in subsequent LSA Policy function calls.</span></span> <span data-ttu-id="6047c-111">Когда приложению больше не требуется этот обработчик, он должен вызвать [**лсаклосе**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose) , чтобы освободить его.</span><span class="sxs-lookup"><span data-stu-id="6047c-111">When your application no longer needs the handle, it should call [**LsaClose**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose) to free it.</span></span>

<span data-ttu-id="6047c-112">В следующем примере показано, как открыть обработчик объекта [**политики**](policy-object.md) .</span><span class="sxs-lookup"><span data-stu-id="6047c-112">The following example shows how to open a [**Policy**](policy-object.md) object handle.</span></span>


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



<span data-ttu-id="6047c-113">В предыдущем примере приложение запросило политику \_ все \_ [*права*](/windows/desktop/SecGloss/p-gly)доступа.</span><span class="sxs-lookup"><span data-stu-id="6047c-113">In the preceding example, the application requested POLICY\_ALL\_ACCESS [*privileges*](/windows/desktop/SecGloss/p-gly).</span></span> <span data-ttu-id="6047c-114">Дополнительные сведения о том, какие разрешения приложение должно запрашивать при вызове [**лсаопенполици**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy), см. в описании функций, в которые приложение будет передавать дескриптор объекта [**политики**](policy-object.md) .</span><span class="sxs-lookup"><span data-stu-id="6047c-114">For details about which permissions your application should request when calling [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy), see the descriptions of the functions that your application will pass the [**Policy**](policy-object.md) object handle to.</span></span>

<span data-ttu-id="6047c-115">Чтобы открыть маркер для объекта [**политики**](policy-object.md) доверенного домена, вызовите [**лсакреатетрустеддомаинекс**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacreatetrusteddomainex) (для создания нового отношения доверия с доменом) или вызовите [**лсаопентрустеддомаинбинаме**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaopentrusteddomainbyname) (для доступа к существующему доверенному домену).</span><span class="sxs-lookup"><span data-stu-id="6047c-115">To open a handle to the [**Policy**](policy-object.md) object of a trusted domain, call [**LsaCreateTrustedDomainEx**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacreatetrusteddomainex) (to create a new trust relationship with a domain) or call [**LsaOpenTrustedDomainByName**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaopentrusteddomainbyname) (to access an existing trusted domain).</span></span> <span data-ttu-id="6047c-116">Обе эти функции устанавливают указатель на [**\_ обработчик LSA**](lsa-handle.md), который затем можно указать в последующих вызовах функции политики LSA.</span><span class="sxs-lookup"><span data-stu-id="6047c-116">Both of these functions set a pointer to an [**LSA\_HANDLE**](lsa-handle.md), which you can then specify in subsequent LSA Policy function calls.</span></span> <span data-ttu-id="6047c-117">Как и в случае с [**лсаопенполици**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy), приложение должно вызывать [**лсаклосе**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose) , когда больше не требуется обращаться к объекту **политики** доверенного домена.</span><span class="sxs-lookup"><span data-stu-id="6047c-117">As with [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy), your application should call [**LsaClose**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose) when it no longer needs the handle to the trusted domain's **Policy** object.</span></span>

 

 
