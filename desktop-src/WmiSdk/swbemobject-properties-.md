---
description: Свойство Properties \_ объекта SWbemObject возвращает объект SWbemPropertySet, являющийся коллекцией свойств текущего класса или экземпляра. Это свойство доступно только для чтения.
ms.assetid: 8dd49678-47e7-4c6b-ab12-42532065eaf2
ms.tgt_platform: multiple
title: Свойство SWbemObject.Properties_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Properties_
- ISWbemObject.Properties_
- ISWbemObject.get_Properties_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 2b215abb7a0ca466c8a93fe20f20518f8d7b2ec8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701957"
---
# <a name="swbemobjectproperties_-property"></a><span data-ttu-id="07bc6-104">SWbemObject. Properties, \_ свойство</span><span class="sxs-lookup"><span data-stu-id="07bc6-104">SWbemObject.Properties\_ property</span></span>

<span data-ttu-id="07bc6-105">Свойство **Properties \_** объекта [**SWbemObject**](swbemobject.md) возвращает объект [**SWbemPropertySet**](swbempropertyset.md) , являющийся коллекцией свойств текущего класса или экземпляра.</span><span class="sxs-lookup"><span data-stu-id="07bc6-105">The **Properties\_** property of the [**SWbemObject**](swbemobject.md) object returns an [**SWbemPropertySet**](swbempropertyset.md) object that is a collection of the properties for the current class or instance.</span></span> <span data-ttu-id="07bc6-106">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="07bc6-106">This property is read-only.</span></span>

<span data-ttu-id="07bc6-107">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="07bc6-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="07bc6-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="07bc6-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="07bc6-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="07bc6-109">Syntax</span></span>


```VB
SWbemObject.Properties_ As Object
```



## <a name="property-value"></a><span data-ttu-id="07bc6-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="07bc6-110">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="07bc6-111">Примеры</span><span class="sxs-lookup"><span data-stu-id="07bc6-111">Examples</span></span>

<span data-ttu-id="07bc6-112">Пример кода PowerShell " [Создание скриптов класса WMI PowerShell](https://Gallery.TechNet.Microsoft.Com/b435aa68-a1df-4f62-af05-1f504f683146) " в коллекции TechNet использует \_ свойство Properties для создания скрипта для каждого класса WMI, в котором будут ПЕРЕЧИСЛЕНЫ имя класса WMI и свойства.</span><span class="sxs-lookup"><span data-stu-id="07bc6-112">The [Generate Powershell WMI Class Scripts](https://Gallery.TechNet.Microsoft.Com/b435aa68-a1df-4f62-af05-1f504f683146) PowerShell code example on TechNet Gallery uses the Properties\_ property to generate a script for each of the WMI classes that will list the WMI class name and the properties.</span></span>

<span data-ttu-id="07bc6-113">Приведенный ниже код, взятый из [списка всех свойств для](https://Gallery.TechNet.Microsoft.Com/0f66f392-05b6-4431-b596-9379124d7a32) примера кода VBScript класса WMI в коллекции TechNet, содержит список свойств для УКАЗАННОГО класса WMI.</span><span class="sxs-lookup"><span data-stu-id="07bc6-113">The following code, taken from the [List All the Properties for a WMI Class](https://Gallery.TechNet.Microsoft.Com/0f66f392-05b6-4431-b596-9379124d7a32) VBScript code example on TechNet Gallery, Lists the properties for a specified WMI class.</span></span>


```VB
strComputer = "." 
strNameSpace = "root\cimv2" 
strClass = "Win32_Service" 
  
Set objClass = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & _  
    strComputer & "\" & strNameSpace & ":" & strClass) 
  
WScript.Echo strClass & " Class Properties" 
WScript.Echo "------------------------------" 
  
For Each objClassProperty In objClass.Properties_ 
    WScript.Echo objClassProperty.Name 
Next 
```



## <a name="requirements"></a><span data-ttu-id="07bc6-114">Требования</span><span class="sxs-lookup"><span data-stu-id="07bc6-114">Requirements</span></span>



| <span data-ttu-id="07bc6-115">Требование</span><span class="sxs-lookup"><span data-stu-id="07bc6-115">Requirement</span></span> | <span data-ttu-id="07bc6-116">Значение</span><span class="sxs-lookup"><span data-stu-id="07bc6-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="07bc6-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="07bc6-117">Minimum supported client</span></span><br/> | <span data-ttu-id="07bc6-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="07bc6-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="07bc6-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="07bc6-119">Minimum supported server</span></span><br/> | <span data-ttu-id="07bc6-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="07bc6-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="07bc6-121">Header</span><span class="sxs-lookup"><span data-stu-id="07bc6-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="07bc6-122"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="07bc6-122"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="07bc6-123">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="07bc6-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="07bc6-124"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="07bc6-124"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="07bc6-125">DLL</span><span class="sxs-lookup"><span data-stu-id="07bc6-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="07bc6-126"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07bc6-126"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="07bc6-127">CLSID</span><span class="sxs-lookup"><span data-stu-id="07bc6-127">CLSID</span></span><br/>                    | <span data-ttu-id="07bc6-128">\_SWBEMOBJECT CLSID</span><span class="sxs-lookup"><span data-stu-id="07bc6-128">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="07bc6-129">IID</span><span class="sxs-lookup"><span data-stu-id="07bc6-129">IID</span></span><br/>                      | <span data-ttu-id="07bc6-130">IID \_ исвбемобжект</span><span class="sxs-lookup"><span data-stu-id="07bc6-130">IID\_ISWbemObject</span></span><br/>                                                            |



 

 




