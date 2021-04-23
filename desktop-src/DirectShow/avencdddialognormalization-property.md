---
description: Задает уровень нормализации диалогового окна в децибел (dB) в потоке цифрового звука Dolby. Это свойство применяется к кодировщикам цифрового аудио Dolby.
ms.assetid: c347f8b2-5132-45d6-af66-43d3c409b0d7
title: Свойство Авенкдддиалогнормализатион (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 586f241dc8d032767ecb2678c1ee5704dc20e0ef
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495624"
---
# <a name="avencdddialognormalization-property"></a><span data-ttu-id="39807-104">Авенкдддиалогнормализатион, свойство</span><span class="sxs-lookup"><span data-stu-id="39807-104">AVEncDDDialogNormalization property</span></span>

<span data-ttu-id="39807-105">Задает уровень нормализации диалогового окна в децибел (dB) в потоке цифрового звука Dolby.</span><span class="sxs-lookup"><span data-stu-id="39807-105">Specifies the dialog normalization level, in decibels (dB), in a Dolby Digital audio stream.</span></span> <span data-ttu-id="39807-106">Это свойство применяется к кодировщикам цифрового аудио Dolby.</span><span class="sxs-lookup"><span data-stu-id="39807-106">This property applies to Dolby Digital audio encoders.</span></span>

<span data-ttu-id="39807-107">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="39807-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="39807-108">Тип данных</span><span class="sxs-lookup"><span data-stu-id="39807-108">Data type</span></span>

<span data-ttu-id="39807-109">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="39807-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="39807-110">GUID свойства</span><span class="sxs-lookup"><span data-stu-id="39807-110">Property GUID</span></span>

<span data-ttu-id="39807-111">**КОДЕКАПИ \_ авенкдддиалогнормализатион**</span><span class="sxs-lookup"><span data-stu-id="39807-111">**CODECAPI\_AVEncDDDialogNormalization**</span></span>

## <a name="property-value"></a><span data-ttu-id="39807-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="39807-112">Property value</span></span>

<span data-ttu-id="39807-113">Это свойство имеет линейный Диапазон значений.</span><span class="sxs-lookup"><span data-stu-id="39807-113">This property has a linear range of values.</span></span> <span data-ttu-id="39807-114">Чтобы получить поддерживаемый диапазон, вызовите метод [**икодекапи:: жетпараметерранже**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="39807-114">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

## <a name="requirements"></a><span data-ttu-id="39807-115">Требования</span><span class="sxs-lookup"><span data-stu-id="39807-115">Requirements</span></span>



| <span data-ttu-id="39807-116">Требование</span><span class="sxs-lookup"><span data-stu-id="39807-116">Requirement</span></span> | <span data-ttu-id="39807-117">Значение</span><span class="sxs-lookup"><span data-stu-id="39807-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="39807-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="39807-118">Minimum supported client</span></span><br/> | <span data-ttu-id="39807-119">Приложения Windows 2000 Professional \[ классические приложения \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="39807-119">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="39807-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="39807-120">Minimum supported server</span></span><br/> | <span data-ttu-id="39807-121">\[Приложения UWP для классических приложений Windows 2000 \|\]</span><span class="sxs-lookup"><span data-stu-id="39807-121">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="39807-122">Header</span><span class="sxs-lookup"><span data-stu-id="39807-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="39807-123"><dt>Кодекапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="39807-123"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39807-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="39807-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39807-125">Свойства кодека API</span><span class="sxs-lookup"><span data-stu-id="39807-125">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="39807-126">**Интерфейс Икодекапи**</span><span class="sxs-lookup"><span data-stu-id="39807-126">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




