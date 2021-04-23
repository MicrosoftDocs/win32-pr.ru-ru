---
description: Устанавливает владельца доверенного платформенного модуля.
ms.assetid: 7b4c8785-0925-41a8-a878-7c1f38d31853
title: Метод Такеовнершип класса Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.TakeOwnership
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: acb0cb03f5e422695623bf6e183d1fd89f63ab60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081436"
---
# <a name="takeownership-method-of-the-win32_tpm-class"></a><span data-ttu-id="fa87f-103">Метод Такеовнершип \_ класса TPM Win32</span><span class="sxs-lookup"><span data-stu-id="fa87f-103">TakeOwnership method of the Win32\_Tpm class</span></span>

<span data-ttu-id="fa87f-104">Метод **такеовнершип** класса [**\_ TPM Win32**](win32-tpm.md) устанавливает владельца для TPM.</span><span class="sxs-lookup"><span data-stu-id="fa87f-104">The **TakeOwnership** method of the [**Win32\_Tpm**](win32-tpm.md) class installs an owner for the TPM.</span></span> <span data-ttu-id="fa87f-105">Владелец TPM может полностью использовать возможности TPM.</span><span class="sxs-lookup"><span data-stu-id="fa87f-105">The owner of the TPM can make full use of TPM capabilities.</span></span> <span data-ttu-id="fa87f-106">После установки владельца никто из других пользователей или программного обеспечения не сможет запрашивать владение TPM.</span><span class="sxs-lookup"><span data-stu-id="fa87f-106">After an owner is set, no other user or software can claim ownership of the TPM.</span></span>

<span data-ttu-id="fa87f-107">Для того, чтобы метод **такеовнершип** мог быть выполнен, необходимо, чтобы методы [**включения**](isenabled-win32-tpm.md), [**активации**](isactivated-win32-tpm.md)и [**исовнершипалловед**](isownershipallowed-win32-tpm.md) были истинными.</span><span class="sxs-lookup"><span data-stu-id="fa87f-107">The [**IsEnabled**](isenabled-win32-tpm.md), [**IsActivated**](isactivated-win32-tpm.md), and [**IsOwnershipAllowed**](isownershipallowed-win32-tpm.md) methods must all be true before the **TakeOwnership** method can succeed.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa87f-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fa87f-108">Syntax</span></span>


```mof
uint32 TakeOwnership(
  [in, optional] string OwnerAuth
);
```



## <a name="parameters"></a><span data-ttu-id="fa87f-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="fa87f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa87f-110">*Овнераус* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="fa87f-110">*OwnerAuth* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="fa87f-111">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="fa87f-111">Type: **string**</span></span>

<span data-ttu-id="fa87f-112">Строка, идентифицирующая владельца доверенного платформенного модуля.</span><span class="sxs-lookup"><span data-stu-id="fa87f-112">A string that identifies the TPM owner.</span></span> <span data-ttu-id="fa87f-113">Эта строка должна быть строкой в кодировке Base64, завершающейся нулем, которая содержит ровно 20 байт двоичных данных.</span><span class="sxs-lookup"><span data-stu-id="fa87f-113">This string must be a base64-encoded null-terminated string that contains exactly 20 bytes of binary data.</span></span> <span data-ttu-id="fa87f-114">Используйте метод [**конверттувнераус**](converttoownerauth-win32-tpm.md) для преобразования парольной фразы в ожидаемый формат.</span><span class="sxs-lookup"><span data-stu-id="fa87f-114">Use the [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) method to translate a passphrase to this expected format.</span></span> <span data-ttu-id="fa87f-115">Параметр *овнераус* считывается из реестра, если он не указан.</span><span class="sxs-lookup"><span data-stu-id="fa87f-115">The *OwnerAuth* parameter is read from the registry if none is provided.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa87f-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fa87f-116">Return value</span></span>

<span data-ttu-id="fa87f-117">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fa87f-117">Type: **uint32**</span></span>

