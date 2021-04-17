---
title: Перечисление WMDM_FIND_SCOPE
description: '\_ \_ Тип перечисления вмдм Find SCOPE определяет область объекта хранилища.'
ms.assetid: 971f84d5-8383-4b38-a201-b21100b2f37e
keywords:
- WMDM_FIND_SCOPE перечисление Windows Media диспетчер устройств
topic_type:
- apiref
api_name:
- WMDM_FIND_SCOPE
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d6b65489d14a4f1100b1da33238669310a2731f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694603"
---
# <a name="wmdm_find_scope-enumeration"></a>\_Перечисление вмдм поиска \_ области

Тип перечисления **вмдм \_ Find \_ Scope** определяет область объекта хранилища.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum tagWMDM_FIND_SCOPE { 
  WMDM_FIND_SCOPE_GLOBAL,
  WMDM_FIND_SCOPE_IMMEDIATE_CHILDREN
} WMDM_FIND_SCOPE;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="WMDM_FIND_SCOPE_GLOBAL"></span><span id="wmdm_find_scope_global"></span>**ВМДМ \_ найти \_ область \_ Global**
</dt> <dd>

Поиск совпадающего объекта в любом месте на устройстве.

</dd> <dt>

<span id="WMDM_FIND_SCOPE_IMMEDIATE_CHILDREN"></span><span id="wmdm_find_scope_immediate_children"></span>**\_ \_ \_ непосредственные \_ дочерние элементы вмдм поиска области**
</dt> <dd>

Поиск соответствующего объекта в этом хранилище и его дочерних элементах.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Вмдм. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Типы перечислений**](enumeration-types.md)
</dt> </dl>

 

 





