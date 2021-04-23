---
title: Имедиарендерер Исаудиосуппортед, метод
description: Получает значение, указывающее, способен ли ДМР воспроизведение звукового содержимого.
ms.assetid: D5F0C4ED-5778-4388-A7BD-E3923145D663
keywords:
- API потоковой передачи мультимедиа метода Исаудиосуппортед
- API потоковой передачи мультимедиа метода Исаудиосуппортед, интерфейс Имедиарендерер
- API потоковой передачи мультимедиа интерфейса Имедиарендерер, метод Исаудиосуппортед
topic_type:
- apiref
api_name:
- IMediaRenderer.IsAudioSupported
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4f7670d0a2818cf5518bee0b2586531caeea20fd
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "105719069"
---
# <a name="imediarendererisaudiosupported-method"></a><span data-ttu-id="e2fe0-106">Метод Имедиарендерер:: Исаудиосуппортед</span><span class="sxs-lookup"><span data-stu-id="e2fe0-106">IMediaRenderer::IsAudioSupported method</span></span>

<span data-ttu-id="e2fe0-107">Получает значение, указывающее, способен ли ДМР воспроизведение звукового содержимого.</span><span class="sxs-lookup"><span data-stu-id="e2fe0-107">Retrieves a value that indicates whether the DMR is capable of playing audio content.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2fe0-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e2fe0-108">Syntax</span></span>


```C++
HRESULT IsAudioSupported(
  [out] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="e2fe0-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="e2fe0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2fe0-110">*значение* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e2fe0-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e2fe0-111">Логическое значение, равное **true** , если ДМР способен воспроизводить аудио-содержимое, и **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="e2fe0-111">A boolean value that is **True** if the DMR is capable of playing audio content and **False** if it is not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2fe0-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e2fe0-112">Return value</span></span>

<span data-ttu-id="e2fe0-113">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="e2fe0-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="e2fe0-114">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="e2fe0-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="e2fe0-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="e2fe0-115">Return code</span></span>                                                                          | <span data-ttu-id="e2fe0-116">Описание</span><span class="sxs-lookup"><span data-stu-id="e2fe0-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="e2fe0-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="e2fe0-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="e2fe0-118">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="e2fe0-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="e2fe0-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e2fe0-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2fe0-120">**имедиарендерер**</span><span class="sxs-lookup"><span data-stu-id="e2fe0-120">**IMediaRenderer**</span></span>](imediarenderer.md)
</dt> </dl>

 

 





