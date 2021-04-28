---
description: MF_MT_FSSourceTypeDecoded атрибут — указывает, может ли декодер использовать отметки времени декодирования (DTS) при установке меток времени.
title: MF_MT_FSSourceTypeDecoded
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3799c11e3b921427ff4a3b05aa3d7f47e297ba14
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093092"
---
# <a name="mf_mt_fssourcetypedecoded-attribute"></a>\_Атрибут MF MT \_ фссаурцетипедекодед

Указывает, что тип носителя является декодированным.

## <a name="data-type"></a>Тип данных

**Bool** , сохраненный как **UINT32**


## <a name="remarks"></a>Remarks
Тип мультимедиа помечен атрибутом, указывающим, что он не существует в физическом источнике и синтезирован конвейером. Значение 1 (TRUE) указывает, что тип носителя является синтезированным. Значение 0 (FALSE) или значение отсутствует, указывает, что это не так.

В текущем выпуске этот атрибут должен быть указан с использованием следующего значения GUID, а не MD_MT_FSSourceTypeDecoded константы:

```ea031a62-8bbb-43c5-b5c4-572d2d231c18```


## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Приложения UWP для классических приложений Windows 8 \|\]<br/>                                  |
| Минимальная версия сервера<br/> | \[Приложения UWP для классических приложений Windows Server 2012 \|\]<br/>                        |



## <a name="see-also"></a>См. также

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




