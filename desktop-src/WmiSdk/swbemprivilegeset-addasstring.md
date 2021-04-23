---
description: Метод Аддасстринг объекта Свбемпривилежесет можно использовать для добавления прав доступа к коллекции Свбемпривилежесет с помощью строки привилегий.
ms.assetid: 729ed4e3-2c5c-4bb4-acc6-cf9ad0d5eaf1
ms.tgt_platform: multiple
title: Свбемпривилежесет. Аддасстринг, метод (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilegeSet.AddAsString
- ISWbemPrivilegeSet.AddAsString
- ISWbemPrivilegeSet.AddAsString
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: b3a740141b14766080a09d01b36b5c0202351eda
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703168"
---
# <a name="swbemprivilegesetaddasstring-method"></a><span data-ttu-id="a50b5-103">Свбемпривилежесет. Аддасстринг, метод</span><span class="sxs-lookup"><span data-stu-id="a50b5-103">SWbemPrivilegeSet.AddAsString method</span></span>

<span data-ttu-id="a50b5-104">Метод **аддасстринг** объекта [**свбемпривилежесет**](swbemprivilegeset.md) можно использовать для добавления прав доступа к коллекции **свбемпривилежесет** с помощью строки привилегий.</span><span class="sxs-lookup"><span data-stu-id="a50b5-104">You can use the **AddAsString** method of the [**SWbemPrivilegeSet**](swbemprivilegeset.md) object to add a privilege to an **SWbemPrivilegeSet** collection using a privilege string.</span></span> <span data-ttu-id="a50b5-105">Этот метод используется для добавления привилегий или для разрешения доступа к объектам [**свбемсекурити**](swbemsecurity.md) .</span><span class="sxs-lookup"><span data-stu-id="a50b5-105">Use this method to add a privilege or to enable a privilege for [**SWbemSecurity**](swbemsecurity.md) objects.</span></span> <span data-ttu-id="a50b5-106">См. раздел [выполнение привилегированных операций с помощью VBScript](executing-privileged-operations-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="a50b5-106">See [Executing Privileged Operations Using VBScript](executing-privileged-operations-using-vbscript.md).</span></span>

<span data-ttu-id="a50b5-107">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="a50b5-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a50b5-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a50b5-108">Syntax</span></span>


```VB
objPrivilege = .AddAsString( _
  ByVal strPrivilege, _
  [ ByVal bIsEnabled ] _
)
```



## <a name="parameters"></a><span data-ttu-id="a50b5-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="a50b5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a50b5-110">*стрпривилеже*</span><span class="sxs-lookup"><span data-stu-id="a50b5-110">*strPrivilege*</span></span> 
</dt> <dd>

<span data-ttu-id="a50b5-111">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="a50b5-111">Required.</span></span> <span data-ttu-id="a50b5-112">Одна из строк привилегий.</span><span class="sxs-lookup"><span data-stu-id="a50b5-112">One of the privilege strings.</span></span> <span data-ttu-id="a50b5-113">Полный список этих строк и связанные с ними константы WMI см. в разделе [**константы прав**](privilege-constants.md).</span><span class="sxs-lookup"><span data-stu-id="a50b5-113">For a complete list of these strings and the associated WMI constants, see [**Privilege Constants**](privilege-constants.md).</span></span> <span data-ttu-id="a50b5-114">Каждая строка прав представляет собой конкретную привилегию.</span><span class="sxs-lookup"><span data-stu-id="a50b5-114">Every privilege string represents a specific privilege.</span></span> <span data-ttu-id="a50b5-115">Например, чтобы добавить привилегию, которая используется для завершения работы компьютерной системы, используйте строку **сешутдовнпривилеже** .</span><span class="sxs-lookup"><span data-stu-id="a50b5-115">For example, to add the privilege that use to shut down a computer system, use the **SeShutdownPrivilege** string.</span></span>

</dd> <dt>

<span data-ttu-id="a50b5-116">*бисенаблед* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="a50b5-116">*bIsEnabled* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a50b5-117">Логическое значение, которое включает или отключает эту привилегию.</span><span class="sxs-lookup"><span data-stu-id="a50b5-117">Boolean value that enables or disables this privilege.</span></span> <span data-ttu-id="a50b5-118">По умолчанию используется значение **True**.</span><span class="sxs-lookup"><span data-stu-id="a50b5-118">The default value is **True**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a50b5-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a50b5-119">Return value</span></span>

<span data-ttu-id="a50b5-120">В случае успеха этот метод возвращает объект [**свбемпривилеже**](swbemprivilege.md) , представляющий новую привилегию.</span><span class="sxs-lookup"><span data-stu-id="a50b5-120">If successful, this method returns an [**SWbemPrivilege**](swbemprivilege.md) object that represents the new privilege.</span></span> <span data-ttu-id="a50b5-121">В противном случае возвращается пустой объект.</span><span class="sxs-lookup"><span data-stu-id="a50b5-121">Otherwise, a null object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a50b5-122">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="a50b5-122">Error codes</span></span>

<span data-ttu-id="a50b5-123">После завершения метода **аддасстринг** объект **Err** может содержать код ошибки из следующего списка.</span><span class="sxs-lookup"><span data-stu-id="a50b5-123">Upon the completion of the **AddAsString** method, the **Err** object may contain the error code in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="a50b5-124">**вбемеррфаилед** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="a50b5-124">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="a50b5-125">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="a50b5-125">Unspecified error.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="a50b5-126">Примеры</span><span class="sxs-lookup"><span data-stu-id="a50b5-126">Examples</span></span>

<span data-ttu-id="a50b5-127">В следующем примере кода VBScript создается новый порт для сервера печати с помощью [**Win32 \_ ткпиппринтерпорт**](/windows/desktop/CIMWin32Prov/win32-tcpipprinterport).</span><span class="sxs-lookup"><span data-stu-id="a50b5-127">The following VBScript code example creates a new port for a print server using [**Win32\_TCPIPPrinterPort**](/windows/desktop/CIMWin32Prov/win32-tcpipprinterport).</span></span> <span data-ttu-id="a50b5-128">Для этой операции требуется **селоаддриверпривилеже** .</span><span class="sxs-lookup"><span data-stu-id="a50b5-128">The **SeLoadDriverPrivilege** is required for this operation.</span></span> <span data-ttu-id="a50b5-129">См. раздел [выполнение привилегированных операций](executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="a50b5-129">See [Executing Privileged Operations](executing-privileged-operations.md).</span></span>


```VB
Set objWMIService = GetObject("Winmgmts:")
objWMIService.Security_.Privileges. _
    AddAsString "SeLoadDriverPrivilege", True
Set objNewPort = objWMIService.Get _
    ("Win32_TCPIPPrinterPort").SpawnInstance_
objNewPort.Name = "IP_111.222.111.11"
objNewPort.Protocol = 1
objNewPort.HostAddress = "111.222.111.11"
objNewPort.PortNumber = "9999"
objNewPort.SNMPEnabled = False
objNewPort.Put_
```



<span data-ttu-id="a50b5-130">Пример кода, использующий этот метод, также описывается в разделе [**свбемпривилежесет**](swbemprivilegeset.md) .</span><span class="sxs-lookup"><span data-stu-id="a50b5-130">A code example using this method is also described in the [**SWbemPrivilegeSet**](swbemprivilegeset.md) topic.</span></span>

## <a name="requirements"></a><span data-ttu-id="a50b5-131">Требования</span><span class="sxs-lookup"><span data-stu-id="a50b5-131">Requirements</span></span>



| <span data-ttu-id="a50b5-132">Требование</span><span class="sxs-lookup"><span data-stu-id="a50b5-132">Requirement</span></span> | <span data-ttu-id="a50b5-133">Значение</span><span class="sxs-lookup"><span data-stu-id="a50b5-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a50b5-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a50b5-134">Minimum supported client</span></span><br/> | <span data-ttu-id="a50b5-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a50b5-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a50b5-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a50b5-136">Minimum supported server</span></span><br/> | <span data-ttu-id="a50b5-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a50b5-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a50b5-138">Header</span><span class="sxs-lookup"><span data-stu-id="a50b5-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="a50b5-139"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a50b5-139"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a50b5-140">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="a50b5-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="a50b5-141"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a50b5-141"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a50b5-142">DLL</span><span class="sxs-lookup"><span data-stu-id="a50b5-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a50b5-143"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a50b5-143"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="a50b5-144">CLSID</span><span class="sxs-lookup"><span data-stu-id="a50b5-144">CLSID</span></span><br/>                    | <span data-ttu-id="a50b5-145">\_СВБЕМПРИВИЛЕЖЕСЕТ CLSID</span><span class="sxs-lookup"><span data-stu-id="a50b5-145">CLSID\_SWbemPrivilegeSet</span></span><br/>                                                     |
| <span data-ttu-id="a50b5-146">IID</span><span class="sxs-lookup"><span data-stu-id="a50b5-146">IID</span></span><br/>                      | <span data-ttu-id="a50b5-147">IID \_ исвбемпривилежесет</span><span class="sxs-lookup"><span data-stu-id="a50b5-147">IID\_ISWbemPrivilegeSet</span></span><br/>                                                      |



## <a name="see-also"></a><span data-ttu-id="a50b5-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a50b5-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a50b5-149">**свбемпривилежесет**</span><span class="sxs-lookup"><span data-stu-id="a50b5-149">**SWbemPrivilegeSet**</span></span>](swbemprivilegeset.md)
</dt> <dt>

[<span data-ttu-id="a50b5-150">**Свбемпривилежесет. Add**</span><span class="sxs-lookup"><span data-stu-id="a50b5-150">**SWbemPrivilegeSet.Add**</span></span>](swbemprivilegeset-add.md)
</dt> <dt>

[<span data-ttu-id="a50b5-151">**Свбемпривилежесет. Remove**</span><span class="sxs-lookup"><span data-stu-id="a50b5-151">**SWbemPrivilegeSet.Remove**</span></span>](swbemprivilegeset-remove.md)
</dt> <dt>

[<span data-ttu-id="a50b5-152">**вбемпривилежеенум**</span><span class="sxs-lookup"><span data-stu-id="a50b5-152">**WbemPrivilegeEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dt>

[<span data-ttu-id="a50b5-153">**Константы прав доступа**</span><span class="sxs-lookup"><span data-stu-id="a50b5-153">**Privilege Constants**</span></span>](privilege-constants.md)
</dt> <dt>

[<span data-ttu-id="a50b5-154">Выполнение привилегированных операций</span><span class="sxs-lookup"><span data-stu-id="a50b5-154">Executing Privileged Operations</span></span>](executing-privileged-operations.md)
</dt> <dt>

[<span data-ttu-id="a50b5-155">Выполнение привилегированных операций с помощью VBScript</span><span class="sxs-lookup"><span data-stu-id="a50b5-155">Executing Privileged Operations Using VBScript</span></span>](executing-privileged-operations-using-vbscript.md)
</dt> </dl>

 

