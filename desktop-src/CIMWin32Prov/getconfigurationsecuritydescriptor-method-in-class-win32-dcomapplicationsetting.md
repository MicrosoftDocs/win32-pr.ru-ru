---
description: Возвращает дескриптор безопасности, определяющий, кому разрешено настраивать DCOM-приложение.
ms.assetid: 2858a7a0-1e5b-47aa-9967-0f578c3c22c1
ms.tgt_platform: multiple
title: Метод Жетконфигуратионсекуритидескриптор класса Win32_DCOMApplicationSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DCOMApplicationSetting.GetConfigurationSecurityDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 320af05b352641c812c51353c2e7bda0da046bb8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807247"
---
# <a name="getconfigurationsecuritydescriptor-method-of-the-win32_dcomapplicationsetting-class"></a><span data-ttu-id="e7d02-103">Метод Жетконфигуратионсекуритидескриптор \_ класса Win32 дкомаппликатионсеттинг</span><span class="sxs-lookup"><span data-stu-id="e7d02-103">GetConfigurationSecurityDescriptor method of the Win32\_DCOMApplicationSetting class</span></span>

<span data-ttu-id="e7d02-104">Метод WMI **жетконфигуратионсекуритидескриптор** получает дескриптор безопасности, который определяет, кому разрешено настраивать DCOM-приложение.</span><span class="sxs-lookup"><span data-stu-id="e7d02-104">The **GetConfigurationSecurityDescriptor** WMI method gets the security descriptor that controls who is allowed to configure a DCOM application.</span></span> <span data-ttu-id="e7d02-105">Дескриптор безопасности является экземпляром класса [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .</span><span class="sxs-lookup"><span data-stu-id="e7d02-105">The security descriptor is a instance of the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class.</span></span> <span data-ttu-id="e7d02-106">Учетная запись, выполняющая скрипт или приложение, вызывающее этот метод, должна иметь права **SeSecurityPrivilege** и **сересторепривилеже** .</span><span class="sxs-lookup"><span data-stu-id="e7d02-106">The account running the script or application that calls this method must have the **SeSecurityPrivilege** and **SeRestorePrivilege** privileges.</span></span> <span data-ttu-id="e7d02-107">Дополнительные сведения см. [в разделе Изменение параметров безопасности доступа к защищаемым объектам](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects).</span><span class="sxs-lookup"><span data-stu-id="e7d02-107">For more information, see [Changing Access Security on Securable Objects](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects).</span></span>

## <a name="syntax"></a><span data-ttu-id="e7d02-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e7d02-108">Syntax</span></span>


```mof
uint32 GetConfigurationSecurityDescriptor(
  [out] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a><span data-ttu-id="e7d02-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="e7d02-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7d02-110">*Дескриптор* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e7d02-110">*Descriptor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e7d02-111">Дескриптор безопасности, заданный для DCOM приложения.</span><span class="sxs-lookup"><span data-stu-id="e7d02-111">The security descriptor to set for the DCOM application.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7d02-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e7d02-112">Return value</span></span>

<span data-ttu-id="e7d02-113">Возвращает одно из значений, перечисленных в следующем списке, или другое значение, указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="e7d02-113">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="e7d02-114">Дополнительные сведения см. в статье [коды возврата WMI](/windows/desktop/WmiSdk/wmi-return-codes) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="e7d02-114">For more information, see [WMI Return Codes](/windows/desktop/WmiSdk/wmi-return-codes) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

<dl> <dt>

<span data-ttu-id="e7d02-115">**Успешно**</span><span class="sxs-lookup"><span data-stu-id="e7d02-115">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="e7d02-116">0</span><span class="sxs-lookup"><span data-stu-id="e7d02-116">0</span></span>

<span data-ttu-id="e7d02-117">Успешное завершение</span><span class="sxs-lookup"><span data-stu-id="e7d02-117">Successful completion</span></span>

</dd> <dt>

<span data-ttu-id="e7d02-118">**2**</span><span class="sxs-lookup"><span data-stu-id="e7d02-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="e7d02-119">У пользователя нет доступа к запрошенной информации</span><span class="sxs-lookup"><span data-stu-id="e7d02-119">The user does not have access to the requested information</span></span>

</dd> <dt>

<span data-ttu-id="e7d02-120">**8**</span><span class="sxs-lookup"><span data-stu-id="e7d02-120">**8**</span></span>
</dt> <dd>

<span data-ttu-id="e7d02-121">Неизвестный сбой</span><span class="sxs-lookup"><span data-stu-id="e7d02-121">Unknown failure</span></span>

</dd> <dt>

<span data-ttu-id="e7d02-122">**9**</span><span class="sxs-lookup"><span data-stu-id="e7d02-122">**9**</span></span>
</dt> <dd>

<span data-ttu-id="e7d02-123">У пользователя нет необходимых прав для выполнения метода</span><span class="sxs-lookup"><span data-stu-id="e7d02-123">The user does not have adequate privileges to execute the method</span></span>

</dd> <dt>

<span data-ttu-id="e7d02-124">**открыт**</span><span class="sxs-lookup"><span data-stu-id="e7d02-124">**21**</span></span>
</dt> <dd>

<span data-ttu-id="e7d02-125">Параметр, указанный в вызове метода, является недопустимым</span><span class="sxs-lookup"><span data-stu-id="e7d02-125">A parameter specified in the method call is invalid</span></span>

</dd> <dt>

<span data-ttu-id="e7d02-126">**Другое**</span><span class="sxs-lookup"><span data-stu-id="e7d02-126">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="e7d02-127">1 4294967295</span><span class="sxs-lookup"><span data-stu-id="e7d02-127">1 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e7d02-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e7d02-128">Remarks</span></span>

<span data-ttu-id="e7d02-129">Экземпляр [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) представляет тип данных [**\_ \_ элемента управления дескриптора безопасности**](/windows/desktop/SecAuthZ/security-descriptor-control) и содержит [*список управления доступом на уровне пользователей*](/windows/desktop/SecGloss/d-gly) (DACL) и [*системный список управления доступом*](/windows/desktop/SecGloss/s-gly) (SACL).</span><span class="sxs-lookup"><span data-stu-id="e7d02-129">The [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance represents a [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) data type and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) and a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="e7d02-130">Дополнительные сведения см. в разделе [списки управления доступом](/windows/desktop/SecAuthZ/access-control-lists).</span><span class="sxs-lookup"><span data-stu-id="e7d02-130">For more information, see [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span></span>

<span data-ttu-id="e7d02-131">Если параметр **SeSecurityPrivilege** не предоставлен или не включен при получении дескриптора безопасности, в возвращенном дескрипторе безопасности возвращается только список DACL.</span><span class="sxs-lookup"><span data-stu-id="e7d02-131">If the **SeSecurityPrivilege** is not granted or enabled when getting a security descriptor, then only the DACL is returned in the returned security descriptor.</span></span> <span data-ttu-id="e7d02-132">Дополнительные сведения см. в статьях [**константы прав**](/windows/desktop/WmiSdk/privilege-constants) и [выполнение привилегированных операций](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="e7d02-132">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants) and [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

## <a name="requirements"></a><span data-ttu-id="e7d02-133">Требования</span><span class="sxs-lookup"><span data-stu-id="e7d02-133">Requirements</span></span>



| <span data-ttu-id="e7d02-134">Требование</span><span class="sxs-lookup"><span data-stu-id="e7d02-134">Requirement</span></span> | <span data-ttu-id="e7d02-135">Значение</span><span class="sxs-lookup"><span data-stu-id="e7d02-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e7d02-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e7d02-136">Minimum supported client</span></span><br/> | <span data-ttu-id="e7d02-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e7d02-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e7d02-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e7d02-138">Minimum supported server</span></span><br/> | <span data-ttu-id="e7d02-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e7d02-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e7d02-140">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e7d02-140">Namespace</span></span><br/>                | <span data-ttu-id="e7d02-141">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="e7d02-141">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e7d02-142">MOF</span><span class="sxs-lookup"><span data-stu-id="e7d02-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e7d02-143"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e7d02-143"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e7d02-144">DLL</span><span class="sxs-lookup"><span data-stu-id="e7d02-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7d02-145"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e7d02-145"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7d02-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e7d02-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7d02-147">**\_Дкомаппликатионсеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="e7d02-147">**Win32\_DCOMApplicationSetting**</span></span>](win32-dcomapplicationsetting.md)
</dt> <dt>

[<span data-ttu-id="e7d02-148">**Константы прав доступа**</span><span class="sxs-lookup"><span data-stu-id="e7d02-148">**Privilege Constants**</span></span>](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[<span data-ttu-id="e7d02-149">Объекты дескрипторов безопасности WMI</span><span class="sxs-lookup"><span data-stu-id="e7d02-149">WMI Security Descriptor Objects</span></span>](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[<span data-ttu-id="e7d02-150">Изменение параметров безопасности доступа для защищаемых объектов</span><span class="sxs-lookup"><span data-stu-id="e7d02-150">Changing Access Security on Securable Objects</span></span>](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> </dl>

 

