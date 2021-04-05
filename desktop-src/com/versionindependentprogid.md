---
title: версиониндепендентпрогид
description: Связывает идентификатор ProgID с идентификатором CLSID. Это значение используется для определения последней версии объектного приложения.
ms.assetid: 5d188db9-ea4f-47fe-882f-a6caa7e86a25
keywords:
- COM раздела реестра Версиониндепендентпрогид
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5774dfa5202521bb5055bab6a62aa7c6a60b3cc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068621"
---
# <a name="versionindependentprogid"></a><span data-ttu-id="88ec1-105">версиониндепендентпрогид</span><span class="sxs-lookup"><span data-stu-id="88ec1-105">VersionIndependentProgID</span></span>

<span data-ttu-id="88ec1-106">Связывает идентификатор ProgID с идентификатором CLSID.</span><span class="sxs-lookup"><span data-stu-id="88ec1-106">Associates a ProgID with a CLSID.</span></span> <span data-ttu-id="88ec1-107">Это значение используется для определения последней версии объектного приложения.</span><span class="sxs-lookup"><span data-stu-id="88ec1-107">This value is used to determine the latest version of an object application.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="88ec1-108">Запись реестра</span><span class="sxs-lookup"><span data-stu-id="88ec1-108">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      VersionIndependentProgID = Program.Component
```

## <a name="remarks"></a><span data-ttu-id="88ec1-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="88ec1-109">Remarks</span></span>

<span data-ttu-id="88ec1-110">Это значение **reg \_ SZ** , которое указывает последнюю версию приложения объекта.</span><span class="sxs-lookup"><span data-stu-id="88ec1-110">This is a **REG\_SZ** value that specifies the latest version of the object application.</span></span>

<span data-ttu-id="88ec1-111">Идентификатор ProgID, не зависящий от версии, хранится и обслуживается исключительно кодом приложения.</span><span class="sxs-lookup"><span data-stu-id="88ec1-111">The version-independent ProgID is stored and maintained solely by application code.</span></span> <span data-ttu-id="88ec1-112">При задании идентификатора ProgID, не зависящего от версии, функция [**клсидфромпрогид**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) возвращает идентификатор CLSID текущей версии.</span><span class="sxs-lookup"><span data-stu-id="88ec1-112">When given the version-independent ProgID, the [**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) function returns the CLSID of the current version.</span></span>

<span data-ttu-id="88ec1-113">Для преобразования между этими двумя представлениями можно использовать [**клсидфромпрогид**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) и [**прогидфромклсид**](/windows/desktop/api/combaseapi/nf-combaseapi-progidfromclsid) .</span><span class="sxs-lookup"><span data-stu-id="88ec1-113">You can use [**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) and [**ProgIDFromCLSID**](/windows/desktop/api/combaseapi/nf-combaseapi-progidfromclsid) to convert between these two representations.</span></span>

 

 




