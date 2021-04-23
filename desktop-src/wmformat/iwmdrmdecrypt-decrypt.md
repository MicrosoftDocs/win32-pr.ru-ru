---
title: Метод дешифровки Ивмдрмдекрипт (Вмдрмсдк. h)
description: Метод дешифровки расшифровывает буфер данных на месте.
ms.assetid: ca0a5b2f-d25f-423e-8956-fca264399083
keywords:
- Расшифровка метода Windows Media Format
- Метод расшифровки формата Windows Media Format, интерфейс Ивмдрмдекрипт
- Интерфейс Ивмдрмдекрипт интерфейса Windows Media Format, метод дешифрации
topic_type:
- apiref
api_name:
- IWMDRMDecrypt.Decrypt
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eb3c1437bc4b4d2f442c61e54f238f176adf66b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717762"
---
# <a name="iwmdrmdecryptdecrypt-method"></a><span data-ttu-id="d71e7-106">Ивмдрмдекрипт: метод:D екрипт</span><span class="sxs-lookup"><span data-stu-id="d71e7-106">IWMDRMDecrypt::Decrypt method</span></span>

<span data-ttu-id="d71e7-107">Метод **дешифровки** расшифровывает буфер данных на месте.</span><span class="sxs-lookup"><span data-stu-id="d71e7-107">The **Decrypt** method decrypts a data buffer in place.</span></span>

## <a name="syntax"></a><span data-ttu-id="d71e7-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d71e7-108">Syntax</span></span>


```C++
HRESULT Decrypt(
  [in, out] BYTE            *pbData,
  [in]      DWORD           cbData,
  [in]      WMDRMCryptoData *pWMCryptoData
);
```



## <a name="parameters"></a><span data-ttu-id="d71e7-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="d71e7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d71e7-110">*pbData* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="d71e7-110">*pbData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d71e7-111">Данные для расшифровки.</span><span class="sxs-lookup"><span data-stu-id="d71e7-111">Data to be decrypted.</span></span> <span data-ttu-id="d71e7-112">Если метод завершился удачно, эти данные расшифровываются при возврате.</span><span class="sxs-lookup"><span data-stu-id="d71e7-112">If the method succeeds, this data is decrypted on return.</span></span>

</dd> <dt>

<span data-ttu-id="d71e7-113">*cbData* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d71e7-113">*cbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d71e7-114">Размер данных в байтах.</span><span class="sxs-lookup"><span data-stu-id="d71e7-114">Size of the data in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="d71e7-115">*пвмкриптодата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d71e7-115">*pWMCryptoData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d71e7-116">Указатель на структуру [**вмдрмкриптодата**](wmdrmcryptodata.md) , содержащую дополнительные параметры.</span><span class="sxs-lookup"><span data-stu-id="d71e7-116">Pointer to a [**WMDRMCryptoData**](wmdrmcryptodata.md) structure containing extra parameters.</span></span> <span data-ttu-id="d71e7-117">Может иметь **значение NULL** , если содержимое было зашифровано с помощью параметров по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d71e7-117">Can be **NULL** if the content was encrypted using the default parameters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d71e7-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d71e7-118">Return value</span></span>

<span data-ttu-id="d71e7-119">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="d71e7-119">The method returns an **HRESULT**.</span></span> <span data-ttu-id="d71e7-120">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="d71e7-120">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="d71e7-121">Код возврата</span><span class="sxs-lookup"><span data-stu-id="d71e7-121">Return code</span></span>                                                                          | <span data-ttu-id="d71e7-122">Описание</span><span class="sxs-lookup"><span data-stu-id="d71e7-122">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="d71e7-123"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="d71e7-123"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="d71e7-124">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="d71e7-124">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d71e7-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d71e7-125">Remarks</span></span>

<span data-ttu-id="d71e7-126">Нет.</span><span class="sxs-lookup"><span data-stu-id="d71e7-126">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="d71e7-127">Требования</span><span class="sxs-lookup"><span data-stu-id="d71e7-127">Requirements</span></span>



| <span data-ttu-id="d71e7-128">Требование</span><span class="sxs-lookup"><span data-stu-id="d71e7-128">Requirement</span></span> | <span data-ttu-id="d71e7-129">Значение</span><span class="sxs-lookup"><span data-stu-id="d71e7-129">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d71e7-130">Header</span><span class="sxs-lookup"><span data-stu-id="d71e7-130">Header</span></span><br/> | <dl> <span data-ttu-id="d71e7-131"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="d71e7-131"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d71e7-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d71e7-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d71e7-133">**Интерфейс Ивмдрмдекрипт**</span><span class="sxs-lookup"><span data-stu-id="d71e7-133">**IWMDRMDecrypt Interface**</span></span>](iwmdrmdecrypt.md)
</dt> <dt>

[<span data-ttu-id="d71e7-134">**вмдрмкриптодата**</span><span class="sxs-lookup"><span data-stu-id="d71e7-134">**WMDRMCryptoData**</span></span>](wmdrmcryptodata.md)
</dt> </dl>

 

 





