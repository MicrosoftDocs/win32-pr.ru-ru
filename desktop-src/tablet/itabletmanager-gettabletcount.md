---
description: Возвращает число планшетов, подключенных к системе.
ms.assetid: b2027336-611b-4d17-8943-f16770effaf8
title: 'Метод Итаблетманажер:: Жеттаблеткаунт'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletManager.GetTabletCount
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 80d5585a96ebae60885e17dae5ebf1550128d6c5c8db5ae2a35c81c284c10977
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119031882"
---
# <a name="itabletmanagergettabletcount-method"></a>Метод Итаблетманажер:: Жеттаблеткаунт

Возвращает число планшетов, подключенных к системе.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetTabletCount(
  [out] ULONG *pcTablets
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пктаблетс* \[ заполняет\]
</dt> <dd>

Число планшетов, подключенных к системе.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод может возвращать одно из этих значений.



| Код возврата                                                                            | Описание                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>   | Успешно.<br/>                       |
| <dl> <dt>**\_Ошибка E**</dt> </dl> | Произошла неизвестная ошибка.<br/> |



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                              |
| Библиотека<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Интерфейс Итаблетманажер**](itabletmanager.md)
</dt> </dl>

 

 




