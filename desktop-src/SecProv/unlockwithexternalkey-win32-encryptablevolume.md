---
description: Использует предоставленный внешний ключ для доступа к содержимому тома данных.
ms.assetid: e383767e-8557-469c-bc44-f67591c46f23
title: Метод Унлокквисекстерналкэй класса Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UnlockWithExternalKey
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 4b599f098856937ae5610156cba96a1deea1f64b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664376"
---
# <a name="unlockwithexternalkey-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="23f9c-103">Метод Унлокквисекстерналкэй \_ класса Win32 енкриптаблеволуме</span><span class="sxs-lookup"><span data-stu-id="23f9c-103">UnlockWithExternalKey method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="23f9c-104">Метод **унлокквисекстерналкэй** класса [**Win32 \_ енкриптаблеволуме**](win32-encryptablevolume.md) использует предоставленный внешний ключ для доступа к содержимому тома данных.</span><span class="sxs-lookup"><span data-stu-id="23f9c-104">The **UnlockWithExternalKey** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class uses a provided external key to access the contents of a data volume.</span></span>

<span data-ttu-id="23f9c-105">Ключ шифрования тома должен быть защищен с помощью одного или нескольких предохранителей ключа типа "внешний ключ" с использованием метода [**протекткэйвисекстерналкэй**](protectkeywithexternalkey-win32-encryptablevolume.md) , чтобы иметь возможность разблокировать том с помощью этого метода.</span><span class="sxs-lookup"><span data-stu-id="23f9c-105">The volume's encryption key must have been secured with one or more key protectors of the type "External Key" using the [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) method to be able to unlock the volume with this method.</span></span>

> [!Note]  
> <span data-ttu-id="23f9c-106">Если диск поддерживает аппаратное шифрование, эта функция устанавливает для полосы состояние "разблокирован".</span><span class="sxs-lookup"><span data-stu-id="23f9c-106">If the disc supports hardware encryption this function sets the band status to "unlocked""</span></span>

 

## <a name="syntax"></a><span data-ttu-id="23f9c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="23f9c-107">Syntax</span></span>


```mof
uint32 UnlockWithExternalKey(
  [in] uint8 ExternalKey[]
);
```



## <a name="parameters"></a><span data-ttu-id="23f9c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="23f9c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23f9c-109">*Екстерналкэй* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="23f9c-109">*ExternalKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23f9c-110">Тип: **Uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="23f9c-110">Type: **uint8\[\]**</span></span>

