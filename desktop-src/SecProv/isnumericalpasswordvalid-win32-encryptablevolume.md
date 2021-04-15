---
description: Указывает, соответствует ли числовой пароль специальным требованиям к формату для этого значения проверки подлинности.
ms.assetid: 3995405f-db4d-4f72-98dc-133a09f9cf65
title: Метод Иснумерикалпассвордвалид класса Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.IsNumericalPasswordValid
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 7cec4aa31ae9ff6aee90c0f46ded935b3d553783
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683924"
---
# <a name="isnumericalpasswordvalid-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="86684-103">Метод Иснумерикалпассвордвалид \_ класса Win32 енкриптаблеволуме</span><span class="sxs-lookup"><span data-stu-id="86684-103">IsNumericalPasswordValid method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="86684-104">Метод **иснумерикалпассвордвалид** класса [**Win32 \_ енкриптаблеволуме**](win32-encryptablevolume.md) указывает, соответствует ли числовой пароль специальным требованиям к формату для этого значения проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="86684-104">The **IsNumericalPasswordValid** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class indicates whether the numerical password meets the special format requirements for this authentication value.</span></span>

## <a name="syntax"></a><span data-ttu-id="86684-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="86684-105">Syntax</span></span>


```mof
uint32 IsNumericalPasswordValid(
  [in]  string  NumericalPassword,
  [out] boolean IsNumericalPasswordValid
);
```



## <a name="parameters"></a><span data-ttu-id="86684-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="86684-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86684-107">*Нумерикалпассворд* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="86684-107">*NumericalPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86684-108">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="86684-108">Type: **string**</span></span>

<span data-ttu-id="86684-109">Строка, указывающая числовой пароль.</span><span class="sxs-lookup"><span data-stu-id="86684-109">A string that specifies the numerical password.</span></span>

<span data-ttu-id="86684-110">Числовой пароль должен содержать 48 цифр.</span><span class="sxs-lookup"><span data-stu-id="86684-110">The numerical password must contain 48 digits.</span></span> <span data-ttu-id="86684-111">Эти цифры можно разделить на 8 групп из 6 цифр, с последней цифрой в каждой группе, указывающей на значение контрольной суммы для группы.</span><span class="sxs-lookup"><span data-stu-id="86684-111">These digits can be divided into 8 groups of 6 digits, with the last digit in each group indicating a checksum value for the group.</span></span> <span data-ttu-id="86684-112">Каждая группа из 6 цифр должна быть кратной 11 и должна быть меньше 720896.</span><span class="sxs-lookup"><span data-stu-id="86684-112">Each group of 6 digits must be divisible by 11 and must be less than 720896.</span></span> <span data-ttu-id="86684-113">При условии, что группа из шести цифр помечена как x1, x2, X3, X4, x5 и X6, контрольная сумма X6 вычисляется как – x1 + x2 – X3 + X4 – x5 mod 11.</span><span class="sxs-lookup"><span data-stu-id="86684-113">Assuming a group of six digits is labeled as x1, x2, x3, x4, x5, and x6, the checksum x6 digit is calculated as –x1+x2–x3+x4–x5 mod 11.</span></span>

<span data-ttu-id="86684-114">Группы цифр можно разделять пробелами или дефисами.</span><span class="sxs-lookup"><span data-stu-id="86684-114">The groups of digits can optionally be separated by a space or hyphen.</span></span> <span data-ttu-id="86684-115">Таким образом, "XXXXXX-XXXXXX-XXXXXX-XXXXXX-XXXXXX-XXXXXX-XXXXXX-XXXXXX" или "XXXXXX XXXXXX XXXXXX XXXXXX (xxxxxx) XXXXXX XXXXXX" может также содержать допустимые числовые пароли.</span><span class="sxs-lookup"><span data-stu-id="86684-115">Therefore, "xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx" or "xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx" may also contain valid numerical passwords.</span></span>

</dd> <dt>

<span data-ttu-id="86684-116">*Иснумерикалпассвордвалид* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="86684-116">*IsNumericalPasswordValid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="86684-117">Тип: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="86684-117">Type: **boolean**</span></span>

<span data-ttu-id="86684-118">Логическое значение, равное true, если числовой пароль соответствует требованиям специального формата для этого значения проверки подлинности, в противном случае — значение false.</span><span class="sxs-lookup"><span data-stu-id="86684-118">A Boolean value that is true if the numerical password meets the special format requirements for this authentication value, otherwise the value is false.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86684-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="86684-119">Return value</span></span>

<span data-ttu-id="86684-120">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="86684-120">Type: **uint32**</span></span>

<span data-ttu-id="86684-121">При сбое этот метод возвращает один из следующих кодов или другой код ошибки.</span><span class="sxs-lookup"><span data-stu-id="86684-121">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="86684-122">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="86684-122">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="86684-123">Описание</span><span class="sxs-lookup"><span data-stu-id="86684-123">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="86684-124"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="86684-124"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="86684-125">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="86684-125">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="86684-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="86684-126">Remarks</span></span>

<span data-ttu-id="86684-127">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="86684-127">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="86684-128">MOF-файлы не устанавливаются в составе Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="86684-128">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="86684-129">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="86684-129">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="86684-130">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="86684-130">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="86684-131">Требования</span><span class="sxs-lookup"><span data-stu-id="86684-131">Requirements</span></span>



| <span data-ttu-id="86684-132">Требование</span><span class="sxs-lookup"><span data-stu-id="86684-132">Requirement</span></span> | <span data-ttu-id="86684-133">Значение</span><span class="sxs-lookup"><span data-stu-id="86684-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86684-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="86684-134">Minimum supported client</span></span><br/> | <span data-ttu-id="86684-135">Windows Vista Enterprise, \[ только для настольных приложений Windows Vista Ultimate\]</span><span class="sxs-lookup"><span data-stu-id="86684-135">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="86684-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="86684-136">Minimum supported server</span></span><br/> | <span data-ttu-id="86684-137">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="86684-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="86684-138">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="86684-138">Namespace</span></span><br/>                | <span data-ttu-id="86684-139">Корневой \\ CIMV2 \\ безопасности \\ микрософтволуминкриптион</span><span class="sxs-lookup"><span data-stu-id="86684-139">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="86684-140">MOF</span><span class="sxs-lookup"><span data-stu-id="86684-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="86684-141"><dt>Win32 \_ енкриптаблеволуме. mof</dt></span><span class="sxs-lookup"><span data-stu-id="86684-141"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86684-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="86684-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86684-143">**\_Енкриптаблеволуме Win32**</span><span class="sxs-lookup"><span data-stu-id="86684-143">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
