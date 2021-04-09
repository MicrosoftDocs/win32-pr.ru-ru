---
title: Метод INapComponentConfig3 Делетеаллконфиг (Напкоммон. h)
description: Реализуется средствами проверки работоспособности системы (SHV) для предоставления способа сброса хранилища SHV в исходное состояние после установки.
ms.assetid: 7f079743-1c32-430d-a250-b49a96b99f14
keywords:
- Метод Делетеаллконфиг NAP
- Метод Делетеаллконфиг NAP, интерфейс INapComponentConfig3
- INapComponentConfig3 интерфейса NAP, метод Делетеаллконфиг
topic_type:
- apiref
api_name:
- INapComponentConfig3.DeleteAllConfig
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12a766690114db20fb9be5cccbd4508f4565f2cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891689"
---
# <a name="inapcomponentconfig3deleteallconfig-method"></a>INapComponentConfig3: метод:D Елетеаллконфиг

> [!Note]  
> Платформа защиты доступа к сети недоступна начиная с Windows 10

 

Метод **делетеаллконфиг** реализуется средствами проверки работоспособности системы (SHV) для предоставления способа сброса хранилища SHV в исходное состояние после установки. Все данные конфигурации, кроме конфигурации по умолчанию, должны быть удалены.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT DeleteAllConfig();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает один из следующих кодов ошибок в зависимости от результата этой операции.



| Код возврата                                                                           | Описание                             |
|---------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**С \_ ОК**</dt> </dl> | Операция прошла успешно.<br/> |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2008 R2 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Напкоммон. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Напкоммон. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**INapComponentConfig3**](inapcomponentconfig3.md)
</dt> </dl>

 

 





