---
title: msc_ver Switch
description: Параметр/МСК \_ ver позволяет использовать MIDL для создания кода, который включает оптимизацию для различных версий компиляторов Microsoft C/C++.
ms.assetid: cdcb8f3e-e791-44c2-8bea-e77f94cc1682
keywords:
- /msc_ver параметр MIDL
topic_type:
- apiref
api_name:
- /msc_ver
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3620b3c8ffb1315a4d34eb0b4b2497c1cb3d805
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "103889780"
---
# <a name="msc_ver-switch"></a>\_коммутатор/МСК ver

Параметр **/МСК \_ ver** позволяет использовать MIDL для создания кода, который включает оптимизацию для различных версий компиляторов Microsoft C/C++.

``` syntax
midl /msc_ver version_number
```

## <a name="switch-options"></a>Параметры коммутатора

<dl> <dt>

*\_номер версии* 
</dt> <dd>

Указывает целочисленный номер версии компилятора Microsoft Visual C++, который будет использоваться для компиляции заглушек клиента и сервера распределенного приложения. Номер версии по умолчанию — 1100, соответствующий версии Visual C++ 5,0. Номер версии 1200 соответствует Visual C++ версии 6,0 и т. д.

</dd> </dl>

## <a name="remarks"></a>Комментарии

В частности, значения версии 1100 или выше приводят к тому, что компилятор MIDL создает код, использующий директиву **\_ \_ declspec (UUID ())** . Он также активирует макросы, использующие директивы **\_ \_ declspec (selectany)** и **\_ \_ declspec (vtable)** .

 

 




