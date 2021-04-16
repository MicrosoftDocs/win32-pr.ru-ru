---
description: Возвращает дескриптор безопасности для пространства имен, к которому подключен пользователь. Этот метод возвращает дескриптор безопасности в двоичном формате массива байтов. При написании скрипта используйте метод Жетсекуритидескриптор.
ms.assetid: aeac1e7b-fcb8-4880-afd1-4950da37602b
ms.tgt_platform: multiple
title: Получение метода класса __SystemSecurity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.GetSD
api_type:
- COM
api_location:
- All
ms.openlocfilehash: d471db22a9f15a38ab693ae72332e5e1893b5c55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702377"
---
# <a name="getsd-method-of-the-__systemsecurity-class"></a><span data-ttu-id="e32cd-105">Получение метода \_ \_ класса системсекурити</span><span class="sxs-lookup"><span data-stu-id="e32cd-105">GetSD method of the \_\_SystemSecurity class</span></span>

<span data-ttu-id="e32cd-106">Метод **получает** дескриптор безопасности для пространства имен, к которому подключен пользователь.</span><span class="sxs-lookup"><span data-stu-id="e32cd-106">The **GetSD** method gets the security descriptor for the namespace to which the user is connected.</span></span> <span data-ttu-id="e32cd-107">Этот метод возвращает дескриптор безопасности в двоичном формате массива байтов.</span><span class="sxs-lookup"><span data-stu-id="e32cd-107">This method returns a security descriptor in binary byte array format.</span></span> <span data-ttu-id="e32cd-108">При написании скрипта используйте метод [**жетсекуритидескриптор**](getsecuritydescriptor-method-in-class---systemsecurity-.md) .</span><span class="sxs-lookup"><span data-stu-id="e32cd-108">If you are writing a script, use the [**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md) method.</span></span> <span data-ttu-id="e32cd-109">Дополнительные сведения см. в разделе [Защита пространств имен WMI](securing-wmi-namespaces.md) и [изменение параметров безопасности доступа для защищаемых объектов](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="e32cd-109">For more information, see [Securing WMI Namespaces](securing-wmi-namespaces.md) and [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span>

<span data-ttu-id="e32cd-110">Пользователь должен иметь разрешение на **Чтение \_** .</span><span class="sxs-lookup"><span data-stu-id="e32cd-110">The user must have the **READ\_CONTROL** permission.</span></span> <span data-ttu-id="e32cd-111">По умолчанию у администраторов есть такое разрешение.</span><span class="sxs-lookup"><span data-stu-id="e32cd-111">By default, administrators have that permission.</span></span> <span data-ttu-id="e32cd-112">Единственной частью действительно используемого дескриптора безопасности является список управления доступом на уровне пользователей (DACL).</span><span class="sxs-lookup"><span data-stu-id="e32cd-112">The only part of the security descriptor that is actually used is the discretionary access control list (DACL).</span></span> <span data-ttu-id="e32cd-113">Список DACL может содержать как наследуемые, так и неунаследованные ACE.</span><span class="sxs-lookup"><span data-stu-id="e32cd-113">The DACL can contain both inherited and non-inherited ACEs.</span></span> <span data-ttu-id="e32cd-114">Разрешены и Deny, и Allow.</span><span class="sxs-lookup"><span data-stu-id="e32cd-114">Both deny and allow ACEs are permitted.</span></span>

<span data-ttu-id="e32cd-115">При программировании на C++ можно управлять двоичным дескриптором безопасности с помощью [SDDL](/windows/desktop/SecAuthZ/security-descriptor-definition-language), а также методами преобразования [**конвертсекуритидескриптортострингсекуритидескриптор**](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) и [**конвертстрингсекуритидескриптортосекуритидескриптор**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora).</span><span class="sxs-lookup"><span data-stu-id="e32cd-115">If you are programming in C++, you can manipulate the binary security descriptor using [SDDL](/windows/desktop/SecAuthZ/security-descriptor-definition-language), and the conversion methods [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) and [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora).</span></span>

## <a name="syntax"></a><span data-ttu-id="e32cd-116">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e32cd-116">Syntax</span></span>


```mof
HRESULT GetSD(
  [out] uint8 SD[]
);
```



## <a name="parameters"></a><span data-ttu-id="e32cd-117">Параметры</span><span class="sxs-lookup"><span data-stu-id="e32cd-117">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e32cd-118">*SD* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e32cd-118">*SD* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e32cd-119">Дескриптор безопасности в двоичном формате байтового массива.</span><span class="sxs-lookup"><span data-stu-id="e32cd-119">Security descriptor in binary byte array format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e32cd-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e32cd-120">Return value</span></span>

<span data-ttu-id="e32cd-121">Этот метод возвращает **значение HRESULT** , указывающее состояние вызова метода.</span><span class="sxs-lookup"><span data-stu-id="e32cd-121">This method returns an **HRESULT** indicating the status of the method call.</span></span> <span data-ttu-id="e32cd-122">В следующем списке перечислены возвращаемые значения, которые являются значимыми **для получения**.</span><span class="sxs-lookup"><span data-stu-id="e32cd-122">The following list lists the return values that are of significance to **GetSD**.</span></span> <span data-ttu-id="e32cd-123">Для сценариев и Visual Basic приложений результат можно получить из [параметров out. returnValue](parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="e32cd-123">For scripting and Visual Basic applications, the result can be obtained from [OutParameters.ReturnValue](parsing-outparameters-objects.md).</span></span> <span data-ttu-id="e32cd-124">Дополнительные сведения см. в разделе [Построение объектов параметров и анализ объектов параметров](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="e32cd-124">For more information, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span>

<dl> <dt>

<span data-ttu-id="e32cd-125">**\_ОК**</span><span class="sxs-lookup"><span data-stu-id="e32cd-125">**S\_OK**</span></span>
</dt> <dd>

<span data-ttu-id="e32cd-126">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="e32cd-126">Method executed successfully.</span></span>

</dd> <dt>

<span data-ttu-id="e32cd-127">**\_ \_ отказано в доступе к WBEM \_**</span><span class="sxs-lookup"><span data-stu-id="e32cd-127">**WBEM\_E\_ACCESS\_DENIED**</span></span>
</dt> <dd>

<span data-ttu-id="e32cd-128">Вызывающий объект не имеет достаточных прав для вызова этого метода.</span><span class="sxs-lookup"><span data-stu-id="e32cd-128">Caller does not have sufficient rights to call this method.</span></span>

</dd> <dt>

<span data-ttu-id="e32cd-129">**\_метод WBEM \_ E \_ отключен**</span><span class="sxs-lookup"><span data-stu-id="e32cd-129">**WBEM\_E\_METHOD\_DISABLED**</span></span>
</dt> <dd>

<span data-ttu-id="e32cd-130">Попытка запустить этот метод в неподдерживаемой системе.</span><span class="sxs-lookup"><span data-stu-id="e32cd-130">Attempted to run this method on an unsupported system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e32cd-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e32cd-131">Remarks</span></span>

<span data-ttu-id="e32cd-132">Дополнительные сведения об изменении безопасности пространства имен программным путем или вручную см. в разделе [Защита пространств имен WMI](securing-wmi-namespaces.md).</span><span class="sxs-lookup"><span data-stu-id="e32cd-132">For more information about modifying namespace security programmatically or manually, see [Securing WMI Namespaces](securing-wmi-namespaces.md).</span></span>

## <a name="examples"></a><span data-ttu-id="e32cd-133">Примеры</span><span class="sxs-lookup"><span data-stu-id="e32cd-133">Examples</span></span>

<span data-ttu-id="e32cd-134">Следующий скрипт показывает, как использовать метод **получает** , чтобы получить текущий дескриптор безопасности для корневого \\ пространства имен CIMV2 и изменить его на массив байтов, показанный в **отображении**.</span><span class="sxs-lookup"><span data-stu-id="e32cd-134">The following script shows you how to use **GetSD** to obtain the current security descriptor for the Root\\Cimv2 namespace and change it to the byte array shown in **DisplaySD**.</span></span>


```VB
Set objServices = GetObject("winmgmts:root\cimv2")
Set CimV2 = objServices.Get("__SystemSecurity=@")
ReturnValue = Cimv2.GetSD(arrSD)

If Err <> 0 Then
   WScript.Echo "Method returned error " & ReturnValue
End If

DisplaySD = "SD = {"
For I = Lbound(arrSD) To Ubound(arrSD)

   DisplaySD = DisplaySD & arrSD(I)

   If I <> Ubound(arrSD) Then
      DisplaySD = DisplaySD & ","
   End If

Next

DisplaySD = DisplaySD & "}"

WScript.Echo DisplaySD
```



## <a name="requirements"></a><span data-ttu-id="e32cd-135">Требования</span><span class="sxs-lookup"><span data-stu-id="e32cd-135">Requirements</span></span>



| <span data-ttu-id="e32cd-136">Требование</span><span class="sxs-lookup"><span data-stu-id="e32cd-136">Requirement</span></span> | <span data-ttu-id="e32cd-137">Значение</span><span class="sxs-lookup"><span data-stu-id="e32cd-137">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="e32cd-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e32cd-138">Minimum supported client</span></span><br/> | <span data-ttu-id="e32cd-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e32cd-139">Windows Vista</span></span><br/>       |
| <span data-ttu-id="e32cd-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e32cd-140">Minimum supported server</span></span><br/> | <span data-ttu-id="e32cd-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e32cd-141">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="e32cd-142">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e32cd-142">Namespace</span></span><br/>                | <span data-ttu-id="e32cd-143">Все пространства имен WMI</span><span class="sxs-lookup"><span data-stu-id="e32cd-143">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="e32cd-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e32cd-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e32cd-145">Системные классы WMI</span><span class="sxs-lookup"><span data-stu-id="e32cd-145">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="e32cd-146">**\_\_системсекурити**</span><span class="sxs-lookup"><span data-stu-id="e32cd-146">**\_\_SystemSecurity**</span></span>](--systemsecurity.md)
</dt> <dt>

[<span data-ttu-id="e32cd-147">Константы безопасности WMI</span><span class="sxs-lookup"><span data-stu-id="e32cd-147">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> <dt>

[<span data-ttu-id="e32cd-148">**\_ACE Win32**</span><span class="sxs-lookup"><span data-stu-id="e32cd-148">**Win32\_ACE**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[<span data-ttu-id="e32cd-149">**\_\_Системсекурити:: настраивается**</span><span class="sxs-lookup"><span data-stu-id="e32cd-149">**\_\_SystemSecurity::SetSD**</span></span>](--systemsecurity-setsd.md)
</dt> <dt>

[<span data-ttu-id="e32cd-150">**\_Дескриптор безопасности**</span><span class="sxs-lookup"><span data-stu-id="e32cd-150">**Security\_Descriptor**</span></span>](/windows/desktop/api/winnt/ns-winnt-security_descriptor)
</dt> <dt>

[<span data-ttu-id="e32cd-151">**\_SecurityDescriptor Win32**</span><span class="sxs-lookup"><span data-stu-id="e32cd-151">**Win32\_SecurityDescriptor**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[<span data-ttu-id="e32cd-152">Защита пространств имен WMI</span><span class="sxs-lookup"><span data-stu-id="e32cd-152">Securing WMI Namespaces</span></span>](securing-wmi-namespaces.md)
</dt> </dl>

 

