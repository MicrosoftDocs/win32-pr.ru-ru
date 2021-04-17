---
description: Структура МАКФРАМЕ — это объединение наиболее распространенных начальных протоколов.
ms.assetid: ec7e3a54-a47f-4390-a137-9574c63c9a11
title: Объединение МАКФРАМЕ (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MACFRAME
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: a7901daf467a63586543c52ca8a214d5d0094982
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662450"
---
# <a name="macframe-union"></a>Объединение МАКФРАМЕ

Структура **макфраме** — это объединение наиболее распространенных начальных протоколов.

## <a name="syntax"></a>Синтаксис


```C++
typedef union {
  LPBYTE      MacHeader;
  LPETHERNET  Ethernet;
  LPTOKENRING Tokenring;
  LPFDDI      Fddi;
} MACFRAME, *LPMACFRAME;
```



## <a name="members"></a>Члены

<dl> <dt>

**мачеадер**
</dt> <dd>

Универсальный указатель на кадр.

</dd> <dt>

**Ethernet**
</dt> <dd>

Указатель Ethernet на кадр.

</dd> <dt>

**токенринг**
</dt> <dd>

Указатель кольца маркера на кадр.

</dd> <dt>

**FDDI**
</dt> <dd>

FDDI-указатель на кадр.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Эта структура чаще всего используется в качестве наложения. Чтобы сделать свойства первого протокола доступными, приведите кадр к тому же типу, что и для протокола.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




