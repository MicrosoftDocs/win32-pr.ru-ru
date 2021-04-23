---
title: Метод Create класса Win32_TSGatewayResourceAuthorizationPolicy
description: Создание удаленный рабочий стол политики авторизации ресурсов (RD \ 160; RAP).
ms.assetid: 3301a543-cdf9-4528-a29e-691054ef81c9
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Create
- Создание службы удаленных рабочих столов метода, Win32_TSGatewayResourceAuthorizationPolicy класса
- Класс Win32_TSGatewayResourceAuthorizationPolicy службы удаленных рабочих столов, метод Create
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.Create
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6372706a294902b03f22807049db9a954de4f7e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414953"
---
# <a name="create-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a><span data-ttu-id="ab302-106">Метод Create \_ класса Win32 тсгатевайресаурцеаусоризатионполици</span><span class="sxs-lookup"><span data-stu-id="ab302-106">Create method of the Win32\_TSGatewayResourceAuthorizationPolicy class</span></span>

<span data-ttu-id="ab302-107">Создание удаленный рабочий стол политики авторизации ресурсов (RD RAP).</span><span class="sxs-lookup"><span data-stu-id="ab302-107">Creates a Remote Desktop resource authorization policy (RD RAP).</span></span>

## <a name="syntax"></a><span data-ttu-id="ab302-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ab302-108">Syntax</span></span>


```mof
uint32 Create(
  [in] string  Name,
  [in] string  Description,
  [in] boolean Enabled,
  [in] string  ResourceGroupType,
  [in] string  ResourceGroupName,
  [in] string  UserGroupNames,
  [in] string  ProtocolNames,
  [in] string  PortNumbers
);
```



## <a name="parameters"></a><span data-ttu-id="ab302-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="ab302-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab302-110">*Имя* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ab302-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab302-111">Имя политики авторизации ресурсов удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="ab302-111">Name of the RD RAP.</span></span>

</dd> <dt>

<span data-ttu-id="ab302-112">*Описание* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ab302-112">*Description* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab302-113">Описание политики авторизации ресурсов удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="ab302-113">Description of the RD RAP.</span></span>

</dd> <dt>

<span data-ttu-id="ab302-114">*Включено* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ab302-114">*Enabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab302-115">Указывает, следует ли включить политику авторизации ресурсов удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="ab302-115">Indicates whether the RD RAP is to be enabled.</span></span>

</dd> <dt>

<span data-ttu-id="ab302-116">*Ресаурцеграуптипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ab302-116">*ResourceGroupType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab302-117">Тип группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ab302-117">Resource group type.</span></span>

<dt>

<span data-ttu-id="ab302-118">RG</span><span class="sxs-lookup"><span data-stu-id="ab302-118">"RG"</span></span>
</dt> <dd>

<span data-ttu-id="ab302-119">группа ресурсов;</span><span class="sxs-lookup"><span data-stu-id="ab302-119">Resource group.</span></span>

</dd> <dt>

<span data-ttu-id="ab302-120">CG</span><span class="sxs-lookup"><span data-stu-id="ab302-120">"CG"</span></span>
</dt> <dd>

<span data-ttu-id="ab302-121">Группа компьютеров, сохраненная в домен Active Directory Services.</span><span class="sxs-lookup"><span data-stu-id="ab302-121">Computer group, as stored in Active Directory Domain Services.</span></span>

</dd> <dt>

<span data-ttu-id="ab302-122">КАЖДОГО</span><span class="sxs-lookup"><span data-stu-id="ab302-122">"ALL"</span></span>
</dt> <dd>

<span data-ttu-id="ab302-123">Все ресурсы.</span><span class="sxs-lookup"><span data-stu-id="ab302-123">All resources.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="ab302-124">*ResourceGroupName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ab302-124">*ResourceGroupName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab302-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ab302-125">Resource group name.</span></span>

</dd> <dt>

