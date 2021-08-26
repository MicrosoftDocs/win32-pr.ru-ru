---
description: Задает локальную политику управления подключаемым модулем.
ms.assetid: 2936F3C9-3BCB-452A-8C03-35D73A200CE2
title: Атрибут MF_LOCAL_PLUGIN_CONTROL_POLICY (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83f32280f48895b9b6a0633613d63f787836573fe13f046126639c28467abe02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119956464"
---
# <a name="mf_local_plugin_control_policy-attribute"></a>\_ \_ \_ Атрибут политики управления локальным подключаемым модулем MF \_

Задает локальную политику управления подключаемым модулем.

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="remarks"></a>Remarks

Присвойте этому атрибуту одно из [**значений \_ \_ \_ политики управления подключаемым модулем MF**](/windows/desktop/api/mfobjects/ne-mfobjects-mf_plugin_control_policy) .

Эти атрибуты позволяют приложению указать более ограниченную локальную политику по сравнению с политикой уровня процесса, настроенной [**имфплугинконтрол**](/windows/desktop/api/mfobjects/nn-mfobjects-imfplugincontrol).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                               |
| Заголовок<br/>                   | <dl> <dt>Мфидл. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Атрибуты типа мультимедиа](media-type-attributes.md)
</dt> </dl>

 

 




