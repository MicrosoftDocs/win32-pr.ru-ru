---
description: Метод Исендорсементкэйпаирпресент \_ класса TPM Win32 указывает, существует ли на устройстве пара ключей подтверждения.
ms.assetid: c36cd0b5-1ac2-4fcf-b140-c5ecb0b3b211
title: Метод Исендорсементкэйпаирпресент класса Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsEndorsementKeyPairPresent
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 63561a4971523fd1554e1d973861c3f0737df2ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156834"
---
# <a name="isendorsementkeypairpresent-method-of-the-win32_tpm-class"></a><span data-ttu-id="961fe-103">Метод Исендорсементкэйпаирпресент \_ класса TPM Win32</span><span class="sxs-lookup"><span data-stu-id="961fe-103">IsEndorsementKeyPairPresent method of the Win32\_Tpm class</span></span>

<span data-ttu-id="961fe-104">Метод **исендорсементкэйпаирпресент** класса [**\_ TPM Win32**](win32-tpm.md) указывает, существует ли на устройстве пара ключей подтверждения.</span><span class="sxs-lookup"><span data-stu-id="961fe-104">The **IsEndorsementKeyPairPresent** method of the [**Win32\_Tpm**](win32-tpm.md) class indicates whether the endorsement key pair exists on the device.</span></span> <span data-ttu-id="961fe-105">Перед владельцем устройства требуется пара ключей подтверждения.</span><span class="sxs-lookup"><span data-stu-id="961fe-105">The endorsement key pair is required before the device can be owned.</span></span> <span data-ttu-id="961fe-106">Эта пара ключей может быть создана методом [**креатиндорсементкэйпаир**](createendorsementkeypair-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="961fe-106">This key pair can be created by the [**CreateEndorsementKeyPair**](createendorsementkeypair-win32-tpm.md) method.</span></span>

<span data-ttu-id="961fe-107">Чтобы этот метод был выполнен, устройство должно быть включено и активировано.</span><span class="sxs-lookup"><span data-stu-id="961fe-107">The device must be enabled and activated for this method to succeed.</span></span> <span data-ttu-id="961fe-108">Сведения о включении и активации непринадлежитного устройства см. в описании метода [**сетфисикалпресенцерекуест**](setphysicalpresencerequest-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="961fe-108">To enable and activate an unowned device, see the [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="961fe-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="961fe-109">Syntax</span></span>


```mof
uint32 IsEndorsementKeyPairPresent(
  [out] boolean IsEndorsementKeyPairPresent
);
```



## <a name="parameters"></a><span data-ttu-id="961fe-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="961fe-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="961fe-111">*Исендорсементкэйпаирпресент* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="961fe-111">*IsEndorsementKeyPairPresent* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="961fe-112">Тип: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="961fe-112">Type: **boolean**</span></span>

<span data-ttu-id="961fe-113">Если **значение — true**, пара ключей подтверждения существует на устройстве.</span><span class="sxs-lookup"><span data-stu-id="961fe-113">If **true**, the endorsement key pair exists on the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="961fe-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="961fe-114">Return value</span></span>

<span data-ttu-id="961fe-115">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="961fe-115">Type: **uint32**</span></span>

<span data-ttu-id="961fe-116">Могут возвращаться все ошибки доверенного платформенного модуля, а также ошибки, относящиеся к базовым службам TPM.</span><span class="sxs-lookup"><span data-stu-id="961fe-116">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="961fe-117">Ниже приведены общие коды возврата.</span><span class="sxs-lookup"><span data-stu-id="961fe-117">Common return codes are listed below.</span></span>



| <span data-ttu-id="961fe-118">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="961fe-118">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="961fe-119">Описание</span><span class="sxs-lookup"><span data-stu-id="961fe-119">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="961fe-120"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="961fe-120"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="961fe-121">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="961fe-121">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="961fe-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="961fe-122">Remarks</span></span>

<span data-ttu-id="961fe-123">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="961fe-123">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="961fe-124">MOF-файлы не устанавливаются в составе Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="961fe-124">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="961fe-125">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="961fe-125">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="961fe-126">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="961fe-126">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="961fe-127">Требования</span><span class="sxs-lookup"><span data-stu-id="961fe-127">Requirements</span></span>



| <span data-ttu-id="961fe-128">Требование</span><span class="sxs-lookup"><span data-stu-id="961fe-128">Requirement</span></span> | <span data-ttu-id="961fe-129">Значение</span><span class="sxs-lookup"><span data-stu-id="961fe-129">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="961fe-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="961fe-130">Minimum supported client</span></span><br/> | <span data-ttu-id="961fe-131">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="961fe-131">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="961fe-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="961fe-132">Minimum supported server</span></span><br/> | <span data-ttu-id="961fe-133">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="961fe-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="961fe-134">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="961fe-134">Namespace</span></span><br/>                | <span data-ttu-id="961fe-135">Корневой \\ CIMV2 \\ безопасности \\ микрософттпм</span><span class="sxs-lookup"><span data-stu-id="961fe-135">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="961fe-136">MOF</span><span class="sxs-lookup"><span data-stu-id="961fe-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="961fe-137"><dt>Win32 \_ TPM. mof</dt></span><span class="sxs-lookup"><span data-stu-id="961fe-137"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="961fe-138">DLL</span><span class="sxs-lookup"><span data-stu-id="961fe-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="961fe-139"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="961fe-139"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="961fe-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="961fe-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="961fe-141">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="961fe-141">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="961fe-142">**креатиндорсементкэйпаир**</span><span class="sxs-lookup"><span data-stu-id="961fe-142">**CreateEndorsementKeyPair**</span></span>](createendorsementkeypair-win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="961fe-143">**сетфисикалпресенцерекуест**</span><span class="sxs-lookup"><span data-stu-id="961fe-143">**SetPhysicalPresenceRequest**</span></span>](setphysicalpresencerequest-win32-tpm.md)
</dt> </dl>

 

 
