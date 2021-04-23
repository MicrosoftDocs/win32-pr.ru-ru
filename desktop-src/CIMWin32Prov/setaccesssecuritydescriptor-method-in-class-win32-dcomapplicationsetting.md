---
description: Обновляет дескриптор безопасности доступа DCOM-приложения с новым дескриптором безопасности, который определяется экземпляром \_ класса SecurityDescriptor Win32.
ms.assetid: 71b708ba-5eb7-400e-bee2-37ca93966c3f
ms.tgt_platform: multiple
title: Метод Сетакцесссекуритидескриптор класса Win32_DCOMApplicationSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DCOMApplicationSetting.SetAccessSecurityDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 53c0975475c5f20682ee77125b66ed703fbb4b9f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896434"
---
# <a name="setaccesssecuritydescriptor-method-of-the-win32_dcomapplicationsetting-class"></a><span data-ttu-id="c2c0f-103">Метод Сетакцесссекуритидескриптор \_ класса Win32 дкомаппликатионсеттинг</span><span class="sxs-lookup"><span data-stu-id="c2c0f-103">SetAccessSecurityDescriptor method of the Win32\_DCOMApplicationSetting class</span></span>

<span data-ttu-id="c2c0f-104">Метод **сетакцесссекуритидескриптор** обновляет дескриптор безопасности доступа DCOM-приложения с новым дескриптором безопасности, который определяется экземпляром класса [**\_ SecurityDescriptor Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .</span><span class="sxs-lookup"><span data-stu-id="c2c0f-104">The **SetAccessSecurityDescriptor** method updates the access security descriptor of the DCOM application with a new security descriptor that is defined by an instance of a [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class.</span></span> <span data-ttu-id="c2c0f-105">Этот дескриптор безопасности управляет доступом к приложению.</span><span class="sxs-lookup"><span data-stu-id="c2c0f-105">This security descriptor controls who is allowed to access the application.</span></span> <span data-ttu-id="c2c0f-106">Учетная запись, выполняющая скрипт или приложение, вызывающее этот метод, должна иметь права **SeSecurityPrivilege** и **сересторепривилеже** .</span><span class="sxs-lookup"><span data-stu-id="c2c0f-106">The account running the script or application that calls this method must have the **SeSecurityPrivilege** and **SeRestorePrivilege** privileges.</span></span> <span data-ttu-id="c2c0f-107">Дополнительные сведения см. [в разделе Изменение параметров безопасности доступа к защищаемым объектам](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects).</span><span class="sxs-lookup"><span data-stu-id="c2c0f-107">For more information, see [Changing Access Security on Securable Objects](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects).</span></span>

## <a name="syntax"></a><span data-ttu-id="c2c0f-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c2c0f-108">Syntax</span></span>


```mof
uint32 SetAccessSecurityDescriptor(
  [in] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a><span data-ttu-id="c2c0f-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="c2c0f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2c0f-110">*Дескриптор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c2c0f-110">*Descriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2c0f-111">Дескриптор безопасности, заданный для DCOM приложения.</span><span class="sxs-lookup"><span data-stu-id="c2c0f-111">The security descriptor to set for the DCOM application.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2c0f-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c2c0f-112">Return value</span></span>

<span data-ttu-id="c2c0f-113">Возвращает одно из значений, перечисленных в следующем списке, или другое значение, указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="c2c0f-113">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="c2c0f-114">Дополнительные сведения см. в статье [коды возврата WMI](/windows/desktop/WmiSdk/wmi-return-codes) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="c2c0f-114">For more information, see [WMI Return Codes](/windows/desktop/WmiSdk/wmi-return-codes) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

<dl> <dt>

<span data-ttu-id="c2c0f-115">**Успешно**</span><span class="sxs-lookup"><span data-stu-id="c2c0f-115">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="c2c0f-116">0</span><span class="sxs-lookup"><span data-stu-id="c2c0f-116">0</span></span>

<span data-ttu-id="c2c0f-117">Успешное завершение</span><span class="sxs-lookup"><span data-stu-id="c2c0f-117">Successful completion</span></span>

</dd> <dt>

<span data-ttu-id="c2c0f-118">**2**</span><span class="sxs-lookup"><span data-stu-id="c2c0f-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="c2c0f-119">У пользователя нет доступа к запрошенной информации</span><span class="sxs-lookup"><span data-stu-id="c2c0f-119">The user does not have access to the requested information</span></span>

</dd> <dt>

<span data-ttu-id="c2c0f-120">**8**</span><span class="sxs-lookup"><span data-stu-id="c2c0f-120">**8**</span></span>
</dt> <dd>

<span data-ttu-id="c2c0f-121">Неизвестный сбой</span><span class="sxs-lookup"><span data-stu-id="c2c0f-121">Unknown failure</span></span>

</dd> <dt>

<span data-ttu-id="c2c0f-122">**9**</span><span class="sxs-lookup"><span data-stu-id="c2c0f-122">**9**</span></span>
</dt> <dd>

<span data-ttu-id="c2c0f-123">У пользователя нет необходимых прав для выполнения метода</span><span class="sxs-lookup"><span data-stu-id="c2c0f-123">The user does not have adequate privileges to execute the method</span></span>

</dd> <dt>

<span data-ttu-id="c2c0f-124">**открыт**</span><span class="sxs-lookup"><span data-stu-id="c2c0f-124">**21**</span></span>
</dt> <dd>

<span data-ttu-id="c2c0f-125">Параметр, указанный в вызове метода, является недопустимым</span><span class="sxs-lookup"><span data-stu-id="c2c0f-125">A parameter specified in the method call is invalid</span></span>

</dd> <dt>

<span data-ttu-id="c2c0f-126">**Другое**</span><span class="sxs-lookup"><span data-stu-id="c2c0f-126">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="c2c0f-127">1 4294967295</span><span class="sxs-lookup"><span data-stu-id="c2c0f-127">1 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c2c0f-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c2c0f-128">Remarks</span></span>

<span data-ttu-id="c2c0f-129">Экземпляр [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) представляет тип данных [**\_ \_ элемента управления дескриптора безопасности**](/windows/desktop/SecAuthZ/security-descriptor-control) и содержит [*список управления доступом на уровне пользователей*](/windows/desktop/SecGloss/d-gly) (DACL) и [*системный список управления доступом*](/windows/desktop/SecGloss/s-gly) (SACL).</span><span class="sxs-lookup"><span data-stu-id="c2c0f-129">The [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance represents a [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) data type and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) and a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="c2c0f-130">Дополнительные сведения см. в разделе [списки управления доступом](/windows/desktop/SecAuthZ/access-control-lists).</span><span class="sxs-lookup"><span data-stu-id="c2c0f-130">For more information, see [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span></span>

<span data-ttu-id="c2c0f-131">Если параметр **SeSecurityPrivilege** не предоставлен или не включен при получении дескриптора безопасности, в возвращенном дескрипторе безопасности возвращается только список DACL.</span><span class="sxs-lookup"><span data-stu-id="c2c0f-131">If the **SeSecurityPrivilege** is not granted or enabled when getting a security descriptor, then only the DACL is returned in the returned security descriptor.</span></span> <span data-ttu-id="c2c0f-132">Дополнительные сведения см. в статьях [**константы прав**](/windows/desktop/WmiSdk/privilege-constants) и [выполнение привилегированных операций](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="c2c0f-132">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants) and [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

<span data-ttu-id="c2c0f-133">При вызове этого метода можно обновить списки DACL и SACL в экземпляре [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) , но вы также можете обновить только список DACL или только список SACL.</span><span class="sxs-lookup"><span data-stu-id="c2c0f-133">You can update both the DACL and the SACL in the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance when calling this method, but you also can update only the DACL or only the SACL.</span></span>

<span data-ttu-id="c2c0f-134">Следующие значения в [**\_ \_ элементе управления дескриптора безопасности**](/windows/desktop/SecAuthZ/security-descriptor-control) определяют, обновляются ли списки DACL, SACL или и то, и другое.</span><span class="sxs-lookup"><span data-stu-id="c2c0f-134">The following values in the [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) determine whether the DACL, the SACL, or both are updated.</span></span>

-   <span data-ttu-id="c2c0f-135">**\_присутствие DACL \_ SE**</span><span class="sxs-lookup"><span data-stu-id="c2c0f-135">**SE\_DACL\_PRESENT**</span></span>

    <span data-ttu-id="c2c0f-136">Указывает, что список DACL должен быть обновлен.</span><span class="sxs-lookup"><span data-stu-id="c2c0f-136">Indicates that the DACL should be updated.</span></span> <span data-ttu-id="c2c0f-137">Если этот параметр не задан, Инструментарий WMI сохраняет исходное значение DACL.</span><span class="sxs-lookup"><span data-stu-id="c2c0f-137">If this is not set, then WMI preserves the original value of the DACL.</span></span>

-   <span data-ttu-id="c2c0f-138">**\_имеется список SACL для SE \_**</span><span class="sxs-lookup"><span data-stu-id="c2c0f-138">**SE\_SACL\_PRESENT**</span></span>

    <span data-ttu-id="c2c0f-139">Указывает, что список SACL должен быть обновлен.</span><span class="sxs-lookup"><span data-stu-id="c2c0f-139">Indicates that the SACL should be updated.</span></span> <span data-ttu-id="c2c0f-140">Если этот параметр не задан, Инструментарий WMI сохраняет исходное значение списка SACL.</span><span class="sxs-lookup"><span data-stu-id="c2c0f-140">If this is not set, then WMI preserves the original value of the SACL.</span></span> <span data-ttu-id="c2c0f-141">Для обновления списка SACL учетная запись должна иметь права **SeSecurityPrivilege** .</span><span class="sxs-lookup"><span data-stu-id="c2c0f-141">To update the SACL, the account must have the **SeSecurityPrivilege** privilege enabled.</span></span> <span data-ttu-id="c2c0f-142">Для сценариев имя привилегии — **SeSecurityPrivilege**.</span><span class="sxs-lookup"><span data-stu-id="c2c0f-142">For scripting, the privilege name is **SeSecurityPrivilege**.</span></span> <span data-ttu-id="c2c0f-143">Дополнительные сведения см. в разделе [**константы прав доступа**](/windows/desktop/WmiSdk/privilege-constants).</span><span class="sxs-lookup"><span data-stu-id="c2c0f-143">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants).</span></span>

<span data-ttu-id="c2c0f-144">Если доверенное лицо группы и свойства доверенного лица владельца не равны **null**, они обновляются.</span><span class="sxs-lookup"><span data-stu-id="c2c0f-144">If the Group trustee and the Owner trustee properties are not **NULL**, then they are updated.</span></span> <span data-ttu-id="c2c0f-145">В противном случае Инструментарий WMI сохраняет исходные значения.</span><span class="sxs-lookup"><span data-stu-id="c2c0f-145">Otherwise, WMI preserves the original values.</span></span> <span data-ttu-id="c2c0f-146">Дополнительные сведения см. в разделе [объекты дескрипторов безопасности WMI](/windows/desktop/WmiSdk/wmi-security-descriptor-objects).</span><span class="sxs-lookup"><span data-stu-id="c2c0f-146">For more information, see [WMI Security Descriptor Objects](/windows/desktop/WmiSdk/wmi-security-descriptor-objects).</span></span>

<span data-ttu-id="c2c0f-147">Если при вызове этого метода новый список SACL имеет **значение NULL** , то список SACL дескриптора безопасности на целевом защищаемом объекте остается без изменений.</span><span class="sxs-lookup"><span data-stu-id="c2c0f-147">When a new SACL is **NULL** in a call to this method, then the security descriptor SACL on the target securable object is left unchanged.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2c0f-148">Требования</span><span class="sxs-lookup"><span data-stu-id="c2c0f-148">Requirements</span></span>



| <span data-ttu-id="c2c0f-149">Требование</span><span class="sxs-lookup"><span data-stu-id="c2c0f-149">Requirement</span></span> | <span data-ttu-id="c2c0f-150">Значение</span><span class="sxs-lookup"><span data-stu-id="c2c0f-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c2c0f-151">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c2c0f-151">Minimum supported client</span></span><br/> | <span data-ttu-id="c2c0f-152">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c2c0f-152">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c2c0f-153">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c2c0f-153">Minimum supported server</span></span><br/> | <span data-ttu-id="c2c0f-154">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c2c0f-154">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c2c0f-155">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c2c0f-155">Namespace</span></span><br/>                | <span data-ttu-id="c2c0f-156">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="c2c0f-156">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c2c0f-157">MOF</span><span class="sxs-lookup"><span data-stu-id="c2c0f-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c2c0f-158"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c2c0f-158"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c2c0f-159">DLL</span><span class="sxs-lookup"><span data-stu-id="c2c0f-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c2c0f-160"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c2c0f-160"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2c0f-161">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c2c0f-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2c0f-162">**\_Дкомаппликатионсеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="c2c0f-162">**Win32\_DCOMApplicationSetting**</span></span>](win32-dcomapplicationsetting.md)
</dt> <dt>

[<span data-ttu-id="c2c0f-163">**Константы прав доступа**</span><span class="sxs-lookup"><span data-stu-id="c2c0f-163">**Privilege Constants**</span></span>](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[<span data-ttu-id="c2c0f-164">Объекты дескрипторов безопасности WMI</span><span class="sxs-lookup"><span data-stu-id="c2c0f-164">WMI Security Descriptor Objects</span></span>](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[<span data-ttu-id="c2c0f-165">Изменение параметров безопасности доступа для защищаемых объектов</span><span class="sxs-lookup"><span data-stu-id="c2c0f-165">Changing Access Security on Securable Objects</span></span>](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> </dl>

 

