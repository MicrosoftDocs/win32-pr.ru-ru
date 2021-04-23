---
title: Метод Ивмдрменкриптскаттер Инитенкриптскаттер (Вмдрмсдк. h)
description: Метод Инитенкриптскаттер инициализирует интерфейс Ивмдрменкриптскаттер для использования.
ms.assetid: c5f2fa14-9465-4c53-bc42-ffcec34af083
keywords:
- Формат Windows Media, Инитенкриптскаттер метод
- Инитенкриптскаттер метод Windows Media Format, интерфейс Ивмдрменкриптскаттер
- Интерфейс Ивмдрменкриптскаттер Windows Media Format, метод Инитенкриптскаттер
topic_type:
- apiref
api_name:
- IWMDRMEncryptScatter.InitEncryptScatter
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef788ecbe85defc7d3593f0c12c035e516f095eb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657374"
---
# <a name="iwmdrmencryptscatterinitencryptscatter-method"></a><span data-ttu-id="88946-106">Метод Ивмдрменкриптскаттер:: Инитенкриптскаттер</span><span class="sxs-lookup"><span data-stu-id="88946-106">IWMDRMEncryptScatter::InitEncryptScatter method</span></span>

<span data-ttu-id="88946-107">Метод **инитенкриптскаттер** инициализирует интерфейс **ивмдрменкриптскаттер** для использования.</span><span class="sxs-lookup"><span data-stu-id="88946-107">The **InitEncryptScatter** method initializes the **IWMDRMEncryptScatter** interface for use.</span></span>

## <a name="syntax"></a><span data-ttu-id="88946-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="88946-108">Syntax</span></span>


```C++
HRESULT InitEncryptScatter(
  [in] DWORD                      cStreams,
  [in] WMDRM_ENCRYPT_SCATTER_INFO *rgInfos
);
```



## <a name="parameters"></a><span data-ttu-id="88946-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="88946-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88946-110">*кстреамс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="88946-110">*cStreams* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88946-111">Число элементов в массиве *ргинфос* .</span><span class="sxs-lookup"><span data-stu-id="88946-111">Number of elements in the *rgInfos* array.</span></span> <span data-ttu-id="88946-112">Это также число потоков, включенных в зашифрованные данные.</span><span class="sxs-lookup"><span data-stu-id="88946-112">This is also the number of streams that are included in the data to be encrypted.</span></span>

</dd> <dt>

<span data-ttu-id="88946-113">*ргинфос* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="88946-113">*rgInfos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88946-114">Массив из одной или нескольких [**структур \_ \_ \_ сведений о шифрующей**](wmdrm-encrypt-scatter-info.md) подразделении WMDRM.</span><span class="sxs-lookup"><span data-stu-id="88946-114">Array of one or more [**WMDRM\_ENCRYPT\_SCATTER\_INFO**](wmdrm-encrypt-scatter-info.md) structures.</span></span> <span data-ttu-id="88946-115">Каждый элемент содержит сведения о шифровании для потока.</span><span class="sxs-lookup"><span data-stu-id="88946-115">Each element contains encryption information for a stream.</span></span> <span data-ttu-id="88946-116">Число элементов в этом массиве должно быть равно значению параметра *кстреамс*.</span><span class="sxs-lookup"><span data-stu-id="88946-116">The number of elements in this array must be equal to the value of *cStreams*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88946-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="88946-117">Return value</span></span>

<span data-ttu-id="88946-118">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="88946-118">The method returns an **HRESULT**.</span></span> <span data-ttu-id="88946-119">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="88946-119">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="88946-120">Код возврата</span><span class="sxs-lookup"><span data-stu-id="88946-120">Return code</span></span>                                                                          | <span data-ttu-id="88946-121">Описание</span><span class="sxs-lookup"><span data-stu-id="88946-121">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="88946-122"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="88946-122"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="88946-123">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="88946-123">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="88946-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="88946-124">Remarks</span></span>

<span data-ttu-id="88946-125">Нет.</span><span class="sxs-lookup"><span data-stu-id="88946-125">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="88946-126">Требования</span><span class="sxs-lookup"><span data-stu-id="88946-126">Requirements</span></span>



| <span data-ttu-id="88946-127">Требование</span><span class="sxs-lookup"><span data-stu-id="88946-127">Requirement</span></span> | <span data-ttu-id="88946-128">Значение</span><span class="sxs-lookup"><span data-stu-id="88946-128">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="88946-129">Header</span><span class="sxs-lookup"><span data-stu-id="88946-129">Header</span></span><br/> | <dl> <span data-ttu-id="88946-130"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="88946-130"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88946-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="88946-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88946-132">**енкриптскаттер**</span><span class="sxs-lookup"><span data-stu-id="88946-132">**EncryptScatter**</span></span>](iwmdrmencryptscatter-encryptscatter.md)
</dt> <dt>

[<span data-ttu-id="88946-133">**Интерфейс Ивмдрменкриптскаттер**</span><span class="sxs-lookup"><span data-stu-id="88946-133">**IWMDRMEncryptScatter Interface**</span></span>](iwmdrmencryptscatter.md)
</dt> </dl>

 

 





