---
description: Идентификатор индекса, к которому будет осуществляться доступ в базе данных.
ms.assetid: 559e73bf-91c2-4dbf-a667-e5c0431aaffa
title: индексид
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79b6ef6b79dd19183f575930e9793a6ab2f1f5cb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142157"
---
# <a name="indexid"></a>индексид

Идентификатор индекса, к которому будет осуществляться доступ в базе данных.


```C++
typedef DWORD INDEXID;
```



## <a name="remarks"></a>Комментарии

**Индексид** может быть целочисленным значением, представляющим индекс, или следующим значением:

<dl> <dt>

<span id="INDEXID_NULL___INDEXID_-1_"></span><span id="indexid_null___indexid_-1_"></span>ИНДЕКСИД \_ null ((индексид)-1)
</dt> <dd>

Недопустимый **индексид**.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**сдбдеклареиндекс**](sdbdeclareindex.md)
</dt> <dt>

[**сдбстартиндексинг**](sdbstartindexing.md)
</dt> <dt>

[**сдбстопиндексинг**](sdbstopindexing.md)
</dt> </dl>

 

 




