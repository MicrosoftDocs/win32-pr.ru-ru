---
title: Имедиарендерер Исимажесуппортед, метод
description: Получает значение, указывающее, поддерживает ли ДМР отображение изображений.
ms.assetid: 3941789B-0FFF-4F00-B63C-2586B39B6546
keywords:
- API потоковой передачи мультимедиа метода Исимажесуппортед
- API потоковой передачи мультимедиа метода Исимажесуппортед, интерфейс Имедиарендерер
- API потоковой передачи мультимедиа интерфейса Имедиарендерер, метод Исимажесуппортед
topic_type:
- apiref
api_name:
- IMediaRenderer.IsImageSupported
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dd68f4d758c67b81c1eefcbc83a0f0a505ec27b6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "105710205"
---
# <a name="imediarendererisimagesupported-method"></a><span data-ttu-id="82562-106">Метод Имедиарендерер:: Исимажесуппортед</span><span class="sxs-lookup"><span data-stu-id="82562-106">IMediaRenderer::IsImageSupported method</span></span>

<span data-ttu-id="82562-107">Получает значение, указывающее, поддерживает ли ДМР отображение изображений.</span><span class="sxs-lookup"><span data-stu-id="82562-107">Retrieves a value that indicates whether the DMR is capable of displaying images.</span></span>

## <a name="syntax"></a><span data-ttu-id="82562-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="82562-108">Syntax</span></span>


```C++
HRESULT IsImageSupported(
  [out] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="82562-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="82562-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82562-110">*значение* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="82562-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="82562-111">Логическое значение, равное **true** , если ДМР способен отображать изображения и **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="82562-111">A boolean value that is **True** if the DMR is capable of displaying images and **False** if it is not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82562-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="82562-112">Return value</span></span>

<span data-ttu-id="82562-113">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="82562-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="82562-114">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="82562-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="82562-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="82562-115">Return code</span></span>                                                                          | <span data-ttu-id="82562-116">Описание</span><span class="sxs-lookup"><span data-stu-id="82562-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="82562-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="82562-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="82562-118">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="82562-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="82562-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="82562-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82562-120">**имедиарендерер**</span><span class="sxs-lookup"><span data-stu-id="82562-120">**IMediaRenderer**</span></span>](imediarenderer.md)
</dt> </dl>

 

 





