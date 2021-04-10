---
description: Изменяет значение авторизации владельца доверенного платформенного модуля.
ms.assetid: ed280037-2360-4889-baba-cfa9e4fd473e
title: Метод Чанжеовнераус класса Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.ChangeOwnerAuth
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: fc4b044d58dcaca5364f0ba669b09030cf3b34dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144416"
---
# <a name="changeownerauth-method-of-the-win32_tpm-class"></a><span data-ttu-id="ca312-103">Метод Чанжеовнераус \_ класса TPM Win32</span><span class="sxs-lookup"><span data-stu-id="ca312-103">ChangeOwnerAuth method of the Win32\_Tpm class</span></span>

<span data-ttu-id="ca312-104">Метод **чанжеовнераус** класса [**\_ TPM Win32**](win32-tpm.md) изменяет значение авторизации владельца доверенного платформенного модуля.</span><span class="sxs-lookup"><span data-stu-id="ca312-104">The **ChangeOwnerAuth** method of the [**Win32\_Tpm**](win32-tpm.md) class changes the TPM owner authorization value.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca312-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ca312-105">Syntax</span></span>


```mof
uint32 ChangeOwnerAuth(
  [in, optional] string OldOwnerAuth,
  [in, optional] string NewOwnerAuth
);
```



## <a name="parameters"></a><span data-ttu-id="ca312-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ca312-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca312-107">*Олдовнераус* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="ca312-107">*OldOwnerAuth* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ca312-108">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="ca312-108">Type: **string**</span></span>

<span data-ttu-id="ca312-109">Строка, которая присваивает имя текущему значению авторизации владельца доверенного платформенного модуля для устройства.</span><span class="sxs-lookup"><span data-stu-id="ca312-109">A string that names the current TPM owner authorization value of the device.</span></span> <span data-ttu-id="ca312-110">Используйте метод [**конверттувнераус**](converttoownerauth-win32-tpm.md) , чтобы преобразовать пароль в это значение авторизации.</span><span class="sxs-lookup"><span data-stu-id="ca312-110">Use the [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) method to translate a password to this authorization value.</span></span> <span data-ttu-id="ca312-111">Параметр *олдовнераус* не указан, или указана пустая строка, этот метод получает значение из реестра, если оно есть.</span><span class="sxs-lookup"><span data-stu-id="ca312-111">The *OldOwnerAuth* parameter is not supplied or an empty string is provided, this method gets the value from the registry if present.</span></span>

</dd> <dt>

<span data-ttu-id="ca312-112">*Невовнераус* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="ca312-112">*NewOwnerAuth* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ca312-113">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="ca312-113">Type: **string**</span></span>

<span data-ttu-id="ca312-114">Строка, которая присваивает имя новому значению авторизации владельца доверенного платформенного модуля.</span><span class="sxs-lookup"><span data-stu-id="ca312-114">A string that names the new TPM owner authorization value.</span></span> <span data-ttu-id="ca312-115">Используйте метод [**конверттувнераус**](converttoownerauth-win32-tpm.md) , чтобы преобразовать пароль в это значение авторизации.</span><span class="sxs-lookup"><span data-stu-id="ca312-115">Use the [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) method to translate a password to this authorization value.</span></span> <span data-ttu-id="ca312-116">Параметр *невовнераус* не может быть пустым или иметь **значение null.**</span><span class="sxs-lookup"><span data-stu-id="ca312-116">The *NewOwnerAuth* parameter cannot be empty or **NULL.**</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca312-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ca312-117">Return value</span></span>

<span data-ttu-id="ca312-118">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ca312-118">Type: **uint32**</span></span>

<span data-ttu-id="ca312-119">Могут возвращаться все ошибки доверенного платформенного модуля, а также ошибки, относящиеся к базовым службам TPM.</span><span class="sxs-lookup"><span data-stu-id="ca312-119">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="ca312-120">В следующей таблице перечислены некоторые распространенные коды возврата.</span><span class="sxs-lookup"><span data-stu-id="ca312-120">The following table lists some of the common return codes.</span></span>



