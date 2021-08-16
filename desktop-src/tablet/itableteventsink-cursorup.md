---
description: Происходит, когда пользователь порождает перо из поверхности планшета дигитайзера.
ms.assetid: 34dc7e6b-101a-4edd-8c3c-9aafb85cf58b
title: 'Метод Итаблетевентсинк:: Курсоруп'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.CursorUp
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 586f18750e832bad653a3df92d14efb41b39547ee532913ac52c986a9b5e137c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119712134"
---
# <a name="itableteventsinkcursorup-method"></a>Метод Итаблетевентсинк:: Курсоруп

Происходит, когда пользователь порождает перо из поверхности планшета дигитайзера.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT CursorUp(
  [in] TABLET_CONTEXT_ID tcid,
  [in] CURSOR_ID         cid,
  [in] ULONG             nSerialNumber,
  [in] ULONG             cbPkt,
  [in] BYTE              *pbPkt
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*тЦид* \[ окне\]
</dt> <dd>

Идентификатор планшета.

</dd> <dt>

*CID* \[ в\]
</dt> <dd>

Идентификатор пера.

</dd> <dt>

*нсериалнумбер* \[ окне\]
</dt> <dd>

Серийный номер пера.

</dd> <dt>

*кбпкт* \[ окне\]
</dt> <dd>

Число байтов в пакете данных пера.

</dd> <dt>

*пбпкт* \[ окне\]
</dt> <dd>

Данные пера, указывающие расположение, в котором перо было удалено из планшета.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

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

 

 




