---
description: Создает том BitLocker с указанным типом файловой системы тома обнаружения.
ms.assetid: 088e7224-a336-4742-a12f-86755defe16c
title: Метод Препареволуме класса Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.PrepareVolume
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 918e4289f8f2c38af2a4a51bfe92f82a74b30b22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144401"
---
# <a name="preparevolume-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="43277-103">Метод Препареволуме \_ класса Win32 енкриптаблеволуме</span><span class="sxs-lookup"><span data-stu-id="43277-103">PrepareVolume method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="43277-104">Метод **препареволуме** класса [**Win32 \_ енкриптаблеволуме**](win32-encryptablevolume.md) создает том BitLocker с указанным типом файловой системы тома обнаружения.</span><span class="sxs-lookup"><span data-stu-id="43277-104">The **PrepareVolume** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class creates a BitLocker volume with the specified file system type of the discovery volume.</span></span> <span data-ttu-id="43277-105">Этот метод должен вызываться до того, как том можно будет защитить с помощью любого из методов \**протекткэйвис \** _.</span><span class="sxs-lookup"><span data-stu-id="43277-105">This method must be called before the volume can be protected with any of the \**ProtectKeyWith\** _ methods.</span></span>

## <a name="syntax"></a><span data-ttu-id="43277-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="43277-106">Syntax</span></span>

```mof
uint32 PrepareVolume(
  [in] string DiscoveryVolumeType,
  [in] uint32 ForceEncryptionType
);
```

## <a name="parameters"></a><span data-ttu-id="43277-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="43277-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43277-108">_DiscoveryVolumeType \* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="43277-108">_DiscoveryVolumeType\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43277-109">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="43277-109">Type: **string**</span></span>

<span data-ttu-id="43277-110">Строка, указывающая тип тома обнаружения.</span><span class="sxs-lookup"><span data-stu-id="43277-110">A string that specifies the type of discovery volume.</span></span>

| <span data-ttu-id="43277-111">Значение</span><span class="sxs-lookup"><span data-stu-id="43277-111">Value</span></span>               | <span data-ttu-id="43277-112">Значение</span><span class="sxs-lookup"><span data-stu-id="43277-112">Meaning</span></span>                                                            |
|---------------------|--------------------------------------------------------------------|
| <span data-ttu-id="43277-113">**&lt;None&gt;**</span><span class="sxs-lookup"><span data-stu-id="43277-113">**&lt;none&gt;**</span></span>    | <span data-ttu-id="43277-114">Нет тома обнаружения.</span><span class="sxs-lookup"><span data-stu-id="43277-114">No discovery volume.</span></span> <span data-ttu-id="43277-115">Это значение создает собственный том BitLocker.</span><span class="sxs-lookup"><span data-stu-id="43277-115">This value creates a native BitLocker volume.</span></span> |
| <span data-ttu-id="43277-116">**&lt;параметры&gt;**</span><span class="sxs-lookup"><span data-stu-id="43277-116">**&lt;default&gt;**</span></span> | <span data-ttu-id="43277-117">Это значение является поведением по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="43277-117">This value is the default behavior.</span></span>                                |
| <span data-ttu-id="43277-118">**FAT32**</span><span class="sxs-lookup"><span data-stu-id="43277-118">**FAT32**</span></span>           | <span data-ttu-id="43277-119">Это значение создает том обнаружения FAT32.</span><span class="sxs-lookup"><span data-stu-id="43277-119">This value creates a FAT32 discovery volume.</span></span>                       |

</dd> <dt>

<span data-ttu-id="43277-120">*Форцеенкриптионтипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="43277-120">*ForceEncryptionType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43277-121">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="43277-121">Type: **uint32**</span></span>

<span data-ttu-id="43277-122">Целое число, указывающее тип шифрования.</span><span class="sxs-lookup"><span data-stu-id="43277-122">Integer that specifies the encryption type.</span></span> <span data-ttu-id="43277-123">Это может быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="43277-123">This can be one of the following values.</span></span>