<span data-ttu-id="ab302-126">*Усерграупнамес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ab302-126">*UserGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab302-127">Разделенный точками с запятой список имен групп пользователей.</span><span class="sxs-lookup"><span data-stu-id="ab302-127">Semicolon-separated list of user group names.</span></span> <span data-ttu-id="ab302-128">Если пользователь принадлежит к любой из этих групп пользователей, доступ будет разрешен.</span><span class="sxs-lookup"><span data-stu-id="ab302-128">If the user belongs to any of these user groups, access will be permitted.</span></span> <span data-ttu-id="ab302-129">Имена групп пользователей должны иметь формат *домена \\ усерграупнаме*.</span><span class="sxs-lookup"><span data-stu-id="ab302-129">User group names should be of the format *Domain\\UserGroupName*.</span></span>

</dd> <dt>

<span data-ttu-id="ab302-130">*Протоколнамес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ab302-130">*ProtocolNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab302-131">Разделенный точками с запятой список имен протоколов, включенных для этой политики.</span><span class="sxs-lookup"><span data-stu-id="ab302-131">Semicolon-separated list of protocol names that are enabled for this policy.</span></span> <span data-ttu-id="ab302-132">Имена должны соответствовать возвращаемому методу [**жетпротоколнаме**](getprotocolname-win32-tsgatewayserversettings.md) класса [**Win32 \_ тсгатевайсерверсеттингс**](win32-tsgatewayserversettings.md) .</span><span class="sxs-lookup"><span data-stu-id="ab302-132">Names must match the return of the [**GetProtocolName**](getprotocolname-win32-tsgatewayserversettings.md) method of the [**Win32\_TSGatewayServerSettings**](win32-tsgatewayserversettings.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="ab302-133">*Портнумберс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ab302-133">*PortNumbers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab302-134">Разделенный точками с запятой список номеров портов, включенных для этой политики.</span><span class="sxs-lookup"><span data-stu-id="ab302-134">Semicolon-separated list of port numbers that are enabled for this policy.</span></span> <span data-ttu-id="ab302-135">Чтобы разрешить любой номер порта, установите " \* ".</span><span class="sxs-lookup"><span data-stu-id="ab302-135">To allow any port number, set "\*".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab302-136">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ab302-136">Return value</span></span>

<span data-ttu-id="ab302-137">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="ab302-137">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="ab302-138">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="ab302-138">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="ab302-139">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="ab302-139">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ab302-140">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ab302-140">Remarks</span></span>

<span data-ttu-id="ab302-141">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="ab302-141">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="ab302-142">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="ab302-142">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="ab302-143">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="ab302-143">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="ab302-144">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="ab302-144">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="ab302-145">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="ab302-145">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="ab302-146">Требования</span><span class="sxs-lookup"><span data-stu-id="ab302-146">Requirements</span></span>



| <span data-ttu-id="ab302-147">Требование</span><span class="sxs-lookup"><span data-stu-id="ab302-147">Requirement</span></span> | <span data-ttu-id="ab302-148">Значение</span><span class="sxs-lookup"><span data-stu-id="ab302-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab302-149">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ab302-149">Minimum supported client</span></span><br/> | <span data-ttu-id="ab302-150">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ab302-150">None supported</span></span><br/>                                                                |
| <span data-ttu-id="ab302-151">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ab302-151">Minimum supported server</span></span><br/> | <span data-ttu-id="ab302-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ab302-152">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="ab302-153">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ab302-153">Namespace</span></span><br/>                | <span data-ttu-id="ab302-154">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="ab302-154">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="ab302-155">MOF</span><span class="sxs-lookup"><span data-stu-id="ab302-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ab302-156"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ab302-156"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="ab302-157">DLL</span><span class="sxs-lookup"><span data-stu-id="ab302-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ab302-158"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ab302-158"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="ab302-159">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ab302-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab302-160">**\_Тсгатевайресаурцеаусоризатионполици Win32**</span><span class="sxs-lookup"><span data-stu-id="ab302-160">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

