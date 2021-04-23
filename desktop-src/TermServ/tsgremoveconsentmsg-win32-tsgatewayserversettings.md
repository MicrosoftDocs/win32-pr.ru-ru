---
title: Метод Тсгремовеконсентмсг класса Win32_TSGatewayServerSettings
description: Удаляет административное сообщение для сервера шлюза. | Метод Тсгремовеконсентмсг класса Win32_TSGatewayServerSettings
ms.assetid: 626dc9ca-d6a1-48ab-84ec-cfccb8e720c2
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Тсгремовеконсентмсг
- Службы удаленных рабочих столов метода Тсгремовеконсентмсг, класс Win32_TSGatewayServerSettings
- Класс Win32_TSGatewayServerSettings службы удаленных рабочих столов, метод Тсгремовеконсентмсг
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.TSGRemoveConsentMsg
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24cd002ebb1a953d25cf129b4e5f3b4174842199
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "103914571"
---
# <a name="tsgremoveconsentmsg-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="a3924-107">Метод Тсгремовеконсентмсг \_ класса Win32 тсгатевайсерверсеттингс</span><span class="sxs-lookup"><span data-stu-id="a3924-107">TSGRemoveConsentMsg method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="a3924-108">Удаляет административное сообщение для сервера шлюза.</span><span class="sxs-lookup"><span data-stu-id="a3924-108">Removes the administrative message for the gateway server.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3924-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a3924-109">Syntax</span></span>


```mof
uint32 TSGRemoveConsentMsg();
```



## <a name="parameters"></a><span data-ttu-id="a3924-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="a3924-110">Parameters</span></span>

<span data-ttu-id="a3924-111">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="a3924-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a3924-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a3924-112">Return value</span></span>

<span data-ttu-id="a3924-113">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a3924-113">Type: **uint32**</span></span>

<span data-ttu-id="a3924-114">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="a3924-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="a3924-115">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="a3924-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="a3924-116">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="a3924-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a3924-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a3924-117">Remarks</span></span>

<span data-ttu-id="a3924-118">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="a3924-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="a3924-119">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="a3924-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="a3924-120">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="a3924-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="a3924-121">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="a3924-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="a3924-122">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="a3924-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="a3924-123">Требования</span><span class="sxs-lookup"><span data-stu-id="a3924-123">Requirements</span></span>



| <span data-ttu-id="a3924-124">Требование</span><span class="sxs-lookup"><span data-stu-id="a3924-124">Requirement</span></span> | <span data-ttu-id="a3924-125">Значение</span><span class="sxs-lookup"><span data-stu-id="a3924-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3924-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a3924-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a3924-127">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="a3924-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="a3924-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a3924-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a3924-129">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a3924-129">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="a3924-130">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a3924-130">Namespace</span></span><br/>                | <span data-ttu-id="a3924-131">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="a3924-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="a3924-132">MOF</span><span class="sxs-lookup"><span data-stu-id="a3924-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a3924-133"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a3924-133"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="a3924-134">DLL</span><span class="sxs-lookup"><span data-stu-id="a3924-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a3924-135"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a3924-135"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="a3924-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a3924-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3924-137">**\_Тсгатевайсерверсеттингс Win32**</span><span class="sxs-lookup"><span data-stu-id="a3924-137">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

