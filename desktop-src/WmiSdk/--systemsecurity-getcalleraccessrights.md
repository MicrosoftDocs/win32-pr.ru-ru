---
description: Устанавливает параметр прав в виде точечного рисунка с каждым битом, соответствующим прав доступа.
ms.assetid: f28391a8-2b34-4234-bf1a-4688726b0b4b
ms.tgt_platform: multiple
title: Метод Жеткаллеракцессригхтс класса __SystemSecurity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.GetCallerAccessRights
api_type:
- COM
api_location:
- All
ms.openlocfilehash: c86ea3044411e33026ed6328fcfc227e615648b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702751"
---
# <a name="getcalleraccessrights-method-of-the-__systemsecurity-class"></a><span data-ttu-id="d072d-103">Метод Жеткаллеракцессригхтс \_ \_ класса системсекурити</span><span class="sxs-lookup"><span data-stu-id="d072d-103">GetCallerAccessRights method of the \_\_SystemSecurity class</span></span>

<span data-ttu-id="d072d-104">Метод **\_ \_ системсекурити:: жеткаллеракцессригхтс** устанавливает параметр *Rights* в виде точечного рисунка с каждым битом, соответствующим право доступа.</span><span class="sxs-lookup"><span data-stu-id="d072d-104">The **\_\_SystemSecurity::GetCallerAccessRights** method sets the *rights* parameter as a bitmap with each bit corresponding to an access right.</span></span> <span data-ttu-id="d072d-105">Любой клиент может вызвать эту функцию, чтобы определить, какие права у клиента.</span><span class="sxs-lookup"><span data-stu-id="d072d-105">Any client can call this to determine which rights the client has.</span></span> <span data-ttu-id="d072d-106">Этот метод полезен для клиентов, которые включают или отключают функции.</span><span class="sxs-lookup"><span data-stu-id="d072d-106">This method is useful for clients that enable or disable features.</span></span> <span data-ttu-id="d072d-107">Например, приложение с графическим пользовательским интерфейсом может отключить кнопку, если у пользователя, выполнившего вход в систему, нет прав на выполнение метода.</span><span class="sxs-lookup"><span data-stu-id="d072d-107">For example, a GUI application might disable a button if the currently logged-on user does not have method execution rights.</span></span>

<span data-ttu-id="d072d-108">Любой включенный клиент имеет право вызывать **жеткаллеракцессригхтс**, даже если у этого клиента нет прав на выполнение метода общего доступа.</span><span class="sxs-lookup"><span data-stu-id="d072d-108">Any enabled client has the right to call **GetCallerAccessRights**, even if that client does not have general method execution rights.</span></span>

## <a name="syntax"></a><span data-ttu-id="d072d-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d072d-109">Syntax</span></span>


```mof
HRESULT GetCallerAccessRights(
  [out] sint32 rights
);
```



## <a name="parameters"></a><span data-ttu-id="d072d-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="d072d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d072d-111">*права доступа* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d072d-111">*rights* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d072d-112">Права доступа клиента.</span><span class="sxs-lookup"><span data-stu-id="d072d-112">Access rights of the client.</span></span> <span data-ttu-id="d072d-113">Дополнительные сведения см. в разделе [**\_ \_ системсекурити**](--systemsecurity.md) и [константы безопасности WMI](wmi-security-constants.md).</span><span class="sxs-lookup"><span data-stu-id="d072d-113">For more information, see [**\_\_SystemSecurity**](--systemsecurity.md) and [WMI Security Constants](wmi-security-constants.md).</span></span>

<dt>

<span id="WBEM_ENABLE"></span><span id="wbem_enable"></span>

<span data-ttu-id="d072d-114"><span id="WBEM_ENABLE"></span><span id="wbem_enable"></span>**WBEM \_ ВКЛЮЧИТЬ** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="d072d-114"><span id="WBEM_ENABLE"></span><span id="wbem_enable"></span>**WBEM\_ENABLE** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="d072d-115">Включает учетную запись и предоставляет пользователю разрешения на чтение.</span><span class="sxs-lookup"><span data-stu-id="d072d-115">Enables the account and grants the user read permissions.</span></span> <span data-ttu-id="d072d-116">Это право доступа по умолчанию для всех пользователей.</span><span class="sxs-lookup"><span data-stu-id="d072d-116">This is the default access right for all users.</span></span>

</dd> <dt>

<span id="WBEM_METHOD_EXECUTE"></span><span id="wbem_method_execute"></span>

<span data-ttu-id="d072d-117"><span id="WBEM_METHOD_EXECUTE"></span><span id="wbem_method_execute"></span>**WBEM \_ \_Выполнение метода** (2 (0x2))</span><span class="sxs-lookup"><span data-stu-id="d072d-117"><span id="WBEM_METHOD_EXECUTE"></span><span id="wbem_method_execute"></span>**WBEM\_METHOD\_EXECUTE** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="d072d-118">Разрешает выполнение методов.</span><span class="sxs-lookup"><span data-stu-id="d072d-118">Allows the execution of methods.</span></span>

