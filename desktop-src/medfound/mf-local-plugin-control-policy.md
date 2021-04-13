---
description: Задает локальную политику управления подключаемым модулем.
ms.assetid: 2936F3C9-3BCB-452A-8C03-35D73A200CE2
title: Атрибут MF_LOCAL_PLUGIN_CONTROL_POLICY (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd1bdaee17651cebfdc844bb5b6998907b1cd295
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647735"
---
# <a name="mf_local_plugin_control_policy-attribute"></a>\_ \_ \_ Атрибут политики управления локальным подключаемым модулем MF \_

Задает локальную политику управления подключаемым модулем.

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="remarks"></a>Комментарии

Присвойте этому атрибуту одно из [**значений \_ \_ \_ политики управления подключаемым модулем MF**](/windows/desktop/api/mfobjects/ne-mfobjects-mf_plugin_control_policy) .

Эти атрибуты позволяют приложению указать более ограниченную локальную политику по сравнению с политикой уровня процесса, настроенной [**имфплугинконтрол**](/windows/desktop/api/mfobjects/nn-mfobjects-imfplugincontrol).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                         |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                               |
| Header<br/>                   | <dl> <dt>Мфидл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Атрибуты типа мультимедиа](media-type-attributes.md)
</dt> </dl>

 

 




