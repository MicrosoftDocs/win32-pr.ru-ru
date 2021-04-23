---
title: Метод Делетикс класса Win32_SessionBrokerFarmAccount
description: Класс Win32 \_ сессионброкерфармаккаунт больше не доступен для использования в Windows Server 2012. | Метод Делетикс класса Win32_SessionBrokerFarmAccount
ms.assetid: d30c5d3e-f63c-4b21-85ae-a0b8d5868d64
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Делетикс
- Службы удаленных рабочих столов метода Делетикс, класс Win32_SessionBrokerFarmAccount
- Класс Win32_SessionBrokerFarmAccount службы удаленных рабочих столов, метод Делетикс
topic_type:
- apiref
api_name:
- Win32_SessionBrokerFarmAccount.DeleteEx
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdad7b1c7af85337ace59690bb44f4309254eb76
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105684831"
---
# <a name="deleteex-method-of-the-win32_sessionbrokerfarmaccount-class"></a><span data-ttu-id="53e7f-107">Метод Делетикс \_ класса Win32 сессионброкерфармаккаунт</span><span class="sxs-lookup"><span data-stu-id="53e7f-107">DeleteEx method of the Win32\_SessionBrokerFarmAccount class</span></span>

<span data-ttu-id="53e7f-108">\[Класс [**Win32 \_ сессионброкерфармаккаунт**](win32-sessionbrokerfarmaccount.md) больше не доступен для использования в Windows Server 2012.\]</span><span class="sxs-lookup"><span data-stu-id="53e7f-108">\[The [**Win32\_SessionBrokerFarmAccount**](win32-sessionbrokerfarmaccount.md) class is no longer available for use as of Windows Server 2012.\]</span></span>

<span data-ttu-id="53e7f-109">Удаляет учетную запись фермы.</span><span class="sxs-lookup"><span data-stu-id="53e7f-109">Deletes the farm account.</span></span>

## <a name="syntax"></a><span data-ttu-id="53e7f-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="53e7f-110">Syntax</span></span>


```mof
uint32 DeleteEx(
  [in] boolean DeleteComputerObject
);
```



## <a name="parameters"></a><span data-ttu-id="53e7f-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="53e7f-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53e7f-112">*Делетекомпутеробжект* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="53e7f-112">*DeleteComputerObject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53e7f-113">Указывает, следует ли удалять объект-компьютер, связанный с фермой, из Active Directory.</span><span class="sxs-lookup"><span data-stu-id="53e7f-113">Indicates whether the computer object associated with the farm is to be removed from Active Directory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53e7f-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="53e7f-114">Return value</span></span>

<span data-ttu-id="53e7f-115">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="53e7f-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="53e7f-116">Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="53e7f-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="53e7f-117">Требования</span><span class="sxs-lookup"><span data-stu-id="53e7f-117">Requirements</span></span>



| <span data-ttu-id="53e7f-118">Требование</span><span class="sxs-lookup"><span data-stu-id="53e7f-118">Requirement</span></span> | <span data-ttu-id="53e7f-119">Значение</span><span class="sxs-lookup"><span data-stu-id="53e7f-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="53e7f-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="53e7f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="53e7f-121">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="53e7f-121">None supported</span></span><br/>                                                              |
| <span data-ttu-id="53e7f-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="53e7f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="53e7f-123">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="53e7f-123">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="53e7f-124">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="53e7f-124">End of client support</span></span><br/>    | <span data-ttu-id="53e7f-125">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="53e7f-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="53e7f-126">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="53e7f-126">End of server support</span></span><br/>    | <span data-ttu-id="53e7f-127">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="53e7f-127">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="53e7f-128">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="53e7f-128">Namespace</span></span><br/>                | <span data-ttu-id="53e7f-129">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="53e7f-129">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="53e7f-130">MOF</span><span class="sxs-lookup"><span data-stu-id="53e7f-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="53e7f-131"><dt>Тссдвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="53e7f-131"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="53e7f-132">DLL</span><span class="sxs-lookup"><span data-stu-id="53e7f-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="53e7f-133"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53e7f-133"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53e7f-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="53e7f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53e7f-135">**\_Сессионброкерфармаккаунт Win32**</span><span class="sxs-lookup"><span data-stu-id="53e7f-135">**Win32\_SessionBrokerFarmAccount**</span></span>](win32-sessionbrokerfarmaccount.md)
</dt> </dl>

 

 





