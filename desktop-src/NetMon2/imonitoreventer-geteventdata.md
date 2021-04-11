---
description: Метод Жетевентдата выделяет место для структур НМЕВЕНТДАТА и НМКОЛУМНИНФО.
ms.assetid: b24a2a30-4543-4311-87ec-66872463aed7
title: 'Метод Имониторевентер:: Жетевентдата (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitorEventer.GetEventData
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: be1654c38f51fa62909e10c12900c087bf0842fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263011"
---
# <a name="imonitoreventergeteventdata-method"></a>Метод Имониторевентер:: Жетевентдата

Метод **жетевентдата** выделяет место для структур [нмевентдата](nmeventdata.md) и [нмколумнинфо](nmcolumninfo.md) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetEventData(
  [in]  BYTE         bNumColumns,
  [out] PNMEVENTDATA *ppNMEventData
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*бнумколумнс* \[ окне\]
</dt> <dd>

Количество необходимых структур **нмколумнинфо** .

</dd> <dt>

*ппнмевентдата* \[ заполняет\]
</dt> <dd>

Адрес возвращаемой структуры **нмевентдата** .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если метод выполнен успешно, возвращается значение S \_ ОК.

Если метод завершился неудачно, возвращаемое значение НМЕРР не \_ хватает \_ \_ памяти.

## <a name="remarks"></a>Комментарии

Мониторы вызывают этот метод, чтобы выделить память для структур данных событий и сведений о столбцах. Сведения о высвобождении памяти, выделенной для структуры **нмевентдата** , см. в разделе [Имониторевентер:: фриевентдата](imonitoreventer-freeeventdata.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[имониторевентер](imonitoreventer.md)
</dt> <dt>

[Имониторевентер:: Фриевентдата](imonitoreventer-freeeventdata.md)
</dt> <dt>

[нмевентдата](nmeventdata.md)
</dt> <dt>

[нмколумнинфо](nmcolumninfo.md)
</dt> </dl>

 

 




