---
description: Метод Исовнершипалловед \_ класса TPM Win32 указывает, разрешена ли возможность установки владельца для устройства.
ms.assetid: dfeb5afe-4169-470b-b5e4-cf1e5781271e
title: Метод Исовнершипалловед класса Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsOwnershipAllowed
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: c818d5a4e4eb16ac637372f0c7ed0f2e9211ef88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262990"
---
# <a name="isownershipallowed-method-of-the-win32_tpm-class"></a><span data-ttu-id="4893f-103">Метод Исовнершипалловед \_ класса TPM Win32</span><span class="sxs-lookup"><span data-stu-id="4893f-103">IsOwnershipAllowed method of the Win32\_Tpm class</span></span>

<span data-ttu-id="4893f-104">Метод **исовнершипалловед** класса [**\_ TPM Win32**](win32-tpm.md) указывает, разрешена ли возможность установки владельца для устройства.</span><span class="sxs-lookup"><span data-stu-id="4893f-104">The **IsOwnershipAllowed** method of the [**Win32\_Tpm**](win32-tpm.md) class indicates whether the ability to install an owner for the device is permitted.</span></span>

## <a name="syntax"></a><span data-ttu-id="4893f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4893f-105">Syntax</span></span>


```mof
uint32 IsOwnershipAllowed(
  [out] boolean IsOwnershipAllowed
);
```



## <a name="parameters"></a><span data-ttu-id="4893f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4893f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4893f-107">*Исовнершипалловед* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="4893f-107">*IsOwnershipAllowed* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4893f-108">Тип: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="4893f-108">Type: **boolean**</span></span>

<span data-ttu-id="4893f-109">Если задано **значение true**, то разрешена возможность установки владельца устройства.</span><span class="sxs-lookup"><span data-stu-id="4893f-109">If **true**, the ability to install an owner for the device is permitted.</span></span> <span data-ttu-id="4893f-110">Если задано **значение false**, методу [**такеовнершип**](takeownership-win32-tpm.md) не удастся установить владельца для устройства.</span><span class="sxs-lookup"><span data-stu-id="4893f-110">If **false**, the method [**TakeOwnership**](takeownership-win32-tpm.md) will fail to install an owner for the device.</span></span>

<span data-ttu-id="4893f-111">Это значение можно изменить с помощью метода [**сетфисикалпресенцерекуест**](setphysicalpresencerequest-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="4893f-111">This value can be changed with the [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) method.</span></span> <span data-ttu-id="4893f-112">После выполнения метода [**clear**](clear-win32-tpm.md) значение сбрасывается в **true** .</span><span class="sxs-lookup"><span data-stu-id="4893f-112">The value is reset to **true** after the [**Clear**](clear-win32-tpm.md) method is run.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4893f-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4893f-113">Return value</span></span>

<span data-ttu-id="4893f-114">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4893f-114">Type: **uint32**</span></span>

<span data-ttu-id="4893f-115">Могут возвращаться все ошибки доверенного платформенного модуля, а также ошибки, относящиеся к базовым службам TPM.</span><span class="sxs-lookup"><span data-stu-id="4893f-115">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="4893f-116">Ниже приведены общие коды возврата.</span><span class="sxs-lookup"><span data-stu-id="4893f-116">Common return codes are listed below.</span></span>



| <span data-ttu-id="4893f-117">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="4893f-117">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="4893f-118">Описание</span><span class="sxs-lookup"><span data-stu-id="4893f-118">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="4893f-119"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="4893f-119"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="4893f-120">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="4893f-120">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4893f-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4893f-121">Remarks</span></span>

<span data-ttu-id="4893f-122">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="4893f-122">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="4893f-123">MOF-файлы не устанавливаются в составе Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="4893f-123">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="4893f-124">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="4893f-124">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="4893f-125">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="4893f-125">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4893f-126">Требования</span><span class="sxs-lookup"><span data-stu-id="4893f-126">Requirements</span></span>



| <span data-ttu-id="4893f-127">Требование</span><span class="sxs-lookup"><span data-stu-id="4893f-127">Requirement</span></span> | <span data-ttu-id="4893f-128">Значение</span><span class="sxs-lookup"><span data-stu-id="4893f-128">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="4893f-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4893f-129">Minimum supported client</span></span><br/> | <span data-ttu-id="4893f-130">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4893f-130">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="4893f-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4893f-131">Minimum supported server</span></span><br/> | <span data-ttu-id="4893f-132">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4893f-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="4893f-133">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4893f-133">Namespace</span></span><br/>                | <span data-ttu-id="4893f-134">Корневой \\ CIMV2 \\ безопасности \\ микрософттпм</span><span class="sxs-lookup"><span data-stu-id="4893f-134">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="4893f-135">MOF</span><span class="sxs-lookup"><span data-stu-id="4893f-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4893f-136"><dt>Win32 \_ TPM. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4893f-136"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="4893f-137">DLL</span><span class="sxs-lookup"><span data-stu-id="4893f-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4893f-138"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="4893f-138"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4893f-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4893f-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4893f-140">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="4893f-140">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
