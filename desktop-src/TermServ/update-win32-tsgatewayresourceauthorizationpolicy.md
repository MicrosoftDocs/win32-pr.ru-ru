---
title: Метод Update класса Win32_TSGatewayResourceAuthorizationPolicy
description: Обновление текущей удаленный рабочий стол политики авторизации ресурсов (RD \ 160; RAP).
ms.assetid: af997bb8-6027-4f37-80fb-e89622840a2b
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода обновления
- Метод Update службы удаленных рабочих столов, класс Win32_TSGatewayResourceAuthorizationPolicy
- Класс Win32_TSGatewayResourceAuthorizationPolicy службы удаленных рабочих столов, метод Update
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.Update
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 904d5fa092cddfbfda1c94f1810a6f6da1a9a8a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136299"
---
# <a name="update-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a><span data-ttu-id="8a8c1-106">Метод Update \_ класса Win32 тсгатевайресаурцеаусоризатионполици</span><span class="sxs-lookup"><span data-stu-id="8a8c1-106">Update method of the Win32\_TSGatewayResourceAuthorizationPolicy class</span></span>

<span data-ttu-id="8a8c1-107">Обновляет текущую удаленный рабочий стол политики авторизации ресурсов (RD RAP).</span><span class="sxs-lookup"><span data-stu-id="8a8c1-107">Updates the current Remote Desktop resource authorization policy (RD RAP).</span></span>

## <a name="syntax"></a><span data-ttu-id="8a8c1-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8a8c1-108">Syntax</span></span>


```mof
uint32 Update(
  [in] string  Name,
  [in] string  Description,
  [in] boolean Enabled,
  [in] string  ResourceGroupName,
  [in] string  ResourceGroupType,
  [in] string  UserGroupNames,
  [in] string  ProtocolNames,
  [in] string  PortNumbers
);
```



## <a name="parameters"></a><span data-ttu-id="8a8c1-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="8a8c1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a8c1-110">*Имя* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8a8c1-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a8c1-111">Имя политики авторизации ресурсов удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="8a8c1-111">Name of the RD RAP.</span></span>

</dd> <dt>

<span data-ttu-id="8a8c1-112">*Описание* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8a8c1-112">*Description* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a8c1-113">Описание политики авторизации ресурсов удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="8a8c1-113">Description of the RD RAP.</span></span>

</dd> <dt>

<span data-ttu-id="8a8c1-114">*Включено* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8a8c1-114">*Enabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a8c1-115">Указывает, следует ли включить политику авторизации ресурсов удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="8a8c1-115">Indicates whether the RD RAP should be enabled.</span></span>

</dd> <dt>

<span data-ttu-id="8a8c1-116">*ResourceGroupName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8a8c1-116">*ResourceGroupName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a8c1-117">Имя группы ресурсов, связанной с этим политик авторизации ресурсов удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="8a8c1-117">Resource group name associated with this RD RAP.</span></span>

</dd> <dt>

<span data-ttu-id="8a8c1-118">*Ресаурцеграуптипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8a8c1-118">*ResourceGroupType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a8c1-119">Тип группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8a8c1-119">Resource group type.</span></span>

<dt>

<span data-ttu-id="8a8c1-120">RG</span><span class="sxs-lookup"><span data-stu-id="8a8c1-120">"RG"</span></span>
</dt> <dd>

<span data-ttu-id="8a8c1-121">группа ресурсов;</span><span class="sxs-lookup"><span data-stu-id="8a8c1-121">Resource group.</span></span>

</dd> <dt>

<span data-ttu-id="8a8c1-122">CG</span><span class="sxs-lookup"><span data-stu-id="8a8c1-122">"CG"</span></span>
</dt> <dd>

<span data-ttu-id="8a8c1-123">Группа компьютеров, сохраненная в домен Active Directory Services.</span><span class="sxs-lookup"><span data-stu-id="8a8c1-123">Computer group, as stored in Active Directory Domain Services.</span></span>

</dd> <dt>

<span data-ttu-id="8a8c1-124">КАЖДОГО</span><span class="sxs-lookup"><span data-stu-id="8a8c1-124">"ALL"</span></span>
</dt> <dd>

