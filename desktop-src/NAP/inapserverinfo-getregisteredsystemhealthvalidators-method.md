---
title: Метод Инапсерверинфо Жетрегистередсистемхеалсвалидаторс (Напсерверманажемент. h)
description: Извлекает список зарегистрированных SHV.
ms.assetid: 029c7d5c-b397-415c-a530-0096de1ef771
keywords:
- Метод Жетрегистередсистемхеалсвалидаторс NAP
- Метод Жетрегистередсистемхеалсвалидаторс NAP, интерфейс Инапсерверинфо
- Инапсерверинфо интерфейса NAP, метод Жетрегистередсистемхеалсвалидаторс
topic_type:
- apiref
api_name:
- INapServerInfo.GetRegisteredSystemHealthValidators
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54e096d706107ca812e569e46c980f56cdc7b8eba14f4742530f632570fd3d08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118133949"
---
# <a name="inapserverinfogetregisteredsystemhealthvalidators-method"></a>Метод Инапсерверинфо:: Жетрегистередсистемхеалсвалидаторс

> [!Note]  
> Платформа защиты доступа к сети недоступна начиная с Windows 10

 

Метод **инапсерверинфо:: жетрегистередсистемхеалсвалидаторс** извлекает список зарегистрированных SHV.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetRegisteredSystemHealthValidators(
  [out] SystemHealthEntityCount      *count,
  [out] NapComponentRegistrationInfo **validators,
  [out] CLSID                        **validatorClsids
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*количество* \[ заполняет\]
</dt> <dd>

Указатель на [**системхеалсентитикаунт**](nap-type-constants.md) , содержащий число зарегистрированных SHV.

</dd> <dt>

*проверяющие элементы управления* \[ заполняет\]
</dt> <dd>

Указатель на указатель на структуру [**напкомпонентрегистратионинфо**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) , содержащую сведения о регистрации SHV.

</dd> <dt>

*валидаторклсидс* \[ заполняет\]
</dt> <dd>

Указатель на массив идентификаторов зарегистрированных SHV.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Также могут возвращаться другие коды ошибок, относящиеся к COM.



| Код возврата                                                                                     | Описание                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**С \_ ОК**</dt> </dl>           | Операция успешно завершена.<br/>                                    |
| <dl> <dt>**Д \_ ACCESSDENIED**</dt> </dl> | Ошибка разрешений, доступ запрещен.<br/>                       |
| <dl> <dt>**Д \_ OUTOFMEMORY**</dt> </dl>  | Не удалось выполнить операцию из – за пределов системных ресурсов.<br/> |



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                          |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                               |
| Заголовок<br/>                   | <dl> <dt>Напсерверманажемент. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Напсерверманажемент. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qsvrmgmt.dll</dt> </dl>            |



## <a name="see-also"></a>См. также

<dl> <dt>

[**напкомпонентрегистратионинфо**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo)
</dt> <dt>

[**инапсерверинфо**](inapserverinfo.md)
</dt> </dl>

 

 





