---
description: Содержит индекс записи и сведения о ТЕГАХ в базе данных оболочек совместимости.
ms.assetid: 2ff58e01-cc47-4612-a3bc-a87ccb343bd2
title: TAGID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd4c65183170c7304bf05a670b1eadb3a5953d6f33b1f6415210f12db8898760
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075787"
---
# <a name="tagid"></a>TAGID

Содержит индекс записи и сведения о ТЕГАХ в базе данных оболочек совместимости.


```C++
typedef DWORD TAGID;
```



## <a name="remarks"></a>Remarks

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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**ТЕГАМИ**](tag.md)
</dt> <dt>

[Типы тегов](tag-types.md)
</dt> <dt>

[**тагреф**](tagref.md)
</dt> </dl>

 

 