> [!Note]  
> <span data-ttu-id="d072d-119">Поставщики могут выполнять дополнительные проверки доступа.</span><span class="sxs-lookup"><span data-stu-id="d072d-119">Providers may perform additional access checks.</span></span>

 

</dd> <dt>

<span id="WBEM_FULL_WRITE_REP"></span><span id="wbem_full_write_rep"></span>

<span data-ttu-id="d072d-120"><span id="WBEM_FULL_WRITE_REP"></span><span id="wbem_full_write_rep"></span>**WBEM \_ ПОЛНЫЙ \_ \_ представитель** (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="d072d-120"><span id="WBEM_FULL_WRITE_REP"></span><span id="wbem_full_write_rep"></span>**WBEM\_FULL\_WRITE\_REP** (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="d072d-121">Позволяет вызывающему, контексту безопасности или пользователю выполнять запись в классы и экземпляры, кроме системных классов.</span><span class="sxs-lookup"><span data-stu-id="d072d-121">Allows the caller, security context, or user to write to classes and instances except for system classes.</span></span>

</dd> <dt>

<span id="WBEM_PARTIAL_WRITE_REP"></span><span id="wbem_partial_write_rep"></span>

<span data-ttu-id="d072d-122"><span id="WBEM_PARTIAL_WRITE_REP"></span><span id="wbem_partial_write_rep"></span>**WBEM \_ \_ \_ Представитель частичной записи** (8 (0x8))</span><span class="sxs-lookup"><span data-stu-id="d072d-122"><span id="WBEM_PARTIAL_WRITE_REP"></span><span id="wbem_partial_write_rep"></span>**WBEM\_PARTIAL\_WRITE\_REP** (8 (0x8))</span></span>


</dt> <dd>

<span data-ttu-id="d072d-123">Позволяет вызывающему, контексту безопасности или пользователю записывать экземпляры поставщика, но не статические классы или статические экземпляры в репозиторий.</span><span class="sxs-lookup"><span data-stu-id="d072d-123">Allows the caller, security context, or user to write provider instances but not static classes or static instances to the repository.</span></span>

</dd> <dt>

<span id="WBEM_WRITE_PROVIDER"></span><span id="wbem_write_provider"></span>

<span data-ttu-id="d072d-124"><span id="WBEM_WRITE_PROVIDER"></span><span id="wbem_write_provider"></span>**WBEM \_ \_Поставщик записи** (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="d072d-124"><span id="WBEM_WRITE_PROVIDER"></span><span id="wbem_write_provider"></span>**WBEM\_WRITE\_PROVIDER** (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="d072d-125">Позволяет вызывающему, контексту безопасности или пользователю создавать классы и экземпляры для поставщиков.</span><span class="sxs-lookup"><span data-stu-id="d072d-125">Allows the caller, security context, or user to write classes and instances to providers.</span></span>

> [!Note]  
> <span data-ttu-id="d072d-126">Олицетворение поставщиков может выполнять дополнительные проверки доступа.</span><span class="sxs-lookup"><span data-stu-id="d072d-126">Impersonating providers may do additional access checks.</span></span>

 

</dd> <dt>

<span id="WBEM_REMOTE_ACCESS"></span><span id="wbem_remote_access"></span>

<span data-ttu-id="d072d-127"><span id="WBEM_REMOTE_ACCESS"></span><span id="wbem_remote_access"></span>**WBEM \_ УДАЛЕННЫЙ \_ доступ** (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="d072d-127"><span id="WBEM_REMOTE_ACCESS"></span><span id="wbem_remote_access"></span>**WBEM\_REMOTE\_ACCESS** (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="d072d-128">Позволяет учетной записи пользователя удаленно выполнять любые операции, разрешенные разрешениями, заданными другими битами.</span><span class="sxs-lookup"><span data-stu-id="d072d-128">Allows a user account to remotely perform any operations allowed by the permissions set by other bits.</span></span>

</dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="d072d-129"><span id="READ_CONTROL"></span><span id="read_control"></span>**Чтение \_ Элемент управления** (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="d072d-129"><span id="READ_CONTROL"></span><span id="read_control"></span>**READ\_CONTROL** (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="d072d-130">Разрешает доступ на чтение к дескрипторам безопасности.</span><span class="sxs-lookup"><span data-stu-id="d072d-130">Allows read access to the security descriptors.</span></span>

</dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="d072d-131"><span id="WRITE_DAC"></span><span id="write_dac"></span>**Запись \_ DAC** (262144 (0x40000))</span><span class="sxs-lookup"><span data-stu-id="d072d-131"><span id="WRITE_DAC"></span><span id="write_dac"></span>**WRITE\_DAC** (262144 (0x40000))</span></span>


</dt> <dd>

<span data-ttu-id="d072d-132">Разрешает доступ на запись к избирательным спискам управления доступом (DACL).</span><span class="sxs-lookup"><span data-stu-id="d072d-132">Allows write access to discretionary access control lists (DACL).</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d072d-133">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d072d-133">Return value</span></span>

<span data-ttu-id="d072d-134">Этот метод возвращает **значение HRESULT** , указывающее состояние вызова метода.</span><span class="sxs-lookup"><span data-stu-id="d072d-134">This method returns an **HRESULT** that indicates the status of the method call.</span></span> <span data-ttu-id="d072d-135">В следующем списке перечислены возвращаемые значения, которые являются значимыми для [**Set9XUserList**](--systemsecurity-set9xuserlist.md).</span><span class="sxs-lookup"><span data-stu-id="d072d-135">The following list lists the return values that are of significance to [**Set9XUserList**](--systemsecurity-set9xuserlist.md).</span></span> <span data-ttu-id="d072d-136">Для сценариев и Visual Basic приложений результат можно получить из [параметров out. returnValue](parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="d072d-136">For scripting and Visual Basic applications, the result can be obtained from [OutParameters.ReturnValue](parsing-outparameters-objects.md).</span></span> <span data-ttu-id="d072d-137">Дополнительные сведения см. в разделе [Построение объектов параметров и анализ объектов параметров](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="d072d-137">For more information, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span>

<dl> <dt>

<span data-ttu-id="d072d-138">**\_метод WBEM \_ E \_ отключен**</span><span class="sxs-lookup"><span data-stu-id="d072d-138">**WBEM\_E\_METHOD\_DISABLED**</span></span>
</dt> <dd>

<span data-ttu-id="d072d-139">Этот метод не поддерживается в поддерживаемых версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="d072d-139">This method is not supported on supported versions of Windows.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d072d-140">Требования</span><span class="sxs-lookup"><span data-stu-id="d072d-140">Requirements</span></span>



| <span data-ttu-id="d072d-141">Требование</span><span class="sxs-lookup"><span data-stu-id="d072d-141">Requirement</span></span> | <span data-ttu-id="d072d-142">Значение</span><span class="sxs-lookup"><span data-stu-id="d072d-142">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="d072d-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d072d-143">Minimum supported client</span></span><br/> | <span data-ttu-id="d072d-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d072d-144">Windows Vista</span></span><br/>       |
| <span data-ttu-id="d072d-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d072d-145">Minimum supported server</span></span><br/> | <span data-ttu-id="d072d-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d072d-146">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="d072d-147">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d072d-147">Namespace</span></span><br/>                | <span data-ttu-id="d072d-148">Все пространства имен WMI</span><span class="sxs-lookup"><span data-stu-id="d072d-148">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="d072d-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d072d-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d072d-150">Системные классы WMI</span><span class="sxs-lookup"><span data-stu-id="d072d-150">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="d072d-151">**\_\_системсекурити**</span><span class="sxs-lookup"><span data-stu-id="d072d-151">**\_\_SystemSecurity**</span></span>](--systemsecurity.md)
</dt> <dt>

[<span data-ttu-id="d072d-152">**\_\_Системсекурити:: получает**</span><span class="sxs-lookup"><span data-stu-id="d072d-152">**\_\_SystemSecurity::GetSD**</span></span>](--systemsecurity-getsd.md)
</dt> <dt>

[<span data-ttu-id="d072d-153">**\_\_Системсекурити:: настраивается**</span><span class="sxs-lookup"><span data-stu-id="d072d-153">**\_\_SystemSecurity::SetSD**</span></span>](--systemsecurity-setsd.md)
</dt> <dt>

[<span data-ttu-id="d072d-154">Константы безопасности WMI</span><span class="sxs-lookup"><span data-stu-id="d072d-154">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> <dt>

[<span data-ttu-id="d072d-155">**\_ACE Win32**</span><span class="sxs-lookup"><span data-stu-id="d072d-155">**Win32\_ACE**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[<span data-ttu-id="d072d-156">**\_SecurityDescriptor Win32**</span><span class="sxs-lookup"><span data-stu-id="d072d-156">**Win32\_SecurityDescriptor**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[<span data-ttu-id="d072d-157">Защита пространств имен WMI</span><span class="sxs-lookup"><span data-stu-id="d072d-157">Securing WMI Namespaces</span></span>](securing-wmi-namespaces.md)
</dt> <dt>

<span data-ttu-id="d072d-158">Константы безопасности WMI</span><span class="sxs-lookup"><span data-stu-id="d072d-158">WMI Security Constants</span></span>
</dt> </dl>

 

