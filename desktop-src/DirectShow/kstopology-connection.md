---
description: Этот раздел относится к пакету обновления 2 (SP2) для Windows XP или более поздней версии. \_Структура подключения кстопологи описывает соединение узла в фильтре потоковой передачи (KS). Узел можно подключить к другому узлу в фильтре или к закрепления фильтра.
ms.assetid: 8fca47b7-4c52-46db-809c-77a0e3414276
title: Структура KSTOPOLOGY_CONNECTION (KS. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KSTOPOLOGY_CONNECTION
api_type:
- HeaderDef
api_location:
- Ks.h
ms.openlocfilehash: f523d378a54311845781c144b33e131d5875e41e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689078"
---
# <a name="kstopology_connection-structure"></a>\_Структура подключения кстопологи

Этот раздел относится к пакету обновления 2 (SP2) для Windows XP или более поздней версии.

Структура **\_ подключения кстопологи** описывает соединение узла в фильтре потоковой передачи (KS). Узел можно подключить к другому узлу в фильтре или к закрепления фильтра.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct {
  ULONG FromNode;
  ULONG FromNodePin;
  ULONG ToNode;
  ULONG ToNodePin;
} KSTOPOLOGY_CONNECTION, *PKSTOPOLOGY_CONNECTION;
```



## <a name="members"></a>Члены

<dl> <dt>

**фромноде**
</dt> <dd>

Индекс вышестоящего узла в соединении. Если вышестоящее соединение является ПИН-кодом, а не узлом, значением является КСФИЛТЕР \_ node.

</dd> <dt>

**фромнодепин**
</dt> <dd>

Если значение поля **фромноде** равно ксфилтер \_ Node, то в этом поле указывается индекс вышестоящего ПИН-кода. В противном случае это поле игнорируется.

</dd> <dt>

**тоноде**
</dt> <dd>

Индекс подчиненного узла в соединении. Если подчиненное соединение является ПИН-кодом, а не узлом, то значением является КСФИЛТЕР \_ node.

</dd> <dt>

**тонодепин**
</dt> <dd>

Если значение поля **тоноде** равно ксфилтер \_ Node, то в этом поле указывается индекс подчиненного ПИН-кода. В противном случае это поле игнорируется.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>KS. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры DirectShow](directshow-structures.md)
</dt> <dt>

[**Икстопологинфо:: Get \_ ConnectionInfo**](/previous-versions/windows/desktop/api/Vidcap/nf-vidcap-ikstopologyinfo-get_connectioninfo)
</dt> </dl>

 

 




