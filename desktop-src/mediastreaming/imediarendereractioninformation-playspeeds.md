---
title: Имедиарендерерактионинформатион Плайспидс, метод
description: Извлекает полный список значений Плайспид, которые принимаются параметром ДМР.
ms.assetid: 0AB63E39-6A26-4199-9978-A10866A7C805
keywords:
- API потоковой передачи мультимедиа метода Плайспидс
- API потоковой передачи мультимедиа метода Плайспидс, интерфейс Имедиарендерерактионинформатион
- API потоковой передачи мультимедиа интерфейса Имедиарендерерактионинформатион, метод Плайспидс
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.PlaySpeeds
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 31089dd7616c035ebde4079c51988b94d1c27562
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337276"
---
# <a name="imediarendereractioninformationplayspeeds-method"></a><span data-ttu-id="fad56-106">Имедиарендерерактионинформатион: метод:P Лайспидс</span><span class="sxs-lookup"><span data-stu-id="fad56-106">IMediaRendererActionInformation::PlaySpeeds method</span></span>

<span data-ttu-id="fad56-107">Извлекает полный список значений [**плайспид**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-playspeed) , которые принимаются параметром ДМР.</span><span class="sxs-lookup"><span data-stu-id="fad56-107">Retrieves the complete list of [**PlaySpeed**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-playspeed) values that are accepted by the DMR.</span></span>

## <a name="syntax"></a><span data-ttu-id="fad56-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fad56-108">Syntax</span></span>


```C++
HRESULT PlaySpeeds(
  [out] IVector< PlaySpeed > **value
);
```



## <a name="parameters"></a><span data-ttu-id="fad56-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="fad56-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fad56-110">*значение* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="fad56-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fad56-111">Получает вектор структур [**плайспид**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-playspeed) , указывающий полный список значений **плайспид** , принимаемых ДМР.</span><span class="sxs-lookup"><span data-stu-id="fad56-111">Receives a vector of [**PlaySpeed**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-playspeed) structures specifying the complete list of **PlaySpeed** values that are accepted by the DMR.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fad56-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fad56-112">Return value</span></span>

<span data-ttu-id="fad56-113">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="fad56-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="fad56-114">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="fad56-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="fad56-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="fad56-115">Return code</span></span>                                                                          | <span data-ttu-id="fad56-116">Описание</span><span class="sxs-lookup"><span data-stu-id="fad56-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="fad56-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="fad56-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="fad56-118">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="fad56-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="fad56-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fad56-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fad56-120">**имедиарендерерактионинформатион**</span><span class="sxs-lookup"><span data-stu-id="fad56-120">**IMediaRendererActionInformation**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

