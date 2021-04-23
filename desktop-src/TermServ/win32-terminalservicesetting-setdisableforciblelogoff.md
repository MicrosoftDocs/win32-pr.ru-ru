---
title: Метод СетдисаблефорЦиблелогофф класса Win32_TerminalServiceSetting
description: Этот метод не поддерживается.
ms.assetid: 1b7ac0f2-c242-4ca8-bc4d-8111e63851eb
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода СетдисаблефорЦиблелогофф
- Службы удаленных рабочих столов метода СетдисаблефорЦиблелогофф, класс Win32_TerminalServiceSetting
- Класс Win32_TerminalServiceSetting службы удаленных рабочих столов, метод СетдисаблефорЦиблелогофф
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetDisableForcibleLogoff
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4ae62db188d0e3aa31ffd8e3993e793e9bb2bf3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490296"
---
# <a name="setdisableforciblelogoff-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="4c6a7-106">Метод СетдисаблефорЦиблелогофф \_ класса Win32 терминалсервицесеттинг</span><span class="sxs-lookup"><span data-stu-id="4c6a7-106">SetDisableForcibleLogoff method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="4c6a7-107">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="4c6a7-107">This method is not supported.</span></span>

<span data-ttu-id="4c6a7-108">**Windows Vista и Windows Server 2008:** Включает или отключает возможность принудительного завершения работы администратора, вошедшего в консоль.</span><span class="sxs-lookup"><span data-stu-id="4c6a7-108">**Windows Vista and Windows Server 2008:** Enables or disables whether an administrator logged onto the console can be forcibly logged off.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c6a7-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4c6a7-109">Syntax</span></span>


```mof
uint32 SetDisableForcibleLogoff(
  [in] uint32 DisableForcibleLogoff
);
```



## <a name="parameters"></a><span data-ttu-id="4c6a7-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="4c6a7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c6a7-111">*ДисаблефорЦиблелогофф* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4c6a7-111">*DisableForcibleLogoff* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c6a7-112">Флаг отключения или включения свойства **дисаблефорЦиблелогофф** , которое определяет, можно ли принудительно завершить работу администратора, выполнившего вход в консоль.</span><span class="sxs-lookup"><span data-stu-id="4c6a7-112">Flag disabling or enabling the **DisableForcibleLogoff** property, which determines whether an administrator that is logged on to the console can be forcibly logged off.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="4c6a7-113"><span id="0"></span>**0,0**</span><span class="sxs-lookup"><span data-stu-id="4c6a7-113"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="4c6a7-114">Отключите свойство.</span><span class="sxs-lookup"><span data-stu-id="4c6a7-114">Disable the property.</span></span> <span data-ttu-id="4c6a7-115">Подключенный администратор может принудительно завершить работу.</span><span class="sxs-lookup"><span data-stu-id="4c6a7-115">The connected administrator can be forcibly logged off.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="4c6a7-116"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="4c6a7-116"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="4c6a7-117">Включите свойство.</span><span class="sxs-lookup"><span data-stu-id="4c6a7-117">Enable the property.</span></span> <span data-ttu-id="4c6a7-118">Не удается принудительно завершить работу подключенного администратора.</span><span class="sxs-lookup"><span data-stu-id="4c6a7-118">The connected administrator cannot be forcibly logged off.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c6a7-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4c6a7-119">Return value</span></span>

<span data-ttu-id="4c6a7-120">Возвращает успешное завершение; в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="4c6a7-120">Returns Success on success; otherwise, returns a WMI error code.</span></span> <span data-ttu-id="4c6a7-121">Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="4c6a7-121">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c6a7-122">Требования</span><span class="sxs-lookup"><span data-stu-id="4c6a7-122">Requirements</span></span>



| <span data-ttu-id="4c6a7-123">Требование</span><span class="sxs-lookup"><span data-stu-id="4c6a7-123">Requirement</span></span> | <span data-ttu-id="4c6a7-124">Значение</span><span class="sxs-lookup"><span data-stu-id="4c6a7-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4c6a7-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4c6a7-125">Minimum supported client</span></span><br/> | <span data-ttu-id="4c6a7-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4c6a7-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4c6a7-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4c6a7-127">Minimum supported server</span></span><br/> | <span data-ttu-id="4c6a7-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4c6a7-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4c6a7-129">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="4c6a7-129">End of client support</span></span><br/>    | <span data-ttu-id="4c6a7-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4c6a7-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4c6a7-131">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="4c6a7-131">End of server support</span></span><br/>    | <span data-ttu-id="4c6a7-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4c6a7-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4c6a7-133">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4c6a7-133">Namespace</span></span><br/>                | <span data-ttu-id="4c6a7-134">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="4c6a7-134">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="4c6a7-135">MOF</span><span class="sxs-lookup"><span data-stu-id="4c6a7-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4c6a7-136"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4c6a7-136"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="4c6a7-137">DLL</span><span class="sxs-lookup"><span data-stu-id="4c6a7-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4c6a7-138"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4c6a7-138"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c6a7-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4c6a7-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c6a7-140">**\_Терминалсервицесеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="4c6a7-140">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

 





