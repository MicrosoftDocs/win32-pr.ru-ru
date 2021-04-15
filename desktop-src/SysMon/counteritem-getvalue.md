---
title: Каунтеритем. GetValue, метод
description: Извлекает Последнее значение счетчика.
ms.assetid: cf50d878-a119-42b0-bc59-b0e37ed15321
keywords:
- Метод GetValue Сисмон
- Метод GetValue Сисмон, класс Каунтеритем
- Класс Каунтеритем Сисмон, метод GetValue
topic_type:
- apiref
api_name:
- CounterItem.GetValue
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94e40950ce4a8bf24a6a4301db133779b34ce4ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661955"
---
# <a name="counteritemgetvalue-method"></a>Каунтеритем. GetValue, метод

Извлекает Последнее значение счетчика.

## <a name="syntax"></a>Синтаксис


```VB
CounterItem.GetValue( _
  ByRef value As Double, _
  ByRef status As Long _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*значение* \[ заполняет\]
</dt> <dd>

Последнее значение выборки счетчика.

</dd> <dt>

*состояние* \[ заполняет\]
</dt> <dd>

Указывает, является ли значение допустимым.



| Значение                                                                                              | Значение                            |
|----------------------------------------------------------------------------------------------------|------------------------------------|
| <dl> <dt>0</dt> </dl>                       | Значение является допустимым.<br/>     |
| <dl> <dt>0xC0000BBA (3221228474)</dt> </dl> | Недопустимое значение.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Если источником данных счетчика является файл журнала, значение является последним значением счетчика в файле журнала.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                            |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Сисмон. ocx</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**каунтеритем**](counteritem.md)
</dt> <dt>

[**Каунтеритем. статистики**](counteritem-getstatistics.md)
</dt> <dt>

[**Каунтеритем. Value**](counteritem-value.md)
</dt> </dl>

 

 





