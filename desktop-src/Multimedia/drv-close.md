---
title: Сообщение DRV_CLOSE (Ммсистем. h)
description: Указывает драйверу закрыть заданный экземпляр. Если другие экземпляры не открыты, драйвер должен подготовиться к последующему выпуску из памяти.
ms.assetid: 98d7fe47-5194-4912-a9d6-3af3d1fa4e60
keywords:
- DRV_CLOSE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- DRV_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a205b7e6edb4a427b0e80d32cc711d9bf2b052c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105650398"
---
# <a name="drv_close-message"></a>\_Сообщение о закрытии DRV

Указывает драйверу закрыть заданный экземпляр. Если другие экземпляры не открыты, драйвер должен подготовиться к последующему выпуску из памяти.

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*двдриверид*
</dt> <dd>

Идентификатор устанавливаемого драйвера. Это то же значение, которое ранее было возвращено драйвером [**из \_ открытого сообщения DRV**](drv-open.md) .

</dd> <dt>

<span id="hdrvr"></span><span id="HDRVR"></span>*хдрвр*
</dt> <dd>

Описатель устанавливаемого экземпляра драйвера.

</dd> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

32-разрядное значение, заданное в качестве параметра *lParam1* в вызове функции **дриверклосе** .

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

32-разрядное значение, заданное в качестве параметра *lParam2* в вызове функции **дриверклосе** .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает ненулевое значение в случае успеха или ноль в противном случае.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                                |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                      |
| Заголовок<br/>                   | <dl> <dt>Ммсистем. h (включение Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Устанавливаемые драйверы](installable-drivers.md)
</dt> <dt>

[Устанавливаемые сообщения драйверов](installable-driver-messages.md)
</dt> </dl>

 

 





