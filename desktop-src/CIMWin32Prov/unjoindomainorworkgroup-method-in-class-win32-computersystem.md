---
description: Удаляет компьютерную систему из домена или рабочей группы.
ms.assetid: 79ee177e-81e2-441b-b39a-2fb53a0145bf
ms.tgt_platform: multiple
title: Метод Унжоиндомаинорворкграуп класса Win32_ComputerSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComputerSystem.UnjoinDomainOrWorkgroup
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1c6942c5367b6deb02accd9d06927a4d923fa8f5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896369"
---
# <a name="unjoindomainorworkgroup-method-of-the-win32_computersystem-class"></a><span data-ttu-id="a430a-103">Метод Унжоиндомаинорворкграуп \_ класса ComputerSystem Win32</span><span class="sxs-lookup"><span data-stu-id="a430a-103">UnjoinDomainOrWorkgroup method of the Win32\_ComputerSystem class</span></span>

<span data-ttu-id="a430a-104">Метод **унжоиндомаинорворкграуп** удаляет компьютерную систему из домена или рабочей группы.</span><span class="sxs-lookup"><span data-stu-id="a430a-104">The **UnjoinDomainOrWorkgroup** method removes a computer system from a domain or workgroup.</span></span>

<span data-ttu-id="a430a-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="a430a-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="a430a-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="a430a-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="a430a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a430a-107">Syntax</span></span>


```mof
uint32 UnjoinDomainOrWorkgroup(
  [in] string Password,
  [in] string UserName,
  [in] uint32 FUnjoinOptions = 
);
```



## <a name="parameters"></a><span data-ttu-id="a430a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a430a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a430a-109">*Пароль* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a430a-109">*Password* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a430a-110">Если параметр *username* указывает имя учетной записи, параметр *Password* должен указывать на пароль, используемый при подключении к контроллеру домена.</span><span class="sxs-lookup"><span data-stu-id="a430a-110">If the *UserName* parameter specifies an account name, the *Password* parameter must point to the password to use when connecting to the domain controller.</span></span> <span data-ttu-id="a430a-111">В противном случае этот параметр должен иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="a430a-111">Otherwise, this parameter must be **NULL**.</span></span>

> [!Note]  
> <span data-ttu-id="a430a-112">При подключении к WINMGMT или [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) по указателю [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) *пароль* должен использовать высокий уровень проверки подлинности, а не менее **AUTHN на \_ \_ \_ уровне \_ \_ безопасности RPC C**.</span><span class="sxs-lookup"><span data-stu-id="a430a-112">*Password* must use a high authentication level, not less than **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**, when connecting to Winmgmt or [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) on the [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) pointer.</span></span> <span data-ttu-id="a430a-113">Если локальная для WinMgmt, это не проблема.</span><span class="sxs-lookup"><span data-stu-id="a430a-113">If local to Winmgmt, this is not a concern.</span></span>

 

</dd> <dt>

<span data-ttu-id="a430a-114">*Имя пользователя* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a430a-114">*UserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a430a-115">Указатель на постоянную строку символов, завершающуюся нулем, которая указывает имя учетной записи, используемой при подключении к контроллеру домена.</span><span class="sxs-lookup"><span data-stu-id="a430a-115">Pointer to a constant null-terminated character string that specifies the account name to use when connecting to the domain controller.</span></span> <span data-ttu-id="a430a-116">Необходимо указать домен и учетную запись пользователя, например "пользователь домена \\ " или " user@domain ".</span><span class="sxs-lookup"><span data-stu-id="a430a-116">Must specify a domain and user account, for example, "domain\\user" or "user@domain".</span></span> <span data-ttu-id="a430a-117">Если этот параметр имеет **значение NULL**, используется контекст вызывающего объекта.</span><span class="sxs-lookup"><span data-stu-id="a430a-117">If this parameter is **NULL**, the caller context is used.</span></span>

> [!Note]  
> <span data-ttu-id="a430a-118">При подключении к WINMGMT или [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) по указателю [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) *имя пользователя* должно использовать высокий уровень проверки подлинности, а не меньше, чем **RPC \_ C \_ AUTHN \_ уровня \_ \_ безопасности PKT**.</span><span class="sxs-lookup"><span data-stu-id="a430a-118">*UserName* must use a high authentication level, not less than **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**, when connecting to Winmgmt or [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) on the [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) pointer.</span></span> <span data-ttu-id="a430a-119">Если локальная для WinMgmt, это не проблема.</span><span class="sxs-lookup"><span data-stu-id="a430a-119">If local to Winmgmt, this is not a concern.</span></span>

 

</dd> <dt>

<span data-ttu-id="a430a-120">*Фунжоиноптионс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a430a-120">*FUnjoinOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a430a-121">Набор битовых флагов, определяющих параметры отсоединений.</span><span class="sxs-lookup"><span data-stu-id="a430a-121">Set of bit flags defining the unjoin options.</span></span>

<dt>



 <span data-ttu-id="a430a-122"> (0)</span><span class="sxs-lookup"><span data-stu-id="a430a-122">(0)</span></span>


</dt> <dd>

<span data-ttu-id="a430a-123">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a430a-123">Default.</span></span> <span data-ttu-id="a430a-124">Без параметров.</span><span class="sxs-lookup"><span data-stu-id="a430a-124">No options.</span></span>

