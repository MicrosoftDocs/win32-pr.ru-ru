---
title: Метод уведомления Иамвмбуфферпасскаллбакк
description: Метод notify вызывается ПИН-кодом для каждого буфера, который доставляется во время потоковой передачи.
ms.assetid: 3f252754-c784-4ffd-bcfc-fab73fa02b9a
keywords:
- Уведомлять о методе Windows Media Format
- Уведомлять о методе Windows Media Format, интерфейс Иамвмбуфферпасскаллбакк
- Интерфейс Иамвмбуфферпасскаллбакк Windows Media Format, метод notify
topic_type:
- apiref
api_name:
- IAMWMBufferPassCallback.Notify
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e8f362262b36dee0bfc9a18e57010d102b2fa2cb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104134378"
---
# <a name="iamwmbufferpasscallbacknotify-method"></a><span data-ttu-id="793b4-106">Метод Иамвмбуфферпасскаллбакк:: notify</span><span class="sxs-lookup"><span data-stu-id="793b4-106">IAMWMBufferPassCallback::Notify method</span></span>

<span data-ttu-id="793b4-107">Метод **Notify** вызывается ПИН-кодом для каждого буфера, который доставляется во время потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="793b4-107">The **Notify** method is called by the pin for each buffer that is delivered during streaming.</span></span>

## <a name="syntax"></a><span data-ttu-id="793b4-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="793b4-108">Syntax</span></span>


```C++
HRESULT Notify(
  [in] INSSBuffer3    *pNSSBuffer3,
  [in] IPin           *pPin,
  [in] REFERENCE_TIME *prtStart,
  [in] REFERENCE_TIME *prtEnd
);
```



## <a name="parameters"></a><span data-ttu-id="793b4-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="793b4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="793b4-110">*pNSSBuffer3* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="793b4-110">*pNSSBuffer3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="793b4-111">Указатель на интерфейс [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) , предоставленный в примере носителя.</span><span class="sxs-lookup"><span data-stu-id="793b4-111">Pointer to the [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) interface exposed on the media sample.</span></span>

</dd> <dt>

<span data-ttu-id="793b4-112">*ппин* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="793b4-112">*pPin* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="793b4-113">Указатель на ПИН-код, связанный с потоком мультимедиа, к которому принадлежит образец.</span><span class="sxs-lookup"><span data-stu-id="793b4-113">Pointer to the pin associated with the media stream that the sample belongs to.</span></span>

</dd> <dt>

<span data-ttu-id="793b4-114">*пртстарт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="793b4-114">*prtStart* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="793b4-115">Время начала примера.</span><span class="sxs-lookup"><span data-stu-id="793b4-115">Start time of the sample.</span></span>

</dd> <dt>

<span data-ttu-id="793b4-116">*пртенд* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="793b4-116">*prtEnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="793b4-117">Время окончания примера.</span><span class="sxs-lookup"><span data-stu-id="793b4-117">End time of the sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="793b4-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="793b4-118">Return value</span></span>

<span data-ttu-id="793b4-119">Не указано конкретное возвращаемое значение.</span><span class="sxs-lookup"><span data-stu-id="793b4-119">No particular return value is specified.</span></span> <span data-ttu-id="793b4-120">Вызывающий ПИН-код игнорирует значение **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="793b4-120">The calling pin ignores the **HRESULT**.</span></span>

## <a name="remarks"></a><span data-ttu-id="793b4-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="793b4-121">Remarks</span></span>

<span data-ttu-id="793b4-122">Этот метод позволяет приложению проверять данные в буфере мультимедиа перед обработкой содержимого буфера и работать с ними.</span><span class="sxs-lookup"><span data-stu-id="793b4-122">This method enables an application to examine and act on information in the media buffer before the buffer contents are processed.</span></span> <span data-ttu-id="793b4-123">Приложение несет ответственность за знание типа носителя в ПИН-коде.</span><span class="sxs-lookup"><span data-stu-id="793b4-123">The application is responsible for knowing the media type on the pin.</span></span> <span data-ttu-id="793b4-124">Эти сведения можно получить, сначала получив сведения о потоке из профиля, а затем вызвав метод [**IConfigAsfWriter2:: стреамнумфромпин**](iconfigasfwriter2-streamnumfrompin.md) , чтобы определить, какой ПИН-код связан с каждым потоком.</span><span class="sxs-lookup"><span data-stu-id="793b4-124">This information can be obtained by first getting the stream information from the profile and then calling [**IConfigAsfWriter2::StreamNumFromPin**](iconfigasfwriter2-streamnumfrompin.md) method to determine which pin is associated with each stream.</span></span>

## <a name="see-also"></a><span data-ttu-id="793b4-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="793b4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="793b4-126">**Справочник по КАСФ DirectShow**</span><span class="sxs-lookup"><span data-stu-id="793b4-126">**DirectShow QASF Reference**</span></span>](directshow-qasf-reference.md)
</dt> <dt>

[<span data-ttu-id="793b4-127">**Интерфейс Иамвмбуфферпасскаллбакк**</span><span class="sxs-lookup"><span data-stu-id="793b4-127">**IAMWMBufferPassCallback Interface**</span></span>](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpasscallback)
</dt> <dt>

[<span data-ttu-id="793b4-128">**Интерфейс INSSBuffer3**</span><span class="sxs-lookup"><span data-stu-id="793b4-128">**INSSBuffer3 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3)
</dt> </dl>

 

 