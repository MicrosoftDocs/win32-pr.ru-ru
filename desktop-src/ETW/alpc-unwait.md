---
description: Этот класс является классом типа событий для событий окончания ожидания ALPC. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: 89a357dd-c217-4b55-994a-4252fa3cae1c
title: Класс ALPC_Unwait
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ALPC_Unwait
- ALPC_Unwait.Status
api_type:
- NA
api_location: ''
ms.openlocfilehash: de6e04fce0f581b3f37e3a049590914b1355d197952c74190457a402e597edcf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901714"
---
# <a name="alpc_unwait-class"></a>Класс "ALPC — \_ Ожидание"

Этот класс является классом типа событий для событий окончания ожидания ALPC.

Следующий синтаксис упрощен из MOF-кода.

## <a name="syntax"></a>Синтаксис

``` syntax
[EventType(37), EventTypeName("ALPC-Unwait")]
class ALPC_Unwait : ALPC
{
  uint32 Status;
};
```

## <a name="members"></a>Члены

Класс **\_ неожиданий в ALPC** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **с \_ неожиданием «ALPC** » имеет следующие свойства.

<dl> <dt>

**Состояние**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Состояние из операции ожидания.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



 

 




