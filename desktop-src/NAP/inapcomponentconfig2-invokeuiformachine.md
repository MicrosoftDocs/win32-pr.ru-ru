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
ms.openlocfilehash: 6bc0c09f802a63a5bfad92b49f76fcbb4ee242d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135774"
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

Возвращает значение \_ ОК, если успешно, или один из стандартных кодов ошибок Windows.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Напкоммон. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Напкоммон. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**INapComponentConfig2**](inapcomponentconfig2.md)
</dt> </dl>

 

 





