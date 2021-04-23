---
description: Метод Исфисикалклеардисаблед \_ класса TPM Win32 указывает, может ли только владелец устройства очистить устройство.
ms.assetid: b87f1c4f-8735-45c5-9256-53dbb9579f95
title: Метод Исфисикалклеардисаблед класса Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsPhysicalClearDisabled
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 9179aae2f4902ce29e2bab98b4c9c0b793804de6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683923"
---
# <a name="isphysicalcleardisabled-method-of-the-win32_tpm-class"></a><span data-ttu-id="37226-103">Метод Исфисикалклеардисаблед \_ класса TPM Win32</span><span class="sxs-lookup"><span data-stu-id="37226-103">IsPhysicalClearDisabled method of the Win32\_Tpm class</span></span>

<span data-ttu-id="37226-104">Метод **исфисикалклеардисаблед** класса [**\_ TPM Win32**](win32-tpm.md) указывает, может ли только владелец устройства очистить устройство.</span><span class="sxs-lookup"><span data-stu-id="37226-104">The **IsPhysicalClearDisabled** method of the [**Win32\_Tpm**](win32-tpm.md) class indicates whether only the device owner may be able to clear the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="37226-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="37226-105">Syntax</span></span>


```mof
uint32 IsPhysicalClearDisabled(
  [out] boolean IsPhysicalClearDisabled
);
```



## <a name="parameters"></a><span data-ttu-id="37226-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="37226-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37226-107">*Исфисикалклеардисаблед* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="37226-107">*IsPhysicalClearDisabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="37226-108">Тип: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="37226-108">Type: **boolean**</span></span>

<span data-ttu-id="37226-109">Если **значение — true**, устройство может быть очищено только владельцем устройства.</span><span class="sxs-lookup"><span data-stu-id="37226-109">If **true**, only the device owner is able to clear the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37226-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="37226-110">Return value</span></span>

<span data-ttu-id="37226-111">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="37226-111">Type: **uint32**</span></span>

<span data-ttu-id="37226-112">Могут возвращаться все ошибки доверенного платформенного модуля, а также ошибки, относящиеся к базовым службам TPM.</span><span class="sxs-lookup"><span data-stu-id="37226-112">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="37226-113">Ниже приведены общие коды возврата.</span><span class="sxs-lookup"><span data-stu-id="37226-113">Common return codes are listed below.</span></span>



| <span data-ttu-id="37226-114">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="37226-114">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="37226-115">Описание</span><span class="sxs-lookup"><span data-stu-id="37226-115">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="37226-116"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="37226-116"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="37226-117">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="37226-117">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="37226-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="37226-118">Remarks</span></span>

<span data-ttu-id="37226-119">В начале каждого цикла запуска это значение сбрасывается в значение **false** .</span><span class="sxs-lookup"><span data-stu-id="37226-119">This value is reset to **false** at the beginning of each startup cycle.</span></span>

<span data-ttu-id="37226-120">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="37226-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="37226-121">MOF-файлы не устанавливаются в составе Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="37226-121">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="37226-122">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="37226-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="37226-123">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="37226-123">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="37226-124">Требования</span><span class="sxs-lookup"><span data-stu-id="37226-124">Requirements</span></span>



| <span data-ttu-id="37226-125">Требование</span><span class="sxs-lookup"><span data-stu-id="37226-125">Requirement</span></span> | <span data-ttu-id="37226-126">Значение</span><span class="sxs-lookup"><span data-stu-id="37226-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="37226-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="37226-127">Minimum supported client</span></span><br/> | <span data-ttu-id="37226-128">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="37226-128">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="37226-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="37226-129">Minimum supported server</span></span><br/> | <span data-ttu-id="37226-130">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="37226-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="37226-131">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="37226-131">Namespace</span></span><br/>                | <span data-ttu-id="37226-132">Корневой \\ CIMV2 \\ безопасности \\ микрософттпм</span><span class="sxs-lookup"><span data-stu-id="37226-132">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="37226-133">MOF</span><span class="sxs-lookup"><span data-stu-id="37226-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="37226-134"><dt>Win32 \_ TPM. mof</dt></span><span class="sxs-lookup"><span data-stu-id="37226-134"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="37226-135">DLL</span><span class="sxs-lookup"><span data-stu-id="37226-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="37226-136"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="37226-136"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37226-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="37226-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37226-138">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="37226-138">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
