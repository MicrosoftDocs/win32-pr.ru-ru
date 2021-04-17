---
title: Метод Сетсекуреидалловед класса Win32_TSGatewayConnectionAuthorizationPolicy
description: Этот метод зарезервирован для использования в будущем.
ms.assetid: 9f49e69a-c004-4e3e-b238-69865e3bf00b
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетсекуреидалловед
- Службы удаленных рабочих столов метода Сетсекуреидалловед, класс Win32_TSGatewayConnectionAuthorizationPolicy
- Класс Win32_TSGatewayConnectionAuthorizationPolicy службы удаленных рабочих столов, метод Сетсекуреидалловед
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetSecureIdAllowed
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70e61c158a7dfcafb6d1d5ac66833e42284b818d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681964"
---
# <a name="setsecureidallowed-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="1ceae-106">Метод Сетсекуреидалловед \_ класса Win32 тсгатевайконнектионаусоризатионполици</span><span class="sxs-lookup"><span data-stu-id="1ceae-106">SetSecureIdAllowed method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="1ceae-107">Этот метод зарезервирован для использования в будущем.</span><span class="sxs-lookup"><span data-stu-id="1ceae-107">This method is reserved for future use.</span></span>

<span data-ttu-id="1ceae-108">Задает свойство **секуреидалловед** , которое зарезервировано для использования в будущем.</span><span class="sxs-lookup"><span data-stu-id="1ceae-108">Sets the **SecureIdAllowed** property, which is reserved for future use.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ceae-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1ceae-109">Syntax</span></span>


```mof
uint32 SetSecureIdAllowed(
  [in] boolean Allowed
);
```



## <a name="parameters"></a><span data-ttu-id="1ceae-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="1ceae-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ceae-111">*Разрешено* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1ceae-111">*Allowed* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ceae-112">Новое значение **секуреидалловед** .</span><span class="sxs-lookup"><span data-stu-id="1ceae-112">New **SecureIdAllowed** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ceae-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1ceae-113">Return value</span></span>

<span data-ttu-id="1ceae-114">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="1ceae-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="1ceae-115">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="1ceae-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="1ceae-116">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="1ceae-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="1ceae-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1ceae-117">Remarks</span></span>

<span data-ttu-id="1ceae-118">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="1ceae-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="1ceae-119">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="1ceae-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="1ceae-120">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="1ceae-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="1ceae-121">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="1ceae-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="1ceae-122">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="1ceae-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="1ceae-123">Требования</span><span class="sxs-lookup"><span data-stu-id="1ceae-123">Requirements</span></span>



| <span data-ttu-id="1ceae-124">Требование</span><span class="sxs-lookup"><span data-stu-id="1ceae-124">Requirement</span></span> | <span data-ttu-id="1ceae-125">Значение</span><span class="sxs-lookup"><span data-stu-id="1ceae-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ceae-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1ceae-126">Minimum supported client</span></span><br/> | <span data-ttu-id="1ceae-127">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="1ceae-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="1ceae-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1ceae-128">Minimum supported server</span></span><br/> | <span data-ttu-id="1ceae-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1ceae-129">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="1ceae-130">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="1ceae-130">Namespace</span></span><br/>                | <span data-ttu-id="1ceae-131">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="1ceae-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="1ceae-132">MOF</span><span class="sxs-lookup"><span data-stu-id="1ceae-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1ceae-133"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1ceae-133"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="1ceae-134">DLL</span><span class="sxs-lookup"><span data-stu-id="1ceae-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1ceae-135"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1ceae-135"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="1ceae-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1ceae-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ceae-137">**\_Тсгатевайконнектионаусоризатионполици Win32**</span><span class="sxs-lookup"><span data-stu-id="1ceae-137">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

