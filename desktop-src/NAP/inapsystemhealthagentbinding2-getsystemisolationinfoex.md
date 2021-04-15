---
title: Метод INapSystemHealthAgentBinding2 Жетсистемисолатионинфоекс (Напсистемхеалсажент. h)
description: Вызывается SHA для определения состояния изоляции системы и расширенного состояния изоляции.
ms.assetid: 237e5539-889c-457d-8db0-bf3379f28b85
keywords:
- Метод Жетсистемисолатионинфоекс NAP
- Метод Жетсистемисолатионинфоекс NAP, интерфейс INapSystemHealthAgentBinding2
- INapSystemHealthAgentBinding2 интерфейса NAP, метод Жетсистемисолатионинфоекс
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding2.GetSystemIsolationInfoEx
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2643d62afba1a35ebd96b8b39ea2fcf90397576
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534319"
---
# <a name="inapsystemhealthagentbinding2getsystemisolationinfoex-method"></a>Метод INapSystemHealthAgentBinding2:: Жетсистемисолатионинфоекс

> [!Note]  
> Платформа защиты доступа к сети недоступна начиная с Windows 10

 

Метод **INapSystemHealthAgentBinding2:: жетсистемисолатионинфоекс** вызывается SHA для определения состояния изоляции системы и расширенного состояния изоляции.

> [!Note]  
> Используйте [**инапсистемхеалсажентбиндинг:: жетсистемисолатионинфо**](inapsystemhealthagentbinding-getsystemisolationinfo-method.md) , чтобы определить только состояние изоляции системы.

 

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetSystemIsolationInfoEx(
  [out] IsolationInfoEx **isolationInfo,
  [out] BOOL            *unknownConnections
) const;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*исолатионинфо* \[ заполняет\]
</dt> <dd>

Указатель на указатель на структуру [**исолатионинфоекс**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) , содержащий Расширенное состояние изоляции системы для известных соединений. *исолатионинфо* указывает, находится ли система в состоянии ограниченного доступа, надзор или неограниченный доступ, а также информации [**екстендедисолатионстате**](/windows/win32/api/naptypes/ne-naptypes-extendedisolationstate) .

</dd> <dt>

*ункновнконнектионс* \[ заполняет\]
</dt> <dd>

Указатель на **логическое** значение, равное **true** , если какие-либо соединения находятся в неизвестном состоянии, и **false** в противном случае.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Также могут возвращаться другие коды ошибок, относящиеся к COM.



| Код возврата                                                                                             | Описание                                                                                                                    |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**С \_ ОК**</dt> </dl>                   | Операция успешно завершена.<br/>                                                                                                |
| <dl> <dt>**Д \_ ACCESSDENIED**</dt> </dl>         | Ошибка разрешений, доступ запрещен.<br/>                                                                                   |
| <dl> <dt>**Д \_ OUTOFMEMORY**</dt> </dl>          | Не удалось выполнить операцию из – за пределов системных ресурсов.<br/>                                                             |
| <dl> <dt>**Защита доступа к сети \_ E \_ не \_ инициализирована**</dt> </dl> | SHA не был инициализирован ранее.<br/>                                                                        |
| <dl> <dt>**RPC \_ E \_ отключен**</dt> </dl>     | Напажент остановлен. После перезапуска этот объект будет автоматически восстановлен и повторно привязан к Напажент.<br/> |



 

## <a name="remarks"></a>Комментарии

SHA должен освободить структуру [**исолатионинфоекс**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) , вызвав [**фриисолатионинфоекс**](freeisolationinfoex.md).

SHA должен вызвать метод [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) перед вызовом этого метода или любого другого метода интерфейса [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                                      |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                                |
| Header<br/>                   | <dl> <dt>Напсистемхеалсажент. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Напсистемхеалсажент. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md)
</dt> </dl>

 

 





