---
description: Преобразует введенную пользователем парольную фразу в 20-байтную авторизацию владельца, которая может использоваться для взаимодействия с доверенным платформенным модулем. Для таких методов, как Такеовнершип и Ресетауслоккаут, требуется значение авторизации, полученное владельцем.
ms.assetid: 69eed934-1668-495a-b5b7-cd4a87df1ab3
title: Метод Конверттувнераус класса Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.ConvertToOwnerAuth
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: f3de5803d10458156fb453e964d782f7c9760333
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683806"
---
# <a name="converttoownerauth-method-of-the-win32_tpm-class"></a><span data-ttu-id="527cc-104">Метод Конверттувнераус \_ класса TPM Win32</span><span class="sxs-lookup"><span data-stu-id="527cc-104">ConvertToOwnerAuth method of the Win32\_Tpm class</span></span>

<span data-ttu-id="527cc-105">Метод **конверттувнераус** класса [**\_ TPM Win32**](win32-tpm.md) преобразует предоставленный пользователем ввод парольной фразы в 20-байтную авторизацию владельца, которая может использоваться для взаимодействия с доверенным платформенным модулем.</span><span class="sxs-lookup"><span data-stu-id="527cc-105">The **ConvertToOwnerAuth** method of the [**Win32\_Tpm**](win32-tpm.md) class translates a user-provided passphrase input into a 20-byte owner authorization that can be used to interact with the TPM.</span></span> <span data-ttu-id="527cc-106">Для таких методов, как [**такеовнершип**](takeownership-win32-tpm.md) и [**ресетауслоккаут**](resetauthlockout-win32-tpm.md) , требуется значение авторизации, полученное владельцем.</span><span class="sxs-lookup"><span data-stu-id="527cc-106">Methods such as [**TakeOwnership**](takeownership-win32-tpm.md) and [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) require the resulting owner authorization value.</span></span>

