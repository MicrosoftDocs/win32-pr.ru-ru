---
title: Метод Ивмдрменкриптскаттер Енкриптскаттер (Вмдрмсдк. h)
description: Метод Енкриптскаттер выполняет расшифровку и шифрование данных.
ms.assetid: e7f87aac-387b-4483-956e-bfbca0cec0f2
keywords:
- Формат Windows Media, Енкриптскаттер метод
- Енкриптскаттер метод Windows Media Format, интерфейс Ивмдрменкриптскаттер
- Интерфейс Ивмдрменкриптскаттер Windows Media Format, метод Енкриптскаттер
topic_type:
- apiref
api_name:
- IWMDRMEncryptScatter.EncryptScatter
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58b2d1d6182aed55b60aa1cedfbce5dd870691bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105656873"
---
# <a name="iwmdrmencryptscatterencryptscatter-method"></a><span data-ttu-id="d4c3c-106">Метод Ивмдрменкриптскаттер:: Енкриптскаттер</span><span class="sxs-lookup"><span data-stu-id="d4c3c-106">IWMDRMEncryptScatter::EncryptScatter method</span></span>

<span data-ttu-id="d4c3c-107">Метод **енкриптскаттер** выполняет расшифровку и шифрование данных.</span><span class="sxs-lookup"><span data-stu-id="d4c3c-107">The **EncryptScatter** method unscrambles and encrypts data.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4c3c-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d4c3c-108">Syntax</span></span>


```C++
HRESULT EncryptScatter(
  [in]  DWORD                       cBlocks,
  [in]  WMDRM_ENCRYPT_SCATTER_BLOCK *rgBlocks,
  [in]  WMDRMCryptoData             *pWMCryptoData,
  [in]  DWORD                       cbOutput,
  [out] BYTE                        *pbOutput
);
```



## <a name="parameters"></a><span data-ttu-id="d4c3c-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="d4c3c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4c3c-110">*кблоккс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d4c3c-110">*cBlocks* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4c3c-111">Число элементов в массиве *ргблоккс* .</span><span class="sxs-lookup"><span data-stu-id="d4c3c-111">Number of elements in the *rgBlocks* array.</span></span>

</dd> <dt>

<span data-ttu-id="d4c3c-112">*ргблоккс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d4c3c-112">*rgBlocks* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4c3c-113">Массив из одной или нескольких [**структур \_ \_ \_ блоков с шифрованием WMDRM**](wmdrm-encrypt-scatter-block.md) .</span><span class="sxs-lookup"><span data-stu-id="d4c3c-113">Array of one or more [**WMDRM\_ENCRYPT\_SCATTER\_BLOCK**](wmdrm-encrypt-scatter-block.md) structures.</span></span> <span data-ttu-id="d4c3c-114">Каждый элемент описывает блок данных для расшифровки и шифрования.</span><span class="sxs-lookup"><span data-stu-id="d4c3c-114">Each element describes a block of data to be unscrambled and encrypted.</span></span>

</dd> <dt>

<span data-ttu-id="d4c3c-115">*пвмкриптодата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d4c3c-115">*pWMCryptoData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4c3c-116">Указатель на структуру [**вмдрмкриптодата**](wmdrmcryptodata.md) , содержащую параметры шифрования.</span><span class="sxs-lookup"><span data-stu-id="d4c3c-116">Pointer to a [**WMDRMCryptoData**](wmdrmcryptodata.md) structure that contains encryption parameters.</span></span> <span data-ttu-id="d4c3c-117">Задайте для параметра **значение NULL** , чтобы использовать параметры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d4c3c-117">Set to **NULL** to use the default parameters.</span></span>

</dd> <dt>

<span data-ttu-id="d4c3c-118">*кбаутпут* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d4c3c-118">*cbOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4c3c-119">Размер буфера выходных данных, переданного как *пбаутпут*.</span><span class="sxs-lookup"><span data-stu-id="d4c3c-119">Size of the output data buffer passed as *pbOutput*.</span></span>

</dd> <dt>

<span data-ttu-id="d4c3c-120">*пбаутпут* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d4c3c-120">*pbOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d4c3c-121">Выходной буфер.</span><span class="sxs-lookup"><span data-stu-id="d4c3c-121">Output buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4c3c-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d4c3c-122">Return value</span></span>

<span data-ttu-id="d4c3c-123">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="d4c3c-123">The method returns an **HRESULT**.</span></span> <span data-ttu-id="d4c3c-124">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="d4c3c-124">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="d4c3c-125">Код возврата</span><span class="sxs-lookup"><span data-stu-id="d4c3c-125">Return code</span></span>                                                                          | <span data-ttu-id="d4c3c-126">Описание</span><span class="sxs-lookup"><span data-stu-id="d4c3c-126">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="d4c3c-127"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="d4c3c-127"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="d4c3c-128">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="d4c3c-128">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d4c3c-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d4c3c-129">Remarks</span></span>

<span data-ttu-id="d4c3c-130">Нет.</span><span class="sxs-lookup"><span data-stu-id="d4c3c-130">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4c3c-131">Требования</span><span class="sxs-lookup"><span data-stu-id="d4c3c-131">Requirements</span></span>



| <span data-ttu-id="d4c3c-132">Требование</span><span class="sxs-lookup"><span data-stu-id="d4c3c-132">Requirement</span></span> | <span data-ttu-id="d4c3c-133">Значение</span><span class="sxs-lookup"><span data-stu-id="d4c3c-133">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d4c3c-134">Header</span><span class="sxs-lookup"><span data-stu-id="d4c3c-134">Header</span></span><br/> | <dl> <span data-ttu-id="d4c3c-135"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4c3c-135"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4c3c-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d4c3c-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4c3c-137">**инитенкриптскаттер**</span><span class="sxs-lookup"><span data-stu-id="d4c3c-137">**InitEncryptScatter**</span></span>](iwmdrmencryptscatter-initencryptscatter.md)
</dt> <dt>

[<span data-ttu-id="d4c3c-138">**Интерфейс Ивмдрменкриптскаттер**</span><span class="sxs-lookup"><span data-stu-id="d4c3c-138">**IWMDRMEncryptScatter Interface**</span></span>](iwmdrmencryptscatter.md)
</dt> </dl>

 

 





