---
description: Указывает, готов ли доверенный платформенный модуль к использованию.
ms.assetid: 70E9EB90-DC13-4431-97E5-D77B4E345373
title: 'Метод Win32_Tpm:: методом Read'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsReady
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 37c9d579e424c89f8670838b09ed1c557514ca00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540911"
---
# <a name="win32_tpmisready-method"></a><span data-ttu-id="a5c71-103">\_Метод Win32 TPM:: методом Read</span><span class="sxs-lookup"><span data-stu-id="a5c71-103">Win32\_Tpm::IsReady method</span></span>

<span data-ttu-id="a5c71-104">Указывает, готов ли доверенный платформенный модуль к использованию.</span><span class="sxs-lookup"><span data-stu-id="a5c71-104">Indicates whether the TPM is ready for use.</span></span>

<span data-ttu-id="a5c71-105">Этот метод доступен только локальным администраторам.</span><span class="sxs-lookup"><span data-stu-id="a5c71-105">This method is only accessible by local administrators.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5c71-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a5c71-106">Syntax</span></span>


```C++
uint32 IsReady(
  [out] BOOL IsReady
);
```



## <a name="parameters"></a><span data-ttu-id="a5c71-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="a5c71-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5c71-108">*Чтение* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a5c71-108">*IsReady* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a5c71-109">Задайте значение **true** , если TPM и система полностью подготовлены для использования доверенным платформенным модулем.</span><span class="sxs-lookup"><span data-stu-id="a5c71-109">Set to **TRUE** if the TPM and system are fully provisioned for TPM use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5c71-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a5c71-110">Return value</span></span>

<span data-ttu-id="a5c71-111">Могут возвращаться все ошибки доверенного платформенного модуля, а также ошибки, относящиеся к [базовым службам TPM](../tbs/tbs-return-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="a5c71-111">All TPM errors as well as errors specific to [TPM Base Services](../tbs/tbs-return-codes.md) can be returned.</span></span>

<span data-ttu-id="a5c71-112">Ниже приведены общие коды возврата.</span><span class="sxs-lookup"><span data-stu-id="a5c71-112">Common return codes are listed below.</span></span>



| <span data-ttu-id="a5c71-113">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="a5c71-113">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="a5c71-114">Описание</span><span class="sxs-lookup"><span data-stu-id="a5c71-114">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="a5c71-115"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="a5c71-115"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="a5c71-116">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="a5c71-116">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a5c71-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a5c71-117">Remarks</span></span>

<span data-ttu-id="a5c71-118">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="a5c71-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="a5c71-119">MOF-файлы не устанавливаются в составе Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="a5c71-119">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="a5c71-120">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="a5c71-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="a5c71-121">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="a5c71-121">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a5c71-122">Требования</span><span class="sxs-lookup"><span data-stu-id="a5c71-122">Requirements</span></span>



| <span data-ttu-id="a5c71-123">Требование</span><span class="sxs-lookup"><span data-stu-id="a5c71-123">Requirement</span></span> | <span data-ttu-id="a5c71-124">Значение</span><span class="sxs-lookup"><span data-stu-id="a5c71-124">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5c71-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a5c71-125">Minimum supported client</span></span><br/> | <span data-ttu-id="a5c71-126">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="a5c71-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a5c71-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a5c71-127">Minimum supported server</span></span><br/> | <span data-ttu-id="a5c71-128">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="a5c71-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="a5c71-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a5c71-129">Namespace</span></span><br/>                | <span data-ttu-id="a5c71-130">\\\\.\\ корневой \\ CIMV2 \\ безопасности \\ микрософттпм</span><span class="sxs-lookup"><span data-stu-id="a5c71-130">\\\\.\\root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                     |
| <span data-ttu-id="a5c71-131">MOF</span><span class="sxs-lookup"><span data-stu-id="a5c71-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a5c71-132"><dt>Win32 \_ TPM. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a5c71-132"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="a5c71-133">DLL</span><span class="sxs-lookup"><span data-stu-id="a5c71-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a5c71-134"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="a5c71-134"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5c71-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a5c71-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5c71-136">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="a5c71-136">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
