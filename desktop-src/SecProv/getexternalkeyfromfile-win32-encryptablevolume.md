---
description: Возвращает внешний ключ из файла.
ms.assetid: b61b71fb-af6f-4fe3-859b-a9f2f42ca6d2
title: Метод Жетекстерналкэйфромфиле класса Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetExternalKeyFromFile
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: ba0c2cf4744c12143090488d730a1d49bab9b431
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684069"
---
# <a name="getexternalkeyfromfile-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="d880f-103">Метод Жетекстерналкэйфромфиле \_ класса Win32 енкриптаблеволуме</span><span class="sxs-lookup"><span data-stu-id="d880f-103">GetExternalKeyFromFile method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="d880f-104">Метод **жетекстерналкэйфромфиле** класса [**Win32 \_ енкриптаблеволуме**](win32-encryptablevolume.md) возвращает внешний ключ из файла, созданного с помощью [**савикстерналкэйтофиле**](saveexternalkeytofile-win32-encryptablevolume.md), учитывая расположение этого файла.</span><span class="sxs-lookup"><span data-stu-id="d880f-104">The **GetExternalKeyFromFile** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class returns the external key from a file created by [**SaveExternalKeyToFile**](saveexternalkeytofile-win32-encryptablevolume.md), given the location of that file.</span></span>

## <a name="syntax"></a><span data-ttu-id="d880f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d880f-105">Syntax</span></span>


```mof
uint32 GetExternalKeyFromFile(
  [in]  string PathWithFileName,
  [out] uint8  ExternalKey[]
);
```



## <a name="parameters"></a><span data-ttu-id="d880f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d880f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d880f-107">*Пасвисфиленаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d880f-107">*PathWithFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d880f-108">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="d880f-108">Type: **string**</span></span>

<span data-ttu-id="d880f-109">Строка, указывающая расположение файла, содержащего внешний ключ.</span><span class="sxs-lookup"><span data-stu-id="d880f-109">A string that specifies the location of the file containing an external key.</span></span>

</dd> <dt>

<span data-ttu-id="d880f-110">*Екстерналкэй* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d880f-110">*ExternalKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d880f-111">Тип: **Uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="d880f-111">Type: **uint8\[\]**</span></span>

<span data-ttu-id="d880f-112">Массив байтов, который является 256-битным внешним ключом, содержащимся в файле, который можно использовать для разблокировки тома.</span><span class="sxs-lookup"><span data-stu-id="d880f-112">An array of bytes that is the 256-bit external key contained within the file that can be used to unlock a volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d880f-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d880f-113">Return value</span></span>

<span data-ttu-id="d880f-114">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d880f-114">Type: **uint32**</span></span>

<span data-ttu-id="d880f-115">При сбое этот метод возвращает один из следующих кодов или другой код ошибки.</span><span class="sxs-lookup"><span data-stu-id="d880f-115">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="d880f-116">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="d880f-116">Return code/value</span></span>                                                                                                                                                                   | <span data-ttu-id="d880f-117">Описание</span><span class="sxs-lookup"><span data-stu-id="d880f-117">Description</span></span>                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <span data-ttu-id="d880f-118"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="d880f-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                   | <span data-ttu-id="d880f-119">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="d880f-119">The method was successful.</span></span><br/>                  |
| <dl> <span data-ttu-id="d880f-120"><dt>**Д \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="d880f-120"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>           | <span data-ttu-id="d880f-121">Файл не содержит внешний ключ.</span><span class="sxs-lookup"><span data-stu-id="d880f-121">The file does not contain an external key.</span></span><br/>  |
| <dl> <span data-ttu-id="d880f-122"><dt>**Ошибка при \_ ФАЙЛ \_ не \_ найден**</dt> <dt>2147942402 (0x80070002)</dt></span><span class="sxs-lookup"><span data-stu-id="d880f-122"><dt>**ERROR\_FILE\_NOT\_FOUND**</dt> <dt>2147942402 (0x80070002)</dt></span></span> </dl> | <span data-ttu-id="d880f-123">Не удается найти файл в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="d880f-123">Cannot find file at the location specified.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d880f-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d880f-124">Remarks</span></span>

<span data-ttu-id="d880f-125">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="d880f-125">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="d880f-126">MOF-файлы не устанавливаются в составе Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="d880f-126">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="d880f-127">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="d880f-127">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="d880f-128">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="d880f-128">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d880f-129">Требования</span><span class="sxs-lookup"><span data-stu-id="d880f-129">Requirements</span></span>



| <span data-ttu-id="d880f-130">Требование</span><span class="sxs-lookup"><span data-stu-id="d880f-130">Requirement</span></span> | <span data-ttu-id="d880f-131">Значение</span><span class="sxs-lookup"><span data-stu-id="d880f-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d880f-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d880f-132">Minimum supported client</span></span><br/> | <span data-ttu-id="d880f-133">Windows Vista Enterprise, \[ только для настольных приложений Windows Vista Ultimate\]</span><span class="sxs-lookup"><span data-stu-id="d880f-133">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="d880f-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d880f-134">Minimum supported server</span></span><br/> | <span data-ttu-id="d880f-135">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d880f-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d880f-136">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d880f-136">Namespace</span></span><br/>                | <span data-ttu-id="d880f-137">Корневой \\ CIMV2 \\ безопасности \\ микрософтволуминкриптион</span><span class="sxs-lookup"><span data-stu-id="d880f-137">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="d880f-138">MOF</span><span class="sxs-lookup"><span data-stu-id="d880f-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d880f-139"><dt>Win32 \_ енкриптаблеволуме. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d880f-139"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d880f-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d880f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d880f-141">**\_Енкриптаблеволуме Win32**</span><span class="sxs-lookup"><span data-stu-id="d880f-141">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
