---
description: Типы данных для методов защищенного хранилища.
ms.assetid: 4d494326-6d0f-4a12-83a2-3c3dd3ca9c1b
title: Типы PStore (PStore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f1c93af4ae6756a6489b828c50bac505241bdd3d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648742"
---
# <a name="pstore-types"></a>Типы PStore

\[Защищенное хранилище (PStore) доступно для использования в Windows Server 2003 и Windows XP. Она доступна только для операций чтения в Windows Server 2008 и Windows Vista, но может быть недоступна в последующих версиях. PStore использует старую реализацию защиты данных. Разработчикам настоятельно рекомендуется использовать преимущества более надежной защиты данных, предоставляемые функциями [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) и [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Типы данных для методов защищенного хранилища.


```C++
typedef DWORD PST_ACCESSMODE;
typedef DWORD PST_ACCESSCLAUSETYPE;
typedef DWORD PST_KEY;
```



<dl> <dt>

**PST-файл \_ ACCESSMODE**
</dt> <dd>

Определяет режим чтения или записи правила доступа.

</dd> <dt>

**PST-файл \_ акцессклаусетипе**
</dt> <dd>

Определяет тип предложения правила доступа.

</dd> <dt>

**\_ключ PST**
</dt> <dd>

Определяет ключ для хранимого элемента.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>PStore. h</dt> </dl> |



 

 
