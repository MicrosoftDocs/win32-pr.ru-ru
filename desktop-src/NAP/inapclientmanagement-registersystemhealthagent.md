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
ms.openlocfilehash: 581c49a117a2b8aaa2c4dda2c6573e4a6327b688
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491709"
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



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                               |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                         |
| Header<br/>                   | <dl> <dt>Напманажемент. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Напманажемент. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>        |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**инапклиентманажемент**](inapclientmanagement.md)
</dt> </dl>

 

 





