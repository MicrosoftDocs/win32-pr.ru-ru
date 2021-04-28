---
description: Метод Shell. Жетсистеминформатион — получает сведения о системе.
ms.assetid: 94C10DD6-FE49-4dd4-AEED-69B73A75EDEF
title: Метод Shell. Жетсистеминформатион (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.GetSystemInformation
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: b9e021e767309007cfee2cfc78268fb7d7cea042
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104282"
---
# <a name="shellgetsysteminformation-method"></a><span data-ttu-id="7391e-103">Shell. Жетсистеминформатион, метод</span><span class="sxs-lookup"><span data-stu-id="7391e-103">Shell.GetSystemInformation method</span></span>

<span data-ttu-id="7391e-104">Возвращает сведения о системе.</span><span class="sxs-lookup"><span data-stu-id="7391e-104">Retrieves system information.</span></span>

## <a name="syntax"></a><span data-ttu-id="7391e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7391e-105">Syntax</span></span>


```JScript
retVal = Shell.GetSystemInformation(
  sName
)
```


```VB

Shell.GetSystemInformation( _
  ByVal sName As BSTR _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="7391e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7391e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7391e-107">*sName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7391e-107">*sName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7391e-108">Тип: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="7391e-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="7391e-109">**Строка** , указывающая запрашиваемую информацию о системе.</span><span class="sxs-lookup"><span data-stu-id="7391e-109">A **String** that specifies the system information that is being requested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7391e-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7391e-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="7391e-111">Язык JScript</span><span class="sxs-lookup"><span data-stu-id="7391e-111">JScript</span></span>

<span data-ttu-id="7391e-112">Тип: **Variant**</span><span class="sxs-lookup"><span data-stu-id="7391e-112">Type: **Variant**</span></span>

<span data-ttu-id="7391e-113">Возвращает значение запрошенной системной информации.</span><span class="sxs-lookup"><span data-stu-id="7391e-113">Returns the value of the requested system information.</span></span> <span data-ttu-id="7391e-114">Тип возвращаемого значения зависит от того, какие сведения о системе запрашиваются.</span><span class="sxs-lookup"><span data-stu-id="7391e-114">The return type depends on which system information is requested.</span></span> <span data-ttu-id="7391e-115">Подробные сведения см. в разделе "Заметки".</span><span class="sxs-lookup"><span data-stu-id="7391e-115">See the Remarks section for details.</span></span>

### <a name="vb"></a><span data-ttu-id="7391e-116">VB</span><span class="sxs-lookup"><span data-stu-id="7391e-116">VB</span></span>

<span data-ttu-id="7391e-117">Тип: **Variant**</span><span class="sxs-lookup"><span data-stu-id="7391e-117">Type: **Variant**</span></span>

<span data-ttu-id="7391e-118">Возвращает значение запрошенной системной информации.</span><span class="sxs-lookup"><span data-stu-id="7391e-118">Returns the value of the requested system information.</span></span> <span data-ttu-id="7391e-119">Тип возвращаемого значения зависит от того, какие сведения о системе запрашиваются.</span><span class="sxs-lookup"><span data-stu-id="7391e-119">The return type depends on which system information is requested.</span></span> <span data-ttu-id="7391e-120">Подробные сведения см. в разделе "Заметки".</span><span class="sxs-lookup"><span data-stu-id="7391e-120">See the Remarks section for details.</span></span>

## <a name="remarks"></a><span data-ttu-id="7391e-121">Remarks</span><span class="sxs-lookup"><span data-stu-id="7391e-121">Remarks</span></span>

<span data-ttu-id="7391e-122">Этот метод можно использовать для запроса многих значений системных сведений.</span><span class="sxs-lookup"><span data-stu-id="7391e-122">This method can be used to request many system information values.</span></span> <span data-ttu-id="7391e-123">В следующей таблице приводится значение *sName* , которое используется для запроса сведений и связанного типа возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="7391e-123">The following table gives the *sName* value that is used to request the information and the associated type of the returned value.</span></span>



<span data-ttu-id="7391e-124">*sName*</span><span class="sxs-lookup"><span data-stu-id="7391e-124">*sName*</span></span>

<span data-ttu-id="7391e-125">Возвращаемый тип</span><span class="sxs-lookup"><span data-stu-id="7391e-125">Return type</span></span>

<span data-ttu-id="7391e-126">Описание</span><span class="sxs-lookup"><span data-stu-id="7391e-126">Description</span></span>

<span data-ttu-id="7391e-127">директорисервицеаваилабле</span><span class="sxs-lookup"><span data-stu-id="7391e-127">DirectoryServiceAvailable</span></span>

<span data-ttu-id="7391e-128">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="7391e-128">**Boolean**</span></span>

<span data-ttu-id="7391e-129">Задайте **значение true** , если служба каталогов доступна. в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="7391e-129">Set to **true** if the directory service is available; otherwise, **false**.</span></span>

<span data-ttu-id="7391e-130">даублекликктиме</span><span class="sxs-lookup"><span data-stu-id="7391e-130">DoubleClickTime</span></span>

<span data-ttu-id="7391e-131">**Integer**</span><span class="sxs-lookup"><span data-stu-id="7391e-131">**Integer**</span></span>

<span data-ttu-id="7391e-132">Время двойного щелчка в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="7391e-132">The double-click time, in milliseconds.</span></span>

<span data-ttu-id="7391e-133">ProcessorLevel</span><span class="sxs-lookup"><span data-stu-id="7391e-133">ProcessorLevel</span></span>

<span data-ttu-id="7391e-134">**Integer**</span><span class="sxs-lookup"><span data-stu-id="7391e-134">**Integer**</span></span>

<span data-ttu-id="7391e-135">**Windows Vista и более поздние версии**.</span><span class="sxs-lookup"><span data-stu-id="7391e-135">**Windows Vista and later**.</span></span> <span data-ttu-id="7391e-136">Уровень процессора.</span><span class="sxs-lookup"><span data-stu-id="7391e-136">The processor level.</span></span> <span data-ttu-id="7391e-137">Возвращает 3, 4 или 5 для процессоров x386, x486 и Pentium-Level соответственно.</span><span class="sxs-lookup"><span data-stu-id="7391e-137">Returns 3, 4, or 5, for x386, x486, and Pentium-level processors, respectively.</span></span>

<span data-ttu-id="7391e-138">ProcessorSpeed</span><span class="sxs-lookup"><span data-stu-id="7391e-138">ProcessorSpeed</span></span>

<span data-ttu-id="7391e-139">**Integer**</span><span class="sxs-lookup"><span data-stu-id="7391e-139">**Integer**</span></span>

<span data-ttu-id="7391e-140">Скорость процессора в мегагерцах (МГц).</span><span class="sxs-lookup"><span data-stu-id="7391e-140">The processor speed, in megahertz (MHz).</span></span>

<span data-ttu-id="7391e-141">ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="7391e-141">ProcessorArchitecture</span></span>

<span data-ttu-id="7391e-142">**Integer**</span><span class="sxs-lookup"><span data-stu-id="7391e-142">**Integer**</span></span>

<span data-ttu-id="7391e-143">Архитектура процессора.</span><span class="sxs-lookup"><span data-stu-id="7391e-143">The processor architecture.</span></span> <span data-ttu-id="7391e-144">Дополнительные сведения см. в обсуждении члена **впроцессорарчитектуре** структуры [**System \_ info**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-system_info) .</span><span class="sxs-lookup"><span data-stu-id="7391e-144">For details, see the discussion of the **wProcessorArchitecture** member of the [**SYSTEM\_INFO**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-system_info) structure.</span></span>

<span data-ttu-id="7391e-145">фисикалмеморинсталлед</span><span class="sxs-lookup"><span data-stu-id="7391e-145">PhysicalMemoryInstalled</span></span>

<span data-ttu-id="7391e-146">**Integer**</span><span class="sxs-lookup"><span data-stu-id="7391e-146">**Integer**</span></span>

<span data-ttu-id="7391e-147">Объем установленной физической памяти в байтах.</span><span class="sxs-lookup"><span data-stu-id="7391e-147">The amount of physical memory installed, in bytes.</span></span>

<span data-ttu-id="7391e-148">Следующие действия допустимы только в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7391e-148">The following are valid only on Windows XP.</span></span>

<span data-ttu-id="7391e-149">ISO \_ Professional</span><span class="sxs-lookup"><span data-stu-id="7391e-149">IsOS\_Professional</span></span>

<span data-ttu-id="7391e-150">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="7391e-150">**Boolean**</span></span>

<span data-ttu-id="7391e-151">Задайте **значение true** , если операционная система является Windows XP Professional Edition. в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="7391e-151">Set to **true** if the operating system is Windows XP Professional Edition; otherwise, **false**.</span></span>

<span data-ttu-id="7391e-152">ISO \_ персональный</span><span class="sxs-lookup"><span data-stu-id="7391e-152">IsOS\_Personal</span></span>

<span data-ttu-id="7391e-153">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="7391e-153">**Boolean**</span></span>

<span data-ttu-id="7391e-154">Задайте **значение true** , если операционная система является Windows XP Home Edition. в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="7391e-154">Set to **true** if the operating system is Windows XP Home Edition; otherwise, **false**.</span></span>

<span data-ttu-id="7391e-155">Следующие действия применимы только в Windows XP и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="7391e-155">The following is valid only on Windows XP and later.</span></span>

<span data-ttu-id="7391e-156">ISO \_ домаинмембер</span><span class="sxs-lookup"><span data-stu-id="7391e-156">IsOS\_DomainMember</span></span>

<span data-ttu-id="7391e-157">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="7391e-157">**Boolean**</span></span>

<span data-ttu-id="7391e-158">Задайте **значение true** , если компьютер является членом домена. в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="7391e-158">Set to **true** if the computer is a member of a domain; otherwise, **false**.</span></span>



 

<span data-ttu-id="7391e-159">Этот метод в настоящее время недоступен в Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="7391e-159">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="7391e-160">Примеры</span><span class="sxs-lookup"><span data-stu-id="7391e-160">Examples</span></span>

<span data-ttu-id="7391e-161">В следующих примерах показано использование **жетсистеминформатион** для JScript и VBScript.</span><span class="sxs-lookup"><span data-stu-id="7391e-161">The following examples show the use of **GetSystemInformation** for JScript and VBScript.</span></span>

<span data-ttu-id="7391e-162">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="7391e-162">JScript:</span></span>


```JScript
<script language="JavaScript">
    function fnGetSystemInformationJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var vReturn;

        vReturn = objShell.GetSystemInformation("ProcessorLevel");
        document.write(vReturn);
    }
