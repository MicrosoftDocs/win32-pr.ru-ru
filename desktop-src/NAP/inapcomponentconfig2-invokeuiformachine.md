---
title: Метод INapComponentConfig2 Инвокеуиформачине (Напкоммон. h)
description: Реализуется средствами проверки работоспособности системы (SHV), необходимыми для управления удаленной конфигурацией непосредственно на указанном компьютере. Этот метод запускает пользовательский интерфейс управления конфигурацией.
ms.assetid: 67a6d715-250b-4b8b-9c27-8173926b7bfe
keywords:
- Метод Инвокеуиформачине NAP
- Метод Инвокеуиформачине NAP, интерфейс INapComponentConfig2
- INapComponentConfig2 интерфейса NAP, метод Инвокеуиформачине
topic_type:
- apiref
api_name:
- INapComponentConfig2.InvokeUIForMachine
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8321425cf878bd9b3d8702f73fa464ae069420cd0e59f57e2500151fda01b191
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118940192"
---
# <a name="inapcomponentconfig2invokeuiformachine-method"></a>Метод INapComponentConfig2:: Инвокеуиформачине

> [!Note]  
> Платформа защиты доступа к сети недоступна начиная с Windows 10

 

Метод **инвокеуиформачине** реализуется средствами проверки работоспособности системы (SHV), необходимыми для управления удаленной конфигурацией непосредственно на указанном компьютере. Этот метод запускает пользовательский интерфейс управления конфигурацией.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT InvokeUIForMachine(
  [in] HWND          hwndParent,
  [in] CountedString *machineName
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хвндпарент* \[ окне\]
</dt> <dd>

Маркер родительского окна или окно-владельца. Необходимо указать допустимый описатель окна.

</dd> <dt>

*MachineName* \[ окне\]
</dt> <dd>

Указатель на [**каунтедстринг**](/windows/win32/api/naptypes/ns-naptypes-countedstring) , содержащий имя компьютера клиента NAP.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

возвращает значение \_ ок, если успешно, или один из стандартных кодов ошибок Windows.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                     |
| Заголовок<br/>                   | <dl> <dt>Напкоммон. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Напкоммон. idl</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**INapComponentConfig2**](inapcomponentconfig2.md)
</dt> </dl>

 

 





