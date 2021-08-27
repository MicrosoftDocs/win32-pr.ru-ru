---
title: ResourceLocator. Аддселектор, метод (Всмандисп. h)
description: Добавляет селектор в объект ResourceLocator. Селектор указывает конкретный экземпляр ресурса.
ms.assetid: 4b513d39-a377-487f-a03b-f3c5ab0f0b5a
ms.tgt_platform: multiple
keywords:
- служба удаленного управления Windows метода аддселектор
- служба удаленного управления Windows метода аддселектор, объект ResourceLocator
- служба удаленного управления Windows объекта ResourceLocator, метод аддселектор
topic_type:
- apiref
api_name:
- ResourceLocator.AddSelector
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fc59aab6e5194716fa3b0cda98bb874d0045011c0159c5caaa3cbd53e7fbfd5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121644"
---
# <a name="resourcelocatoraddselector-method"></a>ResourceLocator. Аддселектор, метод

Добавляет [*селектор*](windows-remote-management-glossary.md) в объект [**ResourceLocator**](resourcelocator.md) . Селектор указывает конкретный экземпляр *ресурса*. Можно предоставить объект [**ResourceLocator**](resourcelocator.md) вместо указания URI ресурса в операциях объекта [**сеанса**](session.md) , таких как [**Session. Get**](session-get.md), [**Session.**](session-put.md)WHERE или [**Session. Enumerate**](session-enumerate.md).

## <a name="syntax"></a>Синтаксис


```VB
ResourceLocator.AddSelector( _
  ByVal resourceSelName, _
  ByVal selValue _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ресаурцеселнаме* \[ окне\]
</dt> <dd>

Имя селектора. Например, при запросе данных WMI этот параметр является ключевым свойством класса WMI.

</dd> <dt>

*селвалуе* \[ окне\]
</dt> <dd>

Значение селектора. Например, для данных WMI этот параметр содержит значение для ключевого свойства, идентифицирующего конкретный экземпляр.

</dd> </dl>

## <a name="remarks"></a>Remarks

**Ивсманресаурцелокатор:: аддселектор** — соответствующий метод C++.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                 |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                           |
| Заголовок<br/>                   | <dl> <dt>Всмандисп. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Всмандисп. idl</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>Всмандисп. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[**ResourceLocator**](resourcelocator.md)
</dt> </dl>

 

 





