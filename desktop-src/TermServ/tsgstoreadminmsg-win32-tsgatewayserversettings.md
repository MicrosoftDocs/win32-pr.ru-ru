---
title: Метод Тсгстореадминмсг класса Win32_TSGatewayServerSettings
description: Обновляет административное сообщение для сервера шлюза.
ms.assetid: 84e5b967-12fd-47a7-93e4-2550c15c4491
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Тсгстореадминмсг
- Службы удаленных рабочих столов метода Тсгстореадминмсг, класс Win32_TSGatewayServerSettings
- Класс Win32_TSGatewayServerSettings службы удаленных рабочих столов, метод Тсгстореадминмсг
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.TSGStoreAdminMsg
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 398a027d28970b28b4a1e7db37b5fbfee06e881e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892045"
---
# <a name="tsgstoreadminmsg-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="bbf8d-106">Метод Тсгстореадминмсг \_ класса Win32 тсгатевайсерверсеттингс</span><span class="sxs-lookup"><span data-stu-id="bbf8d-106">TSGStoreAdminMsg method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="bbf8d-107">Обновляет административное сообщение для сервера шлюза.</span><span class="sxs-lookup"><span data-stu-id="bbf8d-107">Updates the administrative message for the gateway server.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbf8d-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bbf8d-108">Syntax</span></span>


```mof
uint32 TSGStoreAdminMsg(
  [in] string TSGAdmMsg,
  [in] string MsgStartTime,
  [in] string MsgEndTime
);
```



## <a name="parameters"></a><span data-ttu-id="bbf8d-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="bbf8d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bbf8d-110">*Тсгадммсг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bbf8d-110">*TSGAdmMsg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bbf8d-111">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="bbf8d-111">Type: **string**</span></span>

<span data-ttu-id="bbf8d-112">Текст административного сообщения.</span><span class="sxs-lookup"><span data-stu-id="bbf8d-112">The administrative message text.</span></span>

</dd> <dt>

<span data-ttu-id="bbf8d-113">*Мсгстарттиме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bbf8d-113">*MsgStartTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bbf8d-114">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="bbf8d-114">Type: **string**</span></span>

<span data-ttu-id="bbf8d-115">Время начала административного сообщения.</span><span class="sxs-lookup"><span data-stu-id="bbf8d-115">The administrative message start time.</span></span>

</dd> <dt>

<span data-ttu-id="bbf8d-116">*Мсжендтиме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bbf8d-116">*MsgEndTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bbf8d-117">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="bbf8d-117">Type: **string**</span></span>

<span data-ttu-id="bbf8d-118">Время окончания административного сообщения.</span><span class="sxs-lookup"><span data-stu-id="bbf8d-118">The administrative message end time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bbf8d-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bbf8d-119">Return value</span></span>

<span data-ttu-id="bbf8d-120">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bbf8d-120">Type: **uint32**</span></span>

<span data-ttu-id="bbf8d-121">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="bbf8d-121">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="bbf8d-122">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="bbf8d-122">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="bbf8d-123">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="bbf8d-123">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="bbf8d-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bbf8d-124">Remarks</span></span>

<span data-ttu-id="bbf8d-125">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="bbf8d-125">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="bbf8d-126">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="bbf8d-126">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="bbf8d-127">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="bbf8d-127">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="bbf8d-128">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="bbf8d-128">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="bbf8d-129">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="bbf8d-129">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="bbf8d-130">Требования</span><span class="sxs-lookup"><span data-stu-id="bbf8d-130">Requirements</span></span>



| <span data-ttu-id="bbf8d-131">Требование</span><span class="sxs-lookup"><span data-stu-id="bbf8d-131">Requirement</span></span> | <span data-ttu-id="bbf8d-132">Значение</span><span class="sxs-lookup"><span data-stu-id="bbf8d-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbf8d-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bbf8d-133">Minimum supported client</span></span><br/> | <span data-ttu-id="bbf8d-134">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="bbf8d-134">None supported</span></span><br/>                                                                |
| <span data-ttu-id="bbf8d-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bbf8d-135">Minimum supported server</span></span><br/> | <span data-ttu-id="bbf8d-136">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="bbf8d-136">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="bbf8d-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="bbf8d-137">Namespace</span></span><br/>                | <span data-ttu-id="bbf8d-138">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="bbf8d-138">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="bbf8d-139">MOF</span><span class="sxs-lookup"><span data-stu-id="bbf8d-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bbf8d-140"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bbf8d-140"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="bbf8d-141">DLL</span><span class="sxs-lookup"><span data-stu-id="bbf8d-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bbf8d-142"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bbf8d-142"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="bbf8d-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bbf8d-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbf8d-144">**\_Тсгатевайсерверсеттингс Win32**</span><span class="sxs-lookup"><span data-stu-id="bbf8d-144">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

