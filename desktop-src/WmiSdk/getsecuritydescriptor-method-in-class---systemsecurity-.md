---
description: Возвращает дескриптор безопасности, управляющий доступом к пространству имен WMI, к которому вы подключены. Дескриптор безопасности возвращается в виде экземпляра \_ \_ SecurityDescriptor.
ms.assetid: b031af45-9237-434d-91db-69222306c615
ms.tgt_platform: multiple
title: Метод Жетсекуритидескриптор класса __SystemSecurity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.GetSecurityDescriptor
api_type:
- COM
api_location:
- All
ms.openlocfilehash: 7aece0a50678689141de9b9a38a014414578de3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702665"
---
# <a name="getsecuritydescriptor-method-of-the-__systemsecurity-class"></a><span data-ttu-id="e196c-104">Метод Жетсекуритидескриптор \_ \_ класса системсекурити</span><span class="sxs-lookup"><span data-stu-id="e196c-104">GetSecurityDescriptor method of the \_\_SystemSecurity class</span></span>

<span data-ttu-id="e196c-105">Метод **жетсекуритидескриптор** получает дескриптор безопасности, который управляет доступом к пространству имен WMI, к которому вы подключены.</span><span class="sxs-lookup"><span data-stu-id="e196c-105">The **GetSecurityDescriptor** method gets the security descriptor that controls access to the WMI namespace to which you are connected.</span></span> <span data-ttu-id="e196c-106">Дескриптор безопасности возвращается в виде экземпляра [**\_ \_ SecurityDescriptor**](--securitydescriptor.md).</span><span class="sxs-lookup"><span data-stu-id="e196c-106">The security descriptor is returned as an instance of [**\_\_SecurityDescriptor**](--securitydescriptor.md).</span></span> <span data-ttu-id="e196c-107">Дополнительные сведения см. [в разделе Изменение параметров безопасности доступа к защищаемым объектам](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="e196c-107">For more information, see [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e196c-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e196c-108">Syntax</span></span>


```mof
uint32 GetSecurityDescriptor(
  [out] __SystemSecurity Descriptor
);
```



## <a name="parameters"></a><span data-ttu-id="e196c-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="e196c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e196c-110">*Дескриптор* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e196c-110">*Descriptor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e196c-111">Дескриптор безопасности, связанный с пространством имен WMI.</span><span class="sxs-lookup"><span data-stu-id="e196c-111">The security descriptor associated with the WMI namespace.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e196c-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e196c-112">Return value</span></span>

<span data-ttu-id="e196c-113">Возвращает одно из значений, перечисленных в следующем списке, или другое значение, указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="e196c-113">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="e196c-114">Дополнительные сведения см. в статье [коды возврата WMI](wmi-return-codes.md) или [**вбемерроренум**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="e196c-114">For more information, see [WMI Return Codes](wmi-return-codes.md) or [**WbemErrorEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

<dl> <dt>

<span data-ttu-id="e196c-115">**0**</span><span class="sxs-lookup"><span data-stu-id="e196c-115">**0**</span></span>
</dt> <dd>

<span data-ttu-id="e196c-116">Успешное завершение.</span><span class="sxs-lookup"><span data-stu-id="e196c-116">Successful completion.</span></span>

</dd> <dt>

<span data-ttu-id="e196c-117">**2**</span><span class="sxs-lookup"><span data-stu-id="e196c-117">**2**</span></span>
</dt> <dd>

<span data-ttu-id="e196c-118">У пользователя нет доступа к запрошенной информации.</span><span class="sxs-lookup"><span data-stu-id="e196c-118">The user does not have access to the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="e196c-119">**8**</span><span class="sxs-lookup"><span data-stu-id="e196c-119">**8**</span></span>
</dt> <dd>

<span data-ttu-id="e196c-120">Неизвестный сбой.</span><span class="sxs-lookup"><span data-stu-id="e196c-120">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="e196c-121">**9**</span><span class="sxs-lookup"><span data-stu-id="e196c-121">**9**</span></span>
</dt> <dd>

<span data-ttu-id="e196c-122">У пользователя нет необходимых прав для выполнения метода.</span><span class="sxs-lookup"><span data-stu-id="e196c-122">The user does not have adequate privileges to execute the method.</span></span>

</dd> <dt>

<span data-ttu-id="e196c-123">**открыт**</span><span class="sxs-lookup"><span data-stu-id="e196c-123">**21**</span></span>
</dt> <dd>

<span data-ttu-id="e196c-124">В вызове метода указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="e196c-124">A parameter specified in the method call is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e196c-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e196c-125">Remarks</span></span>

<span data-ttu-id="e196c-126">Экземпляр [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) представляет тип данных [**\_ \_ элемента управления дескриптора безопасности**](/windows/desktop/SecAuthZ/security-descriptor-control) и содержит [*список управления доступом на уровне пользователей*](/windows/desktop/SecGloss/d-gly) (DACL) и [*системный список управления доступом*](/windows/desktop/SecGloss/s-gly) (SACL).</span><span class="sxs-lookup"><span data-stu-id="e196c-126">The [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance represents a [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) data type and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) and a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="e196c-127">Дополнительные сведения см. в разделе [списки управления доступом](/windows/desktop/SecAuthZ/access-control-lists).</span><span class="sxs-lookup"><span data-stu-id="e196c-127">For more information, see [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span></span>

<span data-ttu-id="e196c-128">Если параметр **SeSecurityPrivilege** не предоставлен или не включен при получении дескриптора безопасности, в возвращенном дескрипторе безопасности возвращается только список DACL.</span><span class="sxs-lookup"><span data-stu-id="e196c-128">If the **SeSecurityPrivilege** is not granted or enabled when getting a security descriptor, then only the DACL is returned in the returned security descriptor.</span></span> <span data-ttu-id="e196c-129">Дополнительные сведения см. в статьях [**константы прав**](privilege-constants.md) и [выполнение привилегированных операций](executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="e196c-129">For more information, see [**Privilege Constants**](privilege-constants.md) and [Executing Privileged Operations](executing-privileged-operations.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e196c-130">Требования</span><span class="sxs-lookup"><span data-stu-id="e196c-130">Requirements</span></span>



| <span data-ttu-id="e196c-131">Требование</span><span class="sxs-lookup"><span data-stu-id="e196c-131">Requirement</span></span> | <span data-ttu-id="e196c-132">Значение</span><span class="sxs-lookup"><span data-stu-id="e196c-132">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="e196c-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e196c-133">Minimum supported client</span></span><br/> | <span data-ttu-id="e196c-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e196c-134">Windows Vista</span></span><br/>       |
| <span data-ttu-id="e196c-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e196c-135">Minimum supported server</span></span><br/> | <span data-ttu-id="e196c-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e196c-136">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="e196c-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e196c-137">Namespace</span></span><br/>                | <span data-ttu-id="e196c-138">Все пространства имен WMI</span><span class="sxs-lookup"><span data-stu-id="e196c-138">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="e196c-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e196c-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e196c-140">**\_\_системсекурити**</span><span class="sxs-lookup"><span data-stu-id="e196c-140">**\_\_SystemSecurity**</span></span>](--systemsecurity.md)
</dt> <dt>

[<span data-ttu-id="e196c-141">Настройка дескрипторов безопасности Намепаце</span><span class="sxs-lookup"><span data-stu-id="e196c-141">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> </dl>

 

