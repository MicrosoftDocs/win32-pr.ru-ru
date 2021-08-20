---
description: Перевод гостевой службы в состояние запуска.
ms.assetid: 1DC6A5B3-0F91-4AC1-99D5-0E8CF5ED35A2
title: 'Метод Msvm_GuestService:: StartService'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestService.StartService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 52f3f05eef622940e0fb1a9645a66097a8930fac9a236f432d5471c4ee20c208
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050404"
---
# <a name="msvm_guestservicestartservice-method"></a>Мсвм \_ гуестсервице:: StartService, метод

Перевод гостевой службы в состояние запуска.

## <a name="syntax"></a>Синтаксис


```C++
uint32 StartService();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает одно из следующих значений.



| Возвращаемый код и значение                                                                                                                                             | Описание         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|
| <dl> <dt>**Завершено без ошибки**</dt> <dt>0</dt> </dl> | Успешно.<br/> |
| <dl> <dt>**Не поддерживается**</dt> <dt>1</dt> </dl>           |                     |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8.1 \[ только классические приложения\]<br/>                                                            |
| Минимальная версия сервера<br/> | Windows Server 2012 \[Только классические приложения R2\]<br/>                                                 |
| Пространство имен<br/>                | \\\\Корневая \\ виртуализация \\ версии 2<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Мсвм \_ гуестсервице**](msvm-guestservice.md)
</dt> </dl>

 

 




