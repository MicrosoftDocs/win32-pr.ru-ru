---
description: Копирует содержимое открытого хранилища сертификатов в закодированную строку.
ms.assetid: 00697579-f929-42ed-8e8e-5c970fe4465b
title: Метод Store. Export
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Export
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: dbf4a2912cb62935447daa1589b6829c5a96488e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669074"
---
# <a name="storeexport-method"></a><span data-ttu-id="a67e4-103">Метод Store. Export</span><span class="sxs-lookup"><span data-stu-id="a67e4-103">Store.Export method</span></span>

<span data-ttu-id="a67e4-104">\[Метод **Export** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="a67e4-104">\[The **Export** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a67e4-105">Вместо этого используйте [**класс X509Store**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="a67e4-105">Instead, use the [**X509Store Class**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="a67e4-106">Метод **Export** копирует содержимое открытого [*хранилища сертификатов*](../secgloss/c-gly.md) в закодированную строку.</span><span class="sxs-lookup"><span data-stu-id="a67e4-106">The **Export** method copies the contents of an open [*certificate store*](../secgloss/c-gly.md) to an encoded string.</span></span>

## <a name="syntax"></a><span data-ttu-id="a67e4-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a67e4-107">Syntax</span></span>


```VB
Store.Export( _
  [ ByVal SaveAs ], _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a><span data-ttu-id="a67e4-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a67e4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a67e4-109">*Сохранить* \[ как в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="a67e4-109">*SaveAs* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a67e4-110">Значение перечисления " [CAPICOM \_ Store \_ \_ — \_ тип](capicom-store-save-as-type.md) ", которое указывает формат для операции экспорта.</span><span class="sxs-lookup"><span data-stu-id="a67e4-110">A value of the [CAPICOM\_STORE\_SAVE\_AS\_TYPE](capicom-store-save-as-type.md) enumeration that indicates the format for the export operation.</span></span> <span data-ttu-id="a67e4-111">Значение по умолчанию — CAPICOM \_ Store \_ Сохранить \_ как \_ сериализованное.</span><span class="sxs-lookup"><span data-stu-id="a67e4-111">The default value is CAPICOM\_STORE\_SAVE\_AS\_SERIALIZED.</span></span> <span data-ttu-id="a67e4-112">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="a67e4-112">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="a67e4-113">Значение</span><span class="sxs-lookup"><span data-stu-id="a67e4-113">Value</span></span>                                                                                                                                                                                                                     | <span data-ttu-id="a67e4-114">Значение</span><span class="sxs-lookup"><span data-stu-id="a67e4-114">Meaning</span></span>                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="CAPICOM_STORE_SAVE_AS_SERIALIZED"></span><span id="capicom_store_save_as_serialized"></span><dl> <span data-ttu-id="a67e4-115"><dt>**CAPICOM \_ Store \_ Сохранить \_ как \_ сериализованный**</dt></span><span class="sxs-lookup"><span data-stu-id="a67e4-115"><dt>**CAPICOM\_STORE\_SAVE\_AS\_SERIALIZED**</dt></span></span> </dl> | <span data-ttu-id="a67e4-116">Хранилище сохраняется в сериализованном формате.</span><span class="sxs-lookup"><span data-stu-id="a67e4-116">The store is saved in serialized format.</span></span><br/> |
| <span id="CAPICOM_STORE_SAVE_AS_PKCS7"></span><span id="capicom_store_save_as_pkcs7"></span><dl> <span data-ttu-id="a67e4-117"><dt>**CAPICOM \_ Store \_ Сохранить \_ как \_ PKCS7**</dt></span><span class="sxs-lookup"><span data-stu-id="a67e4-117"><dt>**CAPICOM\_STORE\_SAVE\_AS\_PKCS7**</dt></span></span> </dl>                | <span data-ttu-id="a67e4-118">Хранилище сохраняется в \# формате PKCS 7.</span><span class="sxs-lookup"><span data-stu-id="a67e4-118">The store is saved in PKCS \#7 format.</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="a67e4-119">*Енкодингтипе* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="a67e4-119">*EncodingType* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a67e4-120">Значение перечисления [ \_ \_ типа CAPICOM Encoding](capicom-encoding-type.md) , указывающее тип кодировки экспортируемого хранилища.</span><span class="sxs-lookup"><span data-stu-id="a67e4-120">A value of the [CAPICOM\_ENCODING\_TYPE](capicom-encoding-type.md) enumeration that indicates the encoding type of the exported store.</span></span> <span data-ttu-id="a67e4-121">Значение по умолчанию — CAPICOM- \_ кодировать \_ Base64.</span><span class="sxs-lookup"><span data-stu-id="a67e4-121">The default value is CAPICOM\_ENCODE\_BASE64.</span></span> <span data-ttu-id="a67e4-122">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="a67e4-122">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="a67e4-123">Значение</span><span class="sxs-lookup"><span data-stu-id="a67e4-123">Value</span></span>                                                                                                                                                                                  | <span data-ttu-id="a67e4-124">Значение</span><span class="sxs-lookup"><span data-stu-id="a67e4-124">Meaning</span></span>                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <span data-ttu-id="a67e4-125"><dt>**CAPICOM \_ кодирует \_ ANY**</dt></span><span class="sxs-lookup"><span data-stu-id="a67e4-125"><dt>**CAPICOM\_ENCODE\_ANY**</dt></span></span> </dl>          | <span data-ttu-id="a67e4-126">Этот тип кодирования используется только в том случае, если входные данные имеют неизвестный тип кодирования.</span><span class="sxs-lookup"><span data-stu-id="a67e4-126">This encoding type is used only when the input data has an unknown encoding type.</span></span> <span data-ttu-id="a67e4-127">Если это значение используется для указания типа кодирования вывода, \_ \_ вместо этого будет использоваться CAPICOM-Encoding Base64.</span><span class="sxs-lookup"><span data-stu-id="a67e4-127">If this value is used to specify the output's encoding type, CAPICOM\_ENCODE\_BASE64 will be used instead.</span></span> <span data-ttu-id="a67e4-128">Представлено в CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="a67e4-128">Introduced in CAPICOM 2.0.</span></span><br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <span data-ttu-id="a67e4-129"><dt>**CAPICOM \_ кодирует \_ Base64**</dt></span><span class="sxs-lookup"><span data-stu-id="a67e4-129"><dt>**CAPICOM\_ENCODE\_BASE64**</dt></span></span> </dl> | <span data-ttu-id="a67e4-130">Данные сохраняются в виде строки в кодировке Base64.</span><span class="sxs-lookup"><span data-stu-id="a67e4-130">Data is saved as a base64-encoded string.</span></span><br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <span data-ttu-id="a67e4-131"><dt>**\_двоичная кодировка CAPICOM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a67e4-131"><dt>**CAPICOM\_ENCODE\_BINARY**</dt></span></span> </dl> | <span data-ttu-id="a67e4-132">Данные сохраняются в виде чисто двоичной последовательности.</span><span class="sxs-lookup"><span data-stu-id="a67e4-132">Data is saved as a pure binary sequence.</span></span><br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a67e4-133">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a67e4-133">Return value</span></span>

<span data-ttu-id="a67e4-134">Этот метод возвращает строку, содержащую сертификаты из хранилища в указанной форме кодировки.</span><span class="sxs-lookup"><span data-stu-id="a67e4-134">This method returns a string that contains the certificates in the store in the specified encoding form.</span></span>

## <a name="requirements"></a><span data-ttu-id="a67e4-135">Требования</span><span class="sxs-lookup"><span data-stu-id="a67e4-135">Requirements</span></span>



| <span data-ttu-id="a67e4-136">Требование</span><span class="sxs-lookup"><span data-stu-id="a67e4-136">Requirement</span></span> | <span data-ttu-id="a67e4-137">Значение</span><span class="sxs-lookup"><span data-stu-id="a67e4-137">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a67e4-138">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="a67e4-138">Redistributable</span></span><br/> | <span data-ttu-id="a67e4-139">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="a67e4-139">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="a67e4-140">DLL</span><span class="sxs-lookup"><span data-stu-id="a67e4-140">DLL</span></span><br/>             | <dl> <span data-ttu-id="a67e4-141"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a67e4-141"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a67e4-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a67e4-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a67e4-143">**Магазин**</span><span class="sxs-lookup"><span data-stu-id="a67e4-143">**Store**</span></span>](store.md)
</dt> <dt>

[<span data-ttu-id="a67e4-144">**Криптографические объекты**</span><span class="sxs-lookup"><span data-stu-id="a67e4-144">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
