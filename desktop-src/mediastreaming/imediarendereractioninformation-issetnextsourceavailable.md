---
title: Имедиарендерерактионинформатион Иссетнекстсаурцеаваилабле, метод
description: Извлекает значение, указывающее, принимает ли ДМР в настоящее время метод Сетнекстсаурцефромуриасинк, метод Сетнекстсаурцефромстреамасинк или метод Сетнекстсаурцефроммедиасаурцеасинк.
ms.assetid: 7588E992-4070-4E0F-8C4B-7DFC097A5076
keywords:
- API потоковой передачи мультимедиа метода Иссетнекстсаурцеаваилабле
- API потоковой передачи мультимедиа метода Иссетнекстсаурцеаваилабле, интерфейс Имедиарендерерактионинформатион
- API потоковой передачи мультимедиа интерфейса Имедиарендерерактионинформатион, метод Иссетнекстсаурцеаваилабле
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsSetNextSourceAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 265a9a96d5229e47008c60813fd6c0e3bc567800
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790567"
---
# <a name="imediarendereractioninformationissetnextsourceavailable-method"></a><span data-ttu-id="4253e-106">Метод Имедиарендерерактионинформатион:: Иссетнекстсаурцеаваилабле</span><span class="sxs-lookup"><span data-stu-id="4253e-106">IMediaRendererActionInformation::IsSetNextSourceAvailable method</span></span>

<span data-ttu-id="4253e-107">Извлекает значение, указывающее, принимает ли ДМР в настоящее время метод [**сетнекстсаурцефромуриасинк**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefromuriasync) , метод [**Сетнекстсаурцефромстреамасинк**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefromstreamasync) или метод [**сетнекстсаурцефроммедиасаурцеасинк**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefrommediasourceasync) .</span><span class="sxs-lookup"><span data-stu-id="4253e-107">Retrieves a value that indicates whether the DMR is currently accepting the [**SetNextSourceFromUriAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefromuriasync) method, the [**SetNextSourceFromStreamAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefromstreamasync) method or the [**SetNextSourceFromMediaSourceAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefrommediasourceasync) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4253e-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4253e-108">Syntax</span></span>


```C++
HRESULT IsSetNextSourceAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="4253e-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="4253e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4253e-110">*значение* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="4253e-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4253e-111">Логическое значение, равное **true** , если ДМР в настоящее время принимает метод [**Сетнекстсаурцефромуриасинк**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefromuriasync) , метод [**Сетнекстсаурцефромстреамасинк**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefromstreamasync) или метод [**сетнекстсаурцефроммедиасаурцеасинк**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefrommediasourceasync) и **значение false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="4253e-111">A boolean value that is **True** if the DMR is currently accepting the [**SetNextSourceFromUriAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefromuriasync) method, the [**SetNextSourceFromStreamAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefromstreamasync) method or the [**SetNextSourceFromMediaSourceAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefrommediasourceasync) method and **False** if it is not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4253e-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4253e-112">Return value</span></span>

<span data-ttu-id="4253e-113">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="4253e-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="4253e-114">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="4253e-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="4253e-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="4253e-115">Return code</span></span>                                                                          | <span data-ttu-id="4253e-116">Описание</span><span class="sxs-lookup"><span data-stu-id="4253e-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="4253e-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="4253e-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="4253e-118">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="4253e-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="4253e-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4253e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4253e-120">**имедиарендерерактионинформатион**</span><span class="sxs-lookup"><span data-stu-id="4253e-120">**IMediaRendererActionInformation**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

