---
title: Методы свойств Иадспринтжобоператионс (iAds. h)
description: Методы свойств интерфейса Иадспринтжобоператионс считывают и записывают свойства, перечисленные в следующей таблице. Дополнительные сведения о методах свойств см. в разделе методы свойств интерфейса.
ms.assetid: d1710bd4-e600-4d92-892a-16b4316851d4
ms.tgt_platform: multiple
keywords:
- Методы свойств Иадспринтжобоператионс ADSI
topic_type:
- apiref
api_name:
- IADsPrintJobOperations Property Methods
- IADsPrintJobOperations.Status
- IADsPrintJobOperations.get_Status
- IADsPrintJobOperations.TimeElapsed
- IADsPrintJobOperations.get_TimeElapsed
- IADsPrintJobOperations.PagesPrinted
- IADsPrintJobOperations.get_PagesPrinted
- IADsPrintJobOperations.Position
- IADsPrintJobOperations.get_Position
- IADsPrintJobOperations.put_Position
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70f337681cb7e75a478000bd06daaac1165edaaaf1cb4255b2890347fbcff7de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118691073"
---
# <a name="iadsprintjoboperations-property-methods"></a>Методы свойств Иадспринтжобоператионс

Методы свойств интерфейса [**иадспринтжобоператионс**](/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations) считывают и записывают свойства, перечисленные в следующей таблице. Дополнительные сведения о методах свойств см. в разделе [методы свойств интерфейса](interface-property-methods.md).

## <a name="properties"></a>Свойства

<dl> <dt>

**пажеспринтед**
</dt> <dd> <dl>

Содержит число напечатанных страниц.

<dt>

Тип доступа: только для чтения
</dt> <dt>

Тип данных скрипта: **Long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PagesPrinted(
  [out] LONG* plPagesPrinted
);
```


</dt> </dl> </dd> <dt>

**Позиция**
</dt> <dd> <dl>

Содержит расположение этого задания печати в очереди печати.

<dt>

Тип доступа: чтение и запись
</dt> <dt>

Тип данных скрипта: **Long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Position(
  [out] LONG* plPosition
);
HRESULT put_Position(
  [in] LONG lPosition
);
```


</dt> </dl> </dd> <dt>

**Состояние**
</dt> <dd> <dl>

Содержит текущее состояние задания печати, как указано одним из значений [**констант состояния задания печати ADSI**](adsi-print-job-status-constants.md) .

<dt>

Тип доступа: только для чтения
</dt> <dt>

Тип данных скрипта: **Long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Status(
  [out] LONG* plStatus
);
```


</dt> </dl> </dd> <dt>

**тимилапсед**
</dt> <dd> <dl>

Содержит число миллисекунд, прошедших с момента запуска задания печати.

<dt>

Тип доступа: только для чтения
</dt> <dt>

Тип данных скрипта: **Long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_TimeElapsed(
  [out] LONG* plTimeElapsed
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a>Примеры

В следующем примере кода показано, как можно использовать свойства для [**иадспринтжобоператионс**](/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations) .


```VB
Dim pqo As IADsPrintQueueOperations
Dim pjo As IADsPrintJobOperations

On Error GoTo Cleanup

Set pqo = GetObject("WinNT://aMachine/aPrinter")
For Each pj In pqo.PrintJobs
    Set pjo = pj
    MsgBox pjo.PagesPrinted & " pages printed for job " & pj.Name
    If (pjo.position > 1) Then
        pjo.Position = pjo.status - 1
    End If
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set pqo = Nothing
    Set pjo = Nothing
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                  |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                            |
| Header<br/>                   | <dl> <dt>IAds. h</dt> </dl>         |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl>   |
| IID<br/>                      | IID \_ иадспринтжобоператионс определен как 32FB6780-1ED0-11CF-A988-00AA006BC149<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**иадспринтжоб**](/windows/desktop/api/Iads/nn-iads-iadsprintjob)
</dt> <dt>

[**иадспринтжобоператионс**](/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations)
</dt> <dt>

[**иадспринткуеуе**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)
</dt> <dt>

[**Константы состояния задания печати ADSI**](adsi-print-job-status-constants.md)
</dt> </dl>

 

 





