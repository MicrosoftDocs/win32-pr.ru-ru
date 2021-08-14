---
description: этот раздел относится к Windows XP с пакетом обновления 2 (sp2) или более поздней версии. \_Структура подключения кстопологи описывает соединение узла в фильтре потоковой передачи (KS). Узел можно подключить к другому узлу в фильтре или к закрепления фильтра.
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
ms.openlocfilehash: 80a7b6f046edd1cd7f602487a11d6a79c375276814f9374f4142d148699bb8b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118397248"
---
# <a name="kstopology_connection-structure"></a>\_Структура подключения кстопологи

этот раздел относится к Windows XP с пакетом обновления 2 (sp2) или более поздней версии.

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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>KS. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[DirectShow Сотрудник](directshow-structures.md)
</dt> <dt>

[**Икстопологинфо:: Get \_ ConnectionInfo**](/previous-versions/windows/desktop/api/Vidcap/nf-vidcap-ikstopologyinfo-get_connectioninfo)
</dt> </dl>

 

 




