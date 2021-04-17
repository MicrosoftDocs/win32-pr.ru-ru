---
title: Метод Сетполиципропертинаме класса Win32_TerminalServiceSetting
description: Метод Сетполиципропертинаме задает свойство Делететемпфолдерс, Усетемпфолдерс или Help для класса.
ms.assetid: 18d9927a-b7db-46c7-90ee-00da6de06202
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетполиципропертинаме
- Службы удаленных рабочих столов метода Сетполиципропертинаме, класс Win32_TerminalServiceSetting
- Класс Win32_TerminalServiceSetting службы удаленных рабочих столов, метод Сетполиципропертинаме
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetPolicyPropertyName
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f49732fa916dd3c37539dc35d6cef7a4d920d81
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492723"
---
# <a name="setpolicypropertyname-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="fbf08-106">Метод Сетполиципропертинаме \_ класса Win32 терминалсервицесеттинг</span><span class="sxs-lookup"><span data-stu-id="fbf08-106">SetPolicyPropertyName method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="fbf08-107">Метод **сетполиципропертинаме** задает свойство **делететемпфолдерс**, **усетемпфолдерс** или **Help** для класса.</span><span class="sxs-lookup"><span data-stu-id="fbf08-107">The **SetPolicyPropertyName** method sets the **DeleteTempFolders**, **UseTempFolders** or **Help** property for the class.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbf08-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fbf08-108">Syntax</span></span>


```mof
uint32 SetPolicyPropertyName(
  [in] string  PropertyName,
  [in] boolean Value
);
```



## <a name="parameters"></a><span data-ttu-id="fbf08-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="fbf08-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fbf08-110">*PropertyName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fbf08-110">*PropertyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbf08-111">Задает свойство политики, которое задается методом.</span><span class="sxs-lookup"><span data-stu-id="fbf08-111">Specifies the policy property that the method is setting.</span></span>

<dt>

<span id="DeleteTempFolders"></span><span id="deletetempfolders"></span><span id="DELETETEMPFOLDERS"></span>

<span data-ttu-id="fbf08-112"><span id="DeleteTempFolders"></span><span id="deletetempfolders"></span><span id="DELETETEMPFOLDERS"></span>**делететемпфолдерс**</span><span class="sxs-lookup"><span data-stu-id="fbf08-112"><span id="DeleteTempFolders"></span><span id="deletetempfolders"></span><span id="DELETETEMPFOLDERS"></span>**DeleteTempFolders**</span></span>


</dt> <dd>

<span data-ttu-id="fbf08-113">Метод устанавливает свойство **делететемпфолдерс** .</span><span class="sxs-lookup"><span data-stu-id="fbf08-113">The method is setting the **DeleteTempFolders** property.</span></span>

</dd> <dt>

<span id="UseTempFolders"></span><span id="usetempfolders"></span><span id="USETEMPFOLDERS"></span>

<span data-ttu-id="fbf08-114"><span id="UseTempFolders"></span><span id="usetempfolders"></span><span id="USETEMPFOLDERS"></span>**усетемпфолдерс**</span><span class="sxs-lookup"><span data-stu-id="fbf08-114"><span id="UseTempFolders"></span><span id="usetempfolders"></span><span id="USETEMPFOLDERS"></span>**UseTempFolders**</span></span>


</dt> <dd>

<span data-ttu-id="fbf08-115">Метод устанавливает свойство **усетемпфолдерс** .</span><span class="sxs-lookup"><span data-stu-id="fbf08-115">The method is setting the **UseTempFolders** property.</span></span>

</dd> <dt>

<span id="Help"></span><span id="help"></span><span id="HELP"></span>

<span data-ttu-id="fbf08-116"><span id="Help"></span><span id="help"></span><span id="HELP"></span>**Справка**</span><span class="sxs-lookup"><span data-stu-id="fbf08-116"><span id="Help"></span><span id="help"></span><span id="HELP"></span>**Help**</span></span>


</dt> <dd>

<span data-ttu-id="fbf08-117">Метод задает свойство **Help** .</span><span class="sxs-lookup"><span data-stu-id="fbf08-117">The method is setting the **Help** property.</span></span>

<span data-ttu-id="fbf08-118">**Справка по** **заметкам** не поддерживается  </span><span class="sxs-lookup"><span data-stu-id="fbf08-118">**Note**  **Help** is not supported</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="fbf08-119">*Значение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fbf08-119">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbf08-120">Значение, указывающее, следует ли включать или отключать свойство, заданное параметром *PropertyName* .</span><span class="sxs-lookup"><span data-stu-id="fbf08-120">Value that indicates whether to enable or disable the property specified by the *PropertyName* parameter.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="fbf08-121"><span id="0"></span>**0,0**</span><span class="sxs-lookup"><span data-stu-id="fbf08-121"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="fbf08-122">Отключите свойство.</span><span class="sxs-lookup"><span data-stu-id="fbf08-122">Disable the property.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="fbf08-123"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="fbf08-123"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="fbf08-124">Включите свойство.</span><span class="sxs-lookup"><span data-stu-id="fbf08-124">Enable the property.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fbf08-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fbf08-125">Return value</span></span>

<span data-ttu-id="fbf08-126">Возвращает успешное завершение, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="fbf08-126">Returns Success on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="fbf08-127">Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="fbf08-127">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="fbf08-128">Метод возвращает ошибку, если параметр находится в разделе Управление групповой политикой.</span><span class="sxs-lookup"><span data-stu-id="fbf08-128">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="fbf08-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fbf08-129">Remarks</span></span>

<span data-ttu-id="fbf08-130">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="fbf08-130">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="fbf08-131">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="fbf08-131">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="fbf08-132">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="fbf08-132">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="fbf08-133">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="fbf08-133">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="fbf08-134">Требования</span><span class="sxs-lookup"><span data-stu-id="fbf08-134">Requirements</span></span>



| <span data-ttu-id="fbf08-135">Требование</span><span class="sxs-lookup"><span data-stu-id="fbf08-135">Requirement</span></span> | <span data-ttu-id="fbf08-136">Значение</span><span class="sxs-lookup"><span data-stu-id="fbf08-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fbf08-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fbf08-137">Minimum supported client</span></span><br/> | <span data-ttu-id="fbf08-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fbf08-138">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fbf08-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fbf08-139">Minimum supported server</span></span><br/> | <span data-ttu-id="fbf08-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fbf08-140">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fbf08-141">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="fbf08-141">Namespace</span></span><br/>                | <span data-ttu-id="fbf08-142">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="fbf08-142">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="fbf08-143">MOF</span><span class="sxs-lookup"><span data-stu-id="fbf08-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fbf08-144"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fbf08-144"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="fbf08-145">DLL</span><span class="sxs-lookup"><span data-stu-id="fbf08-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fbf08-146"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fbf08-146"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fbf08-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fbf08-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbf08-148">**\_Терминалсервицесеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="fbf08-148">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

