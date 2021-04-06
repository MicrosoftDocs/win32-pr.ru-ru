---
description: Содержит индекс записи и сведения о ТЕГАХ в базе данных оболочек совместимости.
ms.assetid: 2ff58e01-cc47-4612-a3bc-a87ccb343bd2
title: TAGID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e7d8b8a25633d3505936d105b0eef7ed38746ce
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990440"
---
# <a name="tagid"></a>TAGID

Содержит индекс записи и сведения о ТЕГАХ в базе данных оболочек совместимости.


```C++
typedef DWORD TAGID;
```



## <a name="remarks"></a>Комментарии

**TAGID** зависит от базы данных. Это может быть целочисленное значение, представляющее индекс, или одно из следующих значений:

<dl> <dt>

<span id="TAGID_NULL__0_"></span><span id="tagid_null__0_"></span>TAGID \_ null (0)
</dt> <dd>

**TAGID** не существует. Это значение возвращается из функции, если оно не может возвращать допустимый **TAGID**.

</dd> <dt>

<span id="TAGID_ROOT__0_"></span><span id="tagid_root__0_"></span>\_Корневой TAGID (0)
</dt> <dd>

Указывает тег корневого списка, который можно использовать в качестве родителя для получения дочернего **TAGID**.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ТЕГАМИ**](tag.md)
</dt> <dt>

[Типы тегов](tag-types.md)
</dt> <dt>

[**тагреф**](tagref.md)
</dt> </dl>

 

 




