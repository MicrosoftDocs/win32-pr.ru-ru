---
title: Метод Ивмдрмлиценсе CreateDecryptor (Вмдрмсдк. h)
description: Метод CreateDecryptor создает объект дешифратора, используя параметры текущей лицензии.
ms.assetid: 69b7f96b-a0d6-455e-8ef9-0faf9690cef1
keywords:
- Формат Windows Media, CreateDecryptor метод
- CreateDecryptor метод Windows Media Format, интерфейс Ивмдрмлиценсе
- Интерфейс Ивмдрмлиценсе Windows Media Format, метод CreateDecryptor
topic_type:
- apiref
api_name:
- IWMDRMLicense.CreateDecryptor
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e987e7ffa3390462889b128f390934f05e64cdff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105656872"
---
# <a name="iwmdrmlicensecreatedecryptor-method"></a><span data-ttu-id="88afc-106">Метод Ивмдрмлиценсе:: CreateDecryptor</span><span class="sxs-lookup"><span data-stu-id="88afc-106">IWMDRMLicense::CreateDecryptor method</span></span>

<span data-ttu-id="88afc-107">Метод **CreateDecryptor** создает объект дешифратора, используя параметры текущей лицензии.</span><span class="sxs-lookup"><span data-stu-id="88afc-107">The **CreateDecryptor** method creates a decryptor object using the settings of the current license.</span></span>

## <a name="syntax"></a><span data-ttu-id="88afc-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="88afc-108">Syntax</span></span>


```C++
HRESULT CreateDecryptor(
  [out] IWMDRMDecrypt **ppDecryptor
);
```



## <a name="parameters"></a><span data-ttu-id="88afc-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="88afc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88afc-110">*ппдекриптор* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="88afc-110">*ppDecryptor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="88afc-111">Получает указатель на интерфейс [**ивмдрмдекрипт**](iwmdrmdecrypt.md) только что созданного объекта.</span><span class="sxs-lookup"><span data-stu-id="88afc-111">Receives a pointer to the [**IWMDRMDecrypt**](iwmdrmdecrypt.md) interface of the newly created object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88afc-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="88afc-112">Return value</span></span>

<span data-ttu-id="88afc-113">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="88afc-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="88afc-114">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="88afc-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="88afc-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="88afc-115">Return code</span></span>                                                                                                | <span data-ttu-id="88afc-116">Описание</span><span class="sxs-lookup"><span data-stu-id="88afc-116">Description</span></span>                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="88afc-117"><dt>**\_ \_ \_ \_ слишком \_ маленький Рив для NS E DRM**</dt></span><span class="sxs-lookup"><span data-stu-id="88afc-117"><dt>**NS\_E\_DRM\_RIV\_TOO\_SMALL**</dt></span></span> </dl> | <span data-ttu-id="88afc-118">Требуется обновленный список отзыва содержимого.</span><span class="sxs-lookup"><span data-stu-id="88afc-118">An updated content revocation list is needed.</span></span><br/> |
| <dl> <span data-ttu-id="88afc-119"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="88afc-119"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="88afc-120">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="88afc-120">The method succeeded.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="88afc-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="88afc-121">Remarks</span></span>

<span data-ttu-id="88afc-122">Нет.</span><span class="sxs-lookup"><span data-stu-id="88afc-122">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="88afc-123">Требования</span><span class="sxs-lookup"><span data-stu-id="88afc-123">Requirements</span></span>



| <span data-ttu-id="88afc-124">Требование</span><span class="sxs-lookup"><span data-stu-id="88afc-124">Requirement</span></span> | <span data-ttu-id="88afc-125">Значение</span><span class="sxs-lookup"><span data-stu-id="88afc-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="88afc-126">Header</span><span class="sxs-lookup"><span data-stu-id="88afc-126">Header</span></span><br/> | <dl> <span data-ttu-id="88afc-127"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="88afc-127"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88afc-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="88afc-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88afc-129">**креатинкриптор**</span><span class="sxs-lookup"><span data-stu-id="88afc-129">**CreateEncryptor**</span></span>](iwmdrmlicense-createencryptor.md)
</dt> <dt>

[<span data-ttu-id="88afc-130">**Интерфейс Ивмдрмлиценсе**</span><span class="sxs-lookup"><span data-stu-id="88afc-130">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 





