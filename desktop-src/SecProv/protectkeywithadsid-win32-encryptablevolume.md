---
description: Защищает ключ шифрования тома с помощью идентификатора безопасности (SID) Active Directory.
ms.assetid: 881EEAF2-49C5-4BBD-B2AA-5E30B61E7D3A
title: Метод Протекткэйвисадсид класса Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithAdSid
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 0279a6edc8aaa275fdf75a855452d987de802d86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683921"
---
# <a name="protectkeywithadsid-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="7fecf-103">Метод Протекткэйвисадсид \_ класса Win32 енкриптаблеволуме</span><span class="sxs-lookup"><span data-stu-id="7fecf-103">ProtectKeyWithAdSid method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="7fecf-104">Метод **протекткэйвисадсид** класса [**Win32 \_ енкриптаблеволуме**](win32-encryptablevolume.md) защищает ключ шифрования тома с помощью идентификатора безопасности Active Directory (SID).</span><span class="sxs-lookup"><span data-stu-id="7fecf-104">The **ProtectKeyWithAdSid** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class secures the volume's encryption key by using a Active Directory security identifier (SID).</span></span>

## <a name="syntax"></a><span data-ttu-id="7fecf-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7fecf-105">Syntax</span></span>


```mof
uint32 ProtectKeyWithAdSid(
  [in, optional] string FriendlyName,
  [in]           string SidString,
  [in]           uint32 Flags,
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="7fecf-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7fecf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7fecf-107">*FriendlyName* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="7fecf-107">*FriendlyName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7fecf-108">Строка, указывающая назначенный пользователем идентификатор для этого предохранителя ключа.</span><span class="sxs-lookup"><span data-stu-id="7fecf-108">A string that specifies a user-assigned identifier for this key protector.</span></span> <span data-ttu-id="7fecf-109">Если этот параметр не указан, используется пустое значение.</span><span class="sxs-lookup"><span data-stu-id="7fecf-109">If this parameter is not specified, a blank value is used.</span></span>

</dd> <dt>

<span data-ttu-id="7fecf-110">*Сидстринг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7fecf-110">*SidString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7fecf-111">Строка, содержащая идентификатор безопасности Active Directory, используемый для защиты ключа шифрования.</span><span class="sxs-lookup"><span data-stu-id="7fecf-111">String that contains the Active Directory SID used to protect the encryption key.</span></span>

</dd> <dt>

<span data-ttu-id="7fecf-112">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7fecf-112">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7fecf-113">Флаги, изменяющие поведение функции.</span><span class="sxs-lookup"><span data-stu-id="7fecf-113">Flags that change the function behavior.</span></span> <span data-ttu-id="7fecf-114">Это может быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="7fecf-114">This can be one of the following values.</span></span>



| <span data-ttu-id="7fecf-115">Значение</span><span class="sxs-lookup"><span data-stu-id="7fecf-115">Value</span></span>                                                                                                                                                                                                                                                                                                                     | <span data-ttu-id="7fecf-116">Значение</span><span class="sxs-lookup"><span data-stu-id="7fecf-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FVE_DPAPI_NG_FLAG_NONE"></span><span id="fve_dpapi_ng_flag_none"></span><dl> <span data-ttu-id="7fecf-117"><dt>**ФВЕ \_ DPAPI \_ NG \_ флаг \_ None**</dt> <dt>Символ 0x0000</dt></span><span class="sxs-lookup"><span data-stu-id="7fecf-117"><dt>**FVE\_DPAPI\_NG\_FLAG\_NONE**</dt> <dt>0x0000</dt></span></span> </dl>                                                                   | <span data-ttu-id="7fecf-118">Не влияет.</span><span class="sxs-lookup"><span data-stu-id="7fecf-118">No effect.</span></span><br/>                                                                                                                                                                                                                                                                                                                   |
| <span id="FVE_DPAPI_NG_FLAG_UNLOCK_AS_SERVICE_ACCOUNT"></span><span id="fve_dpapi_ng_flag_unlock_as_service_account"></span><dl> <span data-ttu-id="7fecf-119"><dt>**ФВЕ \_ DPAPI \_ NG \_ флаг \_ разблокировки \_ в качестве \_ \_ учетной записи службы**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="7fecf-119"><dt>**FVE\_DPAPI\_NG\_FLAG\_UNLOCK\_AS\_SERVICE\_ACCOUNT**</dt> <dt>0x0001</dt></span></span> </dl> | <span data-ttu-id="7fecf-120">Указывает, что предохранитель на основе идентификатора безопасности был защищен учетной записью службы.</span><span class="sxs-lookup"><span data-stu-id="7fecf-120">Specifies that the SID-based protector was protected to a service account.</span></span> <span data-ttu-id="7fecf-121">Если этот флаг указан, вызывающий объект должен убедиться, что он работает как соответствующая учетная запись службы перед вызовом [**унлокквисадсид**](unlockwithadsid-win32-encryptablevolume.md) (например, временное удаление олицетворения).</span><span class="sxs-lookup"><span data-stu-id="7fecf-121">If this flag is specified, the caller should ensure that it is running as the appropriate service account before calling [**UnlockWithAdSid**](unlockwithadsid-win32-encryptablevolume.md) (by temporarily dropping impersonation, for example).</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="7fecf-122">*Волумекэйпротекторид* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7fecf-122">*VolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7fecf-123">Уникальный идентификатор, связанный с созданным предохранителем.</span><span class="sxs-lookup"><span data-stu-id="7fecf-123">A unique identifier associated with the created protector.</span></span> <span data-ttu-id="7fecf-124">Эту строку можно использовать для управления предохранителем ключа.</span><span class="sxs-lookup"><span data-stu-id="7fecf-124">You can use this string to manage the key protector.</span></span>

<span data-ttu-id="7fecf-125">Если диск поддерживает аппаратное шифрование, а BitLocker не использует нестандартное владение, для строки идентификатора задается значение "BitLocker", а предохранитель ключа записывается в метаданные диапазона.</span><span class="sxs-lookup"><span data-stu-id="7fecf-125">If the drive supports hardware encryption and BitLocker has not taken band ownership, the ID string is set to "BitLocker" and the key protector is written to per band metadata.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7fecf-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7fecf-126">Return value</span></span>

<span data-ttu-id="7fecf-127">При сбое этот метод возвращает один из следующих кодов или другой код ошибки.</span><span class="sxs-lookup"><span data-stu-id="7fecf-127">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="7fecf-128">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="7fecf-128">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="7fecf-129">Описание</span><span class="sxs-lookup"><span data-stu-id="7fecf-129">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="7fecf-130"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="7fecf-130"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="7fecf-131">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="7fecf-131">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7fecf-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7fecf-132">Remarks</span></span>

<span data-ttu-id="7fecf-133">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="7fecf-133">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="7fecf-134">MOF-файлы не устанавливаются в составе Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="7fecf-134">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="7fecf-135">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="7fecf-135">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="7fecf-136">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](../wmisdk/managed-object-format--mof-.md) .</span><span class="sxs-lookup"><span data-stu-id="7fecf-136">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md)</span></span>

<span data-ttu-id="7fecf-137">По умолчанию не удается удаленно добавить учетную запись Active Directory или предохранители групп.</span><span class="sxs-lookup"><span data-stu-id="7fecf-137">By default, you cannot add an Active Directory account or group protector remotely.</span></span> <span data-ttu-id="7fecf-138">Необходимо включить ограниченное делегирование на контроллере домена и на исходном компьютере.</span><span class="sxs-lookup"><span data-stu-id="7fecf-138">You must enable constrained delegation on the domain controller and source computer.</span></span> <span data-ttu-id="7fecf-139">На контроллере домена выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="7fecf-139">On the domain controller, perform the following steps:</span></span>

1.  <span data-ttu-id="7fecf-140">Откройте диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="7fecf-140">Open Server Manager</span></span>
2.  <span data-ttu-id="7fecf-141">Выбор компьютеров в Active Directory ролях</span><span class="sxs-lookup"><span data-stu-id="7fecf-141">Select Computers in Active Directory roles</span></span>
3.  <span data-ttu-id="7fecf-142">Выберите целевой клиентский компьютер и щелкните правой кнопкой мыши</span><span class="sxs-lookup"><span data-stu-id="7fecf-142">Select the target client computer and right click</span></span>
4.  <span data-ttu-id="7fecf-143">Выберите вкладку Делегирование</span><span class="sxs-lookup"><span data-stu-id="7fecf-143">Select the Delegation tab</span></span>
5.  <span data-ttu-id="7fecf-144">Выберите переключатель "доверять компьютеру делегирование указанных служб"</span><span class="sxs-lookup"><span data-stu-id="7fecf-144">Select the "Trust this computer for delegation to specified services only" radio button</span></span>
6.  <span data-ttu-id="7fecf-145">Выберите переключатель "использовать только Kerberos"</span><span class="sxs-lookup"><span data-stu-id="7fecf-145">Select the "Use Kerberos only" radio button</span></span>
7.  <span data-ttu-id="7fecf-146">Нажмите "Добавить"</span><span class="sxs-lookup"><span data-stu-id="7fecf-146">Click Add</span></span>
8.  <span data-ttu-id="7fecf-147">Выберите "пользователи или компьютеры"</span><span class="sxs-lookup"><span data-stu-id="7fecf-147">Select "Users or Computers"</span></span>
9.  <span data-ttu-id="7fecf-148">Выберите узел/как имя субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="7fecf-148">Select host/ as the Service Principal Name</span></span>

<span data-ttu-id="7fecf-149">Выполните шаги с 3 по 9 на исходном компьютере.</span><span class="sxs-lookup"><span data-stu-id="7fecf-149">Perform steps 3 through 9 on the source computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="7fecf-150">Требования</span><span class="sxs-lookup"><span data-stu-id="7fecf-150">Requirements</span></span>



| <span data-ttu-id="7fecf-151">Требование</span><span class="sxs-lookup"><span data-stu-id="7fecf-151">Requirement</span></span> | <span data-ttu-id="7fecf-152">Значение</span><span class="sxs-lookup"><span data-stu-id="7fecf-152">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7fecf-153">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7fecf-153">Minimum supported client</span></span><br/> | <span data-ttu-id="7fecf-154">Windows 8 Корпоративная, \[ только классические приложения Windows 8 Pro\]</span><span class="sxs-lookup"><span data-stu-id="7fecf-154">Windows 8 Enterprise, Windows 8 Pro \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7fecf-155">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7fecf-155">Minimum supported server</span></span><br/> | <span data-ttu-id="7fecf-156">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="7fecf-156">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7fecf-157">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7fecf-157">Namespace</span></span><br/>                | <span data-ttu-id="7fecf-158">Корневой \\ CIMV2 \\ безопасности \\ микрософтволуминкриптион</span><span class="sxs-lookup"><span data-stu-id="7fecf-158">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="7fecf-159">MOF</span><span class="sxs-lookup"><span data-stu-id="7fecf-159">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7fecf-160"><dt>Win32 \_ енкриптаблеволуме. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7fecf-160"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7fecf-161">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7fecf-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fecf-162">**\_Енкриптаблеволуме Win32**</span><span class="sxs-lookup"><span data-stu-id="7fecf-162">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
