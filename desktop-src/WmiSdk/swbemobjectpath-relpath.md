---
description: Свойство Релпас объекта Свбемобжектпас содержит относительный путь от полного пути.
ms.assetid: 9a4363ae-b6b3-4e8c-a7ca-a9e48c28e19b
ms.tgt_platform: multiple
title: Свойство Свбемобжектпас. Релпас (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.Relpath
- ISWbemObjectPath.Relpath
- ISWbemObjectPath.get_Relpath
- ISWbemObjectPath.put_Relpath
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 8330d1cdc65e818acd4fda63b223303b779b5472
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105656677"
---
# <a name="swbemobjectpathrelpath-property"></a><span data-ttu-id="c71fd-103">Свбемобжектпас. Релпас, свойство</span><span class="sxs-lookup"><span data-stu-id="c71fd-103">SWbemObjectPath.Relpath property</span></span>

<span data-ttu-id="c71fd-104">Свойство **релпас** объекта [**свбемобжектпас**](swbemobjectpath.md) содержит относительный путь от полного пути.</span><span class="sxs-lookup"><span data-stu-id="c71fd-104">The **Relpath** property of the [**SWbemObjectPath**](swbemobjectpath.md) object contains the relative path from the complete path.</span></span>

<span data-ttu-id="c71fd-105">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="c71fd-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="c71fd-106">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="c71fd-106">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="c71fd-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c71fd-107">Syntax</span></span>


```VB
SWbemObjectPath.Relpath As String
```



## <a name="property-value"></a><span data-ttu-id="c71fd-108">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="c71fd-108">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="c71fd-109">Примеры</span><span class="sxs-lookup"><span data-stu-id="c71fd-109">Examples</span></span>

<span data-ttu-id="c71fd-110">В следующем примере кода VBScript показано различие между данными, полученными из [**SWbemObject. Path \_**](swbemobject-path-.md) и **свбемобжектпас. релпас**.</span><span class="sxs-lookup"><span data-stu-id="c71fd-110">The following VBScript code example shows the difference between the data obtained from [**SWbemObject.Path\_**](swbemobject-path-.md) and **SWbemObjectPath.Relpath**.</span></span>


```VB
set objWMIService = GetObject ("winmgmts:root/cimv2")

set Processes = objWMIService.ExecQuery( _
    "Select * from win32_process")

For Each Process in Processes
 WScript.Echo Process.Path_ 
 WScript.Echo Process.Path_.Relpath
Next
```



## <a name="requirements"></a><span data-ttu-id="c71fd-111">Требования</span><span class="sxs-lookup"><span data-stu-id="c71fd-111">Requirements</span></span>



| <span data-ttu-id="c71fd-112">Требование</span><span class="sxs-lookup"><span data-stu-id="c71fd-112">Requirement</span></span> | <span data-ttu-id="c71fd-113">Значение</span><span class="sxs-lookup"><span data-stu-id="c71fd-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c71fd-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c71fd-114">Minimum supported client</span></span><br/> | <span data-ttu-id="c71fd-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c71fd-115">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c71fd-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c71fd-116">Minimum supported server</span></span><br/> | <span data-ttu-id="c71fd-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c71fd-117">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c71fd-118">Header</span><span class="sxs-lookup"><span data-stu-id="c71fd-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="c71fd-119"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c71fd-119"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="c71fd-120">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="c71fd-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="c71fd-121"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c71fd-121"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c71fd-122">DLL</span><span class="sxs-lookup"><span data-stu-id="c71fd-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c71fd-123"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c71fd-123"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="c71fd-124">CLSID</span><span class="sxs-lookup"><span data-stu-id="c71fd-124">CLSID</span></span><br/>                    | <span data-ttu-id="c71fd-125">\_СВБЕМОБЖЕКТПАС CLSID</span><span class="sxs-lookup"><span data-stu-id="c71fd-125">CLSID\_SWbemObjectPath</span></span><br/>                                                       |
| <span data-ttu-id="c71fd-126">IID</span><span class="sxs-lookup"><span data-stu-id="c71fd-126">IID</span></span><br/>                      | <span data-ttu-id="c71fd-127">IID \_ исвбемобжектпас</span><span class="sxs-lookup"><span data-stu-id="c71fd-127">IID\_ISWbemObjectPath</span></span><br/>                                                        |



 

 




