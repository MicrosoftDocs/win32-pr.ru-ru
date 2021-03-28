---
description: Задает точки выбранных в данный момент объектов для объекта данных в командах копирования и вырезания. Используется \_ сообщением шшеллфолдервиев.
title: Сообщение SFVM_SETPOINTS (Шлобж. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: d2c3e06a-19e4-4b78-9b7c-1a256582786e
api_name:
- SFVM_SETPOINTS
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 1df501f162fb19335fcf1672299a74135672db22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272847"
---
# <a name="sfvm_setpoints-message"></a>\_Сообщение сфвм сетпоинтс

Задает точки выбранных в данный момент объектов для объекта данных в командах **копирования** и **вырезания** . Используется [**\_ сообщением шшеллфолдервиев**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).


```C++
SFVM_SETPOINTS 

    lParam = (LPARAM) pdtobj;

            
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пдтобж* \[ окне\]
</dt> <dd>Указатель на <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">**IDataObject**</a> команд **Copy** и **Cut** .</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Всегда возвращает значение 0.

## <a name="remarks"></a>Remarks

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Шлобж. h</dt> </dl> |



 

 
