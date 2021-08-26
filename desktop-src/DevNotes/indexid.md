---
description: Идентификатор индекса, к которому будет осуществляться доступ в базе данных.
ms.assetid: 559e73bf-91c2-4dbf-a667-e5c0431aaffa
title: индексид
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5711f2927462325b2a6479dd9506099da4bd50f9a9a99b68152e5c0030a47d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001894"
---
# <a name="indexid"></a>индексид

Идентификатор индекса, к которому будет осуществляться доступ в базе данных.


```C++
typedef DWORD INDEXID;
```



## <a name="remarks"></a>Remarks

**Индексид** может быть целочисленным значением, представляющим индекс, или следующим значением:

<dl> <dt>

<span id="INDEXID_NULL___INDEXID_-1_"></span><span id="indexid_null___indexid_-1_"></span>ИНДЕКСИД \_ null ((индексид)-1)
</dt> <dd>

Недопустимый **индексид**.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**сдбдеклареиндекс**](sdbdeclareindex.md)
</dt> <dt>

[**сдбстартиндексинг**](sdbstartindexing.md)
</dt> <dt>

[**сдбстопиндексинг**](sdbstopindexing.md)
</dt> </dl>

 

 




