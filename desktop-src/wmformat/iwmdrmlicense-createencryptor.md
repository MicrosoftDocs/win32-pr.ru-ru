---
title: Метод Ивмдрмлиценсе Креатинкриптор (Вмдрмсдк. h)
description: Метод Креатинкриптор создает объект шифратора, используя параметры текущей лицензии.
ms.assetid: 570ba898-e846-4981-8ea8-ce16f2dad68a
keywords:
- Формат Windows Media, Креатинкриптор метод
- Креатинкриптор метод Windows Media Format, интерфейс Ивмдрмлиценсе
- Интерфейс Ивмдрмлиценсе Windows Media Format, метод Креатинкриптор
topic_type:
- apiref
api_name:
- IWMDRMLicense.CreateEncryptor
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8031f412129f1d02cc4ef37c6af5f49a6c0b7532
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704476"
---
# <a name="iwmdrmlicensecreateencryptor-method"></a><span data-ttu-id="7d82a-106">Метод Ивмдрмлиценсе:: Креатинкриптор</span><span class="sxs-lookup"><span data-stu-id="7d82a-106">IWMDRMLicense::CreateEncryptor method</span></span>

<span data-ttu-id="7d82a-107">Метод **креатинкриптор** создает объект шифратора, используя параметры текущей лицензии.</span><span class="sxs-lookup"><span data-stu-id="7d82a-107">The **CreateEncryptor** method creates an encryptor object using the settings of the current license.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d82a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7d82a-108">Syntax</span></span>


```C++
HRESULT CreateEncryptor(
  [out] IWMDRMEncrypt **ppEncryptor
);
```



## <a name="parameters"></a><span data-ttu-id="7d82a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="7d82a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d82a-110">*ппенкриптор* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7d82a-110">*ppEncryptor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7d82a-111">Получает указатель на интерфейс [**ивмдрменкрипт**](iwmdrmencrypt.md) только что созданного объекта.</span><span class="sxs-lookup"><span data-stu-id="7d82a-111">Receives a pointer to the [**IWMDRMEncrypt**](iwmdrmencrypt.md) interface of the newly created object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d82a-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7d82a-112">Return value</span></span>

<span data-ttu-id="7d82a-113">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="7d82a-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="7d82a-114">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="7d82a-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="7d82a-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="7d82a-115">Return code</span></span>                                                                                                | <span data-ttu-id="7d82a-116">Описание</span><span class="sxs-lookup"><span data-stu-id="7d82a-116">Description</span></span>                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="7d82a-117"><dt>**\_ \_ \_ \_ слишком \_ маленький Рив для NS E DRM**</dt></span><span class="sxs-lookup"><span data-stu-id="7d82a-117"><dt>**NS\_E\_DRM\_RIV\_TOO\_SMALL**</dt></span></span> </dl> | <span data-ttu-id="7d82a-118">Требуется обновленный список отзыва содержимого.</span><span class="sxs-lookup"><span data-stu-id="7d82a-118">An updated content revocation list is needed.</span></span><br/> |
| <dl> <span data-ttu-id="7d82a-119"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="7d82a-119"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="7d82a-120">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="7d82a-120">The method succeeded.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="7d82a-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7d82a-121">Remarks</span></span>

<span data-ttu-id="7d82a-122">Нет.</span><span class="sxs-lookup"><span data-stu-id="7d82a-122">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d82a-123">Требования</span><span class="sxs-lookup"><span data-stu-id="7d82a-123">Requirements</span></span>



| <span data-ttu-id="7d82a-124">Требование</span><span class="sxs-lookup"><span data-stu-id="7d82a-124">Requirement</span></span> | <span data-ttu-id="7d82a-125">Значение</span><span class="sxs-lookup"><span data-stu-id="7d82a-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7d82a-126">Header</span><span class="sxs-lookup"><span data-stu-id="7d82a-126">Header</span></span><br/> | <dl> <span data-ttu-id="7d82a-127"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d82a-127"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d82a-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7d82a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d82a-129">**CreateDecryptor**</span><span class="sxs-lookup"><span data-stu-id="7d82a-129">**CreateDecryptor**</span></span>](iwmdrmlicense-createdecryptor.md)
</dt> <dt>

[<span data-ttu-id="7d82a-130">**Интерфейс Ивмдрмлиценсе**</span><span class="sxs-lookup"><span data-stu-id="7d82a-130">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 





