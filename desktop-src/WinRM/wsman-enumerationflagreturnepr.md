---
title: Метод WSMan. Енумератионфлагретурнепр (Всмандисп. h)
description: Возвращает значение флага перечисления Енумератионфлагретурнепр для использования в параметре Flags сеанса. Enumerate.
ms.assetid: 5e168aa9-5be1-46b3-bb9b-59895e68a75d
ms.tgt_platform: multiple
keywords:
- служба удаленного управления Windows метода Енумератионфлагретурнепр
- Служба удаленного управления Windows метода Енумератионфлагретурнепр, объект WSMan
- Объект WSMan служба удаленного управления Windows, метод Енумератионфлагретурнепр
topic_type:
- apiref
api_name:
- WSMan.EnumerationFlagReturnEPR
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 129aca059bcca1b1a6f6729d4df97fbf8617fa52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489105"
---
# <a name="wsmanenumerationflagreturnepr-method"></a>Метод WSMan. Енумератионфлагретурнепр

Метод **енумератионфлагретурнепр** возвращает значение флага перечисления **енумератионфлагретурнепр** для использования в параметре *flags* [**сеанса. Enumerate**](session-enumerate.md). Этот метод предоставляет более эффективный синтаксис для использования константы, поэтому скрипты не должны устанавливать постоянное значение. Дополнительные сведения о вызове этого метода см. в разделе [константы сеанса](session-constants.md).

**Енумератионфлагретурнепр** является константой в перечислении **\_ всманенумфлагс** и описана в разделе [**константы перечисления**](enumeration-constants.md).

## <a name="syntax"></a>Синтаксис


```VB
WSMan.EnumerationFlagReturnEPR( _
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
| Header<br/>                   | <dl> <dt>Всмандисп. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Всмандисп. idl</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>Всмандисп. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Ведущий**](wsman.md)
</dt> <dt>

[**Session**](session.md)
</dt> </dl>

 

 





