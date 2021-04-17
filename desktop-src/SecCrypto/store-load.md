---
description: Импортирует сертификаты из файла в хранилище.
ms.assetid: 884326b4-77ca-43d4-bda9-127d823ce9bc
title: Метод Store. Load
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Load
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 32261a6fd8c5cf4382832d8286d63ce5d44fb542
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669507"
---
# <a name="storeload-method"></a><span data-ttu-id="efcc2-103">Метод Store. Load</span><span class="sxs-lookup"><span data-stu-id="efcc2-103">Store.Load method</span></span>

<span data-ttu-id="efcc2-104">\[Метод **Load** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="efcc2-104">\[The **Load** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="efcc2-105">Вместо этого используйте [**класс X509Store**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="efcc2-105">Instead, use the [**X509Store Class**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="efcc2-106">Метод **Load** импортирует сертификаты из файла в хранилище.</span><span class="sxs-lookup"><span data-stu-id="efcc2-106">The **Load** method imports certificates from a file into the store.</span></span>

## <a name="syntax"></a><span data-ttu-id="efcc2-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="efcc2-107">Syntax</span></span>


```VB
Store.Load( _
  ByVal FileName, _
  [ ByVal Password ], _
  [ ByVal KeyStorageFlag ] _
)
```



## <a name="parameters"></a><span data-ttu-id="efcc2-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="efcc2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="efcc2-109">*Имя файла* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="efcc2-109">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="efcc2-110">Строка, содержащая путь к файлу. cer,. SST,. SPC,. P7S или. pfx или любому файлу, подписанному с помощью Authenticode.</span><span class="sxs-lookup"><span data-stu-id="efcc2-110">The string that contains the path to a .cer, .sst, .spc, .p7s, or .pfx file, or any Authenticode signed file.</span></span>

</dd> <dt>

<span data-ttu-id="efcc2-111">*Пароль* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="efcc2-111">*Password* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="efcc2-112">Строка, содержащая пароль в виде открытого текста для файла.</span><span class="sxs-lookup"><span data-stu-id="efcc2-112">The string that contains the plaintext password to the file.</span></span> <span data-ttu-id="efcc2-113">Для пароля можно использовать до 32 символов Юникода, включая завершающий нуль-символ.</span><span class="sxs-lookup"><span data-stu-id="efcc2-113">Up to 32 Unicode characters, including a terminating null character, can be used for the password.</span></span> <span data-ttu-id="efcc2-114">Сведения о защите пароля см. в разделе [обработка паролей](../secbp/handling-passwords.md).</span><span class="sxs-lookup"><span data-stu-id="efcc2-114">For information about protecting the password, see [Handling Passwords](../secbp/handling-passwords.md).</span></span>

</dd> <dt>

<span data-ttu-id="efcc2-115">*Кэйсторажефлаг* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="efcc2-115">*KeyStorageFlag* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="efcc2-116">Значение перечисления [**\_ \_ \_ флагов хранилища CAPICOM Key**](capicom-key-storage-flag.md) , определяющее флаги хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="efcc2-116">A value of the [**CAPICOM\_KEY\_STORAGE\_FLAG**](capicom-key-storage-flag.md) enumeration that defines key storage flags.</span></span> <span data-ttu-id="efcc2-117">По умолчанию используется \_ хранилище CAPICOM key \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="efcc2-117">The default is CAPICOM\_KEY\_STORAGE\_DEFAULT.</span></span> <span data-ttu-id="efcc2-118">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="efcc2-118">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="efcc2-119">Значение</span><span class="sxs-lookup"><span data-stu-id="efcc2-119">Value</span></span>                                                                                                                                                                                                                           | <span data-ttu-id="efcc2-120">Значение</span><span class="sxs-lookup"><span data-stu-id="efcc2-120">Meaning</span></span>                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span id="CAPICOM_KEY_STORAGE_DEFAULT"></span><span id="capicom_key_storage_default"></span><dl> <span data-ttu-id="efcc2-121"><dt>**\_хранилище CAPICOM \_ key \_ по умолчанию**</dt></span><span class="sxs-lookup"><span data-stu-id="efcc2-121"><dt>**CAPICOM\_KEY\_STORAGE\_DEFAULT**</dt></span></span> </dl>                       | <span data-ttu-id="efcc2-122">Хранилище ключей по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="efcc2-122">Default key storage.</span></span><br/>       |
| <span id="CAPICOM_KEY_STORAGE_EXPORTABLE"></span><span id="capicom_key_storage_exportable"></span><dl> <span data-ttu-id="efcc2-123"><dt>**\_хранилище CAPICOM Key, \_ \_ экспортируемое**</dt></span><span class="sxs-lookup"><span data-stu-id="efcc2-123"><dt>**CAPICOM\_KEY\_STORAGE\_EXPORTABLE**</dt></span></span> </dl>              | <span data-ttu-id="efcc2-124">Ключ доступен для экспорта.</span><span class="sxs-lookup"><span data-stu-id="efcc2-124">The key is exportable.</span></span><br/>     |
| <span id="CAPICOM_KEY_STORAGE_USER_PROTECTED"></span><span id="capicom_key_storage_user_protected"></span><dl> <span data-ttu-id="efcc2-125"><dt>**\_ \_ \_ защищенное пользователем хранилище CAPICOM key \_**</dt></span><span class="sxs-lookup"><span data-stu-id="efcc2-125"><dt>**CAPICOM\_KEY\_STORAGE\_USER\_PROTECTED**</dt></span></span> </dl> | <span data-ttu-id="efcc2-126">Ключ защищен пользователем.</span><span class="sxs-lookup"><span data-stu-id="efcc2-126">The key is user protected.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="efcc2-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="efcc2-127">Return value</span></span>

<span data-ttu-id="efcc2-128">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="efcc2-128">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="efcc2-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="efcc2-129">Remarks</span></span>

<span data-ttu-id="efcc2-130">Если метод **Load** вызывается в хранилище памяти, все создаваемые контейнеры ключей будут удалены при удалении хранилища памяти.</span><span class="sxs-lookup"><span data-stu-id="efcc2-130">If the **Load** method is called on a memory store, any key containers that are created will be deleted when the memory store is deleted.</span></span> <span data-ttu-id="efcc2-131">Например, если PFX-файл загружается в хранилище памяти и позднее добавляется в системное хранилище (например, в хранилище My) из хранилища памяти, то сертификат в хранилище My не будет содержать ключ.</span><span class="sxs-lookup"><span data-stu-id="efcc2-131">For example, if a .pfx file is loaded into a memory store and later added to a system store (such as the My store) from the memory store, the certificate in the My store will not contain a key.</span></span> <span data-ttu-id="efcc2-132">В этом случае PFX-файл должен быть загружен непосредственно в хранилище My.</span><span class="sxs-lookup"><span data-stu-id="efcc2-132">In this case, the .pfx file should be loaded directly into the My store.</span></span>

<span data-ttu-id="efcc2-133">Этот метод вызывает CAPICOM \_ E \_ не \_ разрешен при создании скрипта из веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="efcc2-133">This method raises CAPICOM\_E\_NOT\_ALLOWED when it is scripted from a web-based application.</span></span>

<span data-ttu-id="efcc2-134">Если не удалось расшифровать файл закрытого ключа паролем, то необходимо запросить [*поставщик служб шифрования*](../secgloss/c-gly.md) (CSP) по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="efcc2-134">If the password fails to decrypt the private key file, then the default [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) should be queried.</span></span> <span data-ttu-id="efcc2-135">Если CSP по умолчанию является базовым поставщиком служб шифрования Майкрософт и операция расшифровки завершается неудачно, то операцию расшифровки следует повторить с помощью строгого поставщика служб шифрования (Майкрософт) или поставщика Microsoft Enhanced Cryptographic, в зависимости от того, какая из них доступна.</span><span class="sxs-lookup"><span data-stu-id="efcc2-135">If the default CSP is the Microsoft Base Cryptographic Provider and the decrypt operation fails, then the decrypt operation should be tried again with the Microsoft Strong Cryptographic Provider or Microsoft Enhanced Cryptographic Provider, whichever is available.</span></span>

<span data-ttu-id="efcc2-136">Если сертификат, загружаемый в хранилище, совпадает с тем, который уже есть, метод **Load** удалит существующий сертификат из хранилища, а затем добавит новый сертификат.</span><span class="sxs-lookup"><span data-stu-id="efcc2-136">If the certificate being loaded into the store is the same as one that is already there, the **Load** method will delete the existing certificate from the store and then add the new certificate.</span></span> <span data-ttu-id="efcc2-137">Новый сертификат будет наследовать свойства от существующего сертификата.</span><span class="sxs-lookup"><span data-stu-id="efcc2-137">The new certificate will inherit properties from the existing certificate.</span></span> <span data-ttu-id="efcc2-138">Существующий контейнер закрытых ключей заменяется новым контейнером закрытого ключа.</span><span class="sxs-lookup"><span data-stu-id="efcc2-138">The existing private key container is replaced by the new private key container.</span></span>

## <a name="requirements"></a><span data-ttu-id="efcc2-139">Требования</span><span class="sxs-lookup"><span data-stu-id="efcc2-139">Requirements</span></span>



| <span data-ttu-id="efcc2-140">Требование</span><span class="sxs-lookup"><span data-stu-id="efcc2-140">Requirement</span></span> | <span data-ttu-id="efcc2-141">Значение</span><span class="sxs-lookup"><span data-stu-id="efcc2-141">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="efcc2-142">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="efcc2-142">Redistributable</span></span><br/> | <span data-ttu-id="efcc2-143">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="efcc2-143">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="efcc2-144">DLL</span><span class="sxs-lookup"><span data-stu-id="efcc2-144">DLL</span></span><br/>             | <dl> <span data-ttu-id="efcc2-145"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="efcc2-145"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="efcc2-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="efcc2-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efcc2-147">**Магазин**</span><span class="sxs-lookup"><span data-stu-id="efcc2-147">**Store**</span></span>](store.md)
</dt> </dl>

 

 
