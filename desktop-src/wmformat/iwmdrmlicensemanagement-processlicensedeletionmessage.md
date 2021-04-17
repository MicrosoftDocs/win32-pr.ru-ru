---
title: Метод Ивмдрмлиценсеманажемент Процесслиценседелетионмессаже (Вмдрмсдк. h)
description: Метод Процесслиценседелетион удаляет лицензию, которая была импортирована для содержимого, изначально защищенного с помощью другой системы защиты содержимого.
ms.assetid: 478dd156-feb8-4eda-9d3a-35db3e65c227
keywords:
- Формат Windows Media, Процесслиценседелетионмессаже метод
- Процесслиценседелетионмессаже метод Windows Media Format, интерфейс Ивмдрмлиценсеманажемент
- Интерфейс Ивмдрмлиценсеманажемент Windows Media Format, метод Процесслиценседелетионмессаже
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.ProcessLicenseDeletionMessage
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9338c1bc4ef78e658cc25ab95f5c50556af3ed09
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717902"
---
# <a name="iwmdrmlicensemanagementprocesslicensedeletionmessage-method"></a><span data-ttu-id="f481f-106">Ивмдрмлиценсеманажемент: метод:P Роцесслиценседелетионмессаже</span><span class="sxs-lookup"><span data-stu-id="f481f-106">IWMDRMLicenseManagement::ProcessLicenseDeletionMessage method</span></span>

<span data-ttu-id="f481f-107">Метод **процесслиценседелетион** удаляет лицензию, которая была импортирована для содержимого, изначально защищенного с помощью другой системы защиты содержимого.</span><span class="sxs-lookup"><span data-stu-id="f481f-107">The **ProcessLicenseDeletion** method deletes a license that was imported for content originally protected with another content protection system.</span></span>

## <a name="syntax"></a><span data-ttu-id="f481f-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f481f-108">Syntax</span></span>


```C++
HRESULT ProcessLicenseDeletionMessage(
  [in] BSTR bstrDeletionMessage
);
```



## <a name="parameters"></a><span data-ttu-id="f481f-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="f481f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f481f-110">*бстрделетионмессаже* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f481f-110">*bstrDeletionMessage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f481f-111">Сообщение, идентифицирующее удаляемую лицензию.</span><span class="sxs-lookup"><span data-stu-id="f481f-111">Message identifying the license to delete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f481f-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f481f-112">Return value</span></span>

<span data-ttu-id="f481f-113">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="f481f-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="f481f-114">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="f481f-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="f481f-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="f481f-115">Return code</span></span>                                                                          | <span data-ttu-id="f481f-116">Описание</span><span class="sxs-lookup"><span data-stu-id="f481f-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="f481f-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="f481f-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="f481f-118">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="f481f-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f481f-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f481f-119">Remarks</span></span>

<span data-ttu-id="f481f-120">Нет.</span><span class="sxs-lookup"><span data-stu-id="f481f-120">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="f481f-121">Требования</span><span class="sxs-lookup"><span data-stu-id="f481f-121">Requirements</span></span>



| <span data-ttu-id="f481f-122">Требование</span><span class="sxs-lookup"><span data-stu-id="f481f-122">Requirement</span></span> | <span data-ttu-id="f481f-123">Значение</span><span class="sxs-lookup"><span data-stu-id="f481f-123">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f481f-124">Header</span><span class="sxs-lookup"><span data-stu-id="f481f-124">Header</span></span><br/> | <dl> <span data-ttu-id="f481f-125"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="f481f-125"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f481f-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f481f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f481f-127">**Интерфейс Ивмдрмлиценсеманажемент**</span><span class="sxs-lookup"><span data-stu-id="f481f-127">**IWMDRMLicenseManagement Interface**</span></span>](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





