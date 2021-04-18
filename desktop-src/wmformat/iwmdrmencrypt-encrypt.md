---
title: Метод Ивмдрменкрипт Encrypt (Вмдрмсдк. h)
description: Метод Encrypt шифрует буфер данных на месте.
ms.assetid: 9626f53e-3602-4369-99ed-fbcd8d5f4d9e
keywords:
- Шифрование метода Windows Media Format
- Шифрование метода Windows Media Format, интерфейс Ивмдрменкрипт
- Интерфейс Ивмдрменкрипт интерфейса Windows Media Format, метод Encrypt
topic_type:
- apiref
api_name:
- IWMDRMEncrypt.Encrypt
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13380b321b540cbb5edce3c03e422b49c7b90e54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717761"
---
# <a name="iwmdrmencryptencrypt-method"></a><span data-ttu-id="c2e37-106">Метод Ивмдрменкрипт:: Encrypt</span><span class="sxs-lookup"><span data-stu-id="c2e37-106">IWMDRMEncrypt::Encrypt method</span></span>

<span data-ttu-id="c2e37-107">Метод **Encrypt** шифрует буфер данных на месте.</span><span class="sxs-lookup"><span data-stu-id="c2e37-107">The **Encrypt** method encrypts a data buffer in place.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2e37-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c2e37-108">Syntax</span></span>


```C++
HRESULT Encrypt(
  [in, out] BYTE            *pbData,
  [in]      DWORD           cbData,
  [in]      WMDRMCryptoData *pWMCryptoData
);
```



## <a name="parameters"></a><span data-ttu-id="c2e37-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="c2e37-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2e37-110">*pbData* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="c2e37-110">*pbData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c2e37-111">Данные для шифрования.</span><span class="sxs-lookup"><span data-stu-id="c2e37-111">Data to encrypt.</span></span> <span data-ttu-id="c2e37-112">Если метод завершился удачно, данные шифруются при возврате.</span><span class="sxs-lookup"><span data-stu-id="c2e37-112">If the method succeeds, the data is encrypted on return.</span></span>

</dd> <dt>

<span data-ttu-id="c2e37-113">*cbData* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c2e37-113">*cbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2e37-114">Размер данных в байтах.</span><span class="sxs-lookup"><span data-stu-id="c2e37-114">Size of the data in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="c2e37-115">*пвмкриптодата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c2e37-115">*pWMCryptoData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2e37-116">Указатель на структуру [**вмдрмкриптодата**](wmdrmcryptodata.md) , содержащую дополнительные параметры.</span><span class="sxs-lookup"><span data-stu-id="c2e37-116">Pointer to a [**WMDRMCryptoData**](wmdrmcryptodata.md) structure containing extra parameters.</span></span> <span data-ttu-id="c2e37-117">Задайте **значение NULL** , чтобы использовать значения шифрования по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c2e37-117">Set to **NULL** to use the default encryption values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2e37-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c2e37-118">Return value</span></span>

<span data-ttu-id="c2e37-119">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="c2e37-119">The method returns an **HRESULT**.</span></span> <span data-ttu-id="c2e37-120">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="c2e37-120">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="c2e37-121">Код возврата</span><span class="sxs-lookup"><span data-stu-id="c2e37-121">Return code</span></span>                                                                          | <span data-ttu-id="c2e37-122">Описание</span><span class="sxs-lookup"><span data-stu-id="c2e37-122">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="c2e37-123"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="c2e37-123"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="c2e37-124">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="c2e37-124">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c2e37-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c2e37-125">Remarks</span></span>

<span data-ttu-id="c2e37-126">Нет.</span><span class="sxs-lookup"><span data-stu-id="c2e37-126">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2e37-127">Требования</span><span class="sxs-lookup"><span data-stu-id="c2e37-127">Requirements</span></span>



| <span data-ttu-id="c2e37-128">Требование</span><span class="sxs-lookup"><span data-stu-id="c2e37-128">Requirement</span></span> | <span data-ttu-id="c2e37-129">Значение</span><span class="sxs-lookup"><span data-stu-id="c2e37-129">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c2e37-130">Header</span><span class="sxs-lookup"><span data-stu-id="c2e37-130">Header</span></span><br/> | <dl> <span data-ttu-id="c2e37-131"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2e37-131"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2e37-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c2e37-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2e37-133">**Интерфейс Ивмдрменкрипт**</span><span class="sxs-lookup"><span data-stu-id="c2e37-133">**IWMDRMEncrypt Interface**</span></span>](iwmdrmencrypt.md)
</dt> <dt>

[<span data-ttu-id="c2e37-134">**вмдрмкриптодата**</span><span class="sxs-lookup"><span data-stu-id="c2e37-134">**WMDRMCryptoData**</span></span>](wmdrmcryptodata.md)
</dt> </dl>

 

 





