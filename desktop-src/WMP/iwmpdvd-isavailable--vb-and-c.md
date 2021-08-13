---
title: ИВМПДВД. доступ (VB и C)
description: Свойство Available (метод Get- \_ Available в C \) возвращает значение, указывающее, доступен ли указанный тип сведений, или может быть выполнено указанное действие.
ms.assetid: 55690783-df2f-473d-a6f2-a4907b7e8a78
keywords:
- ивмпдвд. доступ (VB и C) проигрыватель Windows Media
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
ms.openlocfilehash: c78c9dda7bff764752dc55524000ccd3695863afe69dcf45c2ed971c9c0373fd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119415930"
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

## <a name="remarks"></a>Remarks

функции dvd проигрыватель Windows Media не будут работать на компьютерах, на которых не установлен декодер DVD. Можно определить, доступен ли декодер, вызвав свойство **Available** (метод **Get- \_ Available** в C#) и передав значение **System. String** "двддекодер".

Каждый DVD-диск создан по-другому. Методы, доступные во время воспроизведения DVD-диска и навигации, зависят от способа создания DVD-диска.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                      |
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

 

 





