---
title: IWMPSettings2 Медиаакцессригхтс, свойство
description: Свойство Медиаакцессригхтс возвращает значение, указывающее разрешения, предоставленные в настоящее время для доступа к библиотеке.
ms.assetid: c4289a2c-e343-405d-9bf5-0e97f6617916
keywords:
- Проигрыватель Windows Media для свойства Медиаакцессригхтс
- Медиаакцессригхтс свойство проигрывателя Windows Media Player, интерфейс IWMPSettings2
- Интерфейс IWMPSettings2 Windows Media Player, свойство Медиаакцессригхтс
topic_type:
- apiref
api_name:
- IWMPSettings2.mediaAccessRights
- IWMPSettings2.get_mediaAccessRights
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96cca06b9618767e7748b4b1308ed97860c7c80b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685056"
---
# <a name="iwmpsettings2mediaaccessrights-property"></a>Свойство IWMPSettings2:: Медиаакцессригхтс

Свойство **медиаакцессригхтс** возвращает значение, указывающее разрешения, предоставленные в настоящее время для доступа к библиотеке.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```CSharp
public System.String mediaAccessRights {get;}
```


```VB

Public ReadOnly Property mediaAccessRights As System.String
```





## <a name="property-value"></a>Значение свойства

**Строка System. String** , которая является одним из следующих значений.



| Значение | Описание                      |
|-------|----------------------------------|
| нет  | Только права доступа к текущему элементу. |
| read  | Права доступа только для чтения.         |
| переполненные  | Права доступа для чтения и записи.        |



 

## <a name="remarks"></a>Комментарии

Веб-страница должна сначала запросить у пользователя разрешение на чтение информации из библиотеки или запись данных в нее. Это означает, что определенные методы, свойства и события будут недоступны из кода, если соответствующие права доступа не были предоставлены. Для получения прав доступа приложение вызывает **IWMPSettings2. Get \_ рекуестмедиаакцессригхтс**, передавая параметр, указывающий требуемый уровень прав доступа.

Приложения, работающие на компьютере пользователя, всегда имеют права полного доступа.

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

[**IWMPSettings2. Рекуестмедиаакцессригхтс (VB и C#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





