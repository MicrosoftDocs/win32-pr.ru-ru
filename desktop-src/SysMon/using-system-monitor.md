---
title: Использование системного монитора
description: Системный монитор (СИСМОН) может быть добавлен в любое приложение, которое поддерживает ActiveX \ 174; элементы управления. Например, можно включить СИСМОН в приложение Microsoft Visual Basic или в HTML-документ.
ms.assetid: 36931aae-b608-42d9-a3e3-09784e80f386
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abd636c8b984f7c891c2222b4674dd8d0d7e747d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105661585"
---
# <a name="using-system-monitor"></a>Использование системного монитора

Системный монитор (СИСМОН) может включаться в любое приложение, которое поддерживает элементы управления ActiveX®. Например, можно включить СИСМОН в приложение Microsoft Visual Basic или в HTML-документ.

В следующем примере показано, как включить СИСМОН в HTML-документ. В примере используется сценарий VBScript для добавления счетчиков, значения которых извлекаются с локального компьютера, изменения некоторых свойств СИСМОН, управляющих отображением монитора, и обработки события Онкаунтерадд. В примере используется символ-шаблон ( \* ) для добавления всех экземпляров счетчика процесса.

``` syntax
<HTML>
<BODY BGCOLOR=#C0C0C0>

<SCRIPT LANGUAGE="VBScript">
  Sub Monitor_OnCounterAdded(index)
    Monitor.Counters.Item(1).Width = 8
  End Sub
</Script>
<OBJECT
  CLASSID="clsid:C4D2D8E0-D1DD-11CE-940F-008029004347"
  ID="Monitor"
  HEIGHT=80%
  WIDTH=100%>
</OBJECT>

<SCRIPT LANGUAGE="VBScript">
  Sub Window_OnLoad
    On Error Resume Next
    Monitor.ShowValueBar = False
    Monitor.ShowHorizontalGrid = True
    Monitor.Counters.Add("\Process(*)\% Processor Time")
    Monitor.DisplayType=sysmonLineGraph
    Monitor.GraphTitle="System Performance Overview"
  End Sub
</SCRIPT>

</BODY>
</HTML>
```

 

 