<span data-ttu-id="527cc-107">Процесс преобразования соответствует спецификациям из [Организация TCG](https://www.trustedcomputinggroup.org/).</span><span class="sxs-lookup"><span data-stu-id="527cc-107">The conversion process follows the specifications from the [Trusted Computing Group](https://www.trustedcomputinggroup.org/).</span></span>

## <a name="syntax"></a><span data-ttu-id="527cc-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="527cc-108">Syntax</span></span>


```mof
uint32 ConvertToOwnerAuth(
  [in]  string OwnerPassPhrase,
  [out] string OwnerAuth
);
```



## <a name="parameters"></a><span data-ttu-id="527cc-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="527cc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="527cc-110">*Овнерпассфрасе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="527cc-110">*OwnerPassPhrase* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="527cc-111">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="527cc-111">Type: **string**</span></span>

<span data-ttu-id="527cc-112">Строка для преобразования в значение авторизации владельца.</span><span class="sxs-lookup"><span data-stu-id="527cc-112">A string to convert to an owner authorization value.</span></span> <span data-ttu-id="527cc-113">Строка может содержать любое количество буквенно-цифровых символов.</span><span class="sxs-lookup"><span data-stu-id="527cc-113">The string can contain any number of alphanumeric characters.</span></span>

</dd> <dt>

<span data-ttu-id="527cc-114">*Овнераус* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="527cc-114">*OwnerAuth* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="527cc-115">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="527cc-115">Type: **string**</span></span>

<span data-ttu-id="527cc-116">Строка, производная от параметра *овнерпассфрасе* .</span><span class="sxs-lookup"><span data-stu-id="527cc-116">A string derived from the *OwnerPassPhrase* parameter.</span></span> <span data-ttu-id="527cc-117">Это значение является 20-байтовым двоичным значением, закодированным в 28-байтовую строку в кодировке **Base64, завершающуюся нулем.**</span><span class="sxs-lookup"><span data-stu-id="527cc-117">This value is a 20-byte binary value encoded to a 28-byte base64 **null**-terminated string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="527cc-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="527cc-118">Return value</span></span>

<span data-ttu-id="527cc-119">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="527cc-119">Type: **uint32**</span></span>

<span data-ttu-id="527cc-120">Могут возвращаться все ошибки доверенного платформенного модуля, а также ошибки, относящиеся к базовым службам TPM.</span><span class="sxs-lookup"><span data-stu-id="527cc-120">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="527cc-121">В следующих таблицах перечислены некоторые распространенные коды возврата.</span><span class="sxs-lookup"><span data-stu-id="527cc-121">The following tables lists some of the common return codes.</span></span>



| <span data-ttu-id="527cc-122">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="527cc-122">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="527cc-123">Описание</span><span class="sxs-lookup"><span data-stu-id="527cc-123">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="527cc-124"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="527cc-124"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="527cc-125">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="527cc-125">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="527cc-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="527cc-126">Remarks</span></span>

<span data-ttu-id="527cc-127">Строка в кодировке Юникод UTF-16LE преобразуется в значение авторизации владельца доверенного платформенного модуля размером 20 байт, принимая хэш SHA-1 двоичного представления строки.</span><span class="sxs-lookup"><span data-stu-id="527cc-127">A Unicode UTF-16LE encoded string is converted to the 20-byte TPM owner authorization value by taking the SHA-1 hash of the string's binary representation.</span></span> <span data-ttu-id="527cc-128">**Нулевое** завершение строки Юникода не включено в хэш.</span><span class="sxs-lookup"><span data-stu-id="527cc-128">The **null** termination of the Unicode string is not included in the hash.</span></span> <span data-ttu-id="527cc-129">В хэш SHA-1 не используется соль.</span><span class="sxs-lookup"><span data-stu-id="527cc-129">No salt is used in the SHA-1 hash.</span></span>

<span data-ttu-id="527cc-130">Например, чтобы преобразовать парольную фразу владельца TPM "1Sample" в значение авторизации владельца доверенного платформенного модуля, хэш SHA-1 берется из следующего байтового потока:</span><span class="sxs-lookup"><span data-stu-id="527cc-130">For example, to convert the TPM owner passphrase "1Sample" to a TPM owner authorization value, the SHA-1 hash is taken from the following byte stream:</span></span>

`0x31 0x00 0x53 0x00 0x61 0x00 0x6D 0x00 0x70 0x00 0x6C 0x00 0x65 0x00`

<span data-ttu-id="527cc-131">Чтобы преобразовать парольную фразу нулевой длины в значение авторизации владельца, хэш SHA-1 берется из потока байтов **null** .</span><span class="sxs-lookup"><span data-stu-id="527cc-131">To convert a zero-length passphrase to an owner authorization value, the SHA-1 hash is taken of the **NULL** byte stream.</span></span>

<span data-ttu-id="527cc-132">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="527cc-132">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="527cc-133">MOF-файлы не устанавливаются в составе Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="527cc-133">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="527cc-134">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="527cc-134">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="527cc-135">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="527cc-135">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="527cc-136">Требования</span><span class="sxs-lookup"><span data-stu-id="527cc-136">Requirements</span></span>



| <span data-ttu-id="527cc-137">Требование</span><span class="sxs-lookup"><span data-stu-id="527cc-137">Requirement</span></span> | <span data-ttu-id="527cc-138">Значение</span><span class="sxs-lookup"><span data-stu-id="527cc-138">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="527cc-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="527cc-139">Minimum supported client</span></span><br/> | <span data-ttu-id="527cc-140">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="527cc-140">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="527cc-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="527cc-141">Minimum supported server</span></span><br/> | <span data-ttu-id="527cc-142">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="527cc-142">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="527cc-143">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="527cc-143">Namespace</span></span><br/>                | <span data-ttu-id="527cc-144">Корневой \\ CIMV2 \\ безопасности \\ микрософттпм</span><span class="sxs-lookup"><span data-stu-id="527cc-144">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="527cc-145">MOF</span><span class="sxs-lookup"><span data-stu-id="527cc-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="527cc-146"><dt>Win32 \_ TPM. mof</dt></span><span class="sxs-lookup"><span data-stu-id="527cc-146"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="527cc-147">DLL</span><span class="sxs-lookup"><span data-stu-id="527cc-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="527cc-148"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="527cc-148"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="527cc-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="527cc-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="527cc-150">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="527cc-150">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="527cc-151">**TakeOwnership**</span><span class="sxs-lookup"><span data-stu-id="527cc-151">**TakeOwnership**</span></span>](takeownership-win32-tpm.md)
</dt> </dl>

 

 
