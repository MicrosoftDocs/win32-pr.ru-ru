---
title: Константы перечисления (Всмандисп. h)
description: Перечисление содержит константы, перечисленные в следующем списке, которые используются в параметре Flags путем вызова метода Session. Enumerate и IWSManSession Enumerate.
ms.assetid: c0f2763b-a549-43d5-84a6-8cebf33a1ea2
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- WSManFlagReturnObject
- WSManFlagNonXmlText
- EnumerationFlagReturnEPR
- WSManFlagReturnObjectAndEPR
- WSManFlagHierarchyDeep
- WSManFlagHierarchyShallow
- WSManFlagHierarchyDeepBasePropsOnly
api_location:
- WSManDisp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9c8182352d2ebf3763a38f74dd6f100dc836e88cfa10212ffaa971048ebd1aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118113266"
---
# <a name="enumeration-constants"></a>Константы перечисления

Перечисление **\_ \_ всманенумфлагс** содержит константы, перечисленные в следующем списке, которые используются в параметре *flags* при вызове метода [**Session. Enumerate**](session-enumerate.md) и [**IWSManSession:: Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate).

Имейте в виду, что **всманфлагретурнобжект** и **всманфлагхиерарчидип** являются по умолчанию, если не задан параметр *flags* .

<dl> <dt>

<span id="WSManFlagReturnObject"></span><span id="wsmanflagreturnobject"></span><span id="WSMANFLAGRETURNOBJECT"></span>**всманфлагретурнобжект**
</dt> <dd> <dl> <dt>

0 (0x0)
</dt> <dt>



Пакеты содержат запрошенные экземпляры XML. Это значение по умолчанию для параметра flag.

Связанный метод создания скриптов — это [**WSMan. енумератионфлагретурнобжект**](wsman-enumerationflagreturnobject.md) , а метод C++ — [**ивсманекс. енумератионфлагретурнобжект**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnobject).


</dt> </dl> </dd> <dt>

<span id="WSManFlagNonXmlText"></span><span id="wsmanflagnonxmltext"></span><span id="WSMANFLAGNONXMLTEXT"></span>**всманфлагнонксмлтекст**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



Этот флаг управляет тем, как параметр *фильтра* в вызове к [**Session. Enumerate**](session-enumerate.md) интерпретируется службой WinRM.

Формат фильтра может быть фрагментом XML или строкой обычного текста. Формат определяется [*диалектом фильтра*](windows-remote-management-glossary.md) [*фильтра*](windows-remote-management-glossary.md) , используемого в вызове метода [**Session. Enumerate**](session-enumerate.md) или [**IWSManSession:: Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate), который относится к выполняемой операции.

Если параметр *диалекта* не указан, служба WinRM пытается определить диалект на основе первого символа фильтра. Если первый символ <, но фильтр фактически не является фрагментом XML, то следует установить этот флаг. Например, для фильтра в следующем формате требуется задать **всманфлагнонксмлтекст** , чтобы фильтр был правильно интерпретирован:

`<25 && > 1`

Если фильтр является фрагментом XML, этот флаг не требуется, так как фрагмент начинается с <, который правильно интерпретируется в виде XML. Например,

`<filter>select * from aDataStructure</filter>`

Если фильтр имеет обычный текст, который не начинается с <, этот флаг не является обязательным. Например,

`select * from aDataStructure`

Связанный метод создания скриптов — это [**WSMan. енумератионфлагнонксмлтекст**](wsman-enumerationflagnonxmltext.md) , а метод C++ — [**ивсманекс. енумератионфлагнонксмлтекст**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagnonxmltext).


</dt> </dl> </dd> <dt>

<span id="EnumerationFlagReturnEPR"></span><span id="enumerationflagreturnepr"></span><span id="ENUMERATIONFLAGRETURNEPR"></span>**енумератионфлагретурнепр**
</dt> <dd> <dl> <dt>

