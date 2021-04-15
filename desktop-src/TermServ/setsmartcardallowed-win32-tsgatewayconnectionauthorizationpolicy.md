---
title: Метод Сетсмарткардалловед класса Win32_TSGatewayConnectionAuthorizationPolicy
description: Задает свойство Смарткардалловед, которое включает или отключает поддержку использования смарт-карты для подключения к серверу шлюза удаленный рабочий стол (шлюз удаленных рабочих столов).
ms.assetid: 9fe1c7a9-2bab-439f-8dc2-421ed876fcf7
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетсмарткардалловед
- Службы удаленных рабочих столов метода Сетсмарткардалловед, класс Win32_TSGatewayConnectionAuthorizationPolicy
- Класс Win32_TSGatewayConnectionAuthorizationPolicy службы удаленных рабочих столов, метод Сетсмарткардалловед
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetSmartcardAllowed
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 022b5461086ae05f198cbce4faaee0e9c36bf77e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415840"
---
# <a name="setsmartcardallowed-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="740e2-106">Метод Сетсмарткардалловед \_ класса Win32 тсгатевайконнектионаусоризатионполици</span><span class="sxs-lookup"><span data-stu-id="740e2-106">SetSmartcardAllowed method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="740e2-107">Задает свойство **смарткардалловед** , которое включает или отключает поддержку использования смарт-карты для подключения к серверу шлюза удаленный рабочий стол (шлюз удаленных рабочих столов).</span><span class="sxs-lookup"><span data-stu-id="740e2-107">Sets the **SmartcardAllowed** property, which enables or disables support for using a smart card to connect to the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="740e2-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="740e2-108">Syntax</span></span>


```mof
uint32 SetSmartcardAllowed(
  [in] boolean Allowed
);
```



## <a name="parameters"></a><span data-ttu-id="740e2-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="740e2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="740e2-110">*Разрешено* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="740e2-110">*Allowed* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="740e2-111">Новое значение **смарткардалловед** .</span><span class="sxs-lookup"><span data-stu-id="740e2-111">New **SmartcardAllowed** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="740e2-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="740e2-112">Return value</span></span>

<span data-ttu-id="740e2-113">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="740e2-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="740e2-114">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="740e2-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="740e2-115">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="740e2-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="740e2-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="740e2-116">Remarks</span></span>

<span data-ttu-id="740e2-117">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="740e2-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="740e2-118">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="740e2-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="740e2-119">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="740e2-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="740e2-120">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="740e2-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="740e2-121">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="740e2-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="740e2-122">Требования</span><span class="sxs-lookup"><span data-stu-id="740e2-122">Requirements</span></span>



| <span data-ttu-id="740e2-123">Требование</span><span class="sxs-lookup"><span data-stu-id="740e2-123">Requirement</span></span> | <span data-ttu-id="740e2-124">Значение</span><span class="sxs-lookup"><span data-stu-id="740e2-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="740e2-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="740e2-125">Minimum supported client</span></span><br/> | <span data-ttu-id="740e2-126">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="740e2-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="740e2-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="740e2-127">Minimum supported server</span></span><br/> | <span data-ttu-id="740e2-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="740e2-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="740e2-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="740e2-129">Namespace</span></span><br/>                | <span data-ttu-id="740e2-130">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="740e2-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="740e2-131">MOF</span><span class="sxs-lookup"><span data-stu-id="740e2-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="740e2-132"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="740e2-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="740e2-133">DLL</span><span class="sxs-lookup"><span data-stu-id="740e2-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="740e2-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="740e2-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="740e2-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="740e2-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="740e2-136">**\_Тсгатевайконнектионаусоризатионполици Win32**</span><span class="sxs-lookup"><span data-stu-id="740e2-136">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

