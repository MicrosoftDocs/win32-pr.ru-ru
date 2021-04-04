---
title: ResourceLocator. Аддселектор, метод (Всмандисп. h)
description: Добавляет селектор в объект ResourceLocator. Селектор указывает конкретный экземпляр ресурса.
ms.assetid: 4b513d39-a377-487f-a03b-f3c5ab0f0b5a
ms.tgt_platform: multiple
keywords:
- служба удаленного управления Windows метода Аддселектор
- Служба удаленного управления Windows метода Аддселектор, объект ResourceLocator
- Служба удаленного управления Windows объекта ResourceLocator, метод Аддселектор
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
ms.openlocfilehash: 064108f535c9f46dc074d1b37754e626dc3f1d40
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988703"
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

## <a name="remarks"></a>Комментарии

**Ивсманресаурцелокатор:: аддселектор** — соответствующий метод C++.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                 |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                           |
| Header<br/>                   | <dl> <dt>Всмандисп. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Всмандисп. idl</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>Всмандисп. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ResourceLocator**](resourcelocator.md)
</dt> </dl>

 

 





