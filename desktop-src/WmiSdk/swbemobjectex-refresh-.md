---
description: Обновляет данные для объектов, имеющих данные, предоставляемые поставщиком производительности, например классы счетчиков производительности. Вы можете получать обновленные данные быстрее и без вызова SWbemServices. Get \_ .
ms.assetid: 6aeaa336-fb98-4eda-b746-fc958198d8ae
ms.tgt_platform: multiple
title: Метод SWbemObjectEx.Refresh_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectEx.Refresh_
- ISWbemObjectEx.Refresh_
- ISWbemObjectEx.Refresh_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 904e2b7f9b256596555c8396a699220108d4f37b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711640"
---
# <a name="swbemobjectexrefresh_-method"></a><span data-ttu-id="f0238-104">Свбемобжектекс. Refresh, \_ метод</span><span class="sxs-lookup"><span data-stu-id="f0238-104">SWbemObjectEx.Refresh\_ method</span></span>

<span data-ttu-id="f0238-105">Метод **Refresh \_** объекта [**свбемобжектекс**](swbemobjectex.md) обновляет данные для объектов, имеющих данные, предоставляемые поставщиком производительности, например [Классы счетчиков производительности](/windows/desktop/CIMWin32Prov/performance-counter-classes).</span><span class="sxs-lookup"><span data-stu-id="f0238-105">The **Refresh\_** method of [**SWbemObjectEx**](swbemobjectex.md) updates the data for objects that have data supplied by a performance provider, such as the [Performance Counter Classes](/windows/desktop/CIMWin32Prov/performance-counter-classes).</span></span> <span data-ttu-id="f0238-106">Вы можете получать обновленные данные быстрее и без вызова [**SwbemServices. Get \_**](swbemservices-get.md).</span><span class="sxs-lookup"><span data-stu-id="f0238-106">You can obtain updated data more quickly and without a call to [**SWbemServices.Get\_**](swbemservices-get.md).</span></span>

