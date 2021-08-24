---
description: типы данных для методов защищенного служба хранилища.
ms.assetid: 4d494326-6d0f-4a12-83a2-3c3dd3ca9c1b
title: Типы PStore (PStore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6def89ea4beb5d27a98cb8e6f44fc12271de7d1642b236f31f4979ed26b54a44
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119538454"
---
# <a name="pstore-types"></a>Типы PStore

\[защищенные служба хранилища (Pstore) доступны для использования в Windows Server 2003 и Windows XP. она доступна только для операций чтения в Windows Server 2008 и Windows Vista, но может быть недоступна в последующих версиях. PStore использует старую реализацию защиты данных. Разработчикам настоятельно рекомендуется использовать преимущества более надежной защиты данных, предоставляемые функциями [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) и [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

типы данных для методов защищенного служба хранилища.


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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>PStore. h</dt> </dl> |



 

 
