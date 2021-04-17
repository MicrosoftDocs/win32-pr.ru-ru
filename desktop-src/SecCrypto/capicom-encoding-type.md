---
description: Указывает используемый тип кодировки.
ms.assetid: 13e78a5e-3a31-44de-b249-28e360e1e087
title: Перечисление CAPICOM_ENCODING_TYPE (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_ENCODING_TYPE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: a546831d6e88b3e35706df59adabe0627ad9fccb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669188"
---
# <a name="capicom_encoding_type-enumeration"></a><span data-ttu-id="96d19-103">\_Перечисление типов кодировки CAPICOM \_</span><span class="sxs-lookup"><span data-stu-id="96d19-103">CAPICOM\_ENCODING\_TYPE enumeration</span></span>

<span data-ttu-id="96d19-104">Тип **перечисления \_ CAPICOM \_ Encoding** указывает используемый тип кодировки.</span><span class="sxs-lookup"><span data-stu-id="96d19-104">The **CAPICOM\_ENCODING\_TYPE** enumeration type indicates the encoding type used.</span></span>

## <a name="members"></a><span data-ttu-id="96d19-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="96d19-105">Members</span></span>



| <span data-ttu-id="96d19-106">Член</span><span class="sxs-lookup"><span data-stu-id="96d19-106">Member</span></span>                      | <span data-ttu-id="96d19-107">Описание</span><span class="sxs-lookup"><span data-stu-id="96d19-107">Description</span></span>                                                                                                                                                                                 | <span data-ttu-id="96d19-108">Значение</span><span class="sxs-lookup"><span data-stu-id="96d19-108">Value</span></span>      |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|
| <span data-ttu-id="96d19-109">**CAPICOM \_ кодирует \_ ANY**</span><span class="sxs-lookup"><span data-stu-id="96d19-109">**CAPICOM\_ENCODE\_ANY**</span></span>    | <span data-ttu-id="96d19-110">Данные сохраняются в виде строки в кодировке Base64 или в виде чисто двоичной последовательности.</span><span class="sxs-lookup"><span data-stu-id="96d19-110">Data is saved as a base64-encoded string or a pure binary sequence.</span></span> <span data-ttu-id="96d19-111">Этот тип кодирования используется только для входных данных, имеющих неизвестный тип кодирования.</span><span class="sxs-lookup"><span data-stu-id="96d19-111">This encoding type is used only for input data that has an unknown encoding type.</span></span> <span data-ttu-id="96d19-112">Представлено в CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="96d19-112">Introduced in CAPICOM 2.0.</span></span><br/> | <span data-ttu-id="96d19-113">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="96d19-113">0xffffffff</span></span> |
| <span data-ttu-id="96d19-114">**CAPICOM \_ кодирует \_ Base64**</span><span class="sxs-lookup"><span data-stu-id="96d19-114">**CAPICOM\_ENCODE\_BASE64**</span></span> | <span data-ttu-id="96d19-115">Данные сохраняются в виде строки в кодировке Base64.</span><span class="sxs-lookup"><span data-stu-id="96d19-115">Data is saved as a base64-encoded string.</span></span><br/>                                                                                                                                        | <span data-ttu-id="96d19-116">0</span><span class="sxs-lookup"><span data-stu-id="96d19-116">0</span></span>          |
| <span data-ttu-id="96d19-117">**\_двоичная кодировка CAPICOM \_**</span><span class="sxs-lookup"><span data-stu-id="96d19-117">**CAPICOM\_ENCODE\_BINARY**</span></span> | <span data-ttu-id="96d19-118">Данные сохраняются в виде чисто двоичной последовательности.</span><span class="sxs-lookup"><span data-stu-id="96d19-118">Data is saved as a pure binary sequence.</span></span><br/>                                                                                                                                         | <span data-ttu-id="96d19-119">1</span><span class="sxs-lookup"><span data-stu-id="96d19-119">1</span></span>          |



## <a name="remarks"></a><span data-ttu-id="96d19-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="96d19-120">Remarks</span></span>

<span data-ttu-id="96d19-121">Этот тип перечисления используется следующими методами и свойствами элемента CAPICOM:</span><span class="sxs-lookup"><span data-stu-id="96d19-121">This enumeration type is used by the following CAPICOM methods and properties:</span></span>

-   <span data-ttu-id="96d19-122">Метод [**Certificate. Export**](certificate-export.md)</span><span class="sxs-lookup"><span data-stu-id="96d19-122">[**Certificate.Export**](certificate-export.md) method</span></span>
-   <span data-ttu-id="96d19-123">[**Енкодеддата. Value,**](encodeddata-value.md) свойство</span><span class="sxs-lookup"><span data-stu-id="96d19-123">[**EncodedData.Value**](encodeddata-value.md) property</span></span>
-   <span data-ttu-id="96d19-124">Метод [**EncryptedData. Encrypt**](encrypteddata-encrypt.md)</span><span class="sxs-lookup"><span data-stu-id="96d19-124">[**EncryptedData.Encrypt**](encrypteddata-encrypt.md) method</span></span>
-   <span data-ttu-id="96d19-125">[**Енвелопеддата. Encrypt,**](envelopeddata-encrypt.md) метод</span><span class="sxs-lookup"><span data-stu-id="96d19-125">[**EnvelopedData.Encrypt**](envelopeddata-encrypt.md) method</span></span>
-   <span data-ttu-id="96d19-126">[**ExtendedProperty. Value,**](extendedproperty-value.md) свойство</span><span class="sxs-lookup"><span data-stu-id="96d19-126">[**ExtendedProperty.Value**](extendedproperty-value.md) property</span></span>
-   <span data-ttu-id="96d19-127">[**Сигнеддата. Sign,**](signeddata-sign.md) метод</span><span class="sxs-lookup"><span data-stu-id="96d19-127">[**SignedData.Sign**](signeddata-sign.md) method</span></span>
-   <span data-ttu-id="96d19-128">[**Сигнеддата. Кознаковый**](signeddata-cosign.md) метод</span><span class="sxs-lookup"><span data-stu-id="96d19-128">[**SignedData.CoSign**](signeddata-cosign.md) method</span></span>
-   <span data-ttu-id="96d19-129">Метод [**Store. Export**](store-export.md)</span><span class="sxs-lookup"><span data-stu-id="96d19-129">[**Store.Export**](store-export.md) method</span></span>
-   <span data-ttu-id="96d19-130">Метод [**Utilities. Random**](utilities-getrandom.md)</span><span class="sxs-lookup"><span data-stu-id="96d19-130">[**Utilities.GetRandom**](utilities-getrandom.md) method</span></span>

## <a name="requirements"></a><span data-ttu-id="96d19-131">Требования</span><span class="sxs-lookup"><span data-stu-id="96d19-131">Requirements</span></span>



| <span data-ttu-id="96d19-132">Требование</span><span class="sxs-lookup"><span data-stu-id="96d19-132">Requirement</span></span> | <span data-ttu-id="96d19-133">Значение</span><span class="sxs-lookup"><span data-stu-id="96d19-133">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="96d19-134">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="96d19-134">Redistributable</span></span><br/> | <span data-ttu-id="96d19-135">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="96d19-135">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="96d19-136">Header</span><span class="sxs-lookup"><span data-stu-id="96d19-136">Header</span></span><br/>          | <dl> <span data-ttu-id="96d19-137"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="96d19-137"><dt>Capicom.h</dt></span></span> </dl> |



 

 




