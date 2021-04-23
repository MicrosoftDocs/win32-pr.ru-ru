---
description: Копирует сертификат в зашифрованную строку.
ms.assetid: bae7fb57-6b44-4aac-a635-b5b82de1f68d
title: 'Метод ICertificate2:: Export'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Export
- ICertificate2.Export
- ICertificate.Export
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: aee48fe3d9ba56cba90c9645a3fb9752e3367a20
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669187"
---
# <a name="icertificate2export-method"></a><span data-ttu-id="d27bb-103">Метод ICertificate2:: Export</span><span class="sxs-lookup"><span data-stu-id="d27bb-103">ICertificate2::Export method</span></span>

<span data-ttu-id="d27bb-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d27bb-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="d27bb-105">Вместо этого используйте [**класс X509Certificate2**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="d27bb-105">Instead, use the [**X509Certificate2 Class**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="d27bb-106">Метод **Export** копирует сертификат в зашифрованную строку.</span><span class="sxs-lookup"><span data-stu-id="d27bb-106">The **Export** method copies a certificate to an encoded string.</span></span> <span data-ttu-id="d27bb-107">Закодированная строка может быть записана в файл или импортирована в новый объект [**сертификата**](certificate.md) .</span><span class="sxs-lookup"><span data-stu-id="d27bb-107">The encoded string can be written to a file or imported into a new [**Certificate**](certificate.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d27bb-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d27bb-108">Syntax</span></span>


```VB
Certificate.Export( _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a><span data-ttu-id="d27bb-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="d27bb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d27bb-110">*Енкодингтипе* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="d27bb-110">*EncodingType* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d27bb-111">Значение перечисления [**\_ \_ типа CAPICOM Encoding**](capicom-encoding-type.md) , указывающее тип кодировки для операции экспорта.</span><span class="sxs-lookup"><span data-stu-id="d27bb-111">A value of the [**CAPICOM\_ENCODING\_TYPE**](capicom-encoding-type.md) enumeration that specifies the encoding type for the export operation.</span></span> <span data-ttu-id="d27bb-112">Значение по умолчанию — **CAPICOM- \_ кодировать \_ Base64**.</span><span class="sxs-lookup"><span data-stu-id="d27bb-112">The default value is **CAPICOM\_ENCODE\_BASE64**.</span></span> <span data-ttu-id="d27bb-113">В следующей таблице приводятся возможные значения.</span><span class="sxs-lookup"><span data-stu-id="d27bb-113">The following table shows the possible values.</span></span>



| <span data-ttu-id="d27bb-114">Значение</span><span class="sxs-lookup"><span data-stu-id="d27bb-114">Value</span></span>                                                                                                                                                                                  | <span data-ttu-id="d27bb-115">Значение</span><span class="sxs-lookup"><span data-stu-id="d27bb-115">Meaning</span></span>                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <span data-ttu-id="d27bb-116"><dt>**CAPICOM \_ кодирует \_ ANY**</dt></span><span class="sxs-lookup"><span data-stu-id="d27bb-116"><dt>**CAPICOM\_ENCODE\_ANY**</dt></span></span> </dl>          | <span data-ttu-id="d27bb-117">Этот тип кодирования используется только в том случае, если входные данные имеют неизвестный тип кодирования.</span><span class="sxs-lookup"><span data-stu-id="d27bb-117">This encoding type is used only when the input data has an unknown encoding type.</span></span> <span data-ttu-id="d27bb-118">Если это значение используется для указания типа кодирования вывода, \_ \_ вместо этого будет использоваться CAPICOM-Encoding Base64.</span><span class="sxs-lookup"><span data-stu-id="d27bb-118">If this value is used to specify the output's encoding type, CAPICOM\_ENCODE\_BASE64 will be used instead.</span></span> <span data-ttu-id="d27bb-119">Представлено в CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="d27bb-119">Introduced in CAPICOM 2.0.</span></span><br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <span data-ttu-id="d27bb-120"><dt>**CAPICOM \_ кодирует \_ Base64**</dt></span><span class="sxs-lookup"><span data-stu-id="d27bb-120"><dt>**CAPICOM\_ENCODE\_BASE64**</dt></span></span> </dl> | <span data-ttu-id="d27bb-121">Данные сохраняются в виде строки в кодировке Base64.</span><span class="sxs-lookup"><span data-stu-id="d27bb-121">Data is saved as a base64-encoded string.</span></span><br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <span data-ttu-id="d27bb-122"><dt>**\_двоичная кодировка CAPICOM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d27bb-122"><dt>**CAPICOM\_ENCODE\_BINARY**</dt></span></span> </dl> | <span data-ttu-id="d27bb-123">Данные сохраняются в виде чисто двоичной последовательности.</span><span class="sxs-lookup"><span data-stu-id="d27bb-123">Data is saved as a pure binary sequence.</span></span><br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d27bb-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d27bb-124">Return value</span></span>

<span data-ttu-id="d27bb-125">Строка, содержащая экспортированный сертификат в указанной форме кодировки.</span><span class="sxs-lookup"><span data-stu-id="d27bb-125">A string that contains the exported certificate in the specified encoding form.</span></span>

## <a name="requirements"></a><span data-ttu-id="d27bb-126">Требования</span><span class="sxs-lookup"><span data-stu-id="d27bb-126">Requirements</span></span>



| <span data-ttu-id="d27bb-127">Требование</span><span class="sxs-lookup"><span data-stu-id="d27bb-127">Requirement</span></span> | <span data-ttu-id="d27bb-128">Значение</span><span class="sxs-lookup"><span data-stu-id="d27bb-128">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d27bb-129">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="d27bb-129">End of client support</span></span><br/> | <span data-ttu-id="d27bb-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d27bb-130">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="d27bb-131">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="d27bb-131">End of server support</span></span><br/> | <span data-ttu-id="d27bb-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d27bb-132">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="d27bb-133">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="d27bb-133">Redistributable</span></span><br/>       | <span data-ttu-id="d27bb-134">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="d27bb-134">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="d27bb-135">DLL</span><span class="sxs-lookup"><span data-stu-id="d27bb-135">DLL</span></span><br/>                   | <dl> <span data-ttu-id="d27bb-136"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d27bb-136"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d27bb-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d27bb-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d27bb-138">Криптографические объекты</span><span class="sxs-lookup"><span data-stu-id="d27bb-138">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="d27bb-139">**Certificate**</span><span class="sxs-lookup"><span data-stu-id="d27bb-139">**Certificate**</span></span>](certificate.md)
</dt> </dl>

 

 
