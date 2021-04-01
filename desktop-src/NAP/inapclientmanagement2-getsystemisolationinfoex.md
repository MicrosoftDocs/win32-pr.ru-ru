---
title: Метод INapClientManagement2 Жетсистемисолатионинфоекс (Напманажемент. h)
description: Извлекает сведения о состоянии изоляции и расширенном состоянии изоляции Напклиент.
ms.assetid: 614bcf19-873e-4043-98b2-dcb152bae3e2
keywords:
- Метод Жетсистемисолатионинфоекс NAP
- Метод Жетсистемисолатионинфоекс NAP, интерфейс INapClientManagement2
- INapClientManagement2 интерфейса NAP, метод Жетсистемисолатионинфоекс
topic_type:
- apiref
api_name:
- INapClientManagement2.GetSystemIsolationInfoEx
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e75a6554ea7e55c3bebe35b797f888494a55627
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071422"
---
# <a name="inapclientmanagement2getsystemisolationinfoex-method"></a>Метод INapClientManagement2:: Жетсистемисолатионинфоекс

> [!Note]  
> Платформа защиты доступа к сети недоступна начиная с Windows 10

 

Метод **жетсистемисолатионинфоекс** извлекает сведения о состоянии изоляции и расширенном состоянии изоляции напклиент.

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

Указатель на указатель на структуру [**исолатионинфоекс**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) , содержащую сведения о состоянии изоляции.

</dd> <dt>

*ункновнконнектионс* \[ заполняет\]
</dt> <dd>

Указатель на логическое значение, равное **true** , если какое-либо из соединений находится в неизвестном состоянии, и **false** в противном случае.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает код состояния HRESULT, включая, помимо прочего, один из следующих.



| Код возврата                                                                                         | Описание                                                        |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>                | Операция выполнена успешно.<br/>                                   |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>      | Ошибка разрешений, доступ запрещен.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>       | Не удалось выполнить операцию из – за пределов системных ресурсов.<br/> |
| <dl> <dt>**RPC \_ E \_ отключен**</dt> </dl> | Напажент не работает.<br/>                            |



 

## <a name="remarks"></a>Комментарии

Извлеченные сведения о изоляции не отображают неизвестные состояния.

SHA должен освободить структуру [**исолатионинфоекс**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) , вызвав [**фриисолатионинфоекс**](freeisolationinfoex.md).

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

[**INapClientManagement2**](inapclientmanagement2.md)
</dt> </dl>

 

 