<span data-ttu-id="f0238-107">Дополнительные сведения об этом синтаксисе см. [в разделе соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="f0238-107">For more information about this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f0238-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f0238-108">Syntax</span></span>


```VB
SWbemObjectEx.Refresh_( _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="f0238-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="f0238-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0238-110">*ифлагс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="f0238-110">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f0238-111">Зарезервированные флаги операции, если они заданы, должны быть равны 0 (нулю).</span><span class="sxs-lookup"><span data-stu-id="f0238-111">Reserved operation flags which, if specified, must be 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="f0238-112">*обжвбемнамедвалуесет* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="f0238-112">*objWbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f0238-113">Объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , который задает контекст для операции.</span><span class="sxs-lookup"><span data-stu-id="f0238-113">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that sets context for the operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0238-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f0238-114">Return value</span></span>

<span data-ttu-id="f0238-115">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="f0238-115">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f0238-116">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="f0238-116">Error codes</span></span>

<span data-ttu-id="f0238-117">После завершения метода **Refresh \_** объект **Err** может содержать один из кодов ошибок из следующего списка.</span><span class="sxs-lookup"><span data-stu-id="f0238-117">After completion of the **Refresh\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="f0238-118">**вбемеррфаилед** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="f0238-118">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="f0238-119">Произошел сбой внутреннего поставщика, хотя операция была допустимой.</span><span class="sxs-lookup"><span data-stu-id="f0238-119">The provider failed internally, even though the operation was valid.</span></span>

</dd> <dt>

<span data-ttu-id="f0238-120">**вбемеррнотфаунд** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="f0238-120">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="f0238-121">Запрошенный формат не найден.</span><span class="sxs-lookup"><span data-stu-id="f0238-121">The requested format was not found.</span></span>

</dd> <dt>

<span data-ttu-id="f0238-122">**вбемерринвалидпараметер** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="f0238-122">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="f0238-123">Один из параметров вызова указан неправильно.</span><span class="sxs-lookup"><span data-stu-id="f0238-123">One of the parameters to the call is not correct.</span></span>

</dd> <dt>

<span data-ttu-id="f0238-124">**вбемерррефрешербуси** -2147749975 (0x80041057)</span><span class="sxs-lookup"><span data-stu-id="f0238-124">**wbemErrRefresherBusy** - 2147749975 (0x80041057)</span></span>
</dt> <dd>

<span data-ttu-id="f0238-125">Обновитель занят другой операцией.</span><span class="sxs-lookup"><span data-stu-id="f0238-125">The refresher is busy with another operation.</span></span>

</dd> <dt>

<span data-ttu-id="f0238-126">**вбемпартиалресултс** -2147745808 (0x80040010)</span><span class="sxs-lookup"><span data-stu-id="f0238-126">**wbemPartialResults** - 2147745808 (0x80040010)</span></span>
</dt> <dd>

<span data-ttu-id="f0238-127">Не все объекты, перечислители или вложенные обновления успешно обновлены.</span><span class="sxs-lookup"><span data-stu-id="f0238-127">Not all of the objects, enumerators, or nested refreshers were successfully updated.</span></span> <span data-ttu-id="f0238-128">Этот возврат не является ошибкой, но указывает на то, что операция была неполной.</span><span class="sxs-lookup"><span data-stu-id="f0238-128">This return is not an error but an indication that the operation was incomplete.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="f0238-129">Примеры</span><span class="sxs-lookup"><span data-stu-id="f0238-129">Examples</span></span>

<span data-ttu-id="f0238-130">В следующем примере кода скрипта показано, как получить необработанные и обработанные счетчики производительности для системного процесса.</span><span class="sxs-lookup"><span data-stu-id="f0238-130">The following script code example shows how to obtain both raw and cooked performance counters for the system process.</span></span> <span data-ttu-id="f0238-131">Объекты обновляются каждые две секунды и отображаются свойствами.</span><span class="sxs-lookup"><span data-stu-id="f0238-131">The objects are refreshed every two seconds and the properties displayed.</span></span>


```VB
' Get the performance counter instance for the System process
set PerfRaw = GetObject( _
    "winmgmts:win32_perfrawdata_perfproc_process.name='system'")
set PerfCooked = GetObject( _
    "winmgmts:win32_perfformatteddata_perfproc_process.name='system'")

' Display some properties in a loop
for I = 1 to 5
    Wscript.Echo "HandleCount = "& PerfRaw.HandleCount & _
         " Raw ThreadCount = " & PerfRaw.ThreadCount & _
        " Cooked ThreadCount = " & PerfCooked.ThreadCount
    
    Wscript.Sleep 2000
    
' Refresh the objects
    PerfRaw.Refresh_
    PerfCooked.Refresh_
next
```



## <a name="requirements"></a><span data-ttu-id="f0238-132">Требования</span><span class="sxs-lookup"><span data-stu-id="f0238-132">Requirements</span></span>



| <span data-ttu-id="f0238-133">Требование</span><span class="sxs-lookup"><span data-stu-id="f0238-133">Requirement</span></span> | <span data-ttu-id="f0238-134">Значение</span><span class="sxs-lookup"><span data-stu-id="f0238-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f0238-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f0238-135">Minimum supported client</span></span><br/> | <span data-ttu-id="f0238-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f0238-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f0238-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f0238-137">Minimum supported server</span></span><br/> | <span data-ttu-id="f0238-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f0238-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f0238-139">Header</span><span class="sxs-lookup"><span data-stu-id="f0238-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0238-140"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0238-140"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="f0238-141">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="f0238-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="f0238-142"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f0238-142"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f0238-143">DLL</span><span class="sxs-lookup"><span data-stu-id="f0238-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f0238-144"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f0238-144"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="f0238-145">CLSID</span><span class="sxs-lookup"><span data-stu-id="f0238-145">CLSID</span></span><br/>                    | <span data-ttu-id="f0238-146">\_СВБЕМОБЖЕКТЕКС CLSID</span><span class="sxs-lookup"><span data-stu-id="f0238-146">CLSID\_SWbemObjectEx</span></span><br/>                                                         |
| <span data-ttu-id="f0238-147">IID</span><span class="sxs-lookup"><span data-stu-id="f0238-147">IID</span></span><br/>                      | <span data-ttu-id="f0238-148">IID \_ исвбемобжектекс</span><span class="sxs-lookup"><span data-stu-id="f0238-148">IID\_ISWbemObjectEx</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="f0238-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f0238-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0238-150">**свбемобжектекс**</span><span class="sxs-lookup"><span data-stu-id="f0238-150">**SWbemObjectEx**</span></span>](swbemobjectex.md)
</dt> <dt>

[<span data-ttu-id="f0238-151">Мониторинг данных производительности</span><span class="sxs-lookup"><span data-stu-id="f0238-151">Monitoring Performance Data</span></span>](monitoring-performance-data.md)
</dt> </dl>

 

