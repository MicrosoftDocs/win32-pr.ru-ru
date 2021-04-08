---
description: Метод Item объекта Свбемпривилежесет возвращает объект Свбемпривилеже из коллекции. Метод Item является методом по умолчанию для объекта Свбемпривилежесет.
ms.assetid: 93a35e65-99ee-40da-9415-4151ac635091
ms.tgt_platform: multiple
title: Метод Свбемпривилежесет. Item (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilegeSet.Item
- ISWbemPrivilegeSet.Item
- ISWbemPrivilegeSet.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 7ea37ae758ec599198fc35a1fd2a4b89ff25a087
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898534"
---
# <a name="swbemprivilegesetitem-method"></a><span data-ttu-id="8b831-104">Свбемпривилежесет. Item, метод</span><span class="sxs-lookup"><span data-stu-id="8b831-104">SWbemPrivilegeSet.Item method</span></span>

<span data-ttu-id="8b831-105">Метод **Item** объекта [**Свбемпривилежесет**](swbemprivilegeset.md) возвращает объект [**свбемпривилеже**](swbemprivilege.md) из коллекции.</span><span class="sxs-lookup"><span data-stu-id="8b831-105">The **Item** method of the [**SWbemPrivilegeSet**](swbemprivilegeset.md) object returns an [**SWbemPrivilege**](swbemprivilege.md) object from the collection.</span></span> <span data-ttu-id="8b831-106">Метод **Item** является методом по умолчанию для объекта **свбемпривилежесет** .</span><span class="sxs-lookup"><span data-stu-id="8b831-106">The **Item** method is the default method of an **SWbemPrivilegeSet** object.</span></span>

<span data-ttu-id="8b831-107">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="8b831-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="8b831-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8b831-108">Syntax</span></span>


```VB
objPrivilege = .Item( _
  ByVal iPrivilege _
)
```



## <a name="parameters"></a><span data-ttu-id="8b831-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="8b831-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b831-110">*ипривилеже*</span><span class="sxs-lookup"><span data-stu-id="8b831-110">*iPrivilege*</span></span> 
</dt> <dd>

<span data-ttu-id="8b831-111">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="8b831-111">Required.</span></span> <span data-ttu-id="8b831-112">Одна из констант WMI из группы [**вбемпривилежеенум**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) .</span><span class="sxs-lookup"><span data-stu-id="8b831-112">One of the WMI constants from the [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) group.</span></span> <span data-ttu-id="8b831-113">Эти константы по сути представляют собой целые числа, представляющие определенные привилегии.</span><span class="sxs-lookup"><span data-stu-id="8b831-113">These constants are essentially integers that represent specific privileges.</span></span> <span data-ttu-id="8b831-114">Например, чтобы получить привилегию, позволяющую завершить работу системы Windows, используйте константу **вбемпривилежешутдовн** или числовой эквивалент 23 (0x17).</span><span class="sxs-lookup"><span data-stu-id="8b831-114">For example, to get the privilege that allows you to shut down a Windows system, use the **wbemPrivilegeShutdown** constant or the numeric equivalent of 23 (0x17).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b831-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8b831-115">Return value</span></span>

<span data-ttu-id="8b831-116">В случае успешного выполнения возвращается запрошенный объект [**свбемпривилеже**](swbemprivilege.md) .</span><span class="sxs-lookup"><span data-stu-id="8b831-116">If successful, the requested [**SWbemPrivilege**](swbemprivilege.md) object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="8b831-117">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="8b831-117">Error codes</span></span>

<span data-ttu-id="8b831-118">После завершения метода **Item** объект **Err** может содержать один из кодов ошибок из следующего списка.</span><span class="sxs-lookup"><span data-stu-id="8b831-118">Upon the completion of the **Item** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="8b831-119">**вбемеррфаилед** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="8b831-119">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="8b831-120">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="8b831-120">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="8b831-121">**вбемеррнотфаунд** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="8b831-121">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="8b831-122">Указанное право доступа не существует.</span><span class="sxs-lookup"><span data-stu-id="8b831-122">Specified privilege does not exist.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="8b831-123">Примеры</span><span class="sxs-lookup"><span data-stu-id="8b831-123">Examples</span></span>

<span data-ttu-id="8b831-124">В следующем примере кода VBScript используется метод **Item** .</span><span class="sxs-lookup"><span data-stu-id="8b831-124">The following VBScript code example uses the **Item** method</span></span>


```VB
strComputer ="."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" & strComputer _
    & "\root\cimv2")
Set colServices = objWMIService.ExecQuery( _
    "Select * from Win32_Service")
For Each objService In colServices
    WScript.Echo objService.Properties_.Item("Caption")
Next
```



## <a name="requirements"></a><span data-ttu-id="8b831-125">Требования</span><span class="sxs-lookup"><span data-stu-id="8b831-125">Requirements</span></span>



| <span data-ttu-id="8b831-126">Требование</span><span class="sxs-lookup"><span data-stu-id="8b831-126">Requirement</span></span> | <span data-ttu-id="8b831-127">Значение</span><span class="sxs-lookup"><span data-stu-id="8b831-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8b831-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8b831-128">Minimum supported client</span></span><br/> | <span data-ttu-id="8b831-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8b831-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8b831-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8b831-130">Minimum supported server</span></span><br/> | <span data-ttu-id="8b831-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8b831-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8b831-132">Header</span><span class="sxs-lookup"><span data-stu-id="8b831-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b831-133"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b831-133"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="8b831-134">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="8b831-134">Type library</span></span><br/>             | <dl> <span data-ttu-id="8b831-135"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="8b831-135"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="8b831-136">DLL</span><span class="sxs-lookup"><span data-stu-id="8b831-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b831-137"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8b831-137"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="8b831-138">CLSID</span><span class="sxs-lookup"><span data-stu-id="8b831-138">CLSID</span></span><br/>                    | <span data-ttu-id="8b831-139">\_СВБЕМПРИВИЛЕЖЕСЕТ CLSID</span><span class="sxs-lookup"><span data-stu-id="8b831-139">CLSID\_SWbemPrivilegeSet</span></span><br/>                                                     |
| <span data-ttu-id="8b831-140">IID</span><span class="sxs-lookup"><span data-stu-id="8b831-140">IID</span></span><br/>                      | <span data-ttu-id="8b831-141">IID \_ исвбемпривилежесет</span><span class="sxs-lookup"><span data-stu-id="8b831-141">IID\_ISWbemPrivilegeSet</span></span><br/>                                                      |



## <a name="see-also"></a><span data-ttu-id="8b831-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8b831-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b831-143">**свбемпривилежесет**</span><span class="sxs-lookup"><span data-stu-id="8b831-143">**SWbemPrivilegeSet**</span></span>](swbemprivilegeset.md)
</dt> <dt>

[<span data-ttu-id="8b831-144">Выполнение привилегированных операций</span><span class="sxs-lookup"><span data-stu-id="8b831-144">Executing Privileged Operations</span></span>](executing-privileged-operations.md)
</dt> <dt>

[<span data-ttu-id="8b831-145">**свбемпривилеже**</span><span class="sxs-lookup"><span data-stu-id="8b831-145">**SWbemPrivilege**</span></span>](swbemprivilege.md)
</dt> </dl>

 

 




