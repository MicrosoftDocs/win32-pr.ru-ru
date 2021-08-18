---
description: Происходит при перемещении пера на дигитайзер.
ms.assetid: 67d55dbc-6119-45d9-8016-a2a59f5f04ea
title: 'Итаблетевентсинк: метод:P аккетс'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.Packets
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 29b118771fb5217ed13c01ef9376ad9b426e1ecd74a4bf931d8412a0b47e913b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119712124"
---
# <a name="itableteventsinkpackets-method"></a>Итаблетевентсинк: метод:P аккетс

Происходит при перемещении пера на дигитайзер.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Packets(
  [in] TABLET_CONTEXT_ID tcid,
  [in] ULONG             cPkts,
  [in] ULONG             cbPkts,
  [in] BYTE              *pbPkts,
  [in] ULONG             *pnSerialNumbers,
       t                 cid
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*тЦид* \[ окне\]
</dt> <dd>

Идентификатор планшета.

</dd> <dt>

*кпктс* \[ окне\]
</dt> <dd>

Число пакетов.

</dd> <dt>

*кбпктс* \[ окне\]
</dt> <dd>

Размер буфера пакета

</dd> <dt>

*пбпктс* \[ окне\]
</dt> <dd>

Буфер пакетов.

</dd> <dt>

*пнсериалнумберс* \[ окне\]
</dt> <dd>

Массив серийных номеров.

</dd> <dt>

*согласуется* 
</dt> <dd>

Идентификатор пера.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод может возвращать одно из этих значений.



| Код возврата                                                                            | Описание                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>   | Успешно.<br/>                       |
| <dl> <dt>**\_Ошибка E**</dt> </dl> | Произошла неизвестная ошибка.<br/> |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                              |
| Библиотека<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Итаблетевентсинк**](itableteventsink.md)
</dt> </dl>

 

 




