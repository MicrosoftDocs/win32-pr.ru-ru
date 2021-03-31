---
title: Имедиарендерерактионинформатион Исмутеаваилабле, метод
description: Получает значение, указывающее, поддерживает ли ДМР звук.
ms.assetid: F744C2D7-5518-4A9F-A71E-60CF0B312177
keywords:
- API потоковой передачи мультимедиа метода Исмутеаваилабле
- API потоковой передачи мультимедиа метода Исмутеаваилабле, интерфейс Имедиарендерерактионинформатион
- API потоковой передачи мультимедиа интерфейса Имедиарендерерактионинформатион, метод Исмутеаваилабле
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsMuteAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 96751a7f2f1aedcd9e29be981ffadf6c43bf4008
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104069891"
---
# <a name="imediarendereractioninformationismuteavailable-method"></a><span data-ttu-id="75b43-106">Метод Имедиарендерерактионинформатион:: Исмутеаваилабле</span><span class="sxs-lookup"><span data-stu-id="75b43-106">IMediaRendererActionInformation::IsMuteAvailable method</span></span>

<span data-ttu-id="75b43-107">Получает значение, указывающее, поддерживает ли ДМР звук.</span><span class="sxs-lookup"><span data-stu-id="75b43-107">Retrieves a value that indicates whether the DMR is capable of muting the audio.</span></span>

## <a name="syntax"></a><span data-ttu-id="75b43-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="75b43-108">Syntax</span></span>


```C++
HRESULT IsMuteAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="75b43-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="75b43-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75b43-110">*значение* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="75b43-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="75b43-111">Логическое значение, равное **true** , если ДМР поддерживает озвучивание звука и **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="75b43-111">A boolean value that is **True** if the DMR is capable of muting the audio and **False** if it is not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75b43-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="75b43-112">Return value</span></span>

<span data-ttu-id="75b43-113">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="75b43-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="75b43-114">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="75b43-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="75b43-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="75b43-115">Return code</span></span>                                                                          | <span data-ttu-id="75b43-116">Описание</span><span class="sxs-lookup"><span data-stu-id="75b43-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="75b43-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="75b43-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="75b43-118">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="75b43-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="75b43-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="75b43-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75b43-120">**имедиарендерерактионинформатион**</span><span class="sxs-lookup"><span data-stu-id="75b43-120">**IMediaRendererActionInformation**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

