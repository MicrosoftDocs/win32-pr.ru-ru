---
title: Получение SDO пользователя
description: Получение SDO пользователя
ms.assetid: 440628f8-081b-4e7f-bdb2-760ff9bd0d77
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfcb5fa88f8febc210e21d223f8dd9e455478311026f2c1fac202f2a5781f161
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128574"
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



## <a name="related-topics"></a>Связанные темы

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

 

 