---
description: Возвращает объект SWbemPropertySet, содержащий коллекцию системных свойств WMI, которые применяются к объекту.
ms.assetid: e95c325a-8851-4f55-a99d-4346d064e308
ms.tgt_platform: multiple
title: Свойство SWbemObjectEx.SystemProperties_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectEx.SystemProperties_
- ISWbemObjectEx.SystemProperties_
- ISWbemObjectEx.get_SystemProperties_
- ISWbemObjectEx.put_SystemProperties_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: cf8b7e15536c0d4e3116f0583662b3cd0b7d0887
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272432"
---
# <a name="swbemobjectexsystemproperties_-property"></a><span data-ttu-id="3a5f4-103">SWbemObjectEx.Sys, \_ свойство темпропертиес</span><span class="sxs-lookup"><span data-stu-id="3a5f4-103">SWbemObjectEx.SystemProperties\_ property</span></span>

<span data-ttu-id="3a5f4-104">Свойство **системпропертиес \_** объекта [**свбемобжектекс**](swbemobjectex.md) возвращает объект [**SWbemPropertySet**](swbempropertyset.md) , содержащий коллекцию [системных свойств WMI](wmi-system-properties.md) , которые применяются к объекту.</span><span class="sxs-lookup"><span data-stu-id="3a5f4-104">The **SystemProperties\_** property of the [**SWbemObjectEx**](swbemobjectex.md) object returns an [**SWbemPropertySet**](swbempropertyset.md) object that contains the collection of [WMI System Properties](wmi-system-properties.md) that apply to the object.</span></span>

<span data-ttu-id="3a5f4-105">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="3a5f4-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="3a5f4-106">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="3a5f4-106">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a5f4-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3a5f4-107">Syntax</span></span>


```VB
SWbemObjectEx.SystemProperties_ As Object
```



## <a name="property-value"></a><span data-ttu-id="3a5f4-108">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="3a5f4-108">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="3a5f4-109">Примеры</span><span class="sxs-lookup"><span data-stu-id="3a5f4-109">Examples</span></span>

<span data-ttu-id="3a5f4-110">В следующем примере кода извлекаются значения свойств для \_ класса процесса Win32.</span><span class="sxs-lookup"><span data-stu-id="3a5f4-110">The following code sample retrieves the property values for the Win32\_Process class.</span></span>


```VB
Set objWmi = GetObject ("winmgmts:root\cimv2")
Set objClass = objWmi.Get("Win32_Process")

' SWbemObjectEx.SystemProperties_ returns 
' an SWbemPropertySet object that contains the collection
' of sytem properties for Win32_Process class

For Each objProperty In objClass.SystemProperties_

    WScript.Echo vbCrLf & objProperty.Name & ":"

    ' Have to take into account that
    ' __Derivation is an array

    If Not objProperty.IsArray Then
        WScript.Echo vbTab & objProperty.Value
    Else
        For Each strValue In objProperty.Value
            WScript.Echo vbTab & strValue
        Next
    End If

Next
```



## <a name="requirements"></a><span data-ttu-id="3a5f4-111">Требования</span><span class="sxs-lookup"><span data-stu-id="3a5f4-111">Requirements</span></span>



| <span data-ttu-id="3a5f4-112">Требование</span><span class="sxs-lookup"><span data-stu-id="3a5f4-112">Requirement</span></span> | <span data-ttu-id="3a5f4-113">Значение</span><span class="sxs-lookup"><span data-stu-id="3a5f4-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3a5f4-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3a5f4-114">Minimum supported client</span></span><br/> | <span data-ttu-id="3a5f4-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3a5f4-115">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3a5f4-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3a5f4-116">Minimum supported server</span></span><br/> | <span data-ttu-id="3a5f4-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3a5f4-117">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3a5f4-118">Header</span><span class="sxs-lookup"><span data-stu-id="3a5f4-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a5f4-119"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a5f4-119"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="3a5f4-120">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="3a5f4-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="3a5f4-121"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="3a5f4-121"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="3a5f4-122">DLL</span><span class="sxs-lookup"><span data-stu-id="3a5f4-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a5f4-123"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3a5f4-123"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="3a5f4-124">CLSID</span><span class="sxs-lookup"><span data-stu-id="3a5f4-124">CLSID</span></span><br/>                    | <span data-ttu-id="3a5f4-125">\_СВБЕМОБЖЕКТЕКС CLSID</span><span class="sxs-lookup"><span data-stu-id="3a5f4-125">CLSID\_SWbemObjectEx</span></span><br/>                                                         |
| <span data-ttu-id="3a5f4-126">IID</span><span class="sxs-lookup"><span data-stu-id="3a5f4-126">IID</span></span><br/>                      | <span data-ttu-id="3a5f4-127">IID \_ исвбемобжектекс</span><span class="sxs-lookup"><span data-stu-id="3a5f4-127">IID\_ISWbemObjectEx</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="3a5f4-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3a5f4-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a5f4-129">**свбемобжектекс**</span><span class="sxs-lookup"><span data-stu-id="3a5f4-129">**SWbemObjectEx**</span></span>](swbemobjectex.md)
</dt> </dl>

 

 




