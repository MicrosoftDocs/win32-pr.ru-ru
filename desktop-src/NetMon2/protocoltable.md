---
description: Структура ПРОТОКОЛТАБЛЕ содержит список протоколов.
ms.assetid: dad2b228-5916-44fe-b78e-ebc6507dc555
title: Структура ПРОТОКОЛТАБЛЕ (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROTOCOLTABLE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: a30d890fa5b6dcbbca1797a53722b97b2109cc9943ce07260c7f47514cfeb7b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120036984"
---
# <a name="protocoltable-structure"></a>Структура ПРОТОКОЛТАБЛЕ

Структура **протоколтабле** содержит список протоколов.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _PROTOCOLTABLE {
  DWORD     nProtocols;
  HPROTOCOL hProtocol[1];
} PROTOCOLTABLE;
```



## <a name="members"></a>Члены

<dl> <dt>

**нпротоколс**
</dt> <dd>

Число включенных протоколов.

</dd> <dt>

**хпротокол**
</dt> <dd>

Массив дескрипторов для включенных протоколов.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




