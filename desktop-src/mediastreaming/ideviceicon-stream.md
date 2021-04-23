---
title: Идевицеикон Stream, метод
description: Получает значок в виде потока.
ms.assetid: 0B9E852F-4F72-4721-8F88-24A850A088C4
keywords:
- Потоковый интерфейс API потоковой передачи мультимедиа
- API потокового метода потокового мультимедиа, интерфейс Идевицеикон
- API потоковой передачи мультимедиа интерфейса Идевицеикон, потоковый метод
topic_type:
- apiref
api_name:
- IDeviceIcon.Stream
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fd00d757fceb90cf5ee7199256b003464063abcb
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337409"
---
# <a name="ideviceiconstream-method"></a><span data-ttu-id="1c09a-106">Метод Идевицеикон:: Stream</span><span class="sxs-lookup"><span data-stu-id="1c09a-106">IDeviceIcon::Stream method</span></span>

<span data-ttu-id="1c09a-107">Получает значок в виде потока.</span><span class="sxs-lookup"><span data-stu-id="1c09a-107">Retrieves the icon as a stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c09a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1c09a-108">Syntax</span></span>


```C++
HRESULT Stream(
  [out] IRandomAccessStreamWithContentType **value
);
```



## <a name="parameters"></a><span data-ttu-id="1c09a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="1c09a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c09a-110">*значение* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="1c09a-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1c09a-111">Получает ссылку на объект [**ирандомакцессстреамвисконтенттипе**](/uwp/api/Windows.Storage.Streams.IRandomAccessStreamWithContentType) , который можно использовать для получения данных изображения.</span><span class="sxs-lookup"><span data-stu-id="1c09a-111">Receives a reference to a [**IRandomAccessStreamWithContentType**](/uwp/api/Windows.Storage.Streams.IRandomAccessStreamWithContentType) that can be used to retrieve the image data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c09a-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1c09a-112">Return value</span></span>

<span data-ttu-id="1c09a-113">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="1c09a-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="1c09a-114">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="1c09a-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="1c09a-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="1c09a-115">Return code</span></span>                                                                          | <span data-ttu-id="1c09a-116">Описание</span><span class="sxs-lookup"><span data-stu-id="1c09a-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="1c09a-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="1c09a-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="1c09a-118">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="1c09a-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="1c09a-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1c09a-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c09a-120">**идевицеикон**</span><span class="sxs-lookup"><span data-stu-id="1c09a-120">**IDeviceIcon**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon)
</dt> </dl>

 

