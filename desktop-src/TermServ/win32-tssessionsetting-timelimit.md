---
title: Метод Тимелимит класса Win32_TSSessionSetting
description: Задает максимальное время, выделенное для указанного типа ограничения сеанса.
ms.assetid: 55194197-ffb6-49ae-827a-478ced867ab0
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Тимелимит
- Службы удаленных рабочих столов метода Тимелимит, класс Win32_TSSessionSetting
- Класс Win32_TSSessionSetting службы удаленных рабочих столов, метод Тимелимит
topic_type:
- apiref
api_name:
- Win32_TSSessionSetting.TimeLimit
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4016c28de50d31338d9bc6ec50ef1497c7a561da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533782"
---
# <a name="timelimit-method-of-the-win32_tssessionsetting-class"></a><span data-ttu-id="b1769-106">Метод Тимелимит \_ класса Win32 тссессионсеттинг</span><span class="sxs-lookup"><span data-stu-id="b1769-106">TimeLimit method of the Win32\_TSSessionSetting class</span></span>

<span data-ttu-id="b1769-107">Задает максимальное время, выделенное для указанного типа ограничения сеанса.</span><span class="sxs-lookup"><span data-stu-id="b1769-107">Sets the maximum time allocated to the specified session-limit type.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1769-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b1769-108">Syntax</span></span>


```mof
uint32 TimeLimit(
  [in] string SessionLimitType,
  [in] uint32 ValueLimit
);
```



## <a name="parameters"></a><span data-ttu-id="b1769-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="b1769-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1769-110">*Сессионлимиттипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b1769-110">*SessionLimitType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1769-111">Указывает тип свойства ограничения сеанса, которое задается методом.</span><span class="sxs-lookup"><span data-stu-id="b1769-111">Specifies the type of session-limit property that the method is setting.</span></span>

<dt>

<span id="ActiveSessionLimit"></span><span id="activesessionlimit"></span><span id="ACTIVESESSIONLIMIT"></span>

<span data-ttu-id="b1769-112"><span id="ActiveSessionLimit"></span><span id="activesessionlimit"></span><span id="ACTIVESESSIONLIMIT"></span>**активесессионлимит**</span><span class="sxs-lookup"><span data-stu-id="b1769-112"><span id="ActiveSessionLimit"></span><span id="activesessionlimit"></span><span id="ACTIVESESSIONLIMIT"></span>**ActiveSessionLimit**</span></span>


</dt> <dd>

<span data-ttu-id="b1769-113">Метод устанавливает свойство **активесессионлимит** .</span><span class="sxs-lookup"><span data-stu-id="b1769-113">The method is setting the **ActiveSessionLimit** property.</span></span>

</dd> <dt>

<span id="DisconnectedSessionLimit"></span><span id="disconnectedsessionlimit"></span><span id="DISCONNECTEDSESSIONLIMIT"></span>

<span data-ttu-id="b1769-114"><span id="DisconnectedSessionLimit"></span><span id="disconnectedsessionlimit"></span><span id="DISCONNECTEDSESSIONLIMIT"></span>**дисконнектедсессионлимит**</span><span class="sxs-lookup"><span data-stu-id="b1769-114"><span id="DisconnectedSessionLimit"></span><span id="disconnectedsessionlimit"></span><span id="DISCONNECTEDSESSIONLIMIT"></span>**DisconnectedSessionLimit**</span></span>


</dt> <dd>

<span data-ttu-id="b1769-115">Метод устанавливает свойство **дисконнектедсессионлимит** .</span><span class="sxs-lookup"><span data-stu-id="b1769-115">The method is setting the **DisconnectedSessionLimit** property.</span></span>

</dd> <dt>

<span id="IdleSessionLimit"></span><span id="idlesessionlimit"></span><span id="IDLESESSIONLIMIT"></span>

<span data-ttu-id="b1769-116"><span id="IdleSessionLimit"></span><span id="idlesessionlimit"></span><span id="IDLESESSIONLIMIT"></span>**идлесессионлимит**</span><span class="sxs-lookup"><span data-stu-id="b1769-116"><span id="IdleSessionLimit"></span><span id="idlesessionlimit"></span><span id="IDLESESSIONLIMIT"></span>**IdleSessionLimit**</span></span>


</dt> <dd>

<span data-ttu-id="b1769-117">Метод устанавливает свойство **идлесессионлимит** .</span><span class="sxs-lookup"><span data-stu-id="b1769-117">The method is setting the **IdleSessionLimit** property.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="b1769-118">*ValueLimit* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b1769-118">*ValueLimit* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1769-119">Новое максимальное время в миллисекундах для свойства, указанного параметром *сессионлимиттипе* .</span><span class="sxs-lookup"><span data-stu-id="b1769-119">The new maximum time, in milliseconds, for the property specified by the *SessionLimitType* parameter.</span></span> <span data-ttu-id="b1769-120">Нулевое значение указывает на отсутствие ограничения сеанса.</span><span class="sxs-lookup"><span data-stu-id="b1769-120">The value zero indicates that there is no session limit.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1769-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b1769-121">Return value</span></span>

<span data-ttu-id="b1769-122">Возвращает успешное завершение, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="b1769-122">Returns Success on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="b1769-123">Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="b1769-123">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="b1769-124">Метод возвращает ошибку, если параметр находится в разделе Управление групповой политикой.</span><span class="sxs-lookup"><span data-stu-id="b1769-124">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1769-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b1769-125">Remarks</span></span>

<span data-ttu-id="b1769-126">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="b1769-126">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="b1769-127">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="b1769-127">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="b1769-128">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="b1769-128">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="b1769-129">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="b1769-129">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="b1769-130">Требования</span><span class="sxs-lookup"><span data-stu-id="b1769-130">Requirements</span></span>



| <span data-ttu-id="b1769-131">Требование</span><span class="sxs-lookup"><span data-stu-id="b1769-131">Requirement</span></span> | <span data-ttu-id="b1769-132">Значение</span><span class="sxs-lookup"><span data-stu-id="b1769-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1769-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b1769-133">Minimum supported client</span></span><br/> | <span data-ttu-id="b1769-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b1769-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b1769-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b1769-135">Minimum supported server</span></span><br/> | <span data-ttu-id="b1769-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b1769-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b1769-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b1769-137">Namespace</span></span><br/>                | <span data-ttu-id="b1769-138">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="b1769-138">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="b1769-139">MOF</span><span class="sxs-lookup"><span data-stu-id="b1769-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b1769-140"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b1769-140"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="b1769-141">DLL</span><span class="sxs-lookup"><span data-stu-id="b1769-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b1769-142"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b1769-142"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1769-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b1769-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1769-144">**\_Тссессионсеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="b1769-144">**Win32\_TSSessionSetting**</span></span>](win32-tssessionsetting.md)
</dt> </dl>

 

