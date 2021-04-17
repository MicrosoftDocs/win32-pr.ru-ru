---
description: Каждое свойство в классе представления должно иметь квалификатор массива строк с именем Пропертисаурцес.
ms.assetid: df89680b-8ea7-4f38-81ba-c4132b944f37
ms.tgt_platform: multiple
title: Квалификатор Пропертисаурцес
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PropertySources
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3809977282a2bdf82d0b51ef8f566541b74fe28a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711371"
---
# <a name="propertysources-qualifier"></a>Квалификатор Пропертисаурцес

Каждое свойство в классе представления должно иметь квалификатор массива строк с именем **пропертисаурцес**. Квалификатор **пропертисаурцес** содержит имя свойства или свойств исходного класса, из которого это свойство класса представления получает данные. Порядок значений в этом массиве соответствует порядку исходных классов, определенных для [квалификатора виевсаурцес](viewsources-qualifier.md). В следующем примере показано, как определить свойство для класса представления объединения, который является объединением класса [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) из двух разных компьютеров:


```mof
[PropertySources{"DeviceID", "DeviceID"},key] String Devname;
```



Первое свойство **DeviceID** соответствует свойству **DeviceID** из класса в первом исходном запросе. Второе свойство **DeviceID** является свойством **DeviceID** из класса во втором исходном запросе.

При определении свойств для классов представлений соединений необходимо определить отдельное свойство представления для каждого свойства исходного класса, если только свойства исходного класса не являются основанием класса представления объединения. В следующем примере создаются свойства в классе представления Join для аналогичных свойств из исходного [**класса \_ принтера Win32**](/windows/desktop/CIMWin32Prov/win32-printer) и исходного класса [**Win32 \_ принтерконфигуратион**](/windows/desktop/CIMWin32Prov/win32-printerconfiguration) :


```mof
[PropertySources{"VerticalResolution", ""}] Uint32 Vres;
[PropertySources{"", "YResolution"}] Uint32 Yres;
```



Если два исходных класса соединены общим свойством, можно определить только одно свойство класса представления, так как значения обоих свойств исходного класса всегда одинаковы. В следующем примере показано, как присоединить [**класс \_ принтера Win32**](/windows/desktop/CIMWin32Prov/win32-printer) и [**\_ принтерконфигуратион Win32**](/windows/desktop/CIMWin32Prov/win32-printerconfiguration) к общему значению свойства:


```mof
[PropertySources{"DeviceId", "DeviceName "}] String Name;
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>       |
| Минимальная версия сервера<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Квалификаторы, относящиеся к поставщику представления**](qualifiers-specific-to-the-view-provider.md)
</dt> </dl>

 

