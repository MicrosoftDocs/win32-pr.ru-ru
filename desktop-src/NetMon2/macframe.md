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
ms.openlocfilehash: dcff7294d2800e797b43b3a05bd25c35418c6fb466c95130b97be73f25040d3a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118364712"
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

## <a name="remarks"></a>Remarks

Эта структура чаще всего используется в качестве наложения. Чтобы сделать свойства первого протокола доступными, приведите кадр к тому же типу, что и для протокола.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




