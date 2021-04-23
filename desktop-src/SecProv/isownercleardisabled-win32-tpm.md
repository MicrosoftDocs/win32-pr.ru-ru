---
description: Метод Исовнерклеардисаблед \_ класса TPM Win32 указывает, ограничен ли владелец устройства очисткой устройства.
ms.assetid: 04f98e9b-c1a0-4828-b7cb-67b32d7470ea
title: Метод Исовнерклеардисаблед класса Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsOwnerClearDisabled
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 13e8b7de707cb1b1af4d4ccdb1208c6391e26987
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683925"
---
# <a name="isownercleardisabled-method-of-the-win32_tpm-class"></a><span data-ttu-id="285ad-103">Метод Исовнерклеардисаблед \_ класса TPM Win32</span><span class="sxs-lookup"><span data-stu-id="285ad-103">IsOwnerClearDisabled method of the Win32\_Tpm class</span></span>

<span data-ttu-id="285ad-104">Метод **исовнерклеардисаблед** класса [**\_ TPM Win32**](win32-tpm.md) указывает, ограничен ли владелец устройства очисткой устройства.</span><span class="sxs-lookup"><span data-stu-id="285ad-104">The **IsOwnerClearDisabled** method of the [**Win32\_Tpm**](win32-tpm.md) class indicates whether the device owner is restricted from clearing the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="285ad-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="285ad-105">Syntax</span></span>


```mof
uint32 IsOwnerClearDisabled(
  [out] boolean IsOwnerClearDisabled
);
```



## <a name="parameters"></a><span data-ttu-id="285ad-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="285ad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="285ad-107">*Исовнерклеардисаблед* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="285ad-107">*IsOwnerClearDisabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="285ad-108">Тип: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="285ad-108">Type: **boolean**</span></span>

<span data-ttu-id="285ad-109">Если **значение — true**, владелец устройства не может очистить устройство.</span><span class="sxs-lookup"><span data-stu-id="285ad-109">If **true**, the device owner is unable to clear the device.</span></span> <span data-ttu-id="285ad-110">Только физически представленный пользователь может очистить устройство.</span><span class="sxs-lookup"><span data-stu-id="285ad-110">Only a physically present user may be able to clear the device.</span></span> <span data-ttu-id="285ad-111">Если задано **значение false**, владелец устройства может очистить устройство.</span><span class="sxs-lookup"><span data-stu-id="285ad-111">If **false**, the device owner is able to clear the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="285ad-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="285ad-112">Return value</span></span>

<span data-ttu-id="285ad-113">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="285ad-113">Type: **uint32**</span></span>

<span data-ttu-id="285ad-114">Могут возвращаться все ошибки доверенного платформенного модуля, а также ошибки, относящиеся к базовым службам TPM.</span><span class="sxs-lookup"><span data-stu-id="285ad-114">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="285ad-115">Ниже приведены общие коды возврата.</span><span class="sxs-lookup"><span data-stu-id="285ad-115">Common return codes are listed below.</span></span>



| <span data-ttu-id="285ad-116">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="285ad-116">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="285ad-117">Описание</span><span class="sxs-lookup"><span data-stu-id="285ad-117">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="285ad-118"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="285ad-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="285ad-119">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="285ad-119">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="285ad-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="285ad-120">Remarks</span></span>

<span data-ttu-id="285ad-121">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="285ad-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="285ad-122">MOF-файлы не устанавливаются в составе Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="285ad-122">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="285ad-123">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="285ad-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="285ad-124">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="285ad-124">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="285ad-125">Требования</span><span class="sxs-lookup"><span data-stu-id="285ad-125">Requirements</span></span>



| <span data-ttu-id="285ad-126">Требование</span><span class="sxs-lookup"><span data-stu-id="285ad-126">Requirement</span></span> | <span data-ttu-id="285ad-127">Значение</span><span class="sxs-lookup"><span data-stu-id="285ad-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="285ad-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="285ad-128">Minimum supported client</span></span><br/> | <span data-ttu-id="285ad-129">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="285ad-129">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="285ad-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="285ad-130">Minimum supported server</span></span><br/> | <span data-ttu-id="285ad-131">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="285ad-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="285ad-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="285ad-132">Namespace</span></span><br/>                | <span data-ttu-id="285ad-133">Корневой \\ CIMV2 \\ безопасности \\ микрософттпм</span><span class="sxs-lookup"><span data-stu-id="285ad-133">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="285ad-134">MOF</span><span class="sxs-lookup"><span data-stu-id="285ad-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="285ad-135"><dt>Win32 \_ TPM. mof</dt></span><span class="sxs-lookup"><span data-stu-id="285ad-135"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="285ad-136">DLL</span><span class="sxs-lookup"><span data-stu-id="285ad-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="285ad-137"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="285ad-137"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="285ad-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="285ad-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="285ad-139">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="285ad-139">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