<span data-ttu-id="23f9c-111">Массив байтов, указывающий 256-разрядный внешний ключ, используемый для разблокировки тома.</span><span class="sxs-lookup"><span data-stu-id="23f9c-111">An array of bytes that specifies the 256-bit external key used to unlock the volume.</span></span> <span data-ttu-id="23f9c-112">Этот ключ можно получить, вызвав метод [**жетекстерналкэйфромфиле**](getexternalkeyfromfile-win32-encryptablevolume.md) .</span><span class="sxs-lookup"><span data-stu-id="23f9c-112">This key can be obtained by calling the [**GetExternalKeyFromFile**](getexternalkeyfromfile-win32-encryptablevolume.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23f9c-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="23f9c-113">Return value</span></span>

<span data-ttu-id="23f9c-114">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="23f9c-114">Type: **uint32**</span></span>

<span data-ttu-id="23f9c-115">При сбое этот метод возвращает один из следующих кодов или другой код ошибки.</span><span class="sxs-lookup"><span data-stu-id="23f9c-115">This method returns one of the following codes or another error code if it fails.</span></span>

<span data-ttu-id="23f9c-116">Если том уже разблокирован, этот метод возвращает значение 0.</span><span class="sxs-lookup"><span data-stu-id="23f9c-116">If the volume is already unlocked, this method returns 0.</span></span>



| <span data-ttu-id="23f9c-117">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="23f9c-117">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="23f9c-118">Описание</span><span class="sxs-lookup"><span data-stu-id="23f9c-118">Description</span></span>                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="23f9c-119"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="23f9c-119"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="23f9c-120">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="23f9c-120">The method was successful.</span></span><br/>                                                                                                       |
| <dl> <span data-ttu-id="23f9c-121"><dt>**Ошибка при \_ Значение не \_ Найдено**</dt> <dt>(0x)</dt></span><span class="sxs-lookup"><span data-stu-id="23f9c-121"><dt>**ERROR\_NOT\_FOUND**</dt> <dt>No value given (0x)</dt></span></span> </dl>          | <span data-ttu-id="23f9c-122">Том не имеет предохранителя ключа типа "внешний ключ".</span><span class="sxs-lookup"><span data-stu-id="23f9c-122">The volume does not have a key protector of the type "External Key".</span></span><br/>                                                             |
| <dl> <span data-ttu-id="23f9c-123"><dt>**Ошибка при \_ Недопустимый \_ пароль**</dt> <dt>не задано значение (0x)</dt></span><span class="sxs-lookup"><span data-stu-id="23f9c-123"><dt>**ERROR\_INVALID\_PASSWORD**</dt> <dt>No value given (0x)</dt></span></span> </dl>   | <span data-ttu-id="23f9c-124">Один или несколько предохранителей ключа типа "внешний ключ" существуют, но указанный параметр *екстерналкэй* не может разблокировать том.</span><span class="sxs-lookup"><span data-stu-id="23f9c-124">One or more key protectors of the type "External Key" exist, but the specified *ExternalKey* parameter cannot unlock the volume.</span></span><br/> |
| <dl> <span data-ttu-id="23f9c-125"><dt>**Д \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="23f9c-125"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>          | <span data-ttu-id="23f9c-126">Параметр *екстерналкэй* не является массивом размером 4.</span><span class="sxs-lookup"><span data-stu-id="23f9c-126">The *ExternalKey* parameter is not an array of size 4.</span></span><br/>                                                                           |
| <dl> <span data-ttu-id="23f9c-127"><dt>**ФВЕ \_ E \_ не \_ активировано**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="23f9c-127"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl> | <span data-ttu-id="23f9c-128">Средство BitLocker не включено в томе.</span><span class="sxs-lookup"><span data-stu-id="23f9c-128">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="23f9c-129">Добавьте предохранитель ключа, чтобы включить BitLocker.</span><span class="sxs-lookup"><span data-stu-id="23f9c-129">Add a key protector to enable BitLocker.</span></span> <br/>                                                |



 

## <a name="remarks"></a><span data-ttu-id="23f9c-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="23f9c-130">Remarks</span></span>

<span data-ttu-id="23f9c-131">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="23f9c-131">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="23f9c-132">MOF-файлы не устанавливаются в составе Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="23f9c-132">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="23f9c-133">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="23f9c-133">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="23f9c-134">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="23f9c-134">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="23f9c-135">Требования</span><span class="sxs-lookup"><span data-stu-id="23f9c-135">Requirements</span></span>



| <span data-ttu-id="23f9c-136">Требование</span><span class="sxs-lookup"><span data-stu-id="23f9c-136">Requirement</span></span> | <span data-ttu-id="23f9c-137">Значение</span><span class="sxs-lookup"><span data-stu-id="23f9c-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23f9c-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="23f9c-138">Minimum supported client</span></span><br/> | <span data-ttu-id="23f9c-139">Windows Vista Enterprise, \[ только для настольных приложений Windows Vista Ultimate\]</span><span class="sxs-lookup"><span data-stu-id="23f9c-139">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="23f9c-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="23f9c-140">Minimum supported server</span></span><br/> | <span data-ttu-id="23f9c-141">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="23f9c-141">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="23f9c-142">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="23f9c-142">Namespace</span></span><br/>                | <span data-ttu-id="23f9c-143">Корневой \\ CIMV2 \\ безопасности \\ микрософтволуминкриптион</span><span class="sxs-lookup"><span data-stu-id="23f9c-143">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="23f9c-144">MOF</span><span class="sxs-lookup"><span data-stu-id="23f9c-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="23f9c-145"><dt>Win32 \_ енкриптаблеволуме. mof</dt></span><span class="sxs-lookup"><span data-stu-id="23f9c-145"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23f9c-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="23f9c-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23f9c-147">**\_Енкриптаблеволуме Win32**</span><span class="sxs-lookup"><span data-stu-id="23f9c-147">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