</script>
```



<span data-ttu-id="7391e-163">Сценариев</span><span class="sxs-lookup"><span data-stu-id="7391e-163">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnGetSystemInformationVB()
        dim objShell
        dim vReturn

        set objShell = CreateObject("shell.application")

        vReturn = objShell.GetSystemInformation("ProcessorLevel")
        document.write(vReturn)

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a><span data-ttu-id="7391e-164">Требования</span><span class="sxs-lookup"><span data-stu-id="7391e-164">Requirements</span></span>



| <span data-ttu-id="7391e-165">Требование</span><span class="sxs-lookup"><span data-stu-id="7391e-165">Requirement</span></span> | <span data-ttu-id="7391e-166">Значение</span><span class="sxs-lookup"><span data-stu-id="7391e-166">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7391e-167">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7391e-167">Minimum supported client</span></span><br/> | <span data-ttu-id="7391e-168">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="7391e-168">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7391e-169">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7391e-169">Minimum supported server</span></span><br/> | <span data-ttu-id="7391e-170">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7391e-170">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="7391e-171">Header</span><span class="sxs-lookup"><span data-stu-id="7391e-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="7391e-172"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="7391e-172"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="7391e-173">IDL</span><span class="sxs-lookup"><span data-stu-id="7391e-173">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7391e-174"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7391e-174"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="7391e-175">DLL</span><span class="sxs-lookup"><span data-stu-id="7391e-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7391e-176"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="7391e-176"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
