---
title: IWMPSettings2 Рекуестмедиаакцессригхтс, метод
description: Метод Рекуестмедиаакцессригхтс запрашивает указанный уровень доступа к библиотеке. | IWMPSettings2 Рекуестмедиаакцессригхтс, метод
ms.assetid: ea33852c-d1e0-45cf-8954-2a1e2fe51910
keywords:
- Рекуестмедиаакцессригхтс метод Windows Media Player
- Рекуестмедиаакцессригхтс метод проигрывателя Windows Media Player, интерфейс IWMPSettings2
- Интерфейс IWMPSettings2 Windows Media Player, метод Рекуестмедиаакцессригхтс
topic_type:
- apiref
api_name:
- IWMPSettings2.requestMediaAccessRights
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c609afffc1d9b228d908d905e0eb1a6ef8741032
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688842"
---
# <a name="iwmpsettings2requestmediaaccessrights-method"></a>Метод IWMPSettings2:: Рекуестмедиаакцессригхтс

Метод **рекуестмедиаакцессригхтс** запрашивает указанный уровень доступа к библиотеке.

## <a name="syntax"></a>Синтаксис


```CSharp
public System.Boolean requestMediaAccessRights(
  System.String bstrDesiredAccess
);
```


```VB

Public Function requestMediaAccessRights( _
  ByVal bstrDesiredAccess As System.String _
) As System.Boolean
Implements IWMPSettings2.requestMediaAccessRights
```





## <a name="parameters"></a>Параметры

<dl> <dt>

*бстрдесиредакцесс* \[ окне\]
</dt> <dd>

**Строка System. String** , которая является одним из следующих значений.



| Значение | Описание                      |
|-------|----------------------------------|
| нет  | Только права доступа к текущему элементу. |
| read  | Права доступа только для чтения.         |
| переполненные  | Права доступа для чтения и записи.        |



 

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Значение **System. Boolean** , указывающее, были ли предоставлены запрошенные права доступа.

## <a name="remarks"></a>Комментарии

Веб-страница должна сначала запросить у пользователя разрешение на чтение информации из библиотеки или запись данных в нее. При вызове этого метода пользователю предлагается диалоговое окно, запрашивающее указанный уровень разрешений. Это означает, что определенные методы, свойства и события будут недоступны из кода, если соответствующие права доступа не были предоставлены. Текущий уровень прав доступа можно получить с помощью **IWMPSettings2. медиаакцессригхтс**.

Для использования этого метода приложения, работающие на компьютере пользователя, не требуются.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | Проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                      |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс IWMPSettings2 (VB и C#)**](iwmpsettings2--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. Медиаакцессригхтс (VB и C#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





