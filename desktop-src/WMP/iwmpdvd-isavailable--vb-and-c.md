---
title: ИВМПДВД. доступ (VB и C)
description: Свойство Available (метод Get- \_ Available в C \) возвращает значение, указывающее, доступен ли указанный тип сведений, или может быть выполнено указанное действие.
ms.assetid: 55690783-df2f-473d-a6f2-a4907b7e8a78
keywords:
- Проигрыватель Windows Media ИВМПДВД. Available (VB и C)
topic_type:
- apiref
api_name:
- IWMPDVD.isAvailable (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e3409da619f337b61606baaf546cebbb438087c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689110"
---
# <a name="iwmpdvdisavailable-vb-and-c"></a>ИВМПДВД. доступ (VB и C#)

Свойство **Available** (метод Get- **\_ Available** в C#) возвращает значение, указывающее, доступен ли указанный тип сведений, или может быть выполнено указанное действие.


```
[Visual Basic]
ReadOnly Property isAvailable(
  bstrItem As System.String
) As System.Boolean
```




```
[C#]
System.Boolean get_isAvailable (
  System.String bstrItem
)
```



## <a name="parameters"></a>Параметры

*бстритем*

Строка System. String, которая является одним из следующих значений.



| Значение      | Описание                                                                                   |
|------------|-----------------------------------------------------------------------------------------------|
| Назад       | Обнаруживает, доступен ли метод **ивмпдвд. Back** .                                   |
| оптически        | Обнаруживает, загружен ли DVD-диск.                                                          |
| двддекодер | Обнаруживает, установлен ли декодер DVD в системе.                                     |
| resume     | Обнаруживает, доступен ли метод **ивмпдвд. Resume** .                                 |
| титлемену  | Обнаруживает, доступен ли метод **ивмпдвд. титлемену** .                              |
| топмену    | Обнаруживает, доступен ли метод **ивмпдвд. топмену** . Обычно называется корневым меню. |



 

## <a name="property-value"></a>Значение свойства

**System.Boolean**

Значение **System. Boolean** , указывающее, доступен ли указанный тип сведений, или может быть выполнено указанное действие.

## <a name="remarks"></a>Комментарии

Возможности DVD проигрывателя Windows Media не будут работать на компьютерах, на которых не установлен декодер DVD. Можно определить, доступен ли декодер, вызвав свойство **Available** (метод **Get- \_ Available** в C#) и передав значение **System. String** "двддекодер".

Каждый DVD-диск создан по-другому. Методы, доступные во время воспроизведения DVD-диска и навигации, зависят от способа создания DVD-диска.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | Проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                      |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс ИВМПДВД (VB и C#)**](iwmpdvd--vb-and-c.md)
</dt> <dt>

[**ИВМПДВД. Back (VB и C#)**](wmplibiwmpdvd-iwmpdvd-back--vb-and-c.md)
</dt> <dt>

[**ИВМПДВД. Resume (VB и C#)**](wmplibiwmpdvd-iwmpdvd-resume--vb-and-c.md)
</dt> <dt>

[**ИВМПДВД. Титлемену (VB и C#)**](wmplibiwmpdvd-iwmpdvd-titlemenu--vb-and-c.md)
</dt> <dt>

[**ИВМПДВД. Топмену (VB и C#)**](wmplibiwmpdvd-iwmpdvd-topmenu--vb-and-c.md)
</dt> </dl>

 

 





