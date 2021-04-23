---
description: Метод, принадлежащий \_ классу TPM Win32, указывает, имеет ли устройство владелец. Это значение изменяется методом Такеовнершип.
ms.assetid: 04a9394f-98de-43e3-8a19-7a8f409823b8
title: Метод, принадлежащий классу Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsOwned
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 6ad2d7d03059d8f96fe726d50ea18c2a70db64f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540927"
---
# <a name="isowned-method-of-the-win32_tpm-class"></a><span data-ttu-id="43f87-104">Метод владеет \_ классом TPM Win32</span><span class="sxs-lookup"><span data-stu-id="43f87-104">IsOwned method of the Win32\_Tpm class</span></span>

<span data-ttu-id="43f87-105">Метод, **принадлежащий** классу [**\_ TPM Win32**](win32-tpm.md) , указывает, имеет ли устройство владелец.</span><span class="sxs-lookup"><span data-stu-id="43f87-105">The **IsOwned** method of the [**Win32\_Tpm**](win32-tpm.md) class indicates whether the device has an owner.</span></span> <span data-ttu-id="43f87-106">Это значение изменяется методом [**такеовнершип**](takeownership-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="43f87-106">This value is changed by the [**TakeOwnership**](takeownership-win32-tpm.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="43f87-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="43f87-107">Syntax</span></span>


```mof
uint32 IsOwned(
  [out] boolean IsOwned
);
```



## <a name="parameters"></a><span data-ttu-id="43f87-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="43f87-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43f87-109">*Владелец* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="43f87-109">*IsOwned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="43f87-110">Тип: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="43f87-110">Type: **boolean**</span></span>

<span data-ttu-id="43f87-111">Если **значение — true**, устройство имеет владельца.</span><span class="sxs-lookup"><span data-stu-id="43f87-111">If **true**, the device has an owner.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43f87-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="43f87-112">Return value</span></span>

<span data-ttu-id="43f87-113">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="43f87-113">Type: **uint32**</span></span>

<span data-ttu-id="43f87-114">Могут возвращаться все ошибки доверенного платформенного модуля, а также ошибки, относящиеся к базовым службам TPM.</span><span class="sxs-lookup"><span data-stu-id="43f87-114">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="43f87-115">Ниже приведены общие коды возврата.</span><span class="sxs-lookup"><span data-stu-id="43f87-115">Common return codes are listed below.</span></span>



| <span data-ttu-id="43f87-116">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="43f87-116">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="43f87-117">Описание</span><span class="sxs-lookup"><span data-stu-id="43f87-117">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="43f87-118"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="43f87-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="43f87-119">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="43f87-119">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="43f87-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="43f87-120">Remarks</span></span>

<span data-ttu-id="43f87-121">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="43f87-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="43f87-122">MOF-файлы не устанавливаются в составе Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="43f87-122">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="43f87-123">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="43f87-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="43f87-124">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="43f87-124">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="43f87-125">Требования</span><span class="sxs-lookup"><span data-stu-id="43f87-125">Requirements</span></span>



| <span data-ttu-id="43f87-126">Требование</span><span class="sxs-lookup"><span data-stu-id="43f87-126">Requirement</span></span> | <span data-ttu-id="43f87-127">Значение</span><span class="sxs-lookup"><span data-stu-id="43f87-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="43f87-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="43f87-128">Minimum supported client</span></span><br/> | <span data-ttu-id="43f87-129">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="43f87-129">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="43f87-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="43f87-130">Minimum supported server</span></span><br/> | <span data-ttu-id="43f87-131">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="43f87-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="43f87-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="43f87-132">Namespace</span></span><br/>                | <span data-ttu-id="43f87-133">Корневой \\ CIMV2 \\ безопасности \\ микрософттпм</span><span class="sxs-lookup"><span data-stu-id="43f87-133">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="43f87-134">MOF</span><span class="sxs-lookup"><span data-stu-id="43f87-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="43f87-135"><dt>Win32 \_ TPM. mof</dt></span><span class="sxs-lookup"><span data-stu-id="43f87-135"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="43f87-136">DLL</span><span class="sxs-lookup"><span data-stu-id="43f87-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="43f87-137"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="43f87-137"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43f87-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="43f87-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43f87-139">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="43f87-139">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
