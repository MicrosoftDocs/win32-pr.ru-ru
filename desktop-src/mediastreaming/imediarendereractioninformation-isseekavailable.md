---
title: Имедиарендерерактионинформатион Иссикаваилабле, метод
description: Получает значение, указывающее, принимает ли ДМР метод Сикасинк в настоящий момент.
ms.assetid: F0817184-70F2-43AC-A2BE-A15F4B195085
keywords:
- API потоковой передачи мультимедиа метода Иссикаваилабле
- API потоковой передачи мультимедиа метода Иссикаваилабле, интерфейс Имедиарендерерактионинформатион
- API потоковой передачи мультимедиа интерфейса Имедиарендерерактионинформатион, метод Иссикаваилабле
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsSeekAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 700afb72efbab01bbd3a8f5e15fa444eb6b06272
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103890588"
---
# <a name="imediarendereractioninformationisseekavailable-method"></a><span data-ttu-id="7f288-106">Метод Имедиарендерерактионинформатион:: Иссикаваилабле</span><span class="sxs-lookup"><span data-stu-id="7f288-106">IMediaRendererActionInformation::IsSeekAvailable method</span></span>

<span data-ttu-id="7f288-107">Получает значение, указывающее, принимает ли ДМР метод [**сикасинк**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-seekasync) в настоящий момент.</span><span class="sxs-lookup"><span data-stu-id="7f288-107">Retrieves a value that indicates whether the DMR is currently accepting the [**SeekAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-seekasync) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f288-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7f288-108">Syntax</span></span>


```C++
HRESULT IsSeekAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="7f288-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="7f288-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f288-110">*значение* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7f288-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7f288-111">Логическое значение, равное **true** , если ДМР в настоящее время принимает метод [**Сикасинк**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-seekasync) , и **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="7f288-111">A boolean value that is **True** if the DMR is currently accepting the [**SeekAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-seekasync) method and **False** if it is not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f288-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7f288-112">Return value</span></span>

<span data-ttu-id="7f288-113">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="7f288-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="7f288-114">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="7f288-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="7f288-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="7f288-115">Return code</span></span>                                                                          | <span data-ttu-id="7f288-116">Описание</span><span class="sxs-lookup"><span data-stu-id="7f288-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="7f288-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="7f288-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="7f288-118">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="7f288-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="7f288-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7f288-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f288-120">**имедиарендерерактионинформатион**</span><span class="sxs-lookup"><span data-stu-id="7f288-120">**IMediaRendererActionInformation**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

