---
title: Метод Сетсслбридгинг класса Win32_TSGatewayServerSettings
description: Задает тип моста SSL, используемый сервером шлюза удаленный рабочий стол (шлюза удаленных рабочих столов).
ms.assetid: 11885b8b-491e-4d90-b4d4-f0a0fbe68cb1
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетсслбридгинг
- Службы удаленных рабочих столов метода Сетсслбридгинг, класс Win32_TSGatewayServerSettings
- Класс Win32_TSGatewayServerSettings службы удаленных рабочих столов, метод Сетсслбридгинг
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetSslBridging
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77181fb8d8661ec7ea7dc0ce70532281fb9c1bde
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415741"
---
# <a name="setsslbridging-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="9f10a-106">Метод Сетсслбридгинг \_ класса Win32 тсгатевайсерверсеттингс</span><span class="sxs-lookup"><span data-stu-id="9f10a-106">SetSslBridging method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="9f10a-107">Задает тип моста SSL, используемый сервером шлюза удаленный рабочий стол (шлюза удаленных рабочих столов).</span><span class="sxs-lookup"><span data-stu-id="9f10a-107">Sets the type of SSL bridging to be used by the Remote Desktop Gateway (RD Gateway) server.</span></span> <span data-ttu-id="9f10a-108">Это значение хранится в свойстве **сслбридгинг** .</span><span class="sxs-lookup"><span data-stu-id="9f10a-108">This value is stored in the **SslBridging** property.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9f10a-109">При изменении типа моста SSL с помощью этого метода необходимо перезапустить службу шлюза удаленных рабочих столов, чтобы изменения вступили в силу.</span><span class="sxs-lookup"><span data-stu-id="9f10a-109">When the SSL bridging type is changed with this method, the RD Gateway service must be restarted to make this change take effect.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="9f10a-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9f10a-110">Syntax</span></span>


```mof
uint32 SetSslBridging(
  [in] uint32 SslBridging
);
```



## <a name="parameters"></a><span data-ttu-id="9f10a-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="9f10a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f10a-112">*Сслбридгинг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9f10a-112">*SslBridging* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f10a-113">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9f10a-113">Type: **uint32**</span></span>

<span data-ttu-id="9f10a-114">Указывает новое значение моста SSL.</span><span class="sxs-lookup"><span data-stu-id="9f10a-114">Specifies the new SSL bridging value.</span></span> <span data-ttu-id="9f10a-115">Это может быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="9f10a-115">This can be one of the following values.</span></span>

<dt>

<span data-ttu-id="9f10a-116">0</span><span class="sxs-lookup"><span data-stu-id="9f10a-116">0</span></span>
</dt> <dd>

<span data-ttu-id="9f10a-117">Мост SSL отсутствует.</span><span class="sxs-lookup"><span data-stu-id="9f10a-117">No SSL bridging.</span></span>

</dd> <dt>

<span data-ttu-id="9f10a-118">1</span><span class="sxs-lookup"><span data-stu-id="9f10a-118">1</span></span>
</dt> <dd>

<span data-ttu-id="9f10a-119">Мост HTTPS для HTTP.</span><span class="sxs-lookup"><span data-stu-id="9f10a-119">HTTPS to HTTP bridging.</span></span>

</dd> <dt>

<span data-ttu-id="9f10a-120">2</span><span class="sxs-lookup"><span data-stu-id="9f10a-120">2</span></span>
</dt> <dd>

<span data-ttu-id="9f10a-121">Мост HTTPS для HTTPS.</span><span class="sxs-lookup"><span data-stu-id="9f10a-121">HTTPS to HTTPS bridging.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f10a-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9f10a-122">Return value</span></span>

<span data-ttu-id="9f10a-123">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9f10a-123">Type: **uint32**</span></span>

<span data-ttu-id="9f10a-124">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="9f10a-124">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="9f10a-125">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="9f10a-125">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="9f10a-126">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="9f10a-126">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9f10a-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9f10a-127">Remarks</span></span>

<span data-ttu-id="9f10a-128">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="9f10a-128">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="9f10a-129">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="9f10a-129">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="9f10a-130">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="9f10a-130">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="9f10a-131">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="9f10a-131">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="9f10a-132">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="9f10a-132">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="9f10a-133">Требования</span><span class="sxs-lookup"><span data-stu-id="9f10a-133">Requirements</span></span>



| <span data-ttu-id="9f10a-134">Требование</span><span class="sxs-lookup"><span data-stu-id="9f10a-134">Requirement</span></span> | <span data-ttu-id="9f10a-135">Значение</span><span class="sxs-lookup"><span data-stu-id="9f10a-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f10a-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9f10a-136">Minimum supported client</span></span><br/> | <span data-ttu-id="9f10a-137">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="9f10a-137">None supported</span></span><br/>                                                                |
| <span data-ttu-id="9f10a-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9f10a-138">Minimum supported server</span></span><br/> | <span data-ttu-id="9f10a-139">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9f10a-139">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="9f10a-140">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="9f10a-140">Namespace</span></span><br/>                | <span data-ttu-id="9f10a-141">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="9f10a-141">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="9f10a-142">MOF</span><span class="sxs-lookup"><span data-stu-id="9f10a-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9f10a-143"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9f10a-143"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="9f10a-144">DLL</span><span class="sxs-lookup"><span data-stu-id="9f10a-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f10a-145"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9f10a-145"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="9f10a-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9f10a-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f10a-147">**\_Тсгатевайсерверсеттингс Win32**</span><span class="sxs-lookup"><span data-stu-id="9f10a-147">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

