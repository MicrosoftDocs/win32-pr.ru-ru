---
title: Имедиарендерерактионинформатион Исплайаваилабле, метод
description: Извлекает значение, указывающее, принимает ли ДМР в настоящее время принятие методов Плайасинк и Плайатспидасинк.
ms.assetid: 969C55FA-872D-4063-B85C-573C8DA5593C
keywords:
- API потоковой передачи мультимедиа метода Исплайаваилабле
- API потоковой передачи мультимедиа метода Исплайаваилабле, интерфейс Имедиарендерерактионинформатион
- API потоковой передачи мультимедиа интерфейса Имедиарендерерактионинформатион, метод Исплайаваилабле
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsPlayAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 87fa3a2005772a4d948bafe32d2a0e10cc5a6914
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104412903"
---
# <a name="imediarendereractioninformationisplayavailable-method"></a><span data-ttu-id="ff302-106">Метод Имедиарендерерактионинформатион:: Исплайаваилабле</span><span class="sxs-lookup"><span data-stu-id="ff302-106">IMediaRendererActionInformation::IsPlayAvailable method</span></span>

<span data-ttu-id="ff302-107">Извлекает значение, указывающее, принимает ли ДМР в настоящее время принятие методов [**плайасинк**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playasync) и [**плайатспидасинк**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playatspeedasync) .</span><span class="sxs-lookup"><span data-stu-id="ff302-107">Retrieves a value that indicates whether the DMR is currently accepting the accepting the [**PlayAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playasync) and [**PlayAtSpeedAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playatspeedasync) methods.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff302-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ff302-108">Syntax</span></span>


```C++
HRESULT IsPlayAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="ff302-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="ff302-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff302-110">*значение* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ff302-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ff302-111">Логическое значение, равное **true** , если в настоящее время ДМР принимает методы [**плайасинк**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playasync) и [**плайатспидасинк**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playatspeedasync) , и **false** , если это не так.</span><span class="sxs-lookup"><span data-stu-id="ff302-111">A boolean value that is **True** if the DMR is currently accepting the accepting the [**PlayAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playasync) and [**PlayAtSpeedAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playatspeedasync) methods and **False** if it is not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff302-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ff302-112">Return value</span></span>

<span data-ttu-id="ff302-113">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="ff302-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="ff302-114">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="ff302-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="ff302-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="ff302-115">Return code</span></span>                                                                          | <span data-ttu-id="ff302-116">Описание</span><span class="sxs-lookup"><span data-stu-id="ff302-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="ff302-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="ff302-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="ff302-118">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="ff302-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="ff302-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ff302-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff302-120">**имедиарендерерактионинформатион**</span><span class="sxs-lookup"><span data-stu-id="ff302-120">**IMediaRendererActionInformation**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

