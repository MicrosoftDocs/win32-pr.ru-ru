---
title: Метод Дисконнектусер класса Win32_TSGatewayConnection (Тсгаусентикатионенгине. h)
description: Отключает все подключения указанного пользователя от сервера шлюза удаленный рабочий стол (шлюза удаленных рабочих столов).
ms.assetid: 3c5d66b6-c1f0-4a91-bf93-be886d8e2391
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Дисконнектусер
- Службы удаленных рабочих столов метода Дисконнектусер, класс Win32_TSGatewayConnection
- Класс Win32_TSGatewayConnection службы удаленных рабочих столов, метод Дисконнектусер
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnection.DisconnectUser
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e223a2de36ad6c2a6fcabc446fe88cad27dc5da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802764"
---
# <a name="disconnectuser-method-of-the-win32_tsgatewayconnection-class"></a><span data-ttu-id="0f865-106">Метод Дисконнектусер \_ класса Win32 тсгатевайконнектион</span><span class="sxs-lookup"><span data-stu-id="0f865-106">DisconnectUser method of the Win32\_TSGatewayConnection class</span></span>

<span data-ttu-id="0f865-107">Отключает все подключения указанного пользователя от сервера шлюза удаленный рабочий стол (шлюза удаленных рабочих столов).</span><span class="sxs-lookup"><span data-stu-id="0f865-107">Disconnects all connections of the specified user from the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f865-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0f865-108">Syntax</span></span>


```mof
uint32 DisconnectUser(
  [in] string UserName
);
```



## <a name="parameters"></a><span data-ttu-id="0f865-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="0f865-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f865-110">*Имя пользователя* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0f865-110">*UserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f865-111">Имя пользователя в формате \* домен \* **\\** _имя пользователя_ , подключения которого должны быть отключены.</span><span class="sxs-lookup"><span data-stu-id="0f865-111">The user name, in \*Domain\***\\**_UserName_ format, whose connections are to be disconnected.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f865-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0f865-112">Return value</span></span>

<span data-ttu-id="0f865-113">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="0f865-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="0f865-114">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="0f865-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="0f865-115">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="0f865-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0f865-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0f865-116">Remarks</span></span>

<span data-ttu-id="0f865-117">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="0f865-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="0f865-118">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="0f865-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="0f865-119">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="0f865-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="0f865-120">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="0f865-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="0f865-121">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="0f865-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="0f865-122">Требования</span><span class="sxs-lookup"><span data-stu-id="0f865-122">Requirements</span></span>



| <span data-ttu-id="0f865-123">Требование</span><span class="sxs-lookup"><span data-stu-id="0f865-123">Requirement</span></span> | <span data-ttu-id="0f865-124">Значение</span><span class="sxs-lookup"><span data-stu-id="0f865-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f865-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0f865-125">Minimum supported client</span></span><br/> | <span data-ttu-id="0f865-126">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="0f865-126">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="0f865-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0f865-127">Minimum supported server</span></span><br/> | <span data-ttu-id="0f865-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0f865-128">Windows Server 2008</span></span><br/>                                                                       |
| <span data-ttu-id="0f865-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="0f865-129">Namespace</span></span><br/>                | <span data-ttu-id="0f865-130">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="0f865-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                             |
| <span data-ttu-id="0f865-131">Header</span><span class="sxs-lookup"><span data-stu-id="0f865-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f865-132"><dt>Тсгаусентикатионенгине. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f865-132"><dt>Tsgauthenticationengine.h</dt></span></span> </dl> |
| <span data-ttu-id="0f865-133">MOF</span><span class="sxs-lookup"><span data-stu-id="0f865-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0f865-134"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0f865-134"><dt>TSGateway.mof</dt></span></span> </dl>             |
| <span data-ttu-id="0f865-135">DLL</span><span class="sxs-lookup"><span data-stu-id="0f865-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f865-136"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f865-136"><dt>AagWmi.dll</dt></span></span> </dl>                |



## <a name="see-also"></a><span data-ttu-id="0f865-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0f865-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f865-138">**\_Тсгатевайконнектион Win32**</span><span class="sxs-lookup"><span data-stu-id="0f865-138">**Win32\_TSGatewayConnection**</span></span>](win32-tsgatewayconnection.md)
</dt> </dl>

 

