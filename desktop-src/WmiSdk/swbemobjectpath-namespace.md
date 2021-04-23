---
description: Свойство Namespace объекта Свбемобжектпас содержит имя пространства имен, которое является частью пути к объекту.
ms.assetid: be88670d-6f0d-4b9d-886f-3e70bf4758ed
ms.tgt_platform: multiple
title: Свойство Свбемобжектпас. Namespace (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.Namespace
- ISWbemObjectPath.Namespace
- ISWbemObjectPath.get_Namespace
- ISWbemObjectPath.put_Namespace
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 885f7069e901d1d4a490ad7539077463f6c1838c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264996"
---
# <a name="swbemobjectpathnamespace-property"></a><span data-ttu-id="41369-103">Свбемобжектпас. Namespace, свойство</span><span class="sxs-lookup"><span data-stu-id="41369-103">SWbemObjectPath.Namespace property</span></span>

<span data-ttu-id="41369-104">Свойство **Namespace** объекта [**свбемобжектпас**](swbemobjectpath.md) содержит имя пространства имен, которое является частью пути к объекту.</span><span class="sxs-lookup"><span data-stu-id="41369-104">The **Namespace** property of the [**SWbemObjectPath**](swbemobjectpath.md) object contains the name of the namespace that is part of the object path.</span></span> <span data-ttu-id="41369-105">Например, следующий путь показывает свойство Namespace, которое возвращает корневой \\ CIMV2:</span><span class="sxs-lookup"><span data-stu-id="41369-105">For example, the following path shows the namespace property that returns root\\cimv2:</span></span>

``` syntax
\\computer\root\cimv2:win32_logicaldisk="a:"
```

<span data-ttu-id="41369-106">Описание синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="41369-106">For the syntax explanation, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="41369-107">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="41369-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="41369-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="41369-108">Syntax</span></span>


```VB
SWbemObjectPath.Namespace As String
```



## <a name="property-value"></a><span data-ttu-id="41369-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="41369-109">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="41369-110">Примеры</span><span class="sxs-lookup"><span data-stu-id="41369-110">Examples</span></span>

<span data-ttu-id="41369-111">В следующем примере показано, как получить имя пространства имен из экземпляров [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) , которые являются жесткими дисками.</span><span class="sxs-lookup"><span data-stu-id="41369-111">The following example shows you how to obtain the namespace name from instances of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) that are hard disks.</span></span> <span data-ttu-id="41369-112">Сценарий подключается к пространству имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="41369-112">The script connects to the default namespace.</span></span>


```VB
Const HARD_DISK = 3
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" & strComputer)

Set colDisks = objWMIService.ExecQuery _
    ("Select * from Win32_LogicalDisk " _
    & "Where DriveType = " & HARD_DISK & "")
For Each objDisk in colDisks
    Set objpath = objDisk.path_
    Wscript.Echo "Path of Win32_Logical disk instance " _
    & objDisk.DeviceID & " = " & objpath.Namespace   
Next
```



## <a name="requirements"></a><span data-ttu-id="41369-113">Требования</span><span class="sxs-lookup"><span data-stu-id="41369-113">Requirements</span></span>



| <span data-ttu-id="41369-114">Требование</span><span class="sxs-lookup"><span data-stu-id="41369-114">Requirement</span></span> | <span data-ttu-id="41369-115">Значение</span><span class="sxs-lookup"><span data-stu-id="41369-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="41369-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="41369-116">Minimum supported client</span></span><br/> | <span data-ttu-id="41369-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="41369-117">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="41369-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="41369-118">Minimum supported server</span></span><br/> | <span data-ttu-id="41369-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="41369-119">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="41369-120">Header</span><span class="sxs-lookup"><span data-stu-id="41369-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="41369-121"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="41369-121"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="41369-122">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="41369-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="41369-123"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="41369-123"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="41369-124">DLL</span><span class="sxs-lookup"><span data-stu-id="41369-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="41369-125"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="41369-125"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="41369-126">CLSID</span><span class="sxs-lookup"><span data-stu-id="41369-126">CLSID</span></span><br/>                    | <span data-ttu-id="41369-127">\_СВБЕМОБЖЕКТПАС CLSID</span><span class="sxs-lookup"><span data-stu-id="41369-127">CLSID\_SWbemObjectPath</span></span><br/>                                                       |
| <span data-ttu-id="41369-128">IID</span><span class="sxs-lookup"><span data-stu-id="41369-128">IID</span></span><br/>                      | <span data-ttu-id="41369-129">IID \_ исвбемобжектпас</span><span class="sxs-lookup"><span data-stu-id="41369-129">IID\_ISWbemObjectPath</span></span><br/>                                                        |



 

