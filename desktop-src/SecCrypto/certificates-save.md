---
description: Сохраняет объекты сертификата в коллекции.
ms.assetid: 1d4b7bd5-3ed3-4ace-9894-4e89c5cf844f
title: Метод Certificates. Save
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Save
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 36ab04b394bddcd829d9f15e7562b72125388d33
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669365"
---
# <a name="certificatessave-method"></a><span data-ttu-id="cf731-103">Метод Certificates. Save</span><span class="sxs-lookup"><span data-stu-id="cf731-103">Certificates.Save method</span></span>

<span data-ttu-id="cf731-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="cf731-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="cf731-105">Вместо этого используйте [**класс X509Certificate2Collection**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="cf731-105">Instead, use the [**X509Certificate2Collection Class**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="cf731-106">Метод **Save** сохраняет объекты [**сертификата**](certificate.md) в коллекции.</span><span class="sxs-lookup"><span data-stu-id="cf731-106">The **Save** method saves the [**Certificate**](certificate.md) objects in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf731-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cf731-107">Syntax</span></span>


```VB
Certificates.Save( _
  ByVal FileName, _
  [ ByVal Password ], _
  [ ByVal SaveAs ], _
  [ ByVal ExportFlag ] _
)
```



## <a name="parameters"></a><span data-ttu-id="cf731-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="cf731-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf731-109">*Имя файла* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cf731-109">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf731-110">Строка, содержащая имя выходного файла, в котором будут сохранены сертификаты.</span><span class="sxs-lookup"><span data-stu-id="cf731-110">A string that contains the name of the output file where the certificates will be saved.</span></span>

</dd> <dt>

<span data-ttu-id="cf731-111">*Пароль* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="cf731-111">*Password* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cf731-112">Строка, содержащая пароль в [*виде открытого текста*](../secgloss/p-gly.md) для файла [*закрытого ключа*](../secgloss/p-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="cf731-112">A string that contains the [*plaintext*](../secgloss/p-gly.md) password for a [*private key*](../secgloss/p-gly.md) file.</span></span> <span data-ttu-id="cf731-113">Значением по умолчанию является пустая строка ("").</span><span class="sxs-lookup"><span data-stu-id="cf731-113">The default value is the empty string ("").</span></span> <span data-ttu-id="cf731-114">Для пароля можно использовать до 32 символов Юникода, включая завершающий нуль-символ.</span><span class="sxs-lookup"><span data-stu-id="cf731-114">Up to 32 Unicode characters, including a terminating null character, can be used for the password.</span></span> <span data-ttu-id="cf731-115">Сведения о защите пароля см. в разделе [обработка паролей](../secbp/handling-passwords.md).</span><span class="sxs-lookup"><span data-stu-id="cf731-115">For information about protecting the password, see [Handling Passwords](../secbp/handling-passwords.md).</span></span>

</dd> <dt>

<span data-ttu-id="cf731-116">*Сохранить* \[ как в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="cf731-116">*SaveAs* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cf731-117">Значение перечисления [**CAPICOM \_ Certificates \_ Сохранить \_ как \_ тип**](capicom-certificates-save-as-type.md) , определяющее формат выходного файла.</span><span class="sxs-lookup"><span data-stu-id="cf731-117">A value of the [**CAPICOM\_CERTIFICATES\_SAVE\_AS\_TYPE**](capicom-certificates-save-as-type.md) enumeration that specifies the format of the output file.</span></span> <span data-ttu-id="cf731-118">По умолчанию CAPICOM \_ Certificates \_ сохраняется \_ как \_ PFX.</span><span class="sxs-lookup"><span data-stu-id="cf731-118">The default is CAPICOM\_CERTIFICATES\_SAVE\_AS\_PFX.</span></span> <span data-ttu-id="cf731-119">В следующей таблице приводятся возможные значения.</span><span class="sxs-lookup"><span data-stu-id="cf731-119">The following table shows the possible values.</span></span>



| <span data-ttu-id="cf731-120">Значение</span><span class="sxs-lookup"><span data-stu-id="cf731-120">Value</span></span>                                                                                                                                                                                                                                          | <span data-ttu-id="cf731-121">Значение</span><span class="sxs-lookup"><span data-stu-id="cf731-121">Meaning</span></span>                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span id="CAPICOM_CERTIFICATES_SAVE_AS_PFX"></span><span id="capicom_certificates_save_as_pfx"></span><dl> <span data-ttu-id="cf731-122"><dt>**CAPICOM \_ Certificates \_ Сохранить \_ как \_ PFX**</dt></span><span class="sxs-lookup"><span data-stu-id="cf731-122"><dt>**CAPICOM\_CERTIFICATES\_SAVE\_AS\_PFX**</dt></span></span> </dl>                      | <span data-ttu-id="cf731-123">Сертификаты сохраняются в формате PFX.</span><span class="sxs-lookup"><span data-stu-id="cf731-123">The certificates are saved as a PFX.</span></span><br/>      |
| <span id="CAPICOM_CERTIFICATES_SAVE_AS_PKCS7"></span><span id="capicom_certificates_save_as_pkcs7"></span><dl> <span data-ttu-id="cf731-124"><dt>**CAPICOM \_ Certificates \_ Сохранить \_ как \_ PKCS7**</dt></span><span class="sxs-lookup"><span data-stu-id="cf731-124"><dt>**CAPICOM\_CERTIFICATES\_SAVE\_AS\_PKCS7**</dt></span></span> </dl>                | <span data-ttu-id="cf731-125">Сертификаты сохраняются в виде PKCS \# 7.</span><span class="sxs-lookup"><span data-stu-id="cf731-125">The certificates are saved as a PKCS \#7.</span></span><br/> |
| <span id="CAPICOM_CERTIFICATES_SAVE_AS_SERIALIZED"></span><span id="capicom_certificates_save_as_serialized"></span><dl> <span data-ttu-id="cf731-126"><dt>**CAPICOM \_ Certificates \_ Сохранить \_ как \_ сериализованный**</dt></span><span class="sxs-lookup"><span data-stu-id="cf731-126"><dt>**CAPICOM\_CERTIFICATES\_SAVE\_AS\_SERIALIZED**</dt></span></span> </dl> | <span data-ttu-id="cf731-127">Сертификаты сохраняются как сериализованные.</span><span class="sxs-lookup"><span data-stu-id="cf731-127">The certificates are saved as serialized.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="cf731-128">*Експортфлаг* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="cf731-128">*ExportFlag* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cf731-129">Значение перечисления [**\_ \_ флагов CAPICOM Export**](capicom-export-flag.md) , которое указывает, пропускаются ли ошибки экспорта закрытого ключа.</span><span class="sxs-lookup"><span data-stu-id="cf731-129">A value of the [**CAPICOM\_EXPORT\_FLAG**](capicom-export-flag.md) enumeration that specifies whether any private key export errors are ignored.</span></span> <span data-ttu-id="cf731-130">Значение по умолчанию — \_ Экспорт \_ по умолчанию CAPICOM.</span><span class="sxs-lookup"><span data-stu-id="cf731-130">The default is CAPICOM\_EXPORT\_DEFAULT.</span></span> <span data-ttu-id="cf731-131">В следующей таблице приводятся возможные значения.</span><span class="sxs-lookup"><span data-stu-id="cf731-131">The following table shows the possible values.</span></span>



| <span data-ttu-id="cf731-132">Значение</span><span class="sxs-lookup"><span data-stu-id="cf731-132">Value</span></span>                                                                                                                                                                                                                                                                                          | <span data-ttu-id="cf731-133">Значение</span><span class="sxs-lookup"><span data-stu-id="cf731-133">Meaning</span></span>                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span id="CAPICOM_EXPORT_DEFAULT"></span><span id="capicom_export_default"></span><dl> <span data-ttu-id="cf731-134"><dt>**\_ \_ по умолчанию для экспорта CAPICOM**</dt></span><span class="sxs-lookup"><span data-stu-id="cf731-134"><dt>**CAPICOM\_EXPORT\_DEFAULT**</dt></span></span> </dl>                                                                                                      | <span data-ttu-id="cf731-135">Ошибки экспорта закрытого ключа не пропускаются.</span><span class="sxs-lookup"><span data-stu-id="cf731-135">Private key export errors are not ignored.</span></span><br/> |
| <span id="CAPICOM_EXPORT_IGNORE_PRIVATE_KEY_NOT_EXPORTABLE_ERROR"></span><span id="capicom_export_ignore_private_key_not_exportable_error"></span><dl> <span data-ttu-id="cf731-136"><dt>**CAPICOM \_ Export \_ игнорировать \_ ошибку закрытого \_ ключа \_ без \_ экспорта \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cf731-136"><dt>**CAPICOM\_EXPORT\_IGNORE\_PRIVATE\_KEY\_NOT\_EXPORTABLE\_ERROR**</dt></span></span> </dl> | <span data-ttu-id="cf731-137">Ошибки экспорта закрытого ключа игнорируются.</span><span class="sxs-lookup"><span data-stu-id="cf731-137">Private key export errors are ignored.</span></span><br/>     |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf731-138">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cf731-138">Return value</span></span>

<span data-ttu-id="cf731-139">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="cf731-139">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf731-140">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cf731-140">Remarks</span></span>

<span data-ttu-id="cf731-141">Этот метод вызывает CAPICOM \_ E \_ не \_ разрешен при создании скрипта из веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="cf731-141">This method raises CAPICOM\_E\_NOT\_ALLOWED when it is scripted from a web-based application.</span></span>

<span data-ttu-id="cf731-142">Объекты [**сертификата**](certificate.md) можно получить с помощью метода [**Store. Load**](store-load.md) .</span><span class="sxs-lookup"><span data-stu-id="cf731-142">The [**Certificate**](certificate.md) objects can be retrieved by using the [**Store.Load**](store-load.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf731-143">Требования</span><span class="sxs-lookup"><span data-stu-id="cf731-143">Requirements</span></span>



| <span data-ttu-id="cf731-144">Требование</span><span class="sxs-lookup"><span data-stu-id="cf731-144">Requirement</span></span> | <span data-ttu-id="cf731-145">Значение</span><span class="sxs-lookup"><span data-stu-id="cf731-145">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cf731-146">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="cf731-146">End of client support</span></span><br/> | <span data-ttu-id="cf731-147">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cf731-147">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="cf731-148">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="cf731-148">End of server support</span></span><br/> | <span data-ttu-id="cf731-149">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cf731-149">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="cf731-150">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="cf731-150">Redistributable</span></span><br/>       | <span data-ttu-id="cf731-151">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="cf731-151">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="cf731-152">DLL</span><span class="sxs-lookup"><span data-stu-id="cf731-152">DLL</span></span><br/>                   | <dl> <span data-ttu-id="cf731-153"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf731-153"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf731-154">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cf731-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf731-155">**Сертификаты**</span><span class="sxs-lookup"><span data-stu-id="cf731-155">**Certificates**</span></span>](certificates.md)
</dt> </dl>

 

 
