---
title: Имедиарендерерактионинформатион Испаусеаваилабле, метод
description: Получает значение, указывающее, принимает ли ДМР метод Паусеасинк в настоящий момент.
ms.assetid: 095A664F-D974-410D-8741-87A171EDD071
keywords:
- API потоковой передачи мультимедиа метода Испаусеаваилабле
- API потоковой передачи мультимедиа метода Испаусеаваилабле, интерфейс Имедиарендерерактионинформатион
- API потоковой передачи мультимедиа интерфейса Имедиарендерерактионинформатион, метод Испаусеаваилабле
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsPauseAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9eb0b750f5a04528aef830d87376c276bdaf6674
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103890589"
---
# <a name="imediarendereractioninformationispauseavailable-method"></a><span data-ttu-id="31ce0-106">Метод Имедиарендерерактионинформатион:: Испаусеаваилабле</span><span class="sxs-lookup"><span data-stu-id="31ce0-106">IMediaRendererActionInformation::IsPauseAvailable method</span></span>

<span data-ttu-id="31ce0-107">Получает значение, указывающее, принимает ли ДМР метод [**паусеасинк**](imediarenderer-pauseasync.md) в настоящий момент.</span><span class="sxs-lookup"><span data-stu-id="31ce0-107">Retrieves a value that indicates whether the DMR is currently accepting the [**PauseAsync**](imediarenderer-pauseasync.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="31ce0-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="31ce0-108">Syntax</span></span>


```C++
HRESULT IsPauseAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="31ce0-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="31ce0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31ce0-110">*значение* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="31ce0-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="31ce0-111">Логическое значение, равное **true** , если ДМР в настоящее время принимает метод [**Паусеасинк**](imediarenderer-pauseasync.md) , и **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="31ce0-111">A boolean value that is **True** if the DMR is currently accepting the [**PauseAsync**](imediarenderer-pauseasync.md) method and **False** if it is not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31ce0-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="31ce0-112">Return value</span></span>

<span data-ttu-id="31ce0-113">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="31ce0-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="31ce0-114">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="31ce0-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="31ce0-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="31ce0-115">Return code</span></span>                                                                          | <span data-ttu-id="31ce0-116">Описание</span><span class="sxs-lookup"><span data-stu-id="31ce0-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="31ce0-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="31ce0-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="31ce0-118">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="31ce0-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="31ce0-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="31ce0-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31ce0-120">**имедиарендерерактионинформатион**</span><span class="sxs-lookup"><span data-stu-id="31ce0-120">**IMediaRendererActionInformation**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

