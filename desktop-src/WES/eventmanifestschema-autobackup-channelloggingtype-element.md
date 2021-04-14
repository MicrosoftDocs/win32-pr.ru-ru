---
title: Элемент автоархивации (Чаннеллоггингтипе)
description: Определяет, следует ли создавать новый файл журнала, когда текущий файл журнала достигает максимального размера.
ms.assetid: 708c5d44-d20b-437a-a01f-6182b244c736
keywords:
- Журнал событий элемента автоархивации
topic_type:
- apiref
api_name:
- autoBackup
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4d69c1a1c43be9d2376d94f39b3158e167f7bd13
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535462"
---
# <a name="autobackup-channelloggingtype-element"></a>Элемент автоархивации (Чаннеллоггингтипе)

Определяет, следует ли создавать новый файл журнала, когда текущий файл журнала достигает максимального размера.

``` syntax
<xs:element name="autoBackup"
    type="boolean"
 />
```

Элемент **автоархивации** определяется сложным типом [**чаннеллоггингтипе**](eventmanifestschema-channelloggingtype-complextype.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Родительский элемент**
</dt> <dt>

[**ведение журнала (Чаннелтипе)**](eventmanifestschema-logging-channeltype-element.md)
</dt> </dl>

 

 





