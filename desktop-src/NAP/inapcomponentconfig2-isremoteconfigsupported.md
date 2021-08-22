---
title: Метод INapComponentConfig2 Исремотеконфигсуппортед (Напкоммон. h)
description: Реализуется с помощью средств проверки работоспособности системы (SHV), чтобы указать, поддерживается ли удаленная конфигурация.
ms.assetid: c4b8e60b-ed60-49ec-b4d6-4e1575e4d1a5
keywords:
- Метод Исремотеконфигсуппортед NAP
- Метод Исремотеконфигсуппортед NAP, интерфейс INapComponentConfig2
- INapComponentConfig2 интерфейса NAP, метод Исремотеконфигсуппортед
topic_type:
- apiref
api_name:
- INapComponentConfig2.IsRemoteConfigSupported
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a42ae316063fc14054c8ffeb6e3987794bc33021441621ee231c9e839fc00248
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118621771"
---
# <a name="inapcomponentconfig2isremoteconfigsupported-method"></a>Метод INapComponentConfig2:: Исремотеконфигсуппортед

> [!Note]  
> Платформа защиты доступа к сети недоступна начиная с Windows 10

 

Метод **исремотеконфигсуппортед** реализуется средствами проверки работоспособности системы (SHV), чтобы указать, поддерживается ли удаленная конфигурация.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IsRemoteConfigSupported(
  [out] BOOL  *isSupported,
  [out] UINT8 *remoteConfigType
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*поддерживается* \[ заполняет\]
</dt> <dd>

Указатель на логическое значение, равное **true** , если компонент поддерживает удаленную настройку, и **значение false** в противном случае.

</dd> <dt>

*ремотеконфигтипе* \[ заполняет\]
</dt> <dd>

Указывает тип удаленной конфигурации, поддерживаемой с помощью значения из перечисления [**ремотеконфигуратионтипе**](/windows/win32/api/naptypes/ne-naptypes-remoteconfigurationtype) :



| Значение                                                                                                 | Значение                                                                                                                                                                                                                                                                                         |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>ремотеконфигтипемачине</dt> </dl>    | [**Инвокеуиформачине**](inapcomponentconfig2-invokeuiformachine.md) реализован.<br/>                                                                                                                                                                                                |
| <dl> <dt>ремотеконфигтипеконфигблоб</dt> </dl> | [**Инвокеуифромконфигблоб**](inapcomponentconfig2-invokeuifromconfigblob.md) реализован. [**Инапкомпонентконфиг:: config**](inapcomponentconfig-getconfig.md) и [**Инапкомпонентконфиг:: сетконфиг**](inapcomponentconfig-setconfig.md) можно вызывать удаленно с помощью DCOM.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

возвращает значение \_ ок, если успешно, или один из стандартных кодов ошибок Windows.

## <a name="remarks"></a>Remarks

Если ни [**инвокеуиформачине**](inapcomponentconfig2-invokeuiformachine.md) , ни [**инвокеуифромконфигблоб**](inapcomponentconfig2-invokeuifromconfigblob.md) не реализованы, удаленная настройка SHV невозможна.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Напкоммон. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Напкоммон. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**INapComponentConfig2**](inapcomponentconfig2.md)
</dt> </dl>

 

 