<span data-ttu-id="fa87f-118">Могут возвращаться все ошибки доверенного платформенного модуля, а также ошибки, относящиеся к базовым службам TPM.</span><span class="sxs-lookup"><span data-stu-id="fa87f-118">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="fa87f-119">В следующей таблице перечислены некоторые распространенные коды возврата.</span><span class="sxs-lookup"><span data-stu-id="fa87f-119">The following table lists some of the common return codes.</span></span>



| <span data-ttu-id="fa87f-120">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="fa87f-120">Return code/value</span></span>                                                                                                                                                                         | <span data-ttu-id="fa87f-121">Описание</span><span class="sxs-lookup"><span data-stu-id="fa87f-121">Description</span></span>                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fa87f-122"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="fa87f-122"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                         | <span data-ttu-id="fa87f-123">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="fa87f-123">The method was successful.</span></span><br/>                                                                                                                                                                              |
| <dl> <span data-ttu-id="fa87f-124"><dt>**Д \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="fa87f-124"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>                 | <span data-ttu-id="fa87f-125">Недопустимый параметр *овнераус* .</span><span class="sxs-lookup"><span data-stu-id="fa87f-125">The *OwnerAuth* parameter is not valid.</span></span><br/>                                                                                                                                                                 |
| <dl> <span data-ttu-id="fa87f-126"><dt>**Доверенный платформенный модуль \_ E \_ owner \_ Set**</dt> <dt>2150105108 (0x80280014)</dt></span><span class="sxs-lookup"><span data-stu-id="fa87f-126"><dt>**TPM\_E\_OWNER\_SET**</dt> <dt>2150105108 (0x80280014)</dt></span></span> </dl>            | <span data-ttu-id="fa87f-127">Владелец уже существует в доверенном платформенном модуле.</span><span class="sxs-lookup"><span data-stu-id="fa87f-127">An owner already exists on the TPM.</span></span><br/>                                                                                                                                                                     |
| <dl> <span data-ttu-id="fa87f-128"><dt>**Доверенный платформенный модуль \_ E \_ без \_ подтверждения**</dt> <dt>2150105123 (0x80280023)</dt></span><span class="sxs-lookup"><span data-stu-id="fa87f-128"><dt>**TPM\_E\_NO\_ENDORSEMENT**</dt> <dt>2150105123 (0x80280023)</dt></span></span> </dl>       | <span data-ttu-id="fa87f-129">Не удается найти ключ подтверждения в доверенном платформенном модуле.</span><span class="sxs-lookup"><span data-stu-id="fa87f-129">No endorsement key can be found on the TPM.</span></span><br/> <span data-ttu-id="fa87f-130">Сведения о создании пары ключей подтверждения в доверенном платформенном модуле см. в описании метода [**креатиндорсементкэйпаир**](createendorsementkeypair-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="fa87f-130">To create an endorsement key pair on the TPM, see the [**CreateEndorsementKeyPair**](createendorsementkeypair-win32-tpm.md) method.</span></span><br/>             |
| <dl> <span data-ttu-id="fa87f-131"><dt>**Доверенный платформенный модуль \_ E. \_ Установка \_ отключена**</dt> <dt>2150105099 (0x8028000B)</dt></span><span class="sxs-lookup"><span data-stu-id="fa87f-131"><dt>**TPM\_E\_INSTALL\_DISABLED**</dt> <dt>2150105099 (0x8028000B)</dt></span></span> </dl>     | <span data-ttu-id="fa87f-132">Невозможно установить владельца для этого доверенного платформенного модуля.</span><span class="sxs-lookup"><span data-stu-id="fa87f-132">An owner cannot be installed on this TPM.</span></span><br/> <span data-ttu-id="fa87f-133">Сведения о том, как разрешить установку владельца устройства, см. в разделе [**сетфисикалпресенцерекуест**](setphysicalpresencerequest-win32-tpm.md).</span><span class="sxs-lookup"><span data-stu-id="fa87f-133">For information about how to allow installation of a device owner, see [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md).</span></span><br/> |
| <dl> <span data-ttu-id="fa87f-134"><dt>**Доверенный платформенный модуль \_ \_Блокировка защиты \_ от \_ перезапуска**</dt> <dt>2150107139 (0x80280803)</dt></span><span class="sxs-lookup"><span data-stu-id="fa87f-134"><dt>**TPM\_E\_DEFEND\_LOCK\_RUNNING**</dt> <dt>2150107139 (0x80280803)</dt></span></span> </dl> | <span data-ttu-id="fa87f-135">TPM защищается от атак из словарей и находится в течение времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="fa87f-135">The TPM is defending against dictionary attacks and is in a time-out period.</span></span> <span data-ttu-id="fa87f-136">Дополнительные сведения см. в описании метода [**ресетауслоккаут**](resetauthlockout-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="fa87f-136">For more information, see the [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) method.</span></span><br/>                               |



 

## <a name="remarks"></a><span data-ttu-id="fa87f-137">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fa87f-137">Remarks</span></span>

<span data-ttu-id="fa87f-138">Для того чтобы **такеовнершип** мог быть выполнен, [**все методы,**](isenabled-win32-tpm.md) [**активированные**](isactivated-win32-tpm.md)и [**исовнершипалловед**](isownershipallowed-win32-tpm.md) , должны быть истинными.</span><span class="sxs-lookup"><span data-stu-id="fa87f-138">The methods [**IsEnabled**](isenabled-win32-tpm.md), [**IsActivated**](isactivated-win32-tpm.md), and [**IsOwnershipAllowed**](isownershipallowed-win32-tpm.md) must all be true before **TakeOwnership** can succeed.</span></span>

<span data-ttu-id="fa87f-139">Используйте метод [**конверттувнераус**](converttoownerauth-win32-tpm.md) , чтобы изменить парольную фразу на входное значение, используемое для параметра *овнераус* .</span><span class="sxs-lookup"><span data-stu-id="fa87f-139">You should use the [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) method to change a passphrase into the input value used for the *OwnerAuth* parameter.</span></span>

<span data-ttu-id="fa87f-140">Метод **такеовнершип** создает резервную копию значения авторизации владельца, чтобы Active Directory, если настроены соответствующие параметры групповая политика.</span><span class="sxs-lookup"><span data-stu-id="fa87f-140">The **TakeOwnership** method backs up the owner authorization value to Active Directory if the appropriate Group Policy settings have been configured.</span></span>

<span data-ttu-id="fa87f-141">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="fa87f-141">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="fa87f-142">MOF-файлы не устанавливаются в составе Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="fa87f-142">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="fa87f-143">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="fa87f-143">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="fa87f-144">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="fa87f-144">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fa87f-145">Требования</span><span class="sxs-lookup"><span data-stu-id="fa87f-145">Requirements</span></span>



| <span data-ttu-id="fa87f-146">Требование</span><span class="sxs-lookup"><span data-stu-id="fa87f-146">Requirement</span></span> | <span data-ttu-id="fa87f-147">Значение</span><span class="sxs-lookup"><span data-stu-id="fa87f-147">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa87f-148">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fa87f-148">Minimum supported client</span></span><br/> | <span data-ttu-id="fa87f-149">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fa87f-149">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="fa87f-150">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fa87f-150">Minimum supported server</span></span><br/> | <span data-ttu-id="fa87f-151">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fa87f-151">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="fa87f-152">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="fa87f-152">Namespace</span></span><br/>                | <span data-ttu-id="fa87f-153">Корневой \\ CIMV2 \\ безопасности \\ микрософттпм</span><span class="sxs-lookup"><span data-stu-id="fa87f-153">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="fa87f-154">MOF</span><span class="sxs-lookup"><span data-stu-id="fa87f-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fa87f-155"><dt>Win32 \_ TPM. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fa87f-155"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="fa87f-156">DLL</span><span class="sxs-lookup"><span data-stu-id="fa87f-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa87f-157"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="fa87f-157"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa87f-158">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fa87f-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa87f-159">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="fa87f-159">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
