---
description: Загружает сертификат подписи из указанного PFX-файла.
ms.assetid: 98963354-c237-40d0-9235-8318728e2c8e
title: Подписывающий. Load, метод
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signer.Load
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9a817a95ca825b67b54a41fc674db10bf81b5740
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668905"
---
# <a name="signerload-method"></a><span data-ttu-id="7ab8c-103">Подписывающий. Load, метод</span><span class="sxs-lookup"><span data-stu-id="7ab8c-103">Signer.Load method</span></span>

<span data-ttu-id="7ab8c-104">\[Метод **Load** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="7ab8c-104">\[The **Load** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="7ab8c-105">Вместо этого используйте [**класс кмссигнер**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) в пространстве имен [**System. Security. Cryptography. PKCS**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="7ab8c-105">Instead, use the [**CmsSigner Class**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="7ab8c-106">Метод **Load** загружает сертификат подписи из указанного PFX-файла.</span><span class="sxs-lookup"><span data-stu-id="7ab8c-106">The **Load** method loads a signing certificate from a specified .pfx file.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ab8c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7ab8c-107">Syntax</span></span>


```VB
Signer.Load( _
  ByVal FileName, _
  [ ByVal Password ] _
)
```



## <a name="parameters"></a><span data-ttu-id="7ab8c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7ab8c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ab8c-109">*FileName*</span><span class="sxs-lookup"><span data-stu-id="7ab8c-109">*FileName*</span></span> 
</dt> <dd>

<span data-ttu-id="7ab8c-110">Имя PFX-файла, содержащего сертификат подписи.</span><span class="sxs-lookup"><span data-stu-id="7ab8c-110">Name of the .pfx file that contains the signing certificate.</span></span>

</dd> <dt>

<span data-ttu-id="7ab8c-111">*Пароль* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="7ab8c-111">*Password* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7ab8c-112">Строка, содержащая пароль в виде открытого текста, используемый для открытия файла.</span><span class="sxs-lookup"><span data-stu-id="7ab8c-112">String containing the plaintext password used to open the file.</span></span> <span data-ttu-id="7ab8c-113">Для пароля можно использовать до 32 символов Юникода, включая завершающий нуль-символ.</span><span class="sxs-lookup"><span data-stu-id="7ab8c-113">Up to 32 Unicode characters, including a terminating null character, can be used for the password.</span></span> <span data-ttu-id="7ab8c-114">Значение по умолчанию — пустая строка.</span><span class="sxs-lookup"><span data-stu-id="7ab8c-114">The default value is an empty string ("").</span></span> <span data-ttu-id="7ab8c-115">Сведения о защите пароля см. в разделе [обработка паролей](../secbp/handling-passwords.md).</span><span class="sxs-lookup"><span data-stu-id="7ab8c-115">For information about protecting the password, see [Handling Passwords](../secbp/handling-passwords.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ab8c-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7ab8c-116">Return value</span></span>

<span data-ttu-id="7ab8c-117">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="7ab8c-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ab8c-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7ab8c-118">Remarks</span></span>

<span data-ttu-id="7ab8c-119">Этот метод загружает первый сертификат из PFX-файла, с которым связан закрытый ключ.</span><span class="sxs-lookup"><span data-stu-id="7ab8c-119">This method loads the first certificate in the .pfx file that has a private key associated with it.</span></span>

<span data-ttu-id="7ab8c-120">Этот метод вызывает CAPICOM \_ E \_ не \_ разрешен при создании скрипта из веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="7ab8c-120">This method raises CAPICOM\_E\_NOT\_ALLOWED when it is scripted from a web-based application.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ab8c-121">Требования</span><span class="sxs-lookup"><span data-stu-id="7ab8c-121">Requirements</span></span>



| <span data-ttu-id="7ab8c-122">Требование</span><span class="sxs-lookup"><span data-stu-id="7ab8c-122">Requirement</span></span> | <span data-ttu-id="7ab8c-123">Значение</span><span class="sxs-lookup"><span data-stu-id="7ab8c-123">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7ab8c-124">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="7ab8c-124">Redistributable</span></span><br/> | <span data-ttu-id="7ab8c-125">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="7ab8c-125">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="7ab8c-126">DLL</span><span class="sxs-lookup"><span data-stu-id="7ab8c-126">DLL</span></span><br/>             | <dl> <span data-ttu-id="7ab8c-127"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7ab8c-127"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ab8c-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7ab8c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ab8c-129">**Автор подписи**</span><span class="sxs-lookup"><span data-stu-id="7ab8c-129">**Signer**</span></span>](signer.md)
</dt> </dl>

 

 
