---
title: Метод WSMan. Енумератионфлагретурнобжект (Всмандисп. h)
description: Возвращает значение флага перечисления Енумератионфлагретурнобжект для использования в параметре Flags сеанса. Enumerate.
ms.assetid: a1d82530-63d7-4050-9e82-e31bec93bf38
ms.tgt_platform: multiple
keywords:
- служба удаленного управления Windows метода Енумератионфлагретурнобжект
- Служба удаленного управления Windows метода Енумератионфлагретурнобжект, объект WSMan
- Объект WSMan служба удаленного управления Windows, метод Енумератионфлагретурнобжект
topic_type:
- apiref
api_name:
- WSMan.EnumerationFlagReturnObject
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3019f880503f91d1488a2b7a41574cadc2df987
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105710519"
---
# <a name="wsmanenumerationflagreturnobject-method"></a>Метод WSMan. Енумератионфлагретурнобжект

Метод **WSMan. енумератионфлагретурнобжект** возвращает значение флага перечисления **енумератионфлагретурнобжект** для использования в параметре *flags* [**сеанса. Enumerate**](session-enumerate.md). Этот метод предоставляет более эффективный синтаксис для использования константы, поэтому скрипты не должны устанавливать постоянное значение. Дополнительные сведения о вызове этого метода см. в разделе [константы сеанса](session-constants.md).

**Енумератионфлагретурнобжект** является константой в перечислении **\_ всманенумфлагс** и описана в разделе [**константы перечисления**](enumeration-constants.md).

## <a name="syntax"></a>Синтаксис


```VB
WSMan.EnumerationFlagReturnObject( _
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

 

 





