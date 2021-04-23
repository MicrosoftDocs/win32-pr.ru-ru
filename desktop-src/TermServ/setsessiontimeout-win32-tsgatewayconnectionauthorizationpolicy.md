---
title: Метод Сетсессионтимеаут класса Win32_TSGatewayConnectionAuthorizationPolicy
description: Задает свойства SessionTimeout и Сессионтимеаутактион.
ms.assetid: 11491c97-3ef8-46c1-9504-696c613e374e
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетсессионтимеаут
- Службы удаленных рабочих столов метода Сетсессионтимеаут, класс Win32_TSGatewayConnectionAuthorizationPolicy
- Класс Win32_TSGatewayConnectionAuthorizationPolicy службы удаленных рабочих столов, метод Сетсессионтимеаут
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetSessionTimeout
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8e544b59ae4fe0b74d0c120e6884ab81743cac6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534547"
---
# <a name="setsessiontimeout-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="c3aa6-106">Метод Сетсессионтимеаут \_ класса Win32 тсгатевайконнектионаусоризатионполици</span><span class="sxs-lookup"><span data-stu-id="c3aa6-106">SetSessionTimeout method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="c3aa6-107">Задает свойства **SessionTimeout** и **сессионтимеаутактион** .</span><span class="sxs-lookup"><span data-stu-id="c3aa6-107">Sets the **SessionTimeout** and **SessionTimeoutAction** properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3aa6-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c3aa6-108">Syntax</span></span>


```mof
uint32 SetSessionTimeout(
  [in] uint32 SessionTimeout,
  [in] uint32 SessionTimeoutAction
);
```



## <a name="parameters"></a><span data-ttu-id="c3aa6-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="c3aa6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3aa6-110">*SessionTimeout* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c3aa6-110">*SessionTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3aa6-111">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c3aa6-111">Type: **uint32**</span></span>

<span data-ttu-id="c3aa6-112">Новое значение времени ожидания в минутах.</span><span class="sxs-lookup"><span data-stu-id="c3aa6-112">The new timeout value, in minutes.</span></span> <span data-ttu-id="c3aa6-113">Значение 0 означает отсутствие времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="c3aa6-113">A value of 0 means there is no timeout.</span></span>

</dd> <dt>

<span data-ttu-id="c3aa6-114">*Сессионтимеаутактион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c3aa6-114">*SessionTimeoutAction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3aa6-115">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c3aa6-115">Type: **uint32**</span></span>

<span data-ttu-id="c3aa6-116">Указывает действие, выполняемое в случае истечения времени ожидания сеанса.</span><span class="sxs-lookup"><span data-stu-id="c3aa6-116">Specifies the action to be taken in case of a session timeout.</span></span> <span data-ttu-id="c3aa6-117">Это может быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="c3aa6-117">This can be one of the following values.</span></span>

<dt>

<span data-ttu-id="c3aa6-118">0</span><span class="sxs-lookup"><span data-stu-id="c3aa6-118">0</span></span>
</dt> <dd>

<span data-ttu-id="c3aa6-119">Отключите сеанс.</span><span class="sxs-lookup"><span data-stu-id="c3aa6-119">Disconnect the session.</span></span>

</dd> <dt>

<span data-ttu-id="c3aa6-120">1</span><span class="sxs-lookup"><span data-stu-id="c3aa6-120">1</span></span>
</dt> <dd>

<span data-ttu-id="c3aa6-121">Попытка повторно авторизовать сеанс.</span><span class="sxs-lookup"><span data-stu-id="c3aa6-121">Attempt to re-authorize the session.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3aa6-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c3aa6-122">Return value</span></span>

<span data-ttu-id="c3aa6-123">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c3aa6-123">Type: **uint32**</span></span>

<span data-ttu-id="c3aa6-124">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="c3aa6-124">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="c3aa6-125">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="c3aa6-125">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="c3aa6-126">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="c3aa6-126">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c3aa6-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c3aa6-127">Remarks</span></span>

<span data-ttu-id="c3aa6-128">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="c3aa6-128">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="c3aa6-129">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="c3aa6-129">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="c3aa6-130">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="c3aa6-130">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="c3aa6-131">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="c3aa6-131">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="c3aa6-132">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="c3aa6-132">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="c3aa6-133">Требования</span><span class="sxs-lookup"><span data-stu-id="c3aa6-133">Requirements</span></span>



| <span data-ttu-id="c3aa6-134">Требование</span><span class="sxs-lookup"><span data-stu-id="c3aa6-134">Requirement</span></span> | <span data-ttu-id="c3aa6-135">Значение</span><span class="sxs-lookup"><span data-stu-id="c3aa6-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3aa6-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c3aa6-136">Minimum supported client</span></span><br/> | <span data-ttu-id="c3aa6-137">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="c3aa6-137">None supported</span></span><br/>                                                                |
| <span data-ttu-id="c3aa6-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c3aa6-138">Minimum supported server</span></span><br/> | <span data-ttu-id="c3aa6-139">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c3aa6-139">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="c3aa6-140">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c3aa6-140">Namespace</span></span><br/>                | <span data-ttu-id="c3aa6-141">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="c3aa6-141">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="c3aa6-142">MOF</span><span class="sxs-lookup"><span data-stu-id="c3aa6-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c3aa6-143"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c3aa6-143"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="c3aa6-144">DLL</span><span class="sxs-lookup"><span data-stu-id="c3aa6-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c3aa6-145"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c3aa6-145"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="c3aa6-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c3aa6-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3aa6-147">**\_Тсгатевайконнектионаусоризатионполици Win32**</span><span class="sxs-lookup"><span data-stu-id="c3aa6-147">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