| <span data-ttu-id="ca312-121">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="ca312-121">Return code/value</span></span>                                                                                                                                                                              | <span data-ttu-id="ca312-122">Описание</span><span class="sxs-lookup"><span data-stu-id="ca312-122">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ca312-123"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="ca312-123"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                              | <span data-ttu-id="ca312-124">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="ca312-124">The method was successful.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="ca312-125"><dt>**Доверенный платформенный модуль \_ E \_ аусфаил**</dt> <dt>2150105089 (0x80280001)</dt></span><span class="sxs-lookup"><span data-stu-id="ca312-125"><dt>**TPM\_E\_AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt></span></span> </dl>                   | <span data-ttu-id="ca312-126">Текущее значение авторизации владельца доверенного платформенного модуля неверно.</span><span class="sxs-lookup"><span data-stu-id="ca312-126">The current TPM owner authorization value is incorrect.</span></span><br/>                                                                                                                                                                                                                                                                                                                               |
| <dl> <span data-ttu-id="ca312-127"><dt>**Доверенный платформенный модуль \_ \_Блокировка защиты \_ от \_ перезапуска**</dt> <dt>2150107139 (0x80280803)</dt></span><span class="sxs-lookup"><span data-stu-id="ca312-127"><dt>**TPM\_E\_DEFEND\_LOCK\_RUNNING**</dt> <dt>2150107139 (0x80280803)</dt></span></span> </dl>      | <span data-ttu-id="ca312-128">TPM защищается от атак из словарей и находится в течение времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="ca312-128">The TPM is defending against dictionary attacks and is in a time-out period.</span></span> <span data-ttu-id="ca312-129">Дополнительные сведения см. в описании метода [**ресетауслоккаут**](resetauthlockout-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="ca312-129">For more information, see the [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) method.</span></span><br/>                                                                                                                                                                                                             |
| <dl> <span data-ttu-id="ca312-130"><dt>**ФВЕ \_ \_Схема E \_ AD \_ не \_ установлена**</dt> <dt>2150694922 (0x8031000A)</dt></span><span class="sxs-lookup"><span data-stu-id="ca312-130"><dt>**FVE\_E\_AD\_SCHEMA\_NOT\_INSTALLED**</dt> <dt>2150694922 (0x8031000A)</dt></span></span> </dl> | <span data-ttu-id="ca312-131">Не удается сохранить сведения о восстановлении в сети.</span><span class="sxs-lookup"><span data-stu-id="ca312-131">Cannot save recovery information to the network.</span></span> <span data-ttu-id="ca312-132">На компьютере настроено хранение сведений о восстановлении в домен Active Directory Services.</span><span class="sxs-lookup"><span data-stu-id="ca312-132">The computer has been configured to store recovery information to Active Directory Domain Services.</span></span> <span data-ttu-id="ca312-133">Инструкции по настройке Active Directory см. в разделе [руководство по настройке шифрование диска BitLocker: резервное копирование BitLocker и сведений о восстановлении TPM в Active Directory](/previous-versions/windows/it-pro/windows-vista/cc766015(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="ca312-133">For instructions on how to set up Active Directory, see [BitLocker Drive Encryption Configuration Guide: Backing Up BitLocker and TPM Recovery Information to Active Directory](/previous-versions/windows/it-pro/windows-vista/cc766015(v=ws.10)).</span></span><br/> |
| <dl> <span data-ttu-id="ca312-134"><dt>**Сбой подключения**</dt> <dt>2147943755 (0x8007054B)</dt></span><span class="sxs-lookup"><span data-stu-id="ca312-134"><dt>**Connection Failed**</dt> <dt>2147943755 (0x8007054B)</dt></span></span> </dl>                  | <span data-ttu-id="ca312-135">Не удается сохранить сведения о восстановлении в сети.</span><span class="sxs-lookup"><span data-stu-id="ca312-135">Cannot save recovery information to the network.</span></span> <span data-ttu-id="ca312-136">На компьютере настроено хранение сведений о восстановлении в домен Active Directory Services.</span><span class="sxs-lookup"><span data-stu-id="ca312-136">The computer has been configured to store recovery information to Active Directory Domain Services.</span></span> <span data-ttu-id="ca312-137">Для продолжения требуется сетевое подключение.</span><span class="sxs-lookup"><span data-stu-id="ca312-137">A network connection is required to continue.</span></span><br/>                                                                                                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="ca312-138">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ca312-138">Remarks</span></span>

<span data-ttu-id="ca312-139">Метод **чанжеовнераус** создает резервную копию новой авторизации владельца доверенного платформенного модуля для домен Active Directory служб, если настроены соответствующие параметры групповая политика.</span><span class="sxs-lookup"><span data-stu-id="ca312-139">The **ChangeOwnerAuth** method backs up the new TPM owner authorization to Active Directory Domain Services if the appropriate Group Policy settings have been configured.</span></span>

<span data-ttu-id="ca312-140">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="ca312-140">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="ca312-141">MOF-файлы не устанавливаются в составе Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="ca312-141">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="ca312-142">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="ca312-142">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="ca312-143">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="ca312-143">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ca312-144">Требования</span><span class="sxs-lookup"><span data-stu-id="ca312-144">Requirements</span></span>



| <span data-ttu-id="ca312-145">Требование</span><span class="sxs-lookup"><span data-stu-id="ca312-145">Requirement</span></span> | <span data-ttu-id="ca312-146">Значение</span><span class="sxs-lookup"><span data-stu-id="ca312-146">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca312-147">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ca312-147">Minimum supported client</span></span><br/> | <span data-ttu-id="ca312-148">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ca312-148">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="ca312-149">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ca312-149">Minimum supported server</span></span><br/> | <span data-ttu-id="ca312-150">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ca312-150">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="ca312-151">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ca312-151">Namespace</span></span><br/>                | <span data-ttu-id="ca312-152">Корневой \\ CIMV2 \\ безопасности \\ микрософттпм</span><span class="sxs-lookup"><span data-stu-id="ca312-152">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="ca312-153">MOF</span><span class="sxs-lookup"><span data-stu-id="ca312-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ca312-154"><dt>Win32 \_ TPM. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ca312-154"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="ca312-155">DLL</span><span class="sxs-lookup"><span data-stu-id="ca312-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ca312-156"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="ca312-156"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca312-157">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ca312-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca312-158">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="ca312-158">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
