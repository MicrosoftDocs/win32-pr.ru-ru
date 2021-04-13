---
description: Объект Свбеммесод. parameters создается и предоставляется с данными с помощью метода поставщика, который исполняется.
ms.assetid: fc06d6a1-770a-4f34-affd-f5035dad9360
ms.tgt_platform: multiple
title: Синтаксический анализ объектов параметров
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5458ae3c5d57e9984fceef55de278ed92eba520
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348895"
---
# <a name="parsing-outparameters-objects"></a>Синтаксический анализ объектов параметров

Объект [**свбеммесод. parameters**](swbemmethod-outparameters.md) создается и предоставляется с данными с помощью метода поставщика, который исполняется. Свойства объекта **Parameters** относятся к методу, который называется. Например, в приведенном ниже скрипте *SD* (содержащийся в *параметре*) является выходным параметром, определенным для метода **\_ \_ системсекурити. Возвращает** . Свойство **ReturnValue** является универсальным свойством, доступным для всех объектов **параметров** , которые содержат результат операции.

В следующем примере кода показано получение выходных параметров из выполнения полученного [**метода в**](--systemsecurity-getsd.md) классе [**\_ \_ системсекурити**](--systemsecurity.md) для локальной системы.


```VB
' Connect to WMI root\cimv2 namespace.
Set svc = GetObject("winmgmts:root/cimv2")
' Execute the GetSD method and obtain the output parameters.
set outParam = svc.Execmethod("__SystemSecurity=@", "GetSD")
wscript.echo outparam.ReturnValue
' Format the security descriptor array
' in the SD parameter into one string to display.
objSD  = Join(outparam.SD,",")
wscript.echo objSD
' Release the out parameters object.
set outParam = nothing
```



Дополнительные сведения см. в разделе [**свбеммесод. parameters**](swbemmethod-inparameters.md).

 

 



