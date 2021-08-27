---
description: MF_MT_FSSourceTypeDecoded атрибут — указывает, может ли декодер использовать отметки времени декодирования (DTS) при установке меток времени.
title: MF_MT_FSSourceTypeDecoded
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ae25fce343d0c24f7b0a79e2623e7c3e2d0f9272b2f95a825860860ff6f88c9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113764"
---
# <a name="mf_mt_fssourcetypedecoded-attribute"></a>\_Атрибут MF MT \_ фссаурцетипедекодед

Указывает, что тип носителя является декодированным.

## <a name="data-type"></a>Тип данных

**Bool** , сохраненный как **UINT32**


## <a name="remarks"></a>Remarks
Тип мультимедиа помечен атрибутом, указывающим, что он не существует в физическом источнике и синтезирован конвейером. Значение 1 (TRUE) указывает, что тип носителя является синтезированным. Значение 0 (FALSE) или значение отсутствует, указывает, что это не так.

В текущем выпуске этот атрибут должен быть указан с использованием следующего значения GUID, а не MD_MT_FSSourceTypeDecoded константы:

```ea031a62-8bbb-43c5-b5c4-572d2d231c18```


## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ приложения UWP для классических приложений \|\]<br/>                                  |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ приложения UWP для классических приложений \|\]<br/>                        |



## <a name="see-also"></a>См. также

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




