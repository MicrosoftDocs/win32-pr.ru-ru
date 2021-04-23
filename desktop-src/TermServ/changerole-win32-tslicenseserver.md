---
title: Метод ChangeRole класса Win32_TSLicenseServer
description: Изменяет область обнаружения сервера лицензирования удаленный рабочий стол. Область обнаружения определяет, какие серверы узла сеансов удаленный рабочий стол (узлы сеансов удаленных рабочих столов) в сети могут автоматически обнаружить сервер лицензирования.
ms.assetid: 3d98fd8a-4ade-489f-8edd-5df1227f15cd
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода ChangeRole
- Службы удаленных рабочих столов метода ChangeRole, класс Win32_TSLicenseServer
- Класс Win32_TSLicenseServer службы удаленных рабочих столов, метод ChangeRole
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.ChangeRole
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9746b856c74e9603751fe85bb861e2b6869f03a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489687"
---
# <a name="changerole-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="1a675-107">Метод ChangeRole \_ класса Win32 тслиценсесервер</span><span class="sxs-lookup"><span data-stu-id="1a675-107">ChangeRole method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="1a675-108">Изменяет область обнаружения сервера лицензирования удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="1a675-108">Changes the discovery scope of the Remote Desktop license server.</span></span> <span data-ttu-id="1a675-109">Область обнаружения определяет, какие серверы узла сеансов удаленный рабочий стол (узлы сеансов удаленных рабочих столов) в сети могут автоматически обнаружить сервер лицензирования.</span><span class="sxs-lookup"><span data-stu-id="1a675-109">The discovery scope determines which Remote Desktop Session Host (RD Session Host) servers on the network can automatically discover the license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a675-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1a675-110">Syntax</span></span>


```mof
uint32 ChangeRole(
  [in] uint32 ServerRole
);
```



## <a name="parameters"></a><span data-ttu-id="1a675-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="1a675-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a675-112">*ServerRole* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1a675-112">*ServerRole* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a675-113">Область обнаружения для сервера лицензирования удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="1a675-113">Discovery scope for the Remote Desktop license server.</span></span> <span data-ttu-id="1a675-114">Можно задать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="1a675-114">You can set one of the following values.</span></span>

<dt>

<span data-ttu-id="1a675-115">0</span><span class="sxs-lookup"><span data-stu-id="1a675-115">0</span></span>
</dt> <dd>

<span data-ttu-id="1a675-116">Серверы узла сеансов удаленных рабочих столов в одной рабочей группе могут обнаружить сервер лицензирования.</span><span class="sxs-lookup"><span data-stu-id="1a675-116">RD Session Host servers in the same workgroup can discover the license server.</span></span>

</dd> <dt>

<span data-ttu-id="1a675-117">1</span><span class="sxs-lookup"><span data-stu-id="1a675-117">1</span></span>
</dt> <dd>

<span data-ttu-id="1a675-118">Серверы узла сеансов удаленных рабочих столов в одном домене могут обнаружить сервер лицензирования.</span><span class="sxs-lookup"><span data-stu-id="1a675-118">RD Session Host servers in the same domain can discover the license server.</span></span> <span data-ttu-id="1a675-119">Чтобы задать это значение, необходимо войти в систему с учетной записью администратора домена.</span><span class="sxs-lookup"><span data-stu-id="1a675-119">You must be logged on as a domain administrator to set this value.</span></span>

</dd> <dt>

<span data-ttu-id="1a675-120">2</span><span class="sxs-lookup"><span data-stu-id="1a675-120">2</span></span>
</dt> <dd>

<span data-ttu-id="1a675-121">Серверы узла сеансов удаленных рабочих столов из нескольких доменов в одном лесу могут обнаружить сервер лицензирования.</span><span class="sxs-lookup"><span data-stu-id="1a675-121">RD Session Host servers from multiple domains in the same forest can discover the license server.</span></span> <span data-ttu-id="1a675-122">Чтобы задать это значение, необходимо войти в систему от имени администратора предприятия.</span><span class="sxs-lookup"><span data-stu-id="1a675-122">You must be logged on as an enterprise administrator to set this value.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a675-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1a675-123">Return value</span></span>

<span data-ttu-id="1a675-124">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="1a675-124">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="1a675-125">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="1a675-125">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="1a675-126">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="1a675-126">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="1a675-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1a675-127">Remarks</span></span>

<span data-ttu-id="1a675-128">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="1a675-128">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="1a675-129">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="1a675-129">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="1a675-130">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="1a675-130">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="1a675-131">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="1a675-131">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="1a675-132">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="1a675-132">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="1a675-133">Требования</span><span class="sxs-lookup"><span data-stu-id="1a675-133">Requirements</span></span>



| <span data-ttu-id="1a675-134">Требование</span><span class="sxs-lookup"><span data-stu-id="1a675-134">Requirement</span></span> | <span data-ttu-id="1a675-135">Значение</span><span class="sxs-lookup"><span data-stu-id="1a675-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a675-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1a675-136">Minimum supported client</span></span><br/> | <span data-ttu-id="1a675-137">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="1a675-137">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="1a675-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1a675-138">Minimum supported server</span></span><br/> | <span data-ttu-id="1a675-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1a675-139">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="1a675-140">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="1a675-140">Namespace</span></span><br/>                | <span data-ttu-id="1a675-141">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="1a675-141">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="1a675-142">MOF</span><span class="sxs-lookup"><span data-stu-id="1a675-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1a675-143"><dt>Тлсвмипров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1a675-143"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="1a675-144">DLL</span><span class="sxs-lookup"><span data-stu-id="1a675-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1a675-145"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1a675-145"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a675-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1a675-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a675-147">**\_Тслиценсесервер Win32**</span><span class="sxs-lookup"><span data-stu-id="1a675-147">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

