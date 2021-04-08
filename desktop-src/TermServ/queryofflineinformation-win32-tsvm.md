---
title: Метод Куерйоффлинеинформатион класса Win32_TSVm
description: Извлекает свойства текущего сервера виртуальных рабочих столов (VDS), но только в том случае, если сервер находится в автономном режиме.
ms.assetid: f6ce74cb-a4a4-4e05-a0a7-bac0b7f52c45
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Куерйоффлинеинформатион
- Службы удаленных рабочих столов метода Куерйоффлинеинформатион, класс Win32_TSVm
- Класс Win32_TSVm службы удаленных рабочих столов, метод Куерйоффлинеинформатион
topic_type:
- apiref
api_name:
- Win32_TSVm.QueryOfflineInformation
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4750ebdb82b08ae1ed0350e1ac448d9aca4003b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892197"
---
# <a name="queryofflineinformation-method-of-the-win32_tsvm-class"></a><span data-ttu-id="bb557-106">Метод Куерйоффлинеинформатион \_ класса Win32 тсвм</span><span class="sxs-lookup"><span data-stu-id="bb557-106">QueryOfflineInformation method of the Win32\_TSVm class</span></span>

<span data-ttu-id="bb557-107">Извлекает свойства текущего сервера виртуальных рабочих столов (VDS), но только в том случае, если сервер находится в автономном режиме.</span><span class="sxs-lookup"><span data-stu-id="bb557-107">Retrieves the properties of the current virtual desktop server (VDS), but only when the server is offline.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb557-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bb557-108">Syntax</span></span>


```mof
uint32 QueryOfflineInformation(
  [out] string  Build,
  [out] string  CurrentVersion,
  [out] string  InstallationType,
  [out] string  EditionId,
  [out] string  SysPrepImageState,
  [out] string  SysPrepMode,
  [out] sint32  ProcArch,
  [out] boolean fIsVmbusCapable,
  [out] boolean fIsRdvIcInstalled
);
```



## <a name="parameters"></a><span data-ttu-id="bb557-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="bb557-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb557-110">*Сборка* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="bb557-110">*Build* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bb557-111">При успешном выполнении возвращает версию сборки VDS.</span><span class="sxs-lookup"><span data-stu-id="bb557-111">On a success, returns the build version of the VDS.</span></span>

</dd> <dt>

<span data-ttu-id="bb557-112">*CurrentVersion* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="bb557-112">*CurrentVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bb557-113">При успешном выполнении возвращает текущую версию VDS.</span><span class="sxs-lookup"><span data-stu-id="bb557-113">On a success, returns the current version of the VDS.</span></span>

</dd> <dt>

<span data-ttu-id="bb557-114">*Инсталлатионтипе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="bb557-114">*InstallationType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bb557-115">При успешном выполнении возвращает тип установки VDS.</span><span class="sxs-lookup"><span data-stu-id="bb557-115">On a success, returns the installation type of the VDS.</span></span>

</dd> <dt>

<span data-ttu-id="bb557-116">*EditionId* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="bb557-116">*EditionId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bb557-117">При успешном выполнении возвращает идентификатор выпуска VDS.</span><span class="sxs-lookup"><span data-stu-id="bb557-117">On a success, returns the edition ID of the VDS.</span></span>

</dd> <dt>

<span data-ttu-id="bb557-118">*Сиспрепимажестате* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="bb557-118">*SysPrepImageState* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bb557-119">При успешном выполнении возвращает состояние образа подготовки системы для службы VDS.</span><span class="sxs-lookup"><span data-stu-id="bb557-119">On success, returns the system prep image state of the VDS.</span></span>

</dd> <dt>

<span data-ttu-id="bb557-120">*Сиспрепмоде* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="bb557-120">*SysPrepMode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bb557-121">При успешном выполнении возвращает режим системной подготовки службы VDS.</span><span class="sxs-lookup"><span data-stu-id="bb557-121">On a success, returns the system prep mode of the VDS.</span></span>

</dd> <dt>

<span data-ttu-id="bb557-122">*Прокарч* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="bb557-122">*ProcArch* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bb557-123">При успешном выполнении возвращает значение, указывающее архитектуру процессора.</span><span class="sxs-lookup"><span data-stu-id="bb557-123">On a success, returns a value indicating the processor architecture.</span></span>

<dt>

<span data-ttu-id="bb557-124">0</span><span class="sxs-lookup"><span data-stu-id="bb557-124">0</span></span>
</dt> <dd>

<span data-ttu-id="bb557-125">x86</span><span class="sxs-lookup"><span data-stu-id="bb557-125">x86</span></span>

</dd> <dt>

<span data-ttu-id="bb557-126">1</span><span class="sxs-lookup"><span data-stu-id="bb557-126">1</span></span>
</dt> <dd>

<span data-ttu-id="bb557-127">amd64</span><span class="sxs-lookup"><span data-stu-id="bb557-127">amd64</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="bb557-128">*фисвмбускапабле* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="bb557-128">*fIsVmbusCapable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bb557-129">При успешном выполнении указывает, поддерживает ли система VMBus.</span><span class="sxs-lookup"><span data-stu-id="bb557-129">on a success, indicates whether the system is VMBus-capable.</span></span>

</dd> <dt>

<span data-ttu-id="bb557-130">*фисрдвиЦинсталлед* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="bb557-130">*fIsRdvIcInstalled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bb557-131">При успешном выполнении указывает, установлен ли РДВИК.</span><span class="sxs-lookup"><span data-stu-id="bb557-131">On a success, indicates if RDVIC is installed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb557-132">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bb557-132">Return value</span></span>

<span data-ttu-id="bb557-133">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="bb557-133">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="bb557-134">Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="bb557-134">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb557-135">Требования</span><span class="sxs-lookup"><span data-stu-id="bb557-135">Requirements</span></span>



| <span data-ttu-id="bb557-136">Требование</span><span class="sxs-lookup"><span data-stu-id="bb557-136">Requirement</span></span> | <span data-ttu-id="bb557-137">Значение</span><span class="sxs-lookup"><span data-stu-id="bb557-137">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb557-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bb557-138">Minimum supported client</span></span><br/> | <span data-ttu-id="bb557-139">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="bb557-139">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="bb557-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bb557-140">Minimum supported server</span></span><br/> | <span data-ttu-id="bb557-141">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bb557-141">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="bb557-142">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="bb557-142">Namespace</span></span><br/>                | <span data-ttu-id="bb557-143">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="bb557-143">Root\\CIMv2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="bb557-144">MOF</span><span class="sxs-lookup"><span data-stu-id="bb557-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bb557-145"><dt>Тсвмхост. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bb557-145"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="bb557-146">DLL</span><span class="sxs-lookup"><span data-stu-id="bb557-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bb557-147"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bb557-147"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb557-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bb557-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb557-149">**\_Тсвм Win32**</span><span class="sxs-lookup"><span data-stu-id="bb557-149">**Win32\_TSVm**</span></span>](win32-tsvm.md)
</dt> </dl>

 

 





