---
description: IShellDispatch2. Жетсистеминформатион, метод возвращает сведения о системе.
ms.assetid: 57c066e3-080f-4ecc-b56e-877f0569e901
title: IShellDispatch2. Жетсистеминформатион, метод (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.GetSystemInformation
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: a81ac091dc1905c1cbcd2c41575c907ce957e60c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117112"
---
# <a name="ishelldispatch2getsysteminformation-method"></a><span data-ttu-id="c5a75-103">IShellDispatch2. Жетсистеминформатион, метод</span><span class="sxs-lookup"><span data-stu-id="c5a75-103">IShellDispatch2.GetSystemInformation method</span></span>

<span data-ttu-id="c5a75-104">Возвращает сведения о системе.</span><span class="sxs-lookup"><span data-stu-id="c5a75-104">Retrieves system information.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5a75-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c5a75-105">Syntax</span></span>


```JScript
retVal = IShellDispatch2.GetSystemInformation(
  sName
)
```


```VB

IShellDispatch2.GetSystemInformation( _
  ByVal sName As BSTR _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="c5a75-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c5a75-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5a75-107">*sName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c5a75-107">*sName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5a75-108">Тип: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="c5a75-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="c5a75-109">**Строка** , указывающая запрашиваемую информацию о системе.</span><span class="sxs-lookup"><span data-stu-id="c5a75-109">A **String** that specifies the system information that is being requested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5a75-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c5a75-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="c5a75-111">Язык JScript</span><span class="sxs-lookup"><span data-stu-id="c5a75-111">JScript</span></span>

<span data-ttu-id="c5a75-112">Тип: **Variant**</span><span class="sxs-lookup"><span data-stu-id="c5a75-112">Type: **Variant**</span></span>

<span data-ttu-id="c5a75-113">Возвращает значение запрошенной системной информации.</span><span class="sxs-lookup"><span data-stu-id="c5a75-113">Returns the value of the requested system information.</span></span> <span data-ttu-id="c5a75-114">Тип возвращаемого значения зависит от того, какие сведения о системе запрашиваются.</span><span class="sxs-lookup"><span data-stu-id="c5a75-114">The return type depends on which system information is requested.</span></span> <span data-ttu-id="c5a75-115">Подробные сведения см. в разделе "Заметки".</span><span class="sxs-lookup"><span data-stu-id="c5a75-115">See the Remarks section for details.</span></span>

### <a name="vb"></a><span data-ttu-id="c5a75-116">VB</span><span class="sxs-lookup"><span data-stu-id="c5a75-116">VB</span></span>

<span data-ttu-id="c5a75-117">Тип: **Variant**</span><span class="sxs-lookup"><span data-stu-id="c5a75-117">Type: **Variant**</span></span>

<span data-ttu-id="c5a75-118">Возвращает значение запрошенной системной информации.</span><span class="sxs-lookup"><span data-stu-id="c5a75-118">Returns the value of the requested system information.</span></span> <span data-ttu-id="c5a75-119">Тип возвращаемого значения зависит от того, какие сведения о системе запрашиваются.</span><span class="sxs-lookup"><span data-stu-id="c5a75-119">The return type depends on which system information is requested.</span></span> <span data-ttu-id="c5a75-120">Подробные сведения см. в разделе "Заметки".</span><span class="sxs-lookup"><span data-stu-id="c5a75-120">See the Remarks section for details.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5a75-121">Remarks</span><span class="sxs-lookup"><span data-stu-id="c5a75-121">Remarks</span></span>

<span data-ttu-id="c5a75-122">Этот метод реализован и доступен через метод [**Shell. жетсистеминформатион**](./shell-getsysteminformation.md) .</span><span class="sxs-lookup"><span data-stu-id="c5a75-122">This method is implemented and accessed through the [**Shell.GetSystemInformation**](./shell-getsysteminformation.md) method.</span></span>

<span data-ttu-id="c5a75-123">Этот метод можно использовать для запроса многих значений системных сведений.</span><span class="sxs-lookup"><span data-stu-id="c5a75-123">This method can be used to request many system information values.</span></span> <span data-ttu-id="c5a75-124">В следующей таблице приводится значение *sName* , которое используется для запроса сведений и связанного типа возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="c5a75-124">The following table gives the *sName* value that is used to request the information and the associated type of the returned value.</span></span>



<span data-ttu-id="c5a75-125">*sName*</span><span class="sxs-lookup"><span data-stu-id="c5a75-125">*sName*</span></span>

<span data-ttu-id="c5a75-126">Возвращаемый тип</span><span class="sxs-lookup"><span data-stu-id="c5a75-126">Return type</span></span>

<span data-ttu-id="c5a75-127">Описание</span><span class="sxs-lookup"><span data-stu-id="c5a75-127">Description</span></span>

<span data-ttu-id="c5a75-128">директорисервицеаваилабле</span><span class="sxs-lookup"><span data-stu-id="c5a75-128">DirectoryServiceAvailable</span></span>

<span data-ttu-id="c5a75-129">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="c5a75-129">**Boolean**</span></span>

<span data-ttu-id="c5a75-130">Задайте **значение true** , если служба каталогов доступна. в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="c5a75-130">Set to **true** if the directory service is available; otherwise, **false**.</span></span>

<span data-ttu-id="c5a75-131">даублекликктиме</span><span class="sxs-lookup"><span data-stu-id="c5a75-131">DoubleClickTime</span></span>

<span data-ttu-id="c5a75-132">**Integer**</span><span class="sxs-lookup"><span data-stu-id="c5a75-132">**Integer**</span></span>

<span data-ttu-id="c5a75-133">Время двойного щелчка в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="c5a75-133">The double-click time, in milliseconds.</span></span>

<span data-ttu-id="c5a75-134">ProcessorLevel</span><span class="sxs-lookup"><span data-stu-id="c5a75-134">ProcessorLevel</span></span>

<span data-ttu-id="c5a75-135">**Integer**</span><span class="sxs-lookup"><span data-stu-id="c5a75-135">**Integer**</span></span>

<span data-ttu-id="c5a75-136">**Windows Vista и более поздние версии**.</span><span class="sxs-lookup"><span data-stu-id="c5a75-136">**Windows Vista and later**.</span></span> <span data-ttu-id="c5a75-137">Уровень процессора.</span><span class="sxs-lookup"><span data-stu-id="c5a75-137">The processor level.</span></span> <span data-ttu-id="c5a75-138">Возвращает 3, 4 или 5 для процессоров x386, x486 и Pentium-Level соответственно.</span><span class="sxs-lookup"><span data-stu-id="c5a75-138">Returns 3, 4, or 5, for x386, x486, and Pentium-level processors, respectively.</span></span>

<span data-ttu-id="c5a75-139">ProcessorSpeed</span><span class="sxs-lookup"><span data-stu-id="c5a75-139">ProcessorSpeed</span></span>

<span data-ttu-id="c5a75-140">**Integer**</span><span class="sxs-lookup"><span data-stu-id="c5a75-140">**Integer**</span></span>

<span data-ttu-id="c5a75-141">Скорость процессора в мегагерцах (МГц).</span><span class="sxs-lookup"><span data-stu-id="c5a75-141">The processor speed, in megahertz (MHz).</span></span>

<span data-ttu-id="c5a75-142">ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="c5a75-142">ProcessorArchitecture</span></span>

<span data-ttu-id="c5a75-143">**Integer**</span><span class="sxs-lookup"><span data-stu-id="c5a75-143">**Integer**</span></span>

<span data-ttu-id="c5a75-144">Архитектура процессора.</span><span class="sxs-lookup"><span data-stu-id="c5a75-144">The processor architecture.</span></span> <span data-ttu-id="c5a75-145">Дополнительные сведения см. в обсуждении члена **впроцессорарчитектуре** структуры [**System \_ info**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-system_info) .</span><span class="sxs-lookup"><span data-stu-id="c5a75-145">For details, see the discussion of the **wProcessorArchitecture** member of the [**SYSTEM\_INFO**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-system_info) structure.</span></span>

<span data-ttu-id="c5a75-146">фисикалмеморинсталлед</span><span class="sxs-lookup"><span data-stu-id="c5a75-146">PhysicalMemoryInstalled</span></span>

<span data-ttu-id="c5a75-147">**Integer**</span><span class="sxs-lookup"><span data-stu-id="c5a75-147">**Integer**</span></span>

<span data-ttu-id="c5a75-148">Объем установленной физической памяти в байтах.</span><span class="sxs-lookup"><span data-stu-id="c5a75-148">The amount of physical memory installed, in bytes.</span></span>

<span data-ttu-id="c5a75-149">Следующие действия допустимы только в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c5a75-149">The following are valid only on Windows XP.</span></span>

<span data-ttu-id="c5a75-150">ISO \_ Professional</span><span class="sxs-lookup"><span data-stu-id="c5a75-150">IsOS\_Professional</span></span>

<span data-ttu-id="c5a75-151">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="c5a75-151">**Boolean**</span></span>

<span data-ttu-id="c5a75-152">Задайте **значение true** , если операционная система является Windows XP Professional Edition. в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="c5a75-152">Set to **true** if the operating system is Windows XP Professional Edition; otherwise, **false**.</span></span>

<span data-ttu-id="c5a75-153">ISO \_ персональный</span><span class="sxs-lookup"><span data-stu-id="c5a75-153">IsOS\_Personal</span></span>

<span data-ttu-id="c5a75-154">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="c5a75-154">**Boolean**</span></span>

<span data-ttu-id="c5a75-155">Задайте **значение true** , если операционная система является Windows XP Home Edition. в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="c5a75-155">Set to **true** if the operating system is Windows XP Home Edition; otherwise, **false**.</span></span>

<span data-ttu-id="c5a75-156">Следующие действия применимы только в Windows XP и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="c5a75-156">The following is valid only on Windows XP and later.</span></span>

<span data-ttu-id="c5a75-157">ISO \_ домаинмембер</span><span class="sxs-lookup"><span data-stu-id="c5a75-157">IsOS\_DomainMember</span></span>

<span data-ttu-id="c5a75-158">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="c5a75-158">**Boolean**</span></span>

<span data-ttu-id="c5a75-159">Задайте **значение true** , если компьютер является членом домена. в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="c5a75-159">Set to **true** if the computer is a member of a domain; otherwise, **false**.</span></span>



 

<span data-ttu-id="c5a75-160">Этот метод в настоящее время недоступен в Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="c5a75-160">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="c5a75-161">Примеры</span><span class="sxs-lookup"><span data-stu-id="c5a75-161">Examples</span></span>

<span data-ttu-id="c5a75-162">В следующих примерах показано использование **жетсистеминформатион** для JScript и VBScript.</span><span class="sxs-lookup"><span data-stu-id="c5a75-162">The following examples show the use of **GetSystemInformation** for JScript and VBScript.</span></span>

<span data-ttu-id="c5a75-163">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="c5a75-163">JScript:</span></span>


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



<span data-ttu-id="c5a75-164">Сценариев</span><span class="sxs-lookup"><span data-stu-id="c5a75-164">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="c5a75-165">Требования</span><span class="sxs-lookup"><span data-stu-id="c5a75-165">Requirements</span></span>



| <span data-ttu-id="c5a75-166">Требование</span><span class="sxs-lookup"><span data-stu-id="c5a75-166">Requirement</span></span> | <span data-ttu-id="c5a75-167">Значение</span><span class="sxs-lookup"><span data-stu-id="c5a75-167">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5a75-168">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c5a75-168">Minimum supported client</span></span><br/> | <span data-ttu-id="c5a75-169">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="c5a75-169">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c5a75-170">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c5a75-170">Minimum supported server</span></span><br/> | <span data-ttu-id="c5a75-171">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c5a75-171">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="c5a75-172">Header</span><span class="sxs-lookup"><span data-stu-id="c5a75-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5a75-173"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5a75-173"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="c5a75-174">IDL</span><span class="sxs-lookup"><span data-stu-id="c5a75-174">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c5a75-175"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c5a75-175"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="c5a75-176">DLL</span><span class="sxs-lookup"><span data-stu-id="c5a75-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c5a75-177"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="c5a75-177"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
