---
description: Сохраняет сертификат в файл.
ms.assetid: 2012b39b-47fd-4071-9752-98bb10954fc0
title: 'Метод ICertificate2:: Save'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Save
- ICertificate2.Save
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3427feb86c705f5558d083bc39673fdf77553f58
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685391"
---
# <a name="icertificate2save-method"></a><span data-ttu-id="9455b-103">Метод ICertificate2:: Save</span><span class="sxs-lookup"><span data-stu-id="9455b-103">ICertificate2::Save method</span></span>

<span data-ttu-id="9455b-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="9455b-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="9455b-105">Вместо этого используйте [**класс X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="9455b-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="9455b-106">Метод **Save** сохраняет сертификат в файл.</span><span class="sxs-lookup"><span data-stu-id="9455b-106">The **Save** method saves the certificate to a file.</span></span> <span data-ttu-id="9455b-107">Этот метод появился в CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="9455b-107">This method was introduced in CAPICOM 2.0.</span></span>

## <a name="syntax"></a><span data-ttu-id="9455b-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9455b-108">Syntax</span></span>


```VB
Certificate.Save( _
  ByVal FileName, _
  [ ByVal Password ], _
  [ ByVal SaveAs ], _
  [ ByVal IncludeOption ] _
)
```



## <a name="parameters"></a><span data-ttu-id="9455b-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="9455b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9455b-110">*Имя файла* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9455b-110">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9455b-111">Строка, содержащая имя выходного файла, в котором будет сохранен сертификат.</span><span class="sxs-lookup"><span data-stu-id="9455b-111">A string that contains the name of the output file where the certificate will be saved.</span></span>

</dd> <dt>

<span data-ttu-id="9455b-112">*Пароль* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="9455b-112">*Password* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9455b-113">Строка, содержащая пароль в [*виде открытого текста*](../secgloss/p-gly.md) для файла [*закрытого ключа*](../secgloss/p-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="9455b-113">A string that contains the [*plaintext*](../secgloss/p-gly.md) password for a [*private key*](../secgloss/p-gly.md) file.</span></span> <span data-ttu-id="9455b-114">Пароль может содержать до 32 символов Юникода, включая завершающий нуль-символ.</span><span class="sxs-lookup"><span data-stu-id="9455b-114">The password can contain up to 32 Unicode characters, including a terminating null character.</span></span> <span data-ttu-id="9455b-115">Сведения о защите пароля см. в разделе [обработка паролей](../secbp/handling-passwords.md).</span><span class="sxs-lookup"><span data-stu-id="9455b-115">For information about protecting the password, see [Handling Passwords](../secbp/handling-passwords.md).</span></span>

</dd> <dt>

<span data-ttu-id="9455b-116">*Сохранить* \[ как в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="9455b-116">*SaveAs* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9455b-117">Значение перечисления [**\_ \_ \_ \_ типа CAPICOM Certificate**](capicom-certificate-save-as-type.md) , определяющее формат выходного файла.</span><span class="sxs-lookup"><span data-stu-id="9455b-117">A value of the [**CAPICOM\_CERTIFICATE\_SAVE\_AS\_TYPE**](capicom-certificate-save-as-type.md) enumeration that specifies the format of the output file.</span></span> <span data-ttu-id="9455b-118">По умолчанию используется элемент **CAPICOM \_ Certificate \_ Save \_ как \_ CER**.</span><span class="sxs-lookup"><span data-stu-id="9455b-118">The default is **CAPICOM\_CERTIFICATE\_SAVE\_AS\_CER**.</span></span> <span data-ttu-id="9455b-119">В следующей таблице приводятся возможные значения.</span><span class="sxs-lookup"><span data-stu-id="9455b-119">The following table shows the possible values.</span></span>



| <span data-ttu-id="9455b-120">Значение</span><span class="sxs-lookup"><span data-stu-id="9455b-120">Value</span></span>                                                                                                                                                                                                                  | <span data-ttu-id="9455b-121">Значение</span><span class="sxs-lookup"><span data-stu-id="9455b-121">Meaning</span></span>                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_CERTIFICATE_SAVE_AS_CER"></span><span id="capicom_certificate_save_as_cer"></span><dl> <span data-ttu-id="9455b-122"><dt>**CAPICOM \_ Certificate \_ Save \_ как \_ CER**</dt></span><span class="sxs-lookup"><span data-stu-id="9455b-122"><dt>**CAPICOM\_CERTIFICATE\_SAVE\_AS\_CER**</dt></span></span> </dl> | <span data-ttu-id="9455b-123">Выходной файл будет отформатирован как CER-файл без сохранения закрытых ключей.</span><span class="sxs-lookup"><span data-stu-id="9455b-123">The output file will be formatted as a .cer file with no private keys saved.</span></span><br/>                                                         |
| <span id="CAPICOM_CERTIFICATE_SAVE_AS_PFX"></span><span id="capicom_certificate_save_as_pfx"></span><dl> <span data-ttu-id="9455b-124"><dt>**CAPICOM \_ Certificate \_ Save \_ как \_ PFX**</dt></span><span class="sxs-lookup"><span data-stu-id="9455b-124"><dt>**CAPICOM\_CERTIFICATE\_SAVE\_AS\_PFX**</dt></span></span> </dl> | <span data-ttu-id="9455b-125">Выходной файл будет отформатирован как PFX-файл (PKCS \# 12), и все связанные с ним закрытые ключи также будут сохранены.</span><span class="sxs-lookup"><span data-stu-id="9455b-125">The output file will be formatted as a .pfx (PKCS \#12) file and any associated private keys that are exportable will also be saved.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9455b-126">*Инклудеоптион* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="9455b-126">*IncludeOption* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9455b-127">Значение элемента [**CAPICOM \_ Certificate \_ включает \_**](capicom-certificate-include-option.md) перечисление параметров, которое указывает, сколько сертификатов в цепочке сохраняется в выходном файле.</span><span class="sxs-lookup"><span data-stu-id="9455b-127">A value of the [**CAPICOM\_CERTIFICATE\_INCLUDE\_OPTION**](capicom-certificate-include-option.md) enumeration that specifies how many certificates in the chain are saved to the output file.</span></span> <span data-ttu-id="9455b-128">По умолчанию CAPICOM \_ Certificate \_ включает \_ только конечную \_ сущность \_ .</span><span class="sxs-lookup"><span data-stu-id="9455b-128">The default is CAPICOM\_CERTIFICATE\_INCLUDE\_END\_ENTITY\_ONLY.</span></span> <span data-ttu-id="9455b-129">В следующей таблице приводятся возможные значения.</span><span class="sxs-lookup"><span data-stu-id="9455b-129">The following table shows the possible values.</span></span>



| <span data-ttu-id="9455b-130">Значение</span><span class="sxs-lookup"><span data-stu-id="9455b-130">Value</span></span>                                                                                                                                                                                                                                                             | <span data-ttu-id="9455b-131">Значение</span><span class="sxs-lookup"><span data-stu-id="9455b-131">Meaning</span></span>                                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| <span id="CAPICOM_CERTIFICATE_INCLUDE_CHAIN_EXCEPT_ROOT"></span><span id="capicom_certificate_include_chain_except_root"></span><dl> <span data-ttu-id="9455b-132"><dt>**CAPICOM \_ Certificate \_ включает \_ цепочку, \_ кроме \_ root**</dt></span><span class="sxs-lookup"><span data-stu-id="9455b-132"><dt>**CAPICOM\_CERTIFICATE\_INCLUDE\_CHAIN\_EXCEPT\_ROOT**</dt></span></span> </dl> | <span data-ttu-id="9455b-133">Сохраняет все сертификаты в цепочке, за исключением корневой сущности</span><span class="sxs-lookup"><span data-stu-id="9455b-133">Saves all certificates in the chain with the exception of the root entity</span></span><br/> |
| <span id="CAPICOM_CERTIFICATE_INCLUDE_WHOLE_CHAIN"></span><span id="capicom_certificate_include_whole_chain"></span><dl> <span data-ttu-id="9455b-134"><dt>**CAPICOM \_ Certificate \_ включает \_ всю \_ цепочку**</dt></span><span class="sxs-lookup"><span data-stu-id="9455b-134"><dt>**CAPICOM\_CERTIFICATE\_INCLUDE\_WHOLE\_CHAIN**</dt></span></span> </dl>                    | <span data-ttu-id="9455b-135">Сохранение всей цепочки сертификатов</span><span class="sxs-lookup"><span data-stu-id="9455b-135">Saves the complete certificate chain</span></span><br/>                                      |
| <span id="CAPICOM_CERTIFICATE_INCLUDE_END_ENTITY_ONLY"></span><span id="capicom_certificate_include_end_entity_only"></span><dl> <span data-ttu-id="9455b-136"><dt>**CAPICOM \_ Certificate \_ — \_ только конечная \_ сущность \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9455b-136"><dt>**CAPICOM\_CERTIFICATE\_INCLUDE\_END\_ENTITY\_ONLY**</dt></span></span> </dl>       | <span data-ttu-id="9455b-137">Сохраняет только сертификат конечного объекта</span><span class="sxs-lookup"><span data-stu-id="9455b-137">Saves only the end entity certificate</span></span><br/>                                     |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9455b-138">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9455b-138">Return value</span></span>

<span data-ttu-id="9455b-139">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="9455b-139">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9455b-140">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9455b-140">Remarks</span></span>

<span data-ttu-id="9455b-141">Этот метод вызывает CAPICOM \_ E \_ не \_ разрешен при создании скрипта из веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="9455b-141">This method raises CAPICOM\_E\_NOT\_ALLOWED when it is scripted from a web-based application.</span></span>

## <a name="requirements"></a><span data-ttu-id="9455b-142">Требования</span><span class="sxs-lookup"><span data-stu-id="9455b-142">Requirements</span></span>



| <span data-ttu-id="9455b-143">Требование</span><span class="sxs-lookup"><span data-stu-id="9455b-143">Requirement</span></span> | <span data-ttu-id="9455b-144">Значение</span><span class="sxs-lookup"><span data-stu-id="9455b-144">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9455b-145">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="9455b-145">End of client support</span></span><br/> | <span data-ttu-id="9455b-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9455b-146">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="9455b-147">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="9455b-147">End of server support</span></span><br/> | <span data-ttu-id="9455b-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9455b-148">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="9455b-149">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="9455b-149">Redistributable</span></span><br/>       | <span data-ttu-id="9455b-150">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="9455b-150">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="9455b-151">DLL</span><span class="sxs-lookup"><span data-stu-id="9455b-151">DLL</span></span><br/>                   | <dl> <span data-ttu-id="9455b-152"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9455b-152"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
