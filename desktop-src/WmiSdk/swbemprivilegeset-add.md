---
description: Метод Add объекта Свбемпривилежесет добавляет объект Свбемпривилеже в коллекцию Свбемпривилежесет. Если в коллекции уже есть привилегия с таким именем, она будет заменена.
ms.assetid: 7d44193f-60e1-4e83-8640-31d8df509d98
ms.tgt_platform: multiple
title: Метод Свбемпривилежесет. Add (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilegeSet.Add
- ISWbemPrivilegeSet.Add
- ISWbemPrivilegeSet.Add
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 080b9d3e3ab6dbfc0ed8afc8ac0476981b7c26e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080527"
---
# <a name="swbemprivilegesetadd-method"></a><span data-ttu-id="97dfa-104">Свбемпривилежесет. Add, метод</span><span class="sxs-lookup"><span data-stu-id="97dfa-104">SWbemPrivilegeSet.Add method</span></span>

<span data-ttu-id="97dfa-105">Метод **Add** объекта [**Свбемпривилежесет**](swbemprivilegeset.md) добавляет объект [**свбемпривилеже**](swbemprivilege.md) в коллекцию **свбемпривилежесет** .</span><span class="sxs-lookup"><span data-stu-id="97dfa-105">The **Add** method of the [**SWbemPrivilegeSet**](swbemprivilegeset.md) object adds an [**SWbemPrivilege**](swbemprivilege.md) object to the **SWbemPrivilegeSet** collection.</span></span> <span data-ttu-id="97dfa-106">Если в коллекции уже есть привилегия с таким именем, она будет заменена.</span><span class="sxs-lookup"><span data-stu-id="97dfa-106">If a privilege with the same name already exists in the collection, it is replaced.</span></span>

<span data-ttu-id="97dfa-107">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="97dfa-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="97dfa-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="97dfa-108">Syntax</span></span>


```VB
objPrivilege = .Add( _
  ByVal iPrivilege, _
  [ ByVal bIsEnabled ] _
)
```



## <a name="parameters"></a><span data-ttu-id="97dfa-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="97dfa-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97dfa-110">*ипривилеже*</span><span class="sxs-lookup"><span data-stu-id="97dfa-110">*iPrivilege*</span></span> 
</dt> <dd>

<span data-ttu-id="97dfa-111">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="97dfa-111">Required.</span></span> <span data-ttu-id="97dfa-112">Одна из констант WMI из группы [**вбемпривилежеенум**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) .</span><span class="sxs-lookup"><span data-stu-id="97dfa-112">One of the WMI constants from the [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) group.</span></span> <span data-ttu-id="97dfa-113">Эти константы по сути представляют собой целые числа, представляющие определенные привилегии.</span><span class="sxs-lookup"><span data-stu-id="97dfa-113">These constants are essentially integers that represent specific privileges.</span></span> <span data-ttu-id="97dfa-114">Например, чтобы добавить привилегию, позволяющую завершить работу компьютера, используйте константу **вбемпривилежешутдовн** .</span><span class="sxs-lookup"><span data-stu-id="97dfa-114">For example, to add the privilege that allows you to shut down a computer system, use the **wbemPrivilegeShutdown** constant.</span></span> <span data-ttu-id="97dfa-115">В скрипте необходимо использовать числовой эквивалент 23 (0x17).</span><span class="sxs-lookup"><span data-stu-id="97dfa-115">In a script, you must use the numeric equivalent of 23 (0x17).</span></span> <span data-ttu-id="97dfa-116">Полный список этих констант и связанные строки прав доступа см. в разделе [**константы прав**](privilege-constants.md).</span><span class="sxs-lookup"><span data-stu-id="97dfa-116">For a complete list of these constants and the associated privilege strings, see [**Privilege Constants**](privilege-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="97dfa-117">*бисенаблед* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="97dfa-117">*bIsEnabled* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="97dfa-118">Логическое значение, которое включает или отключает эту привилегию.</span><span class="sxs-lookup"><span data-stu-id="97dfa-118">Boolean value that enables or disables this privilege.</span></span> <span data-ttu-id="97dfa-119">Значение по умолчанию — **true**.</span><span class="sxs-lookup"><span data-stu-id="97dfa-119">The default value is **TRUE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97dfa-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="97dfa-120">Return value</span></span>

<span data-ttu-id="97dfa-121">В случае успеха метод возвращает объект [**свбемпривилеже**](swbemprivilege.md) , представляющий новую привилегию.</span><span class="sxs-lookup"><span data-stu-id="97dfa-121">If successful, the method returns an [**SWbemPrivilege**](swbemprivilege.md) object that represents the new privilege.</span></span> <span data-ttu-id="97dfa-122">В противном случае возвращается пустой объект.</span><span class="sxs-lookup"><span data-stu-id="97dfa-122">Otherwise, a null object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="97dfa-123">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="97dfa-123">Error codes</span></span>

<span data-ttu-id="97dfa-124">После завершения метода **Add** объект **Err** может содержать код ошибки из следующего списка.</span><span class="sxs-lookup"><span data-stu-id="97dfa-124">Upon the completion of the **Add** method, the **Err** object may contain the error code in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="97dfa-125">**вбемеррфаилед** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="97dfa-125">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="97dfa-126">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="97dfa-126">Unspecified error.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="97dfa-127">Примеры</span><span class="sxs-lookup"><span data-stu-id="97dfa-127">Examples</span></span>

<span data-ttu-id="97dfa-128">Пример кода с использованием этого метода описан в разделе [**свбемпривилежесет**](swbemprivilegeset.md) .</span><span class="sxs-lookup"><span data-stu-id="97dfa-128">A code example using this method is described in the [**SWbemPrivilegeSet**](swbemprivilegeset.md) topic.</span></span>

## <a name="requirements"></a><span data-ttu-id="97dfa-129">Требования</span><span class="sxs-lookup"><span data-stu-id="97dfa-129">Requirements</span></span>



| <span data-ttu-id="97dfa-130">Требование</span><span class="sxs-lookup"><span data-stu-id="97dfa-130">Requirement</span></span> | <span data-ttu-id="97dfa-131">Значение</span><span class="sxs-lookup"><span data-stu-id="97dfa-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="97dfa-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="97dfa-132">Minimum supported client</span></span><br/> | <span data-ttu-id="97dfa-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="97dfa-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="97dfa-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="97dfa-134">Minimum supported server</span></span><br/> | <span data-ttu-id="97dfa-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="97dfa-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="97dfa-136">Header</span><span class="sxs-lookup"><span data-stu-id="97dfa-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="97dfa-137"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="97dfa-137"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="97dfa-138">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="97dfa-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="97dfa-139"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="97dfa-139"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="97dfa-140">DLL</span><span class="sxs-lookup"><span data-stu-id="97dfa-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="97dfa-141"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="97dfa-141"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="97dfa-142">CLSID</span><span class="sxs-lookup"><span data-stu-id="97dfa-142">CLSID</span></span><br/>                    | <span data-ttu-id="97dfa-143">\_СВБЕМПРИВИЛЕЖЕСЕТ CLSID</span><span class="sxs-lookup"><span data-stu-id="97dfa-143">CLSID\_SWbemPrivilegeSet</span></span><br/>                                                     |
| <span data-ttu-id="97dfa-144">IID</span><span class="sxs-lookup"><span data-stu-id="97dfa-144">IID</span></span><br/>                      | <span data-ttu-id="97dfa-145">IID \_ исвбемпривилежесет</span><span class="sxs-lookup"><span data-stu-id="97dfa-145">IID\_ISWbemPrivilegeSet</span></span><br/>                                                      |



## <a name="see-also"></a><span data-ttu-id="97dfa-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="97dfa-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97dfa-147">**свбемпривилежесет**</span><span class="sxs-lookup"><span data-stu-id="97dfa-147">**SWbemPrivilegeSet**</span></span>](swbemprivilegeset.md)
</dt> <dt>

[<span data-ttu-id="97dfa-148">Выполнение привилегированных операций</span><span class="sxs-lookup"><span data-stu-id="97dfa-148">Executing Privileged Operations</span></span>](executing-privileged-operations.md)
</dt> <dt>

[<span data-ttu-id="97dfa-149">Выполнение привилегированных операций с помощью VBScript</span><span class="sxs-lookup"><span data-stu-id="97dfa-149">Executing Privileged Operations Using VBScript</span></span>](executing-privileged-operations-using-vbscript.md)
</dt> <dt>

[<span data-ttu-id="97dfa-150">**Свбемпривилежесет. Аддасстринг**</span><span class="sxs-lookup"><span data-stu-id="97dfa-150">**SWbemPrivilegeSet.AddAsString**</span></span>](swbemprivilegeset-addasstring.md)
</dt> <dt>

[<span data-ttu-id="97dfa-151">**Свбемпривилежесет. Remove**</span><span class="sxs-lookup"><span data-stu-id="97dfa-151">**SWbemPrivilegeSet.Remove**</span></span>](swbemprivilegeset-remove.md)
</dt> <dt>

[<span data-ttu-id="97dfa-152">**вбемпривилежеенум**</span><span class="sxs-lookup"><span data-stu-id="97dfa-152">**WbemPrivilegeEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dt>

[<span data-ttu-id="97dfa-153">**Константы прав доступа**</span><span class="sxs-lookup"><span data-stu-id="97dfa-153">**Privilege Constants**</span></span>](privilege-constants.md)
</dt> </dl>

 

 




