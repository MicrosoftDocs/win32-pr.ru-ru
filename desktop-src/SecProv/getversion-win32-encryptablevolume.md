---
description: Возвращает версию метаданных ФВЕ для тома.
ms.assetid: 21d5bf6d-c613-4200-b35c-1bad1ee72ec7
title: Метод method класса Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetVersion
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 25952c29b6db6db045fe839951d76994cc907b91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682550"
---
# <a name="getversion-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="aae44-103">Метод method \_ класса Win32 енкриптаблеволуме</span><span class="sxs-lookup"><span data-stu-id="aae44-103">GetVersion method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="aae44-104">Метод **WebMethod** класса [**Win32 \_ ЕНКРИПТАБЛЕВОЛУМЕ**](win32-encryptablevolume.md) Возвращает версию метаданных ФВЕ для тома.</span><span class="sxs-lookup"><span data-stu-id="aae44-104">The **GetVersion** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class returns the FVE metadata version of the volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="aae44-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="aae44-105">Syntax</span></span>


```mof
uint32 GetVersion(
  [out] uint32 Version
);
```



## <a name="parameters"></a><span data-ttu-id="aae44-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="aae44-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aae44-107">*Версия* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="aae44-107">*Version* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aae44-108">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aae44-108">Type: **uint32**</span></span>

<span data-ttu-id="aae44-109">Целое число без знака, указывающее версию метаданных тома.</span><span class="sxs-lookup"><span data-stu-id="aae44-109">An unsigned integer that indicates the metadata version of the volume.</span></span>



| <span data-ttu-id="aae44-110">Значение</span><span class="sxs-lookup"><span data-stu-id="aae44-110">Value</span></span>                                                                                                                                                                                                                       | <span data-ttu-id="aae44-111">Значение</span><span class="sxs-lookup"><span data-stu-id="aae44-111">Meaning</span></span>                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="aae44-112"><dt>**Неизвестно**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="aae44-112"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="aae44-113">Операционная система неизвестна.</span><span class="sxs-lookup"><span data-stu-id="aae44-113">The operating system is unknown.</span></span><br/>                                                                                                                                                                                               |
| <span id="Vista"></span><span id="vista"></span><span id="VISTA"></span><dl> <span data-ttu-id="aae44-114"><dt>**Vista**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="aae44-114"><dt>**Vista**</dt> <dt>1</dt></span></span> </dl>         | <span data-ttu-id="aae44-115">Формат Windows Vista, что означает, что том был защищен BitLocker на компьютере под управлением Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="aae44-115">Windows Vista format, meaning that the volume was protected with BitLocker on a computer running Windows Vista.</span></span><br/>                                                                                                                |
| <span id="Win7"></span><span id="win7"></span><span id="WIN7"></span><dl> <span data-ttu-id="aae44-116"><dt>**Win7**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="aae44-116"><dt>**Win7**</dt> <dt>2</dt></span></span> </dl>             | <span data-ttu-id="aae44-117">Формат Windows 7, что означает, что том был защищен с помощью BitLocker на компьютере под управлением Windows 7, или формат метаданных был обновлен с помощью метода [**упградеволуме**](upgradevolume-win32-encryptablevolume.md) .</span><span class="sxs-lookup"><span data-stu-id="aae44-117">Windows 7 format, meaning that the volume was protected with BitLocker on a computer running Windows 7 or the metadata format was upgraded by using the [**UpgradeVolume**](upgradevolume-win32-encryptablevolume.md) method.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aae44-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="aae44-118">Return value</span></span>

<span data-ttu-id="aae44-119">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aae44-119">Type: **uint32**</span></span>

<span data-ttu-id="aae44-120">При сбое этот метод возвращает один из следующих кодов или другой код ошибки.</span><span class="sxs-lookup"><span data-stu-id="aae44-120">This method returns one of the following codes or another error code if it fails.</span></span>

<span data-ttu-id="aae44-121">Если том уже разблокирован и другие ошибки не возникают, этот метод возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="aae44-121">If the volume is already unlocked and no other errors occur, this method returns zero.</span></span>



| <span data-ttu-id="aae44-122">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="aae44-122">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="aae44-123">Описание</span><span class="sxs-lookup"><span data-stu-id="aae44-123">Description</span></span>                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <span data-ttu-id="aae44-124"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="aae44-124"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                       | <span data-ttu-id="aae44-125">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="aae44-125">The method succeeded.</span></span><br/>                               |
| <dl> <span data-ttu-id="aae44-126"><dt>**Д \_ INVALIDARG**</dt> <dt>214794287 (0xCCD802F)</dt></span><span class="sxs-lookup"><span data-stu-id="aae44-126"><dt>**E\_INVALIDARG**</dt> <dt>214794287 (0xCCD802F)</dt></span></span> </dl> | <span data-ttu-id="aae44-127">Недопустимое значение параметра *Version* .</span><span class="sxs-lookup"><span data-stu-id="aae44-127">The value for the *Version* parameter is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="aae44-128"><dt>**Ошибка при \_ Недопустимые \_ данные**</dt> <dt>13 (0xD)</dt></span><span class="sxs-lookup"><span data-stu-id="aae44-128"><dt>**ERROR\_INVALID\_DATA**</dt> <dt>13 (0xD)</dt></span></span> </dl>       | <span data-ttu-id="aae44-129">Драйвер возвратил неподдерживаемый формат данных.</span><span class="sxs-lookup"><span data-stu-id="aae44-129">The driver returned an unsupported data format.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="aae44-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="aae44-130">Remarks</span></span>

<span data-ttu-id="aae44-131">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="aae44-131">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="aae44-132">MOF-файлы не устанавливаются в составе Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="aae44-132">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="aae44-133">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="aae44-133">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="aae44-134">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="aae44-134">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="aae44-135">Требования</span><span class="sxs-lookup"><span data-stu-id="aae44-135">Requirements</span></span>



| <span data-ttu-id="aae44-136">Требование</span><span class="sxs-lookup"><span data-stu-id="aae44-136">Requirement</span></span> | <span data-ttu-id="aae44-137">Значение</span><span class="sxs-lookup"><span data-stu-id="aae44-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aae44-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="aae44-138">Minimum supported client</span></span><br/> | <span data-ttu-id="aae44-139">Windows 7 Корпоративная, \[ только классические приложения Windows 7 Ultimate\]</span><span class="sxs-lookup"><span data-stu-id="aae44-139">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="aae44-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="aae44-140">Minimum supported server</span></span><br/> | <span data-ttu-id="aae44-141">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="aae44-141">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="aae44-142">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="aae44-142">Namespace</span></span><br/>                | <span data-ttu-id="aae44-143">Корневой \\ CIMV2 \\ безопасности \\ микрософтволуминкриптион</span><span class="sxs-lookup"><span data-stu-id="aae44-143">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="aae44-144">MOF</span><span class="sxs-lookup"><span data-stu-id="aae44-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aae44-145"><dt>Win32 \_ енкриптаблеволуме. mof</dt></span><span class="sxs-lookup"><span data-stu-id="aae44-145"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aae44-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="aae44-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aae44-147">**\_Енкриптаблеволуме Win32**</span><span class="sxs-lookup"><span data-stu-id="aae44-147">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
