---
title: Имедиарендерер Исвидеосуппортед, метод
description: Получает значение, указывающее, поддерживает ли ДМР воспроизведение видеосодержимого.
ms.assetid: AE9A14D0-A7A2-4A71-9454-06A05C7D85F9
keywords:
- API потоковой передачи мультимедиа метода Исвидеосуппортед
- API потоковой передачи мультимедиа метода Исвидеосуппортед, интерфейс Имедиарендерер
- API потоковой передачи мультимедиа интерфейса Имедиарендерер, метод Исвидеосуппортед
topic_type:
- apiref
api_name:
- IMediaRenderer.IsVideoSupported
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9808841bf60a384d6a4566e75f53248b0f86338c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104334627"
---
# <a name="imediarendererisvideosupported-method"></a><span data-ttu-id="2ef89-106">Метод Имедиарендерер:: Исвидеосуппортед</span><span class="sxs-lookup"><span data-stu-id="2ef89-106">IMediaRenderer::IsVideoSupported method</span></span>

<span data-ttu-id="2ef89-107">Получает значение, указывающее, поддерживает ли ДМР воспроизведение видеосодержимого.</span><span class="sxs-lookup"><span data-stu-id="2ef89-107">Retrieves a value that indicates whether the DMR is capable of playing video content.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ef89-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2ef89-108">Syntax</span></span>


```C++
HRESULT IsVideoSupported(
  [out] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="2ef89-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="2ef89-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ef89-110">*значение* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2ef89-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2ef89-111">Логическое значение, равное **true** , если ДМР способен воспроизводить видеосодержимое, и **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="2ef89-111">A boolean value that is **True** if the DMR is capable of playing video content and **False** if it is not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ef89-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2ef89-112">Return value</span></span>

<span data-ttu-id="2ef89-113">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="2ef89-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="2ef89-114">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="2ef89-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="2ef89-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="2ef89-115">Return code</span></span>                                                                          | <span data-ttu-id="2ef89-116">Описание</span><span class="sxs-lookup"><span data-stu-id="2ef89-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="2ef89-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="2ef89-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="2ef89-118">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="2ef89-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="2ef89-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2ef89-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ef89-120">**имедиарендерер**</span><span class="sxs-lookup"><span data-stu-id="2ef89-120">**IMediaRenderer**</span></span>](imediarenderer.md)
</dt> </dl>

 

 





