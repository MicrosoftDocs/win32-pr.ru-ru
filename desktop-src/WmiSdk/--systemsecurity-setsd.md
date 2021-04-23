---
description: Задает дескриптор безопасности для пространства имен, к которому подключен пользователь. Этот метод требует наличия дескриптора безопасности в двоичном формате массива байтов. При написании скрипта используйте метод Сетсекуритидескриптор.
ms.assetid: 049f8722-1674-4c4f-9300-09b1cc1412fb
ms.tgt_platform: multiple
title: Набор методов класса __SystemSecurity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.SetSD
api_type:
- COM
api_location:
- All
ms.openlocfilehash: 21f09a412a662cec8629fa9237d8dbb5902426c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683600"
---
# <a name="setsd-method-of-the-__systemsecurity-class"></a><span data-ttu-id="9699d-105">Набор методов \_ \_ класса системсекурити</span><span class="sxs-lookup"><span data-stu-id="9699d-105">SetSD method of the \_\_SystemSecurity class</span></span>

<span data-ttu-id="9699d-106">Этот **метод задает** дескриптор безопасности для пространства имен, к которому подключен пользователь.</span><span class="sxs-lookup"><span data-stu-id="9699d-106">The **SetSD** method sets the security descriptor for the namespace to which a user is connected.</span></span> <span data-ttu-id="9699d-107">Этот метод требует наличия дескриптора безопасности в двоичном формате массива байтов.</span><span class="sxs-lookup"><span data-stu-id="9699d-107">This method requires a security descriptor in binary byte array format.</span></span> <span data-ttu-id="9699d-108">При написании скрипта используйте метод [**сетсекуритидескриптор**](setsecuritydescriptor-method-in-class---systemsecurity.md) .</span><span class="sxs-lookup"><span data-stu-id="9699d-108">If you are writing a script, use the [**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class---systemsecurity.md) method.</span></span> <span data-ttu-id="9699d-109">Дополнительные сведения см. в разделе [Защита пространств имен WMI](securing-wmi-namespaces.md) и [изменение параметров безопасности доступа для защищаемых объектов](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="9699d-109">For more information, see [Securing WMI Namespaces](securing-wmi-namespaces.md) and [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span>

<span data-ttu-id="9699d-110">При программировании на C++ можно управлять двоичным дескриптором безопасности с помощью [SDDL](/windows/desktop/SecAuthZ/security-descriptor-definition-language), а также методами преобразования [**конвертсекуритидескриптортострингсекуритидескриптор**](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) и [**конвертстрингсекуритидескриптортосекуритидескриптор**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora).</span><span class="sxs-lookup"><span data-stu-id="9699d-110">If you are programming in C++, you can manipulate the binary security descriptor using [SDDL](/windows/desktop/SecAuthZ/security-descriptor-definition-language), and the conversion methods [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) and [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora).</span></span>

<span data-ttu-id="9699d-111">Пользователь должен иметь разрешение на **запись \_ DAC** , и по умолчанию администратор имеет соответствующее разрешение.</span><span class="sxs-lookup"><span data-stu-id="9699d-111">A user must have the **WRITE\_DAC** permission, and by default, an administrator has that permission.</span></span> <span data-ttu-id="9699d-112">Единственной частью используемого дескриптора безопасности является неунаследованный элемент управления доступом (ACE) в списке управления доступом на уровне пользователей (DACL).</span><span class="sxs-lookup"><span data-stu-id="9699d-112">The only part of the security descriptor that is used is the noninherited access control entry (ACE) in the discretionary access control list (DACL).</span></span> <span data-ttu-id="9699d-113">Установив флаг **\_ наследования контейнера** в ACE, дескриптор безопасности влияет на дочерние пространства имен.</span><span class="sxs-lookup"><span data-stu-id="9699d-113">By setting the **CONTAINER\_INHERIT** flag in the ACEs, the security descriptor affects child namespaces.</span></span> <span data-ttu-id="9699d-114">Разрешены и запрещены ACE.</span><span class="sxs-lookup"><span data-stu-id="9699d-114">Both allow and deny ACEs are permitted.</span></span>

> [!Note]  
> <span data-ttu-id="9699d-115">Так как запрещено использовать ACE Deny и Allow в списке DACL, важен порядок записей ACE.</span><span class="sxs-lookup"><span data-stu-id="9699d-115">Because deny and allow ACEs are both permitted in a DACL, the order of ACEs is important.</span></span> <span data-ttu-id="9699d-116">Дополнительные сведения см. [в разделе Упорядочение записей ACE в списке DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).</span><span class="sxs-lookup"><span data-stu-id="9699d-116">For more information, see [Ordering of ACEs in a DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="9699d-117">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9699d-117">Syntax</span></span>


```mof
HRESULT SetSD(
  [in] uint8 SD[]
);
```



## <a name="parameters"></a><span data-ttu-id="9699d-118">Параметры</span><span class="sxs-lookup"><span data-stu-id="9699d-118">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9699d-119">*SD* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9699d-119">*SD* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9699d-120">Массив байтов, составляющий дескриптор безопасности.</span><span class="sxs-lookup"><span data-stu-id="9699d-120">Byte array that makes up the security descriptor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9699d-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9699d-121">Return value</span></span>

<span data-ttu-id="9699d-122">Возвращает **значение HRESULT** , указывающее состояние вызова метода.</span><span class="sxs-lookup"><span data-stu-id="9699d-122">Returns an **HRESULT** that indicates the status of a method call.</span></span> <span data-ttu-id="9699d-123">Для сценариев и Visual Basic приложений результат можно получить из [параметров out. returnValue](parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="9699d-123">For scripting and Visual Basic applications, the result can be obtained from [OutParameters.ReturnValue](parsing-outparameters-objects.md).</span></span> <span data-ttu-id="9699d-124">Дополнительные сведения см. в разделе [Построение объектов параметров и анализ объектов параметров](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="9699d-124">For more information, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span>

<span data-ttu-id="9699d-125">В следующем списке перечислены возвращаемые значения, которые являются значимыми для **набора**.</span><span class="sxs-lookup"><span data-stu-id="9699d-125">The following list lists the return values that are significant to **SetSD**.</span></span>

<dl> <dt>

<span data-ttu-id="9699d-126">**\_ОК**</span><span class="sxs-lookup"><span data-stu-id="9699d-126">**S\_OK**</span></span>
</dt> <dd>

<span data-ttu-id="9699d-127">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="9699d-127">Method executed successfully.</span></span>

</dd> <dt>

<span data-ttu-id="9699d-128">**\_ \_ отказано в доступе к WBEM \_**</span><span class="sxs-lookup"><span data-stu-id="9699d-128">**WBEM\_E\_ACCESS\_DENIED**</span></span>
</dt> <dd>

<span data-ttu-id="9699d-129">Вызывающий объект не имеет достаточных прав для вызова этого метода.</span><span class="sxs-lookup"><span data-stu-id="9699d-129">Caller does not have sufficient rights to call this method.</span></span>

</dd> <dt>

<span data-ttu-id="9699d-130">**\_метод WBEM \_ E \_ отключен**</span><span class="sxs-lookup"><span data-stu-id="9699d-130">**WBEM\_E\_METHOD\_DISABLED**</span></span>
</dt> <dd>

<span data-ttu-id="9699d-131">Попытка запуска этого метода в ОС, которая не поддерживает этот метод.</span><span class="sxs-lookup"><span data-stu-id="9699d-131">Attempted to run this method on OS that does not support it.</span></span>

</dd> <dt>

<span data-ttu-id="9699d-132">**\_ \_ Недопустимый \_ объект для WBEM**</span><span class="sxs-lookup"><span data-stu-id="9699d-132">**WBEM\_E\_INVALID\_OBJECT**</span></span>
</dt> <dd>

<span data-ttu-id="9699d-133">SD не передает базовые тесты проверки действительности.</span><span class="sxs-lookup"><span data-stu-id="9699d-133">SD does not pass basic validity tests.</span></span>

</dd> <dt>

<span data-ttu-id="9699d-134">**\_ \_ Недопустимый параметр "WBEM E" \_**</span><span class="sxs-lookup"><span data-stu-id="9699d-134">**WBEM\_E\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="9699d-135">SD является недопустимым по следующей причине:</span><span class="sxs-lookup"><span data-stu-id="9699d-135">SD is not valid due to one of the following:</span></span>

-   <span data-ttu-id="9699d-136">Отсутствует список DACL.</span><span class="sxs-lookup"><span data-stu-id="9699d-136">DACL is missing.</span></span>
-   <span data-ttu-id="9699d-137">Недопустимый список DACL.</span><span class="sxs-lookup"><span data-stu-id="9699d-137">DACL is not valid.</span></span>
-   <span data-ttu-id="9699d-138">В записи ACE установлен флаг " **\_ полная \_ запись \_ " WBEM** , а не установлен флаг **\_ \_ поставщика** **\_ частичной \_ записи \_** или WBEM.</span><span class="sxs-lookup"><span data-stu-id="9699d-138">ACE has the **WBEM\_FULL\_WRITE\_REP** flag set, and the **WBEM\_PARTIAL\_WRITE\_REP** or **WBEM\_WRITE\_PROVIDER** flag is not set.</span></span>
-   <span data-ttu-id="9699d-139">ACE имеет установленный флаг **наследования \_ \_ ACE only** без флага **\_ наследования контейнера \_ ACE** .</span><span class="sxs-lookup"><span data-stu-id="9699d-139">ACE has the **INHERIT\_ONLY\_ACE** flag set without the **CONTAINER\_INHERIT\_ACE** flag.</span></span>
-   <span data-ttu-id="9699d-140">В записи ACE задан неизвестный бит доступа.</span><span class="sxs-lookup"><span data-stu-id="9699d-140">ACE has an unknown access bit set.</span></span>
-   <span data-ttu-id="9699d-141">ACE имеет установленный флаг, который отсутствует в таблице.</span><span class="sxs-lookup"><span data-stu-id="9699d-141">ACE has a flag set that is not in the table.</span></span>
-   <span data-ttu-id="9699d-142">ACE имеет тип, который отсутствует в таблице.</span><span class="sxs-lookup"><span data-stu-id="9699d-142">ACE has a type that is not in the table.</span></span>
-   <span data-ttu-id="9699d-143">Владелец и группа отсутствуют в SD.</span><span class="sxs-lookup"><span data-stu-id="9699d-143">The owner and group are missing from the SD.</span></span>

<span data-ttu-id="9699d-144">Дополнительные сведения о флагах записи управления доступом (ACE) см. в разделе [константы безопасности WMI](wmi-security-constants.md).</span><span class="sxs-lookup"><span data-stu-id="9699d-144">For more information about the access control entry (ACE) flags, see [WMI Security Constants](wmi-security-constants.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9699d-145">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9699d-145">Remarks</span></span>

<span data-ttu-id="9699d-146">Дополнительные сведения об изменении безопасности пространства имен программным путем или вручную см. в разделе [Защита пространств имен WMI](securing-wmi-namespaces.md).</span><span class="sxs-lookup"><span data-stu-id="9699d-146">For more information about modifying namespace security programmatically or manually, see [Securing WMI Namespaces](securing-wmi-namespaces.md).</span></span>

## <a name="examples"></a><span data-ttu-id="9699d-147">Примеры</span><span class="sxs-lookup"><span data-stu-id="9699d-147">Examples</span></span>

<span data-ttu-id="9699d-148">В следующем скрипте **показано, как использовать** setd, чтобы задать дескриптор безопасности пространства имен для корневого пространства имен и изменить его на массив байтов, показанный в *стрсд*.</span><span class="sxs-lookup"><span data-stu-id="9699d-148">The following script shows how to use **SetSD** to set the namespace security descriptor for the root namespace and change it to the byte array shown in *strSD*.</span></span>


```VB
' Hard-coded security descriptor
strSD = array( 1, 0, 4,129,72, 0, 0, 0, _ 
              88, 0, 0,  0, 0, 0, 0, 0, _
              20, 0, 0,  0, 2, 0,52, 0, _
               2, 0, 0,  0, 0, 2,24, 0, _
              63, 0, 6,  0, 1, 2, 0, 0, _
               0, 0, 0,  5,32, 0, 0, 0, _
              32, 2, 0,  0, 0, 2,20, 0, _
              63, 0, 6,  0, 1, 1, 0, 0, _
               0, 0, 0,  1, 0, 0, 0, 0, _
               1, 2, 0,  0, 0, 0, 0, 5, _
              32, 0, 0,  0,32, 2, 0, 0, _
               1, 2, 0,  0, 0, 0, 0, 5, _
              32, 0, 0,  0,32, 2, 0, 0)

' Connect to WMI and the root namespace.
Set oSvc = CreateObject( _
                         "WbemScripting.SWbemLocator"). _
                         ConnectServer(,"Root\Cimv2")

' Get the single __SystemSecurity object in this namespace.
Set oSecurity = oSvc.Get("__SystemSecurity=@")

' Change the namespace security.
nReturn = oSecurity.SetSD(strSD)
WScript.Echo "ReturnValue " & nReturn
```



<span data-ttu-id="9699d-149">В следующем примере кода C# используется System. Security. AccessControl. Равсекуритидескриптор для перечисления, вставки и удаления новых объектов Коммонаце в Равсекуритидескриптор. Дискретионарякл и последующего преобразования обратно в массив байтов, чтобы сохранить его посредством набора.</span><span class="sxs-lookup"><span data-stu-id="9699d-149">The following C# code sample uses the System.Security.AccessControl.RawSecurityDescriptor to enumerate, insert and remove new CommonAce objects in RawSecurityDescriptor.DiscretionaryAcl and then convert it back to an byte array to save it via SetSD.</span></span> <span data-ttu-id="9699d-150">SecurityIdentifier можно получить с помощью NTAccount и преобразования.</span><span class="sxs-lookup"><span data-stu-id="9699d-150">An SecurityIdentifier can be retrieved by using NTAccount and Translate.</span></span>


```CSharp
 byte[] sdValueByteArray = new Byte[0];

            string accountName = "My User or Group";

            AceFlags aceFlags = AceFlags.ContainerInherit;

            int accessRights = 131107; // Search for Namespace Access Rights Constants and build an Flags enum

            RawSecurityDescriptor rawSecurityDescriptor = new RawSecurityDescriptor(sdValueByteArray, 0);

            NTAccount ntAccount = new NTAccount(accountName);

            IdentityReference identityReference = ntAccount.Translate(typeof(SecurityIdentifier));

            if (identityReference == null)

            {

                string message = string.Format("The IdentityReference of NTAccount '{0}' is null.", accountName);

                throw new Exception(message);

            }

            SecurityIdentifier securityIdentifier = identityReference as SecurityIdentifier;

            if (securityIdentifier == null)

            {

                string message = "The IdentityReference of NTAccount '{0}' is not an SecurityIdentifier.";

                throw new Exception(message);

            }

            CommonAce commonAce;

            foreach (GenericAce genericAce in rawSecurityDescriptor.DiscretionaryAcl)

            {

                commonAce = genericAce as CommonAce;

                if (commonAce == null)

                {

                    continue;

                }

                if (commonAce.SecurityIdentifier.Value.Equals(securityIdentifier.Value, StringComparison.OrdinalIgnoreCase))

                {

                    return;

                }

            }

            commonAce = new CommonAce(aceFlags, AceQualifier.AccessAllowed, (int)accessRights, securityIdentifier, false, null);

            rawSecurityDescriptor.DiscretionaryAcl.InsertAce(rawSecurityDescriptor.DiscretionaryAcl.Count, commonAce);

```



## <a name="requirements"></a><span data-ttu-id="9699d-151">Требования</span><span class="sxs-lookup"><span data-stu-id="9699d-151">Requirements</span></span>



| <span data-ttu-id="9699d-152">Требование</span><span class="sxs-lookup"><span data-stu-id="9699d-152">Requirement</span></span> | <span data-ttu-id="9699d-153">Значение</span><span class="sxs-lookup"><span data-stu-id="9699d-153">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="9699d-154">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9699d-154">Minimum supported client</span></span><br/> | <span data-ttu-id="9699d-155">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9699d-155">Windows Vista</span></span><br/>       |
| <span data-ttu-id="9699d-156">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9699d-156">Minimum supported server</span></span><br/> | <span data-ttu-id="9699d-157">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9699d-157">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="9699d-158">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="9699d-158">Namespace</span></span><br/>                | <span data-ttu-id="9699d-159">Все пространства имен WMI</span><span class="sxs-lookup"><span data-stu-id="9699d-159">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="9699d-160">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9699d-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9699d-161">Системные классы WMI</span><span class="sxs-lookup"><span data-stu-id="9699d-161">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="9699d-162">**\_\_системсекурити**</span><span class="sxs-lookup"><span data-stu-id="9699d-162">**\_\_SystemSecurity**</span></span>](--systemsecurity.md)
</dt> <dt>

[<span data-ttu-id="9699d-163">**\_\_Системсекурити:: получает**</span><span class="sxs-lookup"><span data-stu-id="9699d-163">**\_\_SystemSecurity::GetSD**</span></span>](--systemsecurity-getsd.md)
</dt> <dt>

[<span data-ttu-id="9699d-164">Константы безопасности WMI</span><span class="sxs-lookup"><span data-stu-id="9699d-164">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> <dt>

[<span data-ttu-id="9699d-165">**\_ACE Win32**</span><span class="sxs-lookup"><span data-stu-id="9699d-165">**Win32\_ACE**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[<span data-ttu-id="9699d-166">**\_SecurityDescriptor Win32**</span><span class="sxs-lookup"><span data-stu-id="9699d-166">**Win32\_SecurityDescriptor**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[<span data-ttu-id="9699d-167">Защита пространств имен WMI</span><span class="sxs-lookup"><span data-stu-id="9699d-167">Securing WMI Namespaces</span></span>](securing-wmi-namespaces.md)
</dt> </dl>

 

