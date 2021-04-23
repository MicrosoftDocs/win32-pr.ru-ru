---
description: Записывает обновленную версию дескриптора безопасности, которая управляет доступом к пространству имен WMI, к которому вы подключены. Дескриптор безопасности представлен экземпляром \_ \_ SecurityDescriptor.
ms.assetid: e92430fd-61b1-4986-88dc-b85f502f62e6
ms.tgt_platform: multiple
title: Метод Сетсекуритидескриптор класса __SystemSecurity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.SetSecurityDescriptor
api_type:
- COM
api_location:
- All
ms.openlocfilehash: fcdc192801b839451cee256f57090780818d2046
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702559"
---
# <a name="setsecuritydescriptor-method-of-the-__systemsecurity-class"></a><span data-ttu-id="5a832-104">Метод Сетсекуритидескриптор \_ \_ класса системсекурити</span><span class="sxs-lookup"><span data-stu-id="5a832-104">SetSecurityDescriptor method of the \_\_SystemSecurity class</span></span>

<span data-ttu-id="5a832-105">Метод [**сетсекуритидескриптор**](/windows/desktop/CIMWin32Prov/setsecuritydescriptor-method-in-class-win32-printer) записывает обновленную версию дескриптора безопасности, которая управляет доступом к пространству имен WMI, к которому вы подключены.</span><span class="sxs-lookup"><span data-stu-id="5a832-105">The [**SetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/setsecuritydescriptor-method-in-class-win32-printer) method writes an updated version of the security descriptor that controls access to the WMI namespace to which you are connected.</span></span> <span data-ttu-id="5a832-106">Дескриптор безопасности представлен экземпляром [**\_ \_ SecurityDescriptor**](--securitydescriptor.md).</span><span class="sxs-lookup"><span data-stu-id="5a832-106">The security descriptor is represented by an instance of [**\_\_SecurityDescriptor**](--securitydescriptor.md).</span></span> <span data-ttu-id="5a832-107">Дополнительные сведения см. [в разделе Изменение параметров безопасности доступа к защищаемым объектам](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="5a832-107">For more information, see [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5a832-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5a832-108">Syntax</span></span>


```mof
uint32 SetSecurityDescriptor(
  [in] __SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a><span data-ttu-id="5a832-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="5a832-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a832-110">*Дескриптор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5a832-110">*Descriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a832-111">Дескриптор безопасности, связанный с пространством имен WMI.</span><span class="sxs-lookup"><span data-stu-id="5a832-111">The security descriptor associated with the WMI Namespace.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a832-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5a832-112">Return value</span></span>

<span data-ttu-id="5a832-113">Возвращает одно из значений, перечисленных в следующем списке, или другое значение, указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="5a832-113">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="5a832-114">Дополнительные сведения см. в статье [коды возврата WMI](wmi-return-codes.md) или [**вбемерроренум**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="5a832-114">For more information, see [WMI Return Codes](wmi-return-codes.md) or [**WbemErrorEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

<dl> <dt>

<span data-ttu-id="5a832-115">**0**</span><span class="sxs-lookup"><span data-stu-id="5a832-115">**0**</span></span>
</dt> <dd>

<span data-ttu-id="5a832-116">Успешное завершение.</span><span class="sxs-lookup"><span data-stu-id="5a832-116">Successful completion.</span></span>

</dd> <dt>

<span data-ttu-id="5a832-117">**2**</span><span class="sxs-lookup"><span data-stu-id="5a832-117">**2**</span></span>
</dt> <dd>

<span data-ttu-id="5a832-118">У пользователя нет доступа к запрошенной информации.</span><span class="sxs-lookup"><span data-stu-id="5a832-118">The user does not have access to the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="5a832-119">**8**</span><span class="sxs-lookup"><span data-stu-id="5a832-119">**8**</span></span>
</dt> <dd>

<span data-ttu-id="5a832-120">Неизвестный сбой.</span><span class="sxs-lookup"><span data-stu-id="5a832-120">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="5a832-121">**9**</span><span class="sxs-lookup"><span data-stu-id="5a832-121">**9**</span></span>
</dt> <dd>

<span data-ttu-id="5a832-122">У пользователя нет необходимых прав для выполнения метода.</span><span class="sxs-lookup"><span data-stu-id="5a832-122">The user does not have adequate privileges to execute the method.</span></span>

</dd> <dt>

<span data-ttu-id="5a832-123">**открыт**</span><span class="sxs-lookup"><span data-stu-id="5a832-123">**21**</span></span>
</dt> <dd>

<span data-ttu-id="5a832-124">В вызове метода указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="5a832-124">A parameter specified in the method call is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5a832-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5a832-125">Remarks</span></span>

<span data-ttu-id="5a832-126">Экземпляр [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) представляет тип данных [**\_ \_ элемента управления дескриптора безопасности**](/windows/desktop/SecAuthZ/security-descriptor-control) и содержит [*список управления доступом на уровне пользователей*](/windows/desktop/SecGloss/d-gly) (DACL) и [*системный список управления доступом*](/windows/desktop/SecGloss/a-gly) (SACL).</span><span class="sxs-lookup"><span data-stu-id="5a832-126">The [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance represents a [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) data type and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) and a [*System Access Control List*](/windows/desktop/SecGloss/a-gly) (SACL).</span></span> <span data-ttu-id="5a832-127">Дополнительные сведения см. в разделе [списки управления доступом](/windows/desktop/SecAuthZ/access-control-lists).</span><span class="sxs-lookup"><span data-stu-id="5a832-127">For more information, see [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span></span>

<span data-ttu-id="5a832-128">Если параметр **SeSecurityPrivilege** не предоставлен или не включен при получении дескриптора безопасности, в возвращенном дескрипторе безопасности возвращается только список DACL.</span><span class="sxs-lookup"><span data-stu-id="5a832-128">If the **SeSecurityPrivilege** is not granted or enabled when getting a security descriptor, then only the DACL is returned in the returned security descriptor.</span></span> <span data-ttu-id="5a832-129">Дополнительные сведения см. в статьях [**константы прав**](privilege-constants.md) и [выполнение привилегированных операций](executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="5a832-129">For more information, see [**Privilege Constants**](privilege-constants.md) and [Executing Privileged Operations](executing-privileged-operations.md).</span></span>

<span data-ttu-id="5a832-130">При вызове этого метода можно обновить списки DACL и SACL в экземпляре [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) , но вы также можете обновить только список DACL или только список SACL.</span><span class="sxs-lookup"><span data-stu-id="5a832-130">You can update both the DACL and the SACL in the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance when calling this method, but you also can update only the DACL or only the SACL.</span></span>

<span data-ttu-id="5a832-131">Следующие значения в [**\_ \_ элементе управления дескриптора безопасности**](/windows/desktop/SecAuthZ/security-descriptor-control) определяют, обновляются ли списки DACL или SACL или оба этих элемента.</span><span class="sxs-lookup"><span data-stu-id="5a832-131">The following values in [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) determine whether the DACL or the SACL or both are updated.</span></span>

-   <span data-ttu-id="5a832-132">**\_присутствие DACL \_ SE**</span><span class="sxs-lookup"><span data-stu-id="5a832-132">**SE\_DACL\_PRESENT**</span></span>

    <span data-ttu-id="5a832-133">Указывает, что список DACL должен быть обновлен.</span><span class="sxs-lookup"><span data-stu-id="5a832-133">Indicates that the DACL should be updated.</span></span> <span data-ttu-id="5a832-134">Если значение не задано, Инструментарий WMI сохраняет исходное значение DACL.</span><span class="sxs-lookup"><span data-stu-id="5a832-134">If this is not set then WMI preserves the original value of the DACL.</span></span>

-   <span data-ttu-id="5a832-135">**\_имеется список SACL для SE \_**</span><span class="sxs-lookup"><span data-stu-id="5a832-135">**SE\_SACL\_PRESENT**</span></span>

    <span data-ttu-id="5a832-136">Указывает, что список SACL должен быть обновлен.</span><span class="sxs-lookup"><span data-stu-id="5a832-136">Indicates that the SACL should be updated.</span></span> <span data-ttu-id="5a832-137">Если значение не задано, Инструментарий WMI сохраняет исходное значение списка SACL.</span><span class="sxs-lookup"><span data-stu-id="5a832-137">If this is not set then WMI preserves the original value of the SACL.</span></span> <span data-ttu-id="5a832-138">Для обновления списка SACL учетная запись должна иметь права **SeSecurityPrivilege** .</span><span class="sxs-lookup"><span data-stu-id="5a832-138">To update the SACL, the account must have the **SeSecurityPrivilege** privilege enabled.</span></span> <span data-ttu-id="5a832-139">Для сценариев имя привилегии — **SeSecurityPrivilege**.</span><span class="sxs-lookup"><span data-stu-id="5a832-139">For scripting, the privilege name is **SeSecurityPrivilege**.</span></span> <span data-ttu-id="5a832-140">Дополнительные сведения см. в разделе [**константы прав доступа**](privilege-constants.md).</span><span class="sxs-lookup"><span data-stu-id="5a832-140">For more information, see [**Privilege Constants**](privilege-constants.md).</span></span>

<span data-ttu-id="5a832-141">Если доверенное лицо группы и свойства доверенного лица владельца не равны **null**, они обновляются.</span><span class="sxs-lookup"><span data-stu-id="5a832-141">If the Group trustee and the Owner trustee properties are not **NULL**, then they are updated.</span></span> <span data-ttu-id="5a832-142">В противном случае Инструментарий WMI сохраняет исходные значения.</span><span class="sxs-lookup"><span data-stu-id="5a832-142">Otherwise, WMI preserves the original values.</span></span> <span data-ttu-id="5a832-143">Дополнительные сведения см. в разделе [объекты дескрипторов безопасности WMI](wmi-security-descriptor-objects.md).</span><span class="sxs-lookup"><span data-stu-id="5a832-143">For more information, see [WMI Security Descriptor Objects](wmi-security-descriptor-objects.md).</span></span>

<span data-ttu-id="5a832-144">Если в вызове этого метода новый список SACL имеет **значение NULL** , то список SACL дескриптора безопасности на целевом защищаемом объекте остается без изменений.</span><span class="sxs-lookup"><span data-stu-id="5a832-144">When a new SACL is **NULL** in a call this method, then the security descriptor SACL on the target securable object is left unchanged.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a832-145">Требования</span><span class="sxs-lookup"><span data-stu-id="5a832-145">Requirements</span></span>



| <span data-ttu-id="5a832-146">Требование</span><span class="sxs-lookup"><span data-stu-id="5a832-146">Requirement</span></span> | <span data-ttu-id="5a832-147">Значение</span><span class="sxs-lookup"><span data-stu-id="5a832-147">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="5a832-148">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5a832-148">Minimum supported client</span></span><br/> | <span data-ttu-id="5a832-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5a832-149">Windows Vista</span></span><br/>       |
| <span data-ttu-id="5a832-150">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5a832-150">Minimum supported server</span></span><br/> | <span data-ttu-id="5a832-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5a832-151">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="5a832-152">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="5a832-152">Namespace</span></span><br/>                | <span data-ttu-id="5a832-153">Все пространства имен WMI</span><span class="sxs-lookup"><span data-stu-id="5a832-153">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="5a832-154">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5a832-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a832-155">**\_\_системсекурити**</span><span class="sxs-lookup"><span data-stu-id="5a832-155">**\_\_SystemSecurity**</span></span>](--systemsecurity.md)
</dt> <dt>

[<span data-ttu-id="5a832-156">Настройка дескрипторов безопасности Намепаце</span><span class="sxs-lookup"><span data-stu-id="5a832-156">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> </dl>

 

