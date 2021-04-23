---
title: Получение SDO пользователя
description: Получение SDO пользователя
ms.assetid: 440628f8-081b-4e7f-bdb2-760ff9bd0d77
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43c1d6320398afb4eed22f72f0c5e12495010323
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987689"
---
# <a name="retrieving-a-user-sdo"></a><span data-ttu-id="4985b-103">Получение SDO пользователя</span><span class="sxs-lookup"><span data-stu-id="4985b-103">Retrieving a User SDO</span></span>

<span data-ttu-id="4985b-104">Следующий код получает объект данных сервера (SDO) для администратора.</span><span class="sxs-lookup"><span data-stu-id="4985b-104">The following code retrieves a Server Data Object (SDO) for the Administrator.</span></span>


```C++
   HRESULT  hr;
   _bstr_t bstrUserName = L"Administrator";
   CComPtr<IUnknown> pUserUnknown;

   hr = pSdoMachine->GetUserSDO(
      DATA_STORE_LOCAL,
      bstrUserName,
      (IUnknown**) &pUserUnknown
   );
   if (FAILED(hr))
   {
      return hr;
   }

   CComPtr<ISdo> pUserSDO;
   hr = pUserUnknown->QueryInterface(
      __uuidof(ISdo),
      (void**) &pUserSDO
   );
   if (FAILED(hr))
   {
      return hr;
   }
```



## <a name="related-topics"></a><span data-ttu-id="4985b-105">См. также</span><span class="sxs-lookup"><span data-stu-id="4985b-105">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4985b-106">Присоединение к SDO-Enabled компьютеру</span><span class="sxs-lookup"><span data-stu-id="4985b-106">Attaching to an SDO-Enabled Computer</span></span>](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer)
</dt> <dt>

[<span data-ttu-id="4985b-107">**исдо**</span><span class="sxs-lookup"><span data-stu-id="4985b-107">**ISdo**</span></span>](/windows/desktop/api/sdoias/nn-sdoias-isdo)
</dt> <dt>

[<span data-ttu-id="4985b-108">**исдомачине**</span><span class="sxs-lookup"><span data-stu-id="4985b-108">**ISdoMachine**</span></span>](/windows/desktop/api/sdoias/nn-sdoias-isdomachine)
</dt> <dt>

[<span data-ttu-id="4985b-109">**Исдомачине:: Жетусерсдо**</span><span class="sxs-lookup"><span data-stu-id="4985b-109">**ISdoMachine::GetUserSDO**</span></span>](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getusersdo)
</dt> <dt>

[<span data-ttu-id="4985b-110">**сисаллокстринг**</span><span class="sxs-lookup"><span data-stu-id="4985b-110">**SysAllocString**</span></span>](/windows/win32/api/oleauto/nf-oleauto-sysallocstring)
</dt> <dt>

[<span data-ttu-id="4985b-111">**сисфристринг**</span><span class="sxs-lookup"><span data-stu-id="4985b-111">**SysFreeString**</span></span>](/windows/win32/api/oleauto/nf-oleauto-sysfreestring)
</dt> </dl>

 

 