</dd> <dt>

<span id="NETSETUP_ACCT_DELETE"></span><span id="netsetup_acct_delete"></span>

<span data-ttu-id="a430a-125"><span id="NETSETUP_ACCT_DELETE"></span><span id="netsetup_acct_delete"></span>**Нетсетуп \_ \_Удаление acct** (4)</span><span class="sxs-lookup"><span data-stu-id="a430a-125"><span id="NETSETUP_ACCT_DELETE"></span><span id="netsetup_acct_delete"></span>**NETSETUP\_ACCT\_DELETE** (4)</span></span>


</dt> <dd>

<span data-ttu-id="a430a-126">Отключите учетную запись Active Directory после операции отмены объединения, но не удаляйте учетную запись.</span><span class="sxs-lookup"><span data-stu-id="a430a-126">Disable the Active Directory account after the unjoin operation, but do not delete the account.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a430a-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a430a-127">Return value</span></span>

<span data-ttu-id="a430a-128">Метод **унжоиндомаинорворкграуп** возвращает 0 (нуль) при успешном выполнении или при отсутствии параметров.</span><span class="sxs-lookup"><span data-stu-id="a430a-128">The **UnjoinDomainOrWorkgroup** method returns 0 (zero) on success or when no options are involved.</span></span> <span data-ttu-id="a430a-129">Любое другое значение указывает на ошибку.</span><span class="sxs-lookup"><span data-stu-id="a430a-129">Any other value indicates an error.</span></span> <span data-ttu-id="a430a-130">Коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="a430a-130">For error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="a430a-131">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="a430a-131">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="a430a-132">**Успешно** (0)</span><span class="sxs-lookup"><span data-stu-id="a430a-132">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a430a-133">**Другие** (1 4294967295)</span><span class="sxs-lookup"><span data-stu-id="a430a-133">**Other** (1 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="a430a-134">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a430a-134">Remarks</span></span>

<span data-ttu-id="a430a-135">После вызова этого метода перезагрузите затронутый компьютер, чтобы применить изменения.</span><span class="sxs-lookup"><span data-stu-id="a430a-135">After calling this method, restart the affected computer to apply the changes.</span></span>

## <a name="examples"></a><span data-ttu-id="a430a-136">Примеры</span><span class="sxs-lookup"><span data-stu-id="a430a-136">Examples</span></span>

<span data-ttu-id="a430a-137">[Отсоединение компьютера от домена](https://Gallery.TechNet.Microsoft.Com/c2025ace-cb51-4136-9de9-db8871f79f62) Пример сценария VBScript отсоединяет локальный компьютер от текущего домена и отключает учетную запись компьютера.</span><span class="sxs-lookup"><span data-stu-id="a430a-137">[The Unjoin a Computer from a Domain](https://Gallery.TechNet.Microsoft.Com/c2025ace-cb51-4136-9de9-db8871f79f62) VBScript sample unjoins the local computer from its current domain and disables the computer account.</span></span>

<span data-ttu-id="a430a-138">При [отсоединении компьютера из домена с помощью примера сценария VBS](https://Gallery.TechNet.Microsoft.Com/Unjoin-a-Computer-from-a-825249e1) указанный компьютер из домена не присоединяется к указанному компьютеру.</span><span class="sxs-lookup"><span data-stu-id="a430a-138">The [Unjoin a Computer from a Domain using VBS script](https://Gallery.TechNet.Microsoft.Com/Unjoin-a-Computer-from-a-825249e1) sample unjoins a specified computer from a domain.</span></span> <span data-ttu-id="a430a-139">.</span><span class="sxs-lookup"><span data-stu-id="a430a-139">.</span></span>

## <a name="requirements"></a><span data-ttu-id="a430a-140">Требования</span><span class="sxs-lookup"><span data-stu-id="a430a-140">Requirements</span></span>



| <span data-ttu-id="a430a-141">Требование</span><span class="sxs-lookup"><span data-stu-id="a430a-141">Requirement</span></span> | <span data-ttu-id="a430a-142">Значение</span><span class="sxs-lookup"><span data-stu-id="a430a-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a430a-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a430a-143">Minimum supported client</span></span><br/> | <span data-ttu-id="a430a-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a430a-144">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a430a-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a430a-145">Minimum supported server</span></span><br/> | <span data-ttu-id="a430a-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a430a-146">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a430a-147">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a430a-147">Namespace</span></span><br/>                | <span data-ttu-id="a430a-148">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="a430a-148">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a430a-149">MOF</span><span class="sxs-lookup"><span data-stu-id="a430a-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a430a-150"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a430a-150"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a430a-151">DLL</span><span class="sxs-lookup"><span data-stu-id="a430a-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a430a-152"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a430a-152"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a430a-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a430a-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a430a-154">**Win32 \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="a430a-154">**Win32\_ComputerSystem**</span></span>](win32-computersystem.md)
</dt> <dt>

[<span data-ttu-id="a430a-155">**Метод Жоиндомаинорворкграуп**</span><span class="sxs-lookup"><span data-stu-id="a430a-155">**JoinDomainOrWorkgroup method**</span></span>](joindomainorworkgroup-method-in-class-win32-computersystem.md)
</dt> </dl>

 

