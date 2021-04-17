---
title: Метод Брокенконнектион класса Win32_TSSessionSetting (Втспротокол. h)
description: Задает свойство Брокенконнектионактион, которое является действием, которое сервер принимает, если достигнуто предельное время сеанса или если соединение разорвано.
ms.assetid: 2422e314-9e1c-4bed-a958-eedd2daeca66
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Брокенконнектион
- Службы удаленных рабочих столов метода Брокенконнектион, класс Win32_TSSessionSetting
- Класс Win32_TSSessionSetting службы удаленных рабочих столов, метод Брокенконнектион
topic_type:
- apiref
api_name:
- Win32_TSSessionSetting.BrokenConnection
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a90b3f6bada75812b37df014cedadfb4e7ff2e83
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681864"
---
# <a name="brokenconnection-method-of-the-win32_tssessionsetting-class"></a><span data-ttu-id="8eb5d-106">Метод Брокенконнектион \_ класса Win32 тссессионсеттинг</span><span class="sxs-lookup"><span data-stu-id="8eb5d-106">BrokenConnection method of the Win32\_TSSessionSetting class</span></span>

<span data-ttu-id="8eb5d-107">Задает свойство **брокенконнектионактион** , которое является действием, которое сервер принимает, если достигнуто предельное время сеанса или если соединение разорвано.</span><span class="sxs-lookup"><span data-stu-id="8eb5d-107">Sets the **BrokenConnectionAction** property, which is the action the server takes if the session time-limit is reached or if the connection is broken.</span></span>

## <a name="syntax"></a><span data-ttu-id="8eb5d-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8eb5d-108">Syntax</span></span>


```mof
uint32 BrokenConnection(
  [in] uint32 BrokenConnectionAction
);
```



## <a name="parameters"></a><span data-ttu-id="8eb5d-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="8eb5d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8eb5d-110">*Брокенконнектионактион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8eb5d-110">*BrokenConnectionAction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8eb5d-111">Предпринимаемое действие.</span><span class="sxs-lookup"><span data-stu-id="8eb5d-111">The action to take.</span></span>

<dt>

<span id="Disconnect"></span><span id="disconnect"></span><span id="DISCONNECT"></span>

<span data-ttu-id="8eb5d-112"><span id="Disconnect"></span><span id="disconnect"></span><span id="DISCONNECT"></span>**Отключить** (0)</span><span class="sxs-lookup"><span data-stu-id="8eb5d-112"><span id="Disconnect"></span><span id="disconnect"></span><span id="DISCONNECT"></span>**Disconnect** (0)</span></span>


</dt> <dd>

<span data-ttu-id="8eb5d-113">Пользователь отключен от сеанса.</span><span class="sxs-lookup"><span data-stu-id="8eb5d-113">The user is disconnected from the session.</span></span>

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span data-ttu-id="8eb5d-114"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Завершить** (1)</span><span class="sxs-lookup"><span data-stu-id="8eb5d-114"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminate** (1)</span></span>


</dt> <dd>

<span data-ttu-id="8eb5d-115">Сеанс окончательно удаляется с сервера.</span><span class="sxs-lookup"><span data-stu-id="8eb5d-115">The session is permanently deleted from the server.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8eb5d-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8eb5d-116">Return value</span></span>

<span data-ttu-id="8eb5d-117">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="8eb5d-117">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="8eb5d-118">Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="8eb5d-118">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="8eb5d-119">Метод возвращает ошибку, если параметр находится в элементе управления групповая политика.</span><span class="sxs-lookup"><span data-stu-id="8eb5d-119">The method returns an error if the setting is under Group Policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="8eb5d-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8eb5d-120">Remarks</span></span>

<span data-ttu-id="8eb5d-121">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="8eb5d-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="8eb5d-122">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="8eb5d-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="8eb5d-123">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="8eb5d-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="8eb5d-124">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="8eb5d-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="8eb5d-125">Требования</span><span class="sxs-lookup"><span data-stu-id="8eb5d-125">Requirements</span></span>



| <span data-ttu-id="8eb5d-126">Требование</span><span class="sxs-lookup"><span data-stu-id="8eb5d-126">Requirement</span></span> | <span data-ttu-id="8eb5d-127">Значение</span><span class="sxs-lookup"><span data-stu-id="8eb5d-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8eb5d-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8eb5d-128">Minimum supported client</span></span><br/> | <span data-ttu-id="8eb5d-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8eb5d-129">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="8eb5d-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8eb5d-130">Minimum supported server</span></span><br/> | <span data-ttu-id="8eb5d-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8eb5d-131">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="8eb5d-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="8eb5d-132">Namespace</span></span><br/>                | <span data-ttu-id="8eb5d-133">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="8eb5d-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="8eb5d-134">Header</span><span class="sxs-lookup"><span data-stu-id="8eb5d-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="8eb5d-135"><dt>Втспротокол. h</dt></span><span class="sxs-lookup"><span data-stu-id="8eb5d-135"><dt>Wtsprotocol.h</dt></span></span> </dl> |
| <span data-ttu-id="8eb5d-136">MOF</span><span class="sxs-lookup"><span data-stu-id="8eb5d-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8eb5d-137"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8eb5d-137"><dt>TSCfgWmi.mof</dt></span></span> </dl>  |
| <span data-ttu-id="8eb5d-138">DLL</span><span class="sxs-lookup"><span data-stu-id="8eb5d-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8eb5d-139"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8eb5d-139"><dt>TSCfgWmi.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="8eb5d-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8eb5d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8eb5d-141">**\_Тссессионсеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="8eb5d-141">**Win32\_TSSessionSetting**</span></span>](win32-tssessionsetting.md)
</dt> </dl>

 

