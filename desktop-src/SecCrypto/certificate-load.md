---
description: Импортирует сертификат из файла.
ms.assetid: 62c3bf8e-2f52-4342-b3ee-744b032578bf
title: 'Метод ICertificate2:: Load'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Load
- ICertificate2.Load
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9193297ad7eacc1994e4bf3729a87054573b1574
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665111"
---
# <a name="icertificate2load-method"></a><span data-ttu-id="1ad8a-103">Метод ICertificate2:: Load</span><span class="sxs-lookup"><span data-stu-id="1ad8a-103">ICertificate2::Load method</span></span>

<span data-ttu-id="1ad8a-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="1ad8a-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="1ad8a-105">Вместо этого используйте [**класс X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="1ad8a-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="1ad8a-106">Метод **Load** импортирует сертификат из файла.</span><span class="sxs-lookup"><span data-stu-id="1ad8a-106">The **Load** method imports a certificate from a file.</span></span> <span data-ttu-id="1ad8a-107">Этот метод появился в CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="1ad8a-107">This method was introduced in CAPICOM 2.0.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ad8a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1ad8a-108">Syntax</span></span>


```VB
Certificate.Load( _
  ByVal FileName, _
  [ ByVal Password ], _
  [ ByVal KeyStorageFlag ], _
  [ ByVal KeyLocation ] _
)
```



## <a name="parameters"></a><span data-ttu-id="1ad8a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="1ad8a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ad8a-110">*Имя файла* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1ad8a-110">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ad8a-111">Строка, содержащая путь к CER-файлу или PFX, который содержит данные сертификата.</span><span class="sxs-lookup"><span data-stu-id="1ad8a-111">A string that contains the path to a .cer or .pfx file that contains the certificate data.</span></span>

</dd> <dt>

<span data-ttu-id="1ad8a-112">*Пароль* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="1ad8a-112">*Password* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1ad8a-113">Строка, содержащая пароль в [*виде открытого текста*](../secgloss/p-gly.md) для файла [*закрытого ключа*](../secgloss/p-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="1ad8a-113">A string that contains the [*plaintext*](../secgloss/p-gly.md) password to the [*private key*](../secgloss/p-gly.md) file.</span></span> <span data-ttu-id="1ad8a-114">Пароль может содержать до 32 символов Юникода, включая завершающий нуль-символ.</span><span class="sxs-lookup"><span data-stu-id="1ad8a-114">The password can contain up to 32 Unicode characters, including a terminating null character.</span></span> <span data-ttu-id="1ad8a-115">Сведения о защите пароля см. в разделе [обработка паролей](../secbp/handling-passwords.md).</span><span class="sxs-lookup"><span data-stu-id="1ad8a-115">For information about protecting the password, see [Handling Passwords](../secbp/handling-passwords.md).</span></span>

</dd> <dt>

<span data-ttu-id="1ad8a-116">*Кэйсторажефлаг* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="1ad8a-116">*KeyStorageFlag* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1ad8a-117">Значение перечисления [**\_ \_ \_ флагов хранилища CAPICOM Key**](capicom-key-storage-flag.md) , определяющее флаги хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="1ad8a-117">A value of the [**CAPICOM\_KEY\_STORAGE\_FLAG**](capicom-key-storage-flag.md) enumeration that defines key storage flags.</span></span> <span data-ttu-id="1ad8a-118">По умолчанию используется \_ хранилище CAPICOM key \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="1ad8a-118">The default is CAPICOM\_KEY\_STORAGE\_DEFAULT.</span></span> <span data-ttu-id="1ad8a-119">В следующей таблице приводятся возможные значения.</span><span class="sxs-lookup"><span data-stu-id="1ad8a-119">The following table shows the possible values.</span></span>



| <span data-ttu-id="1ad8a-120">Значение</span><span class="sxs-lookup"><span data-stu-id="1ad8a-120">Value</span></span>                                                                                                                                                                                                                           | <span data-ttu-id="1ad8a-121">Значение</span><span class="sxs-lookup"><span data-stu-id="1ad8a-121">Meaning</span></span>                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span id="CAPICOM_KEY_STORAGE_DEFAULT"></span><span id="capicom_key_storage_default"></span><dl> <span data-ttu-id="1ad8a-122"><dt>**\_хранилище CAPICOM \_ key \_ по умолчанию**</dt></span><span class="sxs-lookup"><span data-stu-id="1ad8a-122"><dt>**CAPICOM\_KEY\_STORAGE\_DEFAULT**</dt></span></span> </dl>                       | <span data-ttu-id="1ad8a-123">Хранилище ключей по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1ad8a-123">Default key storage.</span></span><br/>       |
| <span id="CAPICOM_KEY_STORAGE_EXPORTABLE"></span><span id="capicom_key_storage_exportable"></span><dl> <span data-ttu-id="1ad8a-124"><dt>**\_хранилище CAPICOM Key, \_ \_ экспортируемое**</dt></span><span class="sxs-lookup"><span data-stu-id="1ad8a-124"><dt>**CAPICOM\_KEY\_STORAGE\_EXPORTABLE**</dt></span></span> </dl>              | <span data-ttu-id="1ad8a-125">Ключ доступен для экспорта.</span><span class="sxs-lookup"><span data-stu-id="1ad8a-125">The key is exportable.</span></span><br/>     |
| <span id="CAPICOM_KEY_STORAGE_USER_PROTECTED"></span><span id="capicom_key_storage_user_protected"></span><dl> <span data-ttu-id="1ad8a-126"><dt>**\_ \_ \_ защищенное пользователем хранилище CAPICOM key \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1ad8a-126"><dt>**CAPICOM\_KEY\_STORAGE\_USER\_PROTECTED**</dt></span></span> </dl> | <span data-ttu-id="1ad8a-127">Ключ защищен пользователем.</span><span class="sxs-lookup"><span data-stu-id="1ad8a-127">The key is user protected.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="1ad8a-128">*Кэйлокатион* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="1ad8a-128">*KeyLocation* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1ad8a-129">Значение перечисления " [**CAPICOM \_ key \_ Location**](capicom-key-location.md) ", определяющее типы расположения ключей.</span><span class="sxs-lookup"><span data-stu-id="1ad8a-129">A value of the [**CAPICOM\_KEY\_LOCATION**](capicom-key-location.md) enumeration that defines key location types.</span></span> <span data-ttu-id="1ad8a-130">Значение по умолчанию — "CAPICOM \_ текущий \_ ключ пользователя" \_ .</span><span class="sxs-lookup"><span data-stu-id="1ad8a-130">The default value is CAPICOM\_CURRENT\_USER\_KEY.</span></span> <span data-ttu-id="1ad8a-131">В следующей таблице приводятся возможные значения.</span><span class="sxs-lookup"><span data-stu-id="1ad8a-131">The following table shows the possible values.</span></span>



| <span data-ttu-id="1ad8a-132">Значение</span><span class="sxs-lookup"><span data-stu-id="1ad8a-132">Value</span></span>                                                                                                                                                                                               | <span data-ttu-id="1ad8a-133">Значение</span><span class="sxs-lookup"><span data-stu-id="1ad8a-133">Meaning</span></span>                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------|
| <span id="CAPICOM_CURRENT_USER_KEY"></span><span id="capicom_current_user_key"></span><dl> <span data-ttu-id="1ad8a-134"><dt>**CAPICOM \_ текущий \_ \_ ключ пользователя**</dt></span><span class="sxs-lookup"><span data-stu-id="1ad8a-134"><dt>**CAPICOM\_CURRENT\_USER\_KEY**</dt></span></span> </dl>    | <span data-ttu-id="1ad8a-135">Ключ — это ключ пользователя.</span><span class="sxs-lookup"><span data-stu-id="1ad8a-135">The key is a user key.</span></span><br/>    |
| <span id="CAPICOM_LOCAL_MACHINE_KEY"></span><span id="capicom_local_machine_key"></span><dl> <span data-ttu-id="1ad8a-136"><dt>**ключ CAPICOM на \_ локальном \_ компьютере \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1ad8a-136"><dt>**CAPICOM\_LOCAL\_MACHINE\_KEY**</dt></span></span> </dl> | <span data-ttu-id="1ad8a-137">Ключ является ключом компьютера.</span><span class="sxs-lookup"><span data-stu-id="1ad8a-137">The key is a machine key.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ad8a-138">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1ad8a-138">Return value</span></span>

<span data-ttu-id="1ad8a-139">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="1ad8a-139">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ad8a-140">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1ad8a-140">Remarks</span></span>

<span data-ttu-id="1ad8a-141">Этот метод вызывает CAPICOM \_ E \_ не \_ разрешен при создании скрипта из веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="1ad8a-141">This method raises CAPICOM\_E\_NOT\_ALLOWED when it is scripted from a web-based application.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ad8a-142">Требования</span><span class="sxs-lookup"><span data-stu-id="1ad8a-142">Requirements</span></span>



| <span data-ttu-id="1ad8a-143">Требование</span><span class="sxs-lookup"><span data-stu-id="1ad8a-143">Requirement</span></span> | <span data-ttu-id="1ad8a-144">Значение</span><span class="sxs-lookup"><span data-stu-id="1ad8a-144">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1ad8a-145">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="1ad8a-145">End of client support</span></span><br/> | <span data-ttu-id="1ad8a-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1ad8a-146">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="1ad8a-147">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="1ad8a-147">End of server support</span></span><br/> | <span data-ttu-id="1ad8a-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1ad8a-148">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="1ad8a-149">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="1ad8a-149">Redistributable</span></span><br/>       | <span data-ttu-id="1ad8a-150">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="1ad8a-150">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="1ad8a-151">DLL</span><span class="sxs-lookup"><span data-stu-id="1ad8a-151">DLL</span></span><br/>                   | <dl> <span data-ttu-id="1ad8a-152"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1ad8a-152"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
