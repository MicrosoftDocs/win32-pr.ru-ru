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
# <a name="retrieving-a-user-sdo"></a>Получение SDO пользователя

Следующий код получает объект данных сервера (SDO) для администратора.


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



## <a name="related-topics"></a>См. также

<dl> <dt>

[Присоединение к SDO-Enabled компьютеру](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer)
</dt> <dt>

[**исдо**](/windows/desktop/api/sdoias/nn-sdoias-isdo)
</dt> <dt>

[**исдомачине**](/windows/desktop/api/sdoias/nn-sdoias-isdomachine)
</dt> <dt>

[**Исдомачине:: Жетусерсдо**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getusersdo)
</dt> <dt>

[**сисаллокстринг**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring)
</dt> <dt>

[**сисфристринг**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring)
</dt> </dl>

 

 