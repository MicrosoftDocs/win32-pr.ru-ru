---
title: Метод WSMan. Енумератионфлагхиерарчидипбасепропсонли (Всмандисп. h)
description: Возвращает значение флага перечисления Енумератионфлагхиерарчидипбасепропсонли для использования в параметре Flags сеанса. Enumerate.
ms.assetid: f4c5966a-0d9f-4d93-9ccd-2e8a5f32b77f
ms.tgt_platform: multiple
keywords:
- служба удаленного управления Windows метода енумератионфлагхиерарчидипбасепропсонли
- служба удаленного управления Windows метода енумератионфлагхиерарчидипбасепропсонли, объект WSMan
- объект WSMan служба удаленного управления Windows, метод енумератионфлагхиерарчидипбасепропсонли
topic_type:
- apiref
api_name:
- WSMan.EnumerationFlagHierarchyDeepBasePropsOnly
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 197c615b8d805fc142fa8afb2cf4fbb56ef22eec76caf63f03c27f3d9f131b82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742462"
---
# <a name="wsmanenumerationflaghierarchydeepbasepropsonly-method"></a>Метод WSMan. Енумератионфлагхиерарчидипбасепропсонли

Метод **WSMan. енумератионфлагхиерарчидипбасепропсонли** возвращает значение флага перечисления **енумератионфлагхиерарчидипбасепропсонли** для использования в параметре *flags* [**сеанса. Enumerate**](session-enumerate.md). Этот метод предоставляет более эффективный синтаксис для использования константы, поэтому скрипты не должны устанавливать постоянное значение. Дополнительные сведения о вызове этого метода см. в разделе [константы сеанса](session-constants.md).

**Енумератионфлагхиерарчидипбасепропсонли** является константой в перечислении **\_ всманенумфлагс** и описана в разделе [**константы перечисления**](enumeration-constants.md).

## <a name="syntax"></a>Синтаксис


```VB
WSMan.EnumerationFlagHierarchyDeepBasePropsOnly( _
  ByRef flags _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Флаги* \[ заполняет\]
</dt> <dd>

Значение константы.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                 |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                           |
| Заголовок<br/>                   | <dl> <dt>Всмандисп. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Всмандисп. idl</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>Всмандисп. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Ведущий**](wsman.md)
</dt> <dt>

[**Сеанс**](session.md)
</dt> </dl>

 

 





