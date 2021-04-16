---
description: Метод Исфисикалпресенцехардваринаблед \_ класса TPM Win32 указывает, можно ли установить физическое присутствие на платформе с аппаратным сигналом.
ms.assetid: 65dabfa9-bfbe-4b9b-8e80-02269895c7ad
title: Метод Исфисикалпресенцехардваринаблед класса Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsPhysicalPresenceHardwareEnabled
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 674dcaa733d8ec70af172359e3dcde0578955dfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423761"
---
# <a name="isphysicalpresencehardwareenabled-method-of-the-win32_tpm-class"></a><span data-ttu-id="d6638-103">Метод Исфисикалпресенцехардваринаблед \_ класса TPM Win32</span><span class="sxs-lookup"><span data-stu-id="d6638-103">IsPhysicalPresenceHardwareEnabled method of the Win32\_Tpm class</span></span>

<span data-ttu-id="d6638-104">Метод **исфисикалпресенцехардваринаблед** класса [**\_ TPM Win32**](win32-tpm.md) указывает, можно ли установить физическое присутствие на платформе с аппаратным сигналом.</span><span class="sxs-lookup"><span data-stu-id="d6638-104">The **IsPhysicalPresenceHardwareEnabled** method of the [**Win32\_Tpm**](win32-tpm.md) class indicates whether physical presence on the platform can be set with a hardware signal.</span></span> <span data-ttu-id="d6638-105">Это значение настраивается производителем платформы в зависимости от структуры платформы.</span><span class="sxs-lookup"><span data-stu-id="d6638-105">This value is configured by the platform manufacturer based on the design of the platform.</span></span> <span data-ttu-id="d6638-106">Документация производителя платформы может предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="d6638-106">Documentation from the platform manufacturer may provide additional information.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6638-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d6638-107">Syntax</span></span>


```mof
uint32 IsPhysicalPresenceHardwareEnabled(
  [out] boolean IsPhysicalPresenceHardwareEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="d6638-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d6638-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6638-109">*Исфисикалпресенцехардваринаблед* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d6638-109">*IsPhysicalPresenceHardwareEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d6638-110">Тип: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="d6638-110">Type: **boolean**</span></span>

<span data-ttu-id="d6638-111">Если **значение равно true**, физическому присутствию на платформе можно назначить аппаратный сигнал.</span><span class="sxs-lookup"><span data-stu-id="d6638-111">If **true**, physical presence on the platform can be set with a hardware signal.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6638-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d6638-112">Return value</span></span>

<span data-ttu-id="d6638-113">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d6638-113">Type: **uint32**</span></span>

<span data-ttu-id="d6638-114">Могут возвращаться все ошибки доверенного платформенного модуля, а также ошибки, относящиеся к базовым службам TPM.</span><span class="sxs-lookup"><span data-stu-id="d6638-114">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="d6638-115">Ниже приведены общие коды возврата.</span><span class="sxs-lookup"><span data-stu-id="d6638-115">Common return codes are listed below.</span></span>



| <span data-ttu-id="d6638-116">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="d6638-116">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="d6638-117">Описание</span><span class="sxs-lookup"><span data-stu-id="d6638-117">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="d6638-118"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="d6638-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="d6638-119">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="d6638-119">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d6638-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d6638-120">Remarks</span></span>

<span data-ttu-id="d6638-121">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="d6638-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="d6638-122">MOF-файлы не устанавливаются в составе Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="d6638-122">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="d6638-123">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="d6638-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="d6638-124">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="d6638-124">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d6638-125">Требования</span><span class="sxs-lookup"><span data-stu-id="d6638-125">Requirements</span></span>



| <span data-ttu-id="d6638-126">Требование</span><span class="sxs-lookup"><span data-stu-id="d6638-126">Requirement</span></span> | <span data-ttu-id="d6638-127">Значение</span><span class="sxs-lookup"><span data-stu-id="d6638-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6638-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d6638-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d6638-129">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d6638-129">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="d6638-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d6638-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d6638-131">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d6638-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="d6638-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d6638-132">Namespace</span></span><br/>                | <span data-ttu-id="d6638-133">Корневой \\ CIMV2 \\ безопасности \\ микрософттпм</span><span class="sxs-lookup"><span data-stu-id="d6638-133">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="d6638-134">MOF</span><span class="sxs-lookup"><span data-stu-id="d6638-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d6638-135"><dt>Win32 \_ TPM. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d6638-135"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="d6638-136">DLL</span><span class="sxs-lookup"><span data-stu-id="d6638-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d6638-137"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="d6638-137"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6638-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d6638-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6638-139">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="d6638-139">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
