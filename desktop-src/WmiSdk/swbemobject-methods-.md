---
description: Свойство Methods \_ объекта SWbemObject возвращает объект свбеммесодсет, который является коллекцией методов для текущего класса или экземпляра. Это свойство доступно только для чтения.
ms.assetid: ef9abced-5126-4698-b01e-f3e9c871162f
ms.tgt_platform: multiple
title: Свойство SWbemObject.Methods_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Methods_
- ISWbemObject.Methods_
- ISWbemObject.get_Methods_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 6a702f0acf0736810de4d3176f8695fa8008d3ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702993"
---
# <a name="swbemobjectmethods_-property"></a><span data-ttu-id="8da2e-104">SWbemObject. Methods, \_ свойство</span><span class="sxs-lookup"><span data-stu-id="8da2e-104">SWbemObject.Methods\_ property</span></span>

<span data-ttu-id="8da2e-105">Свойство **Methods \_** объекта [**SWbemObject**](swbemobject.md) возвращает объект [**свбеммесодсет**](swbemmethodset.md) , который является коллекцией методов для текущего класса или экземпляра.</span><span class="sxs-lookup"><span data-stu-id="8da2e-105">The **Methods\_** property of the [**SWbemObject**](swbemobject.md) object returns an [**SWbemMethodSet**](swbemmethodset.md) object that is a collection of the methods for the current class or instance.</span></span> <span data-ttu-id="8da2e-106">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="8da2e-106">This property is read-only.</span></span>

<span data-ttu-id="8da2e-107">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="8da2e-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="8da2e-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="8da2e-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="8da2e-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8da2e-109">Syntax</span></span>


```VB
SWbemObject.Methods_ As Object
```



## <a name="property-value"></a><span data-ttu-id="8da2e-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="8da2e-110">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="8da2e-111">Примеры</span><span class="sxs-lookup"><span data-stu-id="8da2e-111">Examples</span></span>

<span data-ttu-id="8da2e-112">Следующий [пример кода](https://Gallery.TechNet.Microsoft.Com/c15624ee-e335-4d58-a022-aed73ad330a1), взятый из коллекции TechNet, описывает, как перечислить все методы класса.</span><span class="sxs-lookup"><span data-stu-id="8da2e-112">The following [code sample](https://Gallery.TechNet.Microsoft.Com/c15624ee-e335-4d58-a022-aed73ad330a1), taken from the TechNet Gallery, describes how to list all methods of a class.</span></span>


```VB
strComputer = "." 
strNameSpace = "root\cimv2" 
strClass = "Win32_Service" 
  
Set objClass = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & _  
    strComputer & "\" & strNameSpace & ":" & strClass) 
  
WScript.Echo strClass & " Class Methods" 
WScript.Echo "---------------------------" 
  
For Each objClassMethod In objClass.Methods_ 
    WScript.Echo objClassMethod.Name 
Next 
```



## <a name="requirements"></a><span data-ttu-id="8da2e-113">Требования</span><span class="sxs-lookup"><span data-stu-id="8da2e-113">Requirements</span></span>



| <span data-ttu-id="8da2e-114">Требование</span><span class="sxs-lookup"><span data-stu-id="8da2e-114">Requirement</span></span> | <span data-ttu-id="8da2e-115">Значение</span><span class="sxs-lookup"><span data-stu-id="8da2e-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8da2e-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8da2e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="8da2e-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8da2e-117">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8da2e-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8da2e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="8da2e-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8da2e-119">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8da2e-120">Header</span><span class="sxs-lookup"><span data-stu-id="8da2e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="8da2e-121"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="8da2e-121"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="8da2e-122">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="8da2e-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="8da2e-123"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="8da2e-123"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="8da2e-124">DLL</span><span class="sxs-lookup"><span data-stu-id="8da2e-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8da2e-125"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8da2e-125"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="8da2e-126">CLSID</span><span class="sxs-lookup"><span data-stu-id="8da2e-126">CLSID</span></span><br/>                    | <span data-ttu-id="8da2e-127">\_SWBEMOBJECT CLSID</span><span class="sxs-lookup"><span data-stu-id="8da2e-127">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="8da2e-128">IID</span><span class="sxs-lookup"><span data-stu-id="8da2e-128">IID</span></span><br/>                      | <span data-ttu-id="8da2e-129">IID \_ исвбемобжект</span><span class="sxs-lookup"><span data-stu-id="8da2e-129">IID\_ISWbemObject</span></span><br/>                                                            |



 

 




