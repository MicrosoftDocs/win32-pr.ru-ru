---
title: IWMPSettings2 Рекуестмедиаакцессригхтс, метод
description: Метод Рекуестмедиаакцессригхтс запрашивает указанный уровень доступа к библиотеке. | IWMPSettings2 Рекуестмедиаакцессригхтс, метод
ms.assetid: ea33852c-d1e0-45cf-8954-2a1e2fe51910
keywords:
- проигрыватель Windows Media метода рекуестмедиаакцессригхтс
- проигрыватель Windows Media метода рекуестмедиаакцессригхтс, интерфейс IWMPSettings2
- проигрыватель Windows Media интерфейса IWMPSettings2, метод рекуестмедиаакцессригхтс
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
ms.openlocfilehash: aba44540717059945f273be23d2e3c63b3c10cfc6d21d35ee1c4756ea1503708
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118568491"
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

## <a name="remarks"></a>Remarks

Веб-страница должна сначала запросить у пользователя разрешение на чтение информации из библиотеки или запись данных в нее. При вызове этого метода пользователю предлагается диалоговое окно, запрашивающее указанный уровень разрешений. Это означает, что определенные методы, свойства и события будут недоступны из кода, если соответствующие права доступа не были предоставлены. Текущий уровень прав доступа можно получить с помощью **IWMPSettings2. медиаакцессригхтс**.

Для использования этого метода приложения, работающие на компьютере пользователя, не требуются.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                      |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс IWMPSettings2 (VB и C#)**](iwmpsettings2--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. Медиаакцессригхтс (VB и C#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





