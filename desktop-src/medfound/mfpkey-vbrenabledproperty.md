---
description: Указывает, использует ли кодировщик кодирование с переменной скоростью (VBR).
ms.assetid: e6826802-99b7-4a38-9b58-8a9cb8b753fb
title: Свойство MFPKEY_VBRENABLED (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab9061abcc6ac7d7338b63eb5a7cd1a13ad22bf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908747"
---
# <a name="mfpkey_vbrenabled-property"></a>МФПКЭЙ \_ вбренаблед, свойство

Указывает, использует ли кодировщик кодирование с переменной скоростью (VBR). Чтение и запись.

## <a name="constant-for-ipropertybag"></a>Константа для Ипропертибаг

**g \_ всзвмвквбренаблед**, **g \_ всзвмкпаудиовбрсуппортед**

## <a name="data-type"></a>Тип данных

**Логическое значение VT \_**

## <a name="default-value"></a>Значение по умолчанию

**ВАРИАНТ \_ false**

## <a name="remarks"></a>Комментарии

Это значение должно быть равно **\_ true** для любого из других свойств VBR, используемых кодеком.

После присвоения этому значению **значения \_ true** в звуковом кодировщике типы выходных данных, полученные с помощью метода [**имедиаобжект:: ЖЕТАУТПУТТИПЕ**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype) , имеют тип VBR.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                             |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Вмкодекдсп. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**МФПКЭЙ \_ ограничение \_ перечисления \_ вбркуалити**](mfpkey-constrain-enumerated-vbrqualityproperty.md)
</dt> <dt>

[**МФПКЭЙ \_ желаемый \_ вбркуалити**](mfpkey-desired-vbrqualityproperty.md)
</dt> <dt>

[Свойства Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
