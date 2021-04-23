---
description: Метод Иссркаускомпатибле \_ класса TPM Win32 указывает, совместима ли авторизация корневого ключа хранилища (SRK) со значением, ожидаемым Windows Vista.
ms.assetid: ce6d05b8-673a-40ab-a1d7-3fedfd099306
title: Метод Иссркаускомпатибле класса Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsSrkAuthCompatible
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: f5250f8d3f9ad38f9d4c46350e06e0fe32f756dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911575"
---
# <a name="issrkauthcompatible-method-of-the-win32_tpm-class"></a><span data-ttu-id="ea3fd-103">Метод Иссркаускомпатибле \_ класса TPM Win32</span><span class="sxs-lookup"><span data-stu-id="ea3fd-103">IsSrkAuthCompatible method of the Win32\_Tpm class</span></span>

<span data-ttu-id="ea3fd-104">Метод **иссркаускомпатибле** класса [**\_ TPM Win32**](win32-tpm.md) указывает, совместима ли авторизация корневого ключа хранилища (SRK) со значением, ожидаемым Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ea3fd-104">The **IsSrkAuthCompatible** method of the [**Win32\_Tpm**](win32-tpm.md) class indicates whether the Storage Root Key (SRK) authorization is compatible with the value expected by Windows Vista.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea3fd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ea3fd-105">Syntax</span></span>


```mof
uint32 IsSrkAuthCompatible(
  [out] boolean IsSrkAuthCompatible
);
```



## <a name="parameters"></a><span data-ttu-id="ea3fd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ea3fd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea3fd-107">*Иссркаускомпатибле* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ea3fd-107">*IsSrkAuthCompatible* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ea3fd-108">Тип: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="ea3fd-108">Type: **boolean**</span></span>

<span data-ttu-id="ea3fd-109">При значении **true** значение авторизации SRK имеет нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="ea3fd-109">If **true**, the SRK authorization value has a value of zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea3fd-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ea3fd-110">Return value</span></span>

<span data-ttu-id="ea3fd-111">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ea3fd-111">Type: **uint32**</span></span>

<span data-ttu-id="ea3fd-112">Могут возвращаться все ошибки доверенного платформенного модуля, а также ошибки, относящиеся к базовым службам TPM.</span><span class="sxs-lookup"><span data-stu-id="ea3fd-112">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="ea3fd-113">Ниже приведены общие коды возврата.</span><span class="sxs-lookup"><span data-stu-id="ea3fd-113">Common return codes are listed below.</span></span>



| <span data-ttu-id="ea3fd-114">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="ea3fd-114">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="ea3fd-115">Описание</span><span class="sxs-lookup"><span data-stu-id="ea3fd-115">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="ea3fd-116"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="ea3fd-116"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="ea3fd-117">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="ea3fd-117">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ea3fd-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ea3fd-118">Remarks</span></span>

<span data-ttu-id="ea3fd-119">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="ea3fd-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="ea3fd-120">MOF-файлы не устанавливаются в составе Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="ea3fd-120">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="ea3fd-121">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="ea3fd-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="ea3fd-122">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="ea3fd-122">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ea3fd-123">Требования</span><span class="sxs-lookup"><span data-stu-id="ea3fd-123">Requirements</span></span>



| <span data-ttu-id="ea3fd-124">Требование</span><span class="sxs-lookup"><span data-stu-id="ea3fd-124">Requirement</span></span> | <span data-ttu-id="ea3fd-125">Значение</span><span class="sxs-lookup"><span data-stu-id="ea3fd-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea3fd-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ea3fd-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ea3fd-127">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ea3fd-127">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="ea3fd-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ea3fd-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ea3fd-129">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ea3fd-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="ea3fd-130">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ea3fd-130">Namespace</span></span><br/>                | <span data-ttu-id="ea3fd-131">Корневой \\ CIMV2 \\ безопасности \\ микрософттпм</span><span class="sxs-lookup"><span data-stu-id="ea3fd-131">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="ea3fd-132">MOF</span><span class="sxs-lookup"><span data-stu-id="ea3fd-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ea3fd-133"><dt>Win32 \_ TPM. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ea3fd-133"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="ea3fd-134">DLL</span><span class="sxs-lookup"><span data-stu-id="ea3fd-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ea3fd-135"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="ea3fd-135"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea3fd-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ea3fd-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea3fd-137">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="ea3fd-137">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
