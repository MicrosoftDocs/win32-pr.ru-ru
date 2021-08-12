---
description: В следующем списке перечислены возможные значения поля flags в записи управления доступом WMI (ACE).
ms.assetid: bd09691d-e285-40e0-8686-edd5a132a06e
ms.tgt_platform: multiple
title: Константы флагов пространства имен ACE (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OBJECT_INHERIT_ACE
- CONTAINER_INHERIT_ACE
- NO_PROPAGATE_INHERIT_ACE
- INHERIT_ONLY_ACE
- INHERITED_ACE
api_type:
- HeaderDef
api_location:
- Winnt.h
ms.openlocfilehash: 7b4051a6c17e9861d656207335b2543cf7d886e74569c269df2a4f680f47fbe3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118555184"
---
# <a name="namespace-ace-flag-constants"></a>Константы флагов пространства имен ACE

В следующем списке перечислены возможные значения поля **flags** в записи управления доступом WMI (ACE).

<dl> <dt>

<span id="OBJECT_INHERIT_ACE"></span><span id="object_inherit_ace"></span>**Объект \_ наследует \_ ACE**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



Дочерние объекты, не являющиеся контейнерами, наследуют ACE как эффективный элемент ACE.


</dt> </dl> </dd> <dt>

<span id="CONTAINER_INHERIT_ACE"></span><span id="container_inherit_ace"></span>**КОНТЕЙНЕР \_ наследует \_ ACE**
</dt> <dd> <dl> <dt>

2 (0x2)
</dt> <dt>



ACE влияет на дочерние пространства имен, а также на текущее пространство имен.


</dt> </dl> </dd> <dt>

<span id="NO_PROPAGATE_INHERIT_ACE"></span><span id="no_propagate_inherit_ace"></span>**НЕТ \_ распространения \_ наследования \_ ACE**
</dt> <dd> <dl> <dt>

4 (0x4)
</dt> <dt>



ACE применяется только к текущему пространству имен и непосредственным дочерним элементам.


</dt> </dl> </dd> <dt>

<span id="INHERIT_ONLY_ACE"></span><span id="inherit_only_ace"></span>**наследовать \_ только \_ ACE**
</dt> <dd> <dl> <dt>

8 (0x8)
</dt> <dt>



ACE применяется только к дочерним пространствам имен.


</dt> </dl> </dd> <dt>

<span id="INHERITED_ACE"></span><span id="inherited_ace"></span>**УНАСЛЕДОВАНный \_ элемент ACE**
</dt> <dd> <dl> <dt>

16 (0x10)
</dt> <dt>



Это значение не задается клиентами, но сообщается клиентам, если источником ACE является родительское пространство имен.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Файл Winnt. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Константы безопасности WMI](wmi-security-constants.md)
</dt> <dt>

[Настройка дескрипторов безопасности Намепаце](setting-namespace-security-descriptors.md)
</dt> <dt>

[Установка наследования безопасности пространства имен](establishing-inheritance-of-namespace-security.md)
</dt> <dt>

[**\_\_SystemSecurity**](--systemsecurity.md)
</dt> </dl>

 

 




