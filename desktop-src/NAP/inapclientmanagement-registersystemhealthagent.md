---
title: Метод Инапклиентманажемент Регистерсистемхеалсажент (Напманажемент. h)
description: Регистрирует SHA в системе защиты доступа к сети.
ms.assetid: 37acfd11-8282-42ba-ae02-9a45c4509b8b
keywords:
- Метод Регистерсистемхеалсажент NAP
- Метод Регистерсистемхеалсажент NAP, интерфейс Инапклиентманажемент
- Инапклиентманажемент интерфейса NAP, метод Регистерсистемхеалсажент
topic_type:
- apiref
api_name:
- INapClientManagement.RegisterSystemHealthAgent
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52e028e1f3dab17fb154ad1676acbf14fe1a31ce69a8f4c511e7f1447d2303bd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119803154"
---
# <a name="inapclientmanagementregistersystemhealthagent-method"></a>Метод Инапклиентманажемент:: Регистерсистемхеалсажент

> [!Note]  
> Платформа защиты доступа к сети недоступна начиная с Windows 10

 

Метод **регистерсистемхеалсажент** регистрирует SHA в системе защиты доступа к сети.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT RegisterSystemHealthAgent(
  [in] const NapComponentRegistrationInfo *agent
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Агент* \[ окне\]
</dt> <dd>

Указатель на структуру [**напкомпонентрегистратионинфо**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) , содержащую сведения о регистрации SHA.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает код состояния HRESULT, включая, помимо прочего, один из следующих.



| Код возврата                                                                                            | Описание                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>                   | Операция выполнена успешно.<br/>                                   |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>         | Ошибка разрешений, доступ запрещен.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>          | Не удалось выполнить операцию из – за пределов системных ресурсов.<br/> |
| <dl> <dt>**\_ \_ конфликтующий идентификатор NAP \_ E**</dt> </dl> | SHA, использующий этот идентификатор, уже зарегистрирован.<br/>         |



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                               |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                         |
| Заголовок<br/>                   | <dl> <dt>Напманажемент. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Напманажемент. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>        |



## <a name="see-also"></a>См. также

<dl> <dt>

[**инапклиентманажемент**](inapclientmanagement.md)
</dt> </dl>

 

 