<span data-ttu-id="8a8c1-125">Все ресурсы.</span><span class="sxs-lookup"><span data-stu-id="8a8c1-125">All resources.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="8a8c1-126">*Усерграупнамес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8a8c1-126">*UserGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a8c1-127">Разделенный точками с запятой список имен групп пользователей.</span><span class="sxs-lookup"><span data-stu-id="8a8c1-127">Semicolon-separated list of user group names.</span></span> <span data-ttu-id="8a8c1-128">Имена имеют формат *домена \\ усерграупнаме*.</span><span class="sxs-lookup"><span data-stu-id="8a8c1-128">The names are of the format *Domain\\UserGroupName*.</span></span> <span data-ttu-id="8a8c1-129">Если пользователь принадлежит к любой из этих групп пользователей, доступ будет разрешен.</span><span class="sxs-lookup"><span data-stu-id="8a8c1-129">If the user belongs to any of these user groups, access will be permitted.</span></span>

</dd> <dt>

<span data-ttu-id="8a8c1-130">*Протоколнамес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8a8c1-130">*ProtocolNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a8c1-131">Разделенный точками с запятой список имен протоколов, включенных для этой политики.</span><span class="sxs-lookup"><span data-stu-id="8a8c1-131">Semicolon-separated list of protocol names that are enabled for this policy.</span></span> <span data-ttu-id="8a8c1-132">Имена должны соответствовать возвращаемому методу [**жетпротоколнаме**](getprotocolname-win32-tsgatewayserversettings.md) класса [**Win32 \_ тсгатевайсерверсеттингс**](win32-tsgatewayserversettings.md) .</span><span class="sxs-lookup"><span data-stu-id="8a8c1-132">Names must match the return of the [**GetProtocolName**](getprotocolname-win32-tsgatewayserversettings.md) method of the [**Win32\_TSGatewayServerSettings**](win32-tsgatewayserversettings.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="8a8c1-133">*Портнумберс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8a8c1-133">*PortNumbers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a8c1-134">Разделенный точками с запятой список номеров портов, включенных для этой политики.</span><span class="sxs-lookup"><span data-stu-id="8a8c1-134">Semicolon-separated list of port numbers that are enabled for this policy.</span></span> <span data-ttu-id="8a8c1-135">Чтобы разрешить любой номер порта, установите " \* ".</span><span class="sxs-lookup"><span data-stu-id="8a8c1-135">To allow any port number, set "\*".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a8c1-136">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8a8c1-136">Return value</span></span>

<span data-ttu-id="8a8c1-137">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="8a8c1-137">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="8a8c1-138">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="8a8c1-138">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="8a8c1-139">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="8a8c1-139">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8a8c1-140">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8a8c1-140">Remarks</span></span>

<span data-ttu-id="8a8c1-141">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="8a8c1-141">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="8a8c1-142">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="8a8c1-142">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="8a8c1-143">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="8a8c1-143">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="8a8c1-144">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="8a8c1-144">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="8a8c1-145">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="8a8c1-145">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="8a8c1-146">Требования</span><span class="sxs-lookup"><span data-stu-id="8a8c1-146">Requirements</span></span>



| <span data-ttu-id="8a8c1-147">Требование</span><span class="sxs-lookup"><span data-stu-id="8a8c1-147">Requirement</span></span> | <span data-ttu-id="8a8c1-148">Значение</span><span class="sxs-lookup"><span data-stu-id="8a8c1-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a8c1-149">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8a8c1-149">Minimum supported client</span></span><br/> | <span data-ttu-id="8a8c1-150">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="8a8c1-150">None supported</span></span><br/>                                                                |
| <span data-ttu-id="8a8c1-151">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8a8c1-151">Minimum supported server</span></span><br/> | <span data-ttu-id="8a8c1-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8a8c1-152">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="8a8c1-153">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="8a8c1-153">Namespace</span></span><br/>                | <span data-ttu-id="8a8c1-154">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="8a8c1-154">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="8a8c1-155">MOF</span><span class="sxs-lookup"><span data-stu-id="8a8c1-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8a8c1-156"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8a8c1-156"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="8a8c1-157">DLL</span><span class="sxs-lookup"><span data-stu-id="8a8c1-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8a8c1-158"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8a8c1-158"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="8a8c1-159">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8a8c1-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a8c1-160">**\_Тсгатевайресаурцеаусоризатионполици Win32**</span><span class="sxs-lookup"><span data-stu-id="8a8c1-160">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