2 (0x2)
</dt> <dt>



Пакеты содержат ссылки на конечные точки (Епрс) для соответствующих экземпляров XML, но не сами экземпляры.

Связанный метод создания скриптов — это [**WSMan. енумератионфлагретурнепр**](wsman-enumerationflagreturnepr.md) , а метод C++ — [**ивсманекс. енумератионфлагретурнепр**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnepr).


</dt> </dl> </dd> <dt>

<span id="WSManFlagReturnObjectAndEPR"></span><span id="wsmanflagreturnobjectandepr"></span><span id="WSMANFLAGRETURNOBJECTANDEPR"></span>**всманфлагретурнобжектандепр**
</dt> <dd> <dl> <dt>

4 (0x4)
</dt> <dt>



Пакеты содержат как запрошенные экземпляры XML, так и соответствующие Епрс, содержащиеся в элементе [*WSMan: Items*](windows-remote-management-glossary.md) .

Связанный метод создания скриптов — это [**WSMan. енумератионфлагретурнобжектандепр**](wsman-enumerationflagreturnobjectandepr.md) , а метод C++ — [**ивсманекс. енумератионфлагретурнобжектандепр**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnobjectandepr).


</dt> </dl> </dd> <dt>

<span id="WSManFlagHierarchyDeep"></span><span id="wsmanflaghierarchydeep"></span><span id="WSMANFLAGHIERARCHYDEEP"></span>**всманфлагхиерарчидип**
</dt> <dd> <dl> <dt>

0 (0x0)
</dt> <dt>



Экземпляры производного класса включены и представлены в соответствии с их реальными схемами.

Связанный метод создания скриптов — это [**WSMan. енумератионфлагхиерарчидип**](wsman-enumerationflaghierarchydeep.md) , а метод C++ — [**ивсманекс. енумератионфлагхиерарчидип**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchydeep).


</dt> </dl> </dd> <dt>

<span id="WSManFlagHierarchyShallow"></span><span id="wsmanflaghierarchyshallow"></span><span id="WSMANFLAGHIERARCHYSHALLOW"></span>**всманфлагхиерарчишаллов**
</dt> <dd> <dl> <dt>

32 (0x20)
</dt> <dt>



Экземпляры производного класса исключаются. Отображаются только экземпляры запрошенного типа.

Связанный метод создания скриптов — это [**WSMan. енумератионфлагхиерарчишаллов**](wsman-enumerationflaghierarchyshallow.md) , а метод C++ — [**ивсманекс. енумератионфлагхиерарчишаллов**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchyshallow).


</dt> </dl> </dd> <dt>

<span id="WSManFlagHierarchyDeepBasePropsOnly"></span><span id="wsmanflaghierarchydeepbasepropsonly"></span><span id="WSMANFLAGHIERARCHYDEEPBASEPROPSONLY"></span>**всманфлагхиерарчидипбасепропсонли**
</dt> <dd> <dl> <dt>

64 (0x40)
</dt> <dt>



Экземпляры производного класса включены и представлены в соответствии со схемой базового класса. Свойства, определенные в производном классе, не отображаются.

Связанный метод создания скриптов — это [**WSMan. енумератионфлагхиерарчидипбасепропсонли**](wsman-enumerationflaghierarchydeepbasepropsonly.md) , а метод C++ — [**ивсманекс. енумератионфлагхиерарчидипбасепропсонли**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchydeepbasepropsonly).


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                 |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                           |
| Заголовок<br/>                   | <dl> <dt>Всмандисп. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Всмандисп. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Константы и перечисления WinRM](winrm-constants-and-enumerations.md)
</dt> <dt>

[Перечисление или составление списка всех экземпляров ресурса](enumerating-or-listing-all-instances-of-a-resource.md)
</dt> <dt>

[Запрос конкретных экземпляров ресурса](querying-for-specific-instances-of-a-resource.md)
</dt> </dl>

 

 





