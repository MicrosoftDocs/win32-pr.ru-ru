---
title: Идрмстатускаллбакк OnStatus, метод
description: Метод OnStatus получает сообщения о состоянии от асинхронных процессов DRM.
ms.assetid: 2a128088-0924-4c54-b08d-a1c7ea91e541
keywords:
- Метод OnStatus формат Windows Media
- Метод OnStatus формат Windows Media Format, интерфейс Идрмстатускаллбакк
- Интерфейс Идрмстатускаллбакк Windows Media Format, метод OnStatus
topic_type:
- apiref
api_name:
- IDRMStatusCallback.OnStatus
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 754d59d74fb0365f423243e92565ac17b46628a5
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104068860"
---
# <a name="idrmstatuscallbackonstatus-method"></a><span data-ttu-id="871aa-106">Метод Идрмстатускаллбакк:: OnStatus</span><span class="sxs-lookup"><span data-stu-id="871aa-106">IDRMStatusCallback::OnStatus method</span></span>

<span data-ttu-id="871aa-107">Метод **OnStatus** получает сообщения о состоянии от асинхронных процессов DRM.</span><span class="sxs-lookup"><span data-stu-id="871aa-107">The **OnStatus** method receives status messages from asynchronous DRM processes.</span></span>

## <a name="syntax"></a><span data-ttu-id="871aa-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="871aa-108">Syntax</span></span>


```C++
HRESULT OnStatus(
  [in] MSDRM_STATUS      Status,
  [in] HRESULT           hr,
  [in] DRM_ATTR_DATATYPE dwType,
  [in] BYTE              *pValue,
  [in] void              *pvContext
);
```



## <a name="parameters"></a><span data-ttu-id="871aa-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="871aa-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="871aa-110">*Состояние* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="871aa-110">*Status* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="871aa-111">Код состояния.</span><span class="sxs-lookup"><span data-stu-id="871aa-111">Status code.</span></span> <span data-ttu-id="871aa-112">Коды сообщений определяются в типе **перечисления \_ состояния Msdrm** .</span><span class="sxs-lookup"><span data-stu-id="871aa-112">Message codes are defined in the **MSDRM\_STATUS** enumeration type.</span></span>

</dd> <dt>

<span data-ttu-id="871aa-113">*HR* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="871aa-113">*hr* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="871aa-114">Код возврата, который поддерживает сообщение о состоянии.</span><span class="sxs-lookup"><span data-stu-id="871aa-114">Return code that supports the status message.</span></span>

</dd> <dt>

<span data-ttu-id="871aa-115">*двтипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="871aa-115">*dwType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="871aa-116">Тип данных, на который указывает *pValue*.</span><span class="sxs-lookup"><span data-stu-id="871aa-116">Type of the data pointed to by *pValue*.</span></span> <span data-ttu-id="871aa-117">Задайте одно из значений перечисления [**\_ \_ DATATYPE attr DRM**](drm-attr-datatype.md) .</span><span class="sxs-lookup"><span data-stu-id="871aa-117">Set to one of the values of the [**DRM\_ATTR\_DATATYPE**](drm-attr-datatype.md) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="871aa-118">*pValue* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="871aa-118">*pValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="871aa-119">Указатель на данные, связанные с сообщением о состоянии.</span><span class="sxs-lookup"><span data-stu-id="871aa-119">Pointer to data related to the status message.</span></span> <span data-ttu-id="871aa-120">Тип данных определяется значением параметра *двтипе* .</span><span class="sxs-lookup"><span data-stu-id="871aa-120">The type of data is determined by the value of the *dwType* parameter.</span></span> <span data-ttu-id="871aa-121">Дополнительные сведения см. в описании перечисления [**\_ \_ DATATYPE attr DRM**](drm-attr-datatype.md) .</span><span class="sxs-lookup"><span data-stu-id="871aa-121">For more information, see the [**DRM\_ATTR\_DATATYPE**](drm-attr-datatype.md) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="871aa-122">*пвконтекст* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="871aa-122">*pvContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="871aa-123">Необязательный параметр, который можно использовать для обнаружения объекта, отправившего сообщение.</span><span class="sxs-lookup"><span data-stu-id="871aa-123">Optional parameter that can be used to identify the object that sent the message.</span></span> <span data-ttu-id="871aa-124">Установив *пвконтекст* при регистрации этого обратного вызова, можно использовать один и тот же обратный вызов для обработки нескольких асинхронных процессов.</span><span class="sxs-lookup"><span data-stu-id="871aa-124">By setting *pvContext* when you register this callback, you can use the same callback to handle multiple asynchronous processes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="871aa-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="871aa-125">Return value</span></span>

<span data-ttu-id="871aa-126">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="871aa-126">The method returns an **HRESULT**.</span></span> <span data-ttu-id="871aa-127">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="871aa-127">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="871aa-128">Код возврата</span><span class="sxs-lookup"><span data-stu-id="871aa-128">Return code</span></span>                                                                          | <span data-ttu-id="871aa-129">Описание</span><span class="sxs-lookup"><span data-stu-id="871aa-129">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="871aa-130"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="871aa-130"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="871aa-131">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="871aa-131">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="871aa-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="871aa-132">Remarks</span></span>

<span data-ttu-id="871aa-133">Нет.</span><span class="sxs-lookup"><span data-stu-id="871aa-133">None.</span></span>

## <a name="see-also"></a><span data-ttu-id="871aa-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="871aa-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="871aa-135">**\_тип данных attr с атрибутом DRM \_**</span><span class="sxs-lookup"><span data-stu-id="871aa-135">**DRM\_ATTR\_DATATYPE**</span></span>](drm-attr-datatype.md)
</dt> <dt>

[<span data-ttu-id="871aa-136">**Интерфейс Идрмстатускаллбакк**</span><span class="sxs-lookup"><span data-stu-id="871aa-136">**IDRMStatusCallback Interface**</span></span>](idrmstatuscallback.md)
</dt> </dl>

 

 





