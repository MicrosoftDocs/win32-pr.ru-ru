---
title: Имедиарендерерактионинформатион Исстопаваилабле, метод
description: Получает значение, указывающее, принимает ли ДМР метод Стопасинк в настоящий момент.
ms.assetid: 6EE8F56D-2A5A-49B0-A9B2-0A7EE57D03FD
keywords:
- API потоковой передачи мультимедиа метода Исстопаваилабле
- API потоковой передачи мультимедиа метода Исстопаваилабле, интерфейс Имедиарендерерактионинформатион
- API потоковой передачи мультимедиа интерфейса Имедиарендерерактионинформатион, метод Исстопаваилабле
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsStopAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5e0a031bafc9a755dfec2498f4e2a52cdd9ef5b1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104133815"
---
# <a name="imediarendereractioninformationisstopavailable-method"></a><span data-ttu-id="c948e-106">Метод Имедиарендерерактионинформатион:: Исстопаваилабле</span><span class="sxs-lookup"><span data-stu-id="c948e-106">IMediaRendererActionInformation::IsStopAvailable method</span></span>

<span data-ttu-id="c948e-107">Получает значение, указывающее, принимает ли ДМР метод [**стопасинк**](imediarenderer-stopasync.md) в настоящий момент.</span><span class="sxs-lookup"><span data-stu-id="c948e-107">Retrieves a value that indicates whether the DMR is currently accepting the [**StopAsync**](imediarenderer-stopasync.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c948e-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c948e-108">Syntax</span></span>


```C++
HRESULT IsStopAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="c948e-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="c948e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c948e-110">*значение* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c948e-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c948e-111">Логическое значение, равное **true** , если ДМР в настоящее время принимает метод [**Стопасинк**](imediarenderer-stopasync.md) , и **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="c948e-111">A boolean value that is **True** if the DMR is currently accepting the [**StopAsync**](imediarenderer-stopasync.md) method and **False** if it is not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c948e-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c948e-112">Return value</span></span>

<span data-ttu-id="c948e-113">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="c948e-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="c948e-114">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="c948e-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="c948e-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="c948e-115">Return code</span></span>                                                                          | <span data-ttu-id="c948e-116">Описание</span><span class="sxs-lookup"><span data-stu-id="c948e-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="c948e-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="c948e-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="c948e-118">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="c948e-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="c948e-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c948e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c948e-120">**имедиарендерерактионинформатион**</span><span class="sxs-lookup"><span data-stu-id="c948e-120">**IMediaRendererActionInformation**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

