---
title: IConfigAsfWriter2 Стреамнумфромпин, метод
description: Метод Стреамнумфромпин извлекает номер потока, связанный с указанным входным закреплением.
ms.assetid: f645a742-e6dc-4041-8a56-3bbb5188a9a9
keywords:
- Формат Windows Media, Стреамнумфромпин метод
- Стреамнумфромпин метод Windows Media Format, интерфейс IConfigAsfWriter2
- Интерфейс IConfigAsfWriter2 Windows Media Format, метод Стреамнумфромпин
topic_type:
- apiref
api_name:
- IConfigAsfWriter2.StreamNumFromPin
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c63a31d515e70b0ee0ac5be617ee52fe23bd5416
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413098"
---
# <a name="iconfigasfwriter2streamnumfrompin-method"></a><span data-ttu-id="4563d-106">Метод IConfigAsfWriter2:: Стреамнумфромпин</span><span class="sxs-lookup"><span data-stu-id="4563d-106">IConfigAsfWriter2::StreamNumFromPin method</span></span>

<span data-ttu-id="4563d-107">Метод **стреамнумфромпин** извлекает номер потока, связанный с указанным входным закреплением.</span><span class="sxs-lookup"><span data-stu-id="4563d-107">The **StreamNumFromPin** method retrieves the stream number associated with the specified input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="4563d-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4563d-108">Syntax</span></span>


```C++
HRESULT StreamNumFromPin(
  [in]  IPin *pPin,
  [out] WORD *pwStreamNum
);
```



## <a name="parameters"></a><span data-ttu-id="4563d-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="4563d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4563d-110">*ппин* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4563d-110">*pPin* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4563d-111">Указатель на интерфейс **Ипин** входного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="4563d-111">Pointer to the **IPin** interface on the input pin.</span></span>

</dd> <dt>

<span data-ttu-id="4563d-112">*пвстреамнум* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="4563d-112">*pwStreamNum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4563d-113">Указатель, получающий номер потока.</span><span class="sxs-lookup"><span data-stu-id="4563d-113">Pointer that receives the stream number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4563d-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4563d-114">Return value</span></span>

<span data-ttu-id="4563d-115">Если метод завершается успешно, возвращается значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="4563d-115">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="4563d-116">В случае сбоя возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4563d-116">If it fails, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4563d-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4563d-117">Remarks</span></span>

<span data-ttu-id="4563d-118">Иногда может потребоваться использовать интерфейсы пакета SDK Windows Media Format напрямую для работы с потоком перед выполнением графа фильтра.</span><span class="sxs-lookup"><span data-stu-id="4563d-118">Sometimes you may need to use the Windows Media Format SDK interfaces directly to manipulate a stream before running a filter graph.</span></span> <span data-ttu-id="4563d-119">Поскольку нельзя предположить, что номер потока ASF совпадает с PIN-номером DirectShow, этот метод предоставляется.</span><span class="sxs-lookup"><span data-stu-id="4563d-119">Because you cannot assume that an ASF stream number is the same as the DirectShow pin number, this method is provided.</span></span>

## <a name="see-also"></a><span data-ttu-id="4563d-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4563d-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="4563d-121">[**Интерфейс IConfigAsfWriter2**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4563d-121">[**IConfigAsfWriter2 Interface**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))</span></span>
</dt> </dl>

 

 