| <span data-ttu-id="43277-124">Значение</span><span class="sxs-lookup"><span data-stu-id="43277-124">Value</span></span>                                                                                                                                                                                                                                       | <span data-ttu-id="43277-125">Значение</span><span class="sxs-lookup"><span data-stu-id="43277-125">Meaning</span></span>                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span><dl> <span data-ttu-id="43277-126">Не <dt>**указано**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="43277-126"><dt>**Unspecified**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="43277-127">Тип шифрования не указан.</span><span class="sxs-lookup"><span data-stu-id="43277-127">The encryption type is not specified.</span></span><br/> |
| <span id="Software"></span><span id="software"></span><span id="SOFTWARE"></span><dl> <span data-ttu-id="43277-128"><dt>**Программное обеспечение**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="43277-128"><dt>**Software**</dt> <dt>1</dt></span></span> </dl>             | <span data-ttu-id="43277-129">Шифрование программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="43277-129">Software encryption.</span></span><br/>                  |
| <span id="Hardware"></span><span id="hardware"></span><span id="HARDWARE"></span><dl> <span data-ttu-id="43277-130"><dt>**Оборудование**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="43277-130"><dt>**Hardware**</dt> <dt>2</dt></span></span> </dl>             | <span data-ttu-id="43277-131">Шифрование оборудования.</span><span class="sxs-lookup"><span data-stu-id="43277-131">Hardware encryption.</span></span><br/>                  |

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43277-132">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="43277-132">Return value</span></span>

<span data-ttu-id="43277-133">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="43277-133">Type: **uint32**</span></span>

<span data-ttu-id="43277-134">При сбое этот метод возвращает один из следующих кодов или другой код ошибки.</span><span class="sxs-lookup"><span data-stu-id="43277-134">This method returns one of the following codes or another error code if it fails.</span></span>

| <span data-ttu-id="43277-135">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="43277-135">Return code/value</span></span>      | <span data-ttu-id="43277-136">Описание</span><span class="sxs-lookup"><span data-stu-id="43277-136">Description</span></span>                     |
|------------------------|---------------------------------|
| <span data-ttu-id="43277-137">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="43277-137">**S_OK**</span></span> <br/> <span data-ttu-id="43277-138">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="43277-138">0 (0x0)</span></span> | <span data-ttu-id="43277-139">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="43277-139">The method was successful.</span></span><br/> |

## <a name="remarks"></a><span data-ttu-id="43277-140">Комментарии</span><span class="sxs-lookup"><span data-stu-id="43277-140">Remarks</span></span>

<span data-ttu-id="43277-141">Если вы не вызываете этот метод при включении тома BitLocker, он аналогичен вызову этого метода со значением по умолчанию в параметре *дисковериволуметипе* .</span><span class="sxs-lookup"><span data-stu-id="43277-141">If you do not call this method when enabling a BitLocker volume, it is the same as calling this method with the default value in the *DiscoveryVolumeType* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="43277-142">Требования</span><span class="sxs-lookup"><span data-stu-id="43277-142">Requirements</span></span>

| <span data-ttu-id="43277-143">Требование</span><span class="sxs-lookup"><span data-stu-id="43277-143">Requirement</span></span> | <span data-ttu-id="43277-144">Значение</span><span class="sxs-lookup"><span data-stu-id="43277-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43277-145">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="43277-145">Minimum supported client</span></span><br/> | <span data-ttu-id="43277-146">Windows 7 Корпоративная, \[ только классические приложения Windows 7 Ultimate\]</span><span class="sxs-lookup"><span data-stu-id="43277-146">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="43277-147">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="43277-147">Minimum supported server</span></span><br/> | <span data-ttu-id="43277-148">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="43277-148">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="43277-149">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="43277-149">Namespace</span></span><br/>                | <span data-ttu-id="43277-150">Корневой \\ CIMV2 \\ безопасности \\ микрософтволуминкриптион</span><span class="sxs-lookup"><span data-stu-id="43277-150">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="43277-151">MOF</span><span class="sxs-lookup"><span data-stu-id="43277-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="43277-152"><dt>Win32 \_ енкриптаблеволуме. mof</dt></span><span class="sxs-lookup"><span data-stu-id="43277-152"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="43277-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="43277-153">See also</span></span>

[<span data-ttu-id="43277-154">**\_Енкриптаблеволуме Win32**</span><span class="sxs-lookup"><span data-stu-id="43277-154">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
