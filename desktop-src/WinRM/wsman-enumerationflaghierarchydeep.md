---
title: Метод WSMan. Енумератионфлагхиерарчидип (Всмандисп. h)
description: Возвращает значение флага перечисления Енумератионфлагхиерарчидип для использования в параметре Flags сеанса. Enumerate.
ms.assetid: b84b82fa-0b2e-418e-850f-6d7a4749fdc1
ms.tgt_platform: multiple
keywords:
- служба удаленного управления Windows метода енумератионфлагхиерарчидип
- служба удаленного управления Windows метода енумератионфлагхиерарчидип, объект WSMan
- объект WSMan служба удаленного управления Windows, метод енумератионфлагхиерарчидип
topic_type:
- apiref
api_name:
- WSMan.EnumerationFlagHierarchyDeep
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38ccd7aa4884a916a9b8ae8d364679263fa0b217dccef1065c58c332678b9f07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742597"
---
# <a name="wsmanenumerationflaghierarchydeep-method"></a>Метод WSMan. Енумератионфлагхиерарчидип

Метод **енумератионфлагхиерарчидип** возвращает значение флага перечисления **енумератионфлагхиерарчидип** для использования в параметре *flags* [**сеанса. Enumerate**](session-enumerate.md). Этот метод предоставляет более эффективный синтаксис для использования константы, поэтому скрипты не должны устанавливать постоянное значение. Дополнительные сведения о вызове этого метода см. в разделе [константы сеанса](session-constants.md).

**Енумератионфлагхиерарчидип** является константой в перечислении **\_ всманенумфлагс** и описана в разделе [**константы перечисления**](enumeration-constants.md).

## <a name="syntax"></a>Синтаксис


```VB
WSMan.EnumerationFlagHierarchyDeep( _
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

## <a name="requirements"></a>Requirements (Требования)



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

[**Ведущий**](wsman.md)
</dt> <dt>

[**Сеанс**](session.md)
</dt> </dl>

 

 





