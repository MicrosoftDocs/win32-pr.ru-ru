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
ms.openlocfilehash: e2981fcdd8043c0eb0ee8b05cfd0331fe3abfabe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892365"
---
# <a name="iadsprintjoboperations-property-methods"></a><span data-ttu-id="bf492-105">Методы свойств Иадспринтжобоператионс</span><span class="sxs-lookup"><span data-stu-id="bf492-105">IADsPrintJobOperations Property Methods</span></span>

<span data-ttu-id="bf492-106">Методы свойств интерфейса [**иадспринтжобоператионс**](/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations) считывают и записывают свойства, перечисленные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="bf492-106">The property methods of the [**IADsPrintJobOperations**](/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations) interface read and write the properties listed in the following table.</span></span> <span data-ttu-id="bf492-107">Дополнительные сведения о методах свойств см. в разделе [методы свойств интерфейса](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="bf492-107">For more information about property methods, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="bf492-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="bf492-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="bf492-109">**пажеспринтед**</span><span class="sxs-lookup"><span data-stu-id="bf492-109">**PagesPrinted**</span></span>
<span data-ttu-id="bf492-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="bf492-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="bf492-111">Содержит число напечатанных страниц.</span><span class="sxs-lookup"><span data-stu-id="bf492-111">Contains the number of pages printed.</span></span>

<dt>

<span data-ttu-id="bf492-112">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bf492-112">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf492-113">Тип данных скрипта: **Long**</span><span class="sxs-lookup"><span data-stu-id="bf492-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PagesPrinted(
  [out] LONG* plPagesPrinted
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf492-114">**Позиция**</span><span class="sxs-lookup"><span data-stu-id="bf492-114">**Position**</span></span>
<span data-ttu-id="bf492-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="bf492-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="bf492-116">Содержит расположение этого задания печати в очереди печати.</span><span class="sxs-lookup"><span data-stu-id="bf492-116">Contains the position of this print job in the print queue.</span></span>

<dt>

<span data-ttu-id="bf492-117">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="bf492-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="bf492-118">Тип данных скрипта: **Long**</span><span class="sxs-lookup"><span data-stu-id="bf492-118">Scripting data type: **LONG**</span></span>
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

<span data-ttu-id="bf492-119">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="bf492-119">**Status**</span></span>
<span data-ttu-id="bf492-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="bf492-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="bf492-121">Содержит текущее состояние задания печати, как указано одним из значений [**констант состояния задания печати ADSI**](adsi-print-job-status-constants.md) .</span><span class="sxs-lookup"><span data-stu-id="bf492-121">Contains the current status of the print job as indicated by one of the [**ADSI Print Job Status Constants**](adsi-print-job-status-constants.md) values.</span></span>

<dt>

<span data-ttu-id="bf492-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bf492-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf492-123">Тип данных скрипта: **Long**</span><span class="sxs-lookup"><span data-stu-id="bf492-123">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Status(
  [out] LONG* plStatus
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf492-124">**тимилапсед**</span><span class="sxs-lookup"><span data-stu-id="bf492-124">**TimeElapsed**</span></span>
<span data-ttu-id="bf492-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="bf492-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="bf492-126">Содержит число миллисекунд, прошедших с момента запуска задания печати.</span><span class="sxs-lookup"><span data-stu-id="bf492-126">Contains the number of milliseconds elapsed since the print job started.</span></span>

<dt>

<span data-ttu-id="bf492-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bf492-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf492-128">Тип данных скрипта: **Long**</span><span class="sxs-lookup"><span data-stu-id="bf492-128">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_TimeElapsed(
  [out] LONG* plTimeElapsed
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="bf492-129">Примеры</span><span class="sxs-lookup"><span data-stu-id="bf492-129">Examples</span></span>

<span data-ttu-id="bf492-130">В следующем примере кода показано, как можно использовать свойства для [**иадспринтжобоператионс**](/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations) .</span><span class="sxs-lookup"><span data-stu-id="bf492-130">The following code example shows how the properties for [**IADsPrintJobOperations**](/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations) may be used.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="bf492-131">Требования</span><span class="sxs-lookup"><span data-stu-id="bf492-131">Requirements</span></span>



| <span data-ttu-id="bf492-132">Требование</span><span class="sxs-lookup"><span data-stu-id="bf492-132">Requirement</span></span> | <span data-ttu-id="bf492-133">Значение</span><span class="sxs-lookup"><span data-stu-id="bf492-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf492-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bf492-134">Minimum supported client</span></span><br/> | <span data-ttu-id="bf492-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bf492-135">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="bf492-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bf492-136">Minimum supported server</span></span><br/> | <span data-ttu-id="bf492-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bf492-137">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="bf492-138">Header</span><span class="sxs-lookup"><span data-stu-id="bf492-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf492-139"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf492-139"><dt>Iads.h</dt></span></span> </dl>         |
| <span data-ttu-id="bf492-140">DLL</span><span class="sxs-lookup"><span data-stu-id="bf492-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf492-141"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf492-141"><dt>Activeds.dll</dt></span></span> </dl>   |
| <span data-ttu-id="bf492-142">IID</span><span class="sxs-lookup"><span data-stu-id="bf492-142">IID</span></span><br/>                      | <span data-ttu-id="bf492-143">IID \_ иадспринтжобоператионс определен как 32FB6780-1ED0-11CF-A988-00AA006BC149</span><span class="sxs-lookup"><span data-stu-id="bf492-143">IID\_IADsPrintJobOperations is defined as 32FB6780-1ED0-11CF-A988-00AA006BC149</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bf492-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bf492-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf492-145">**иадспринтжоб**</span><span class="sxs-lookup"><span data-stu-id="bf492-145">**IADsPrintJob**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsprintjob)
</dt> <dt>

[<span data-ttu-id="bf492-146">**иадспринтжобоператионс**</span><span class="sxs-lookup"><span data-stu-id="bf492-146">**IADsPrintJobOperations**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations)
</dt> <dt>

[<span data-ttu-id="bf492-147">**иадспринткуеуе**</span><span class="sxs-lookup"><span data-stu-id="bf492-147">**IADsPrintQueue**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)
</dt> <dt>

[<span data-ttu-id="bf492-148">**Константы состояния задания печати ADSI**</span><span class="sxs-lookup"><span data-stu-id="bf492-148">**ADSI Print Job Status Constants**</span></span>](adsi-print-job-status-constants.md)
</dt> </dl>

 

 





