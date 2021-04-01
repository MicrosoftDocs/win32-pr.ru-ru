---
title: Идевицеикон, метод ContentType
description: Возвращает тип содержимого значка.
ms.assetid: 01928A98-B7D0-4523-9259-81FEB33F052E
keywords:
- API потоковой передачи мультимедиа метода ContentType
- API потоковой передачи мультимедиа метода ContentType, интерфейс Идевицеикон
- API потоковой передачи мультимедиа интерфейса Идевицеикон, метод ContentType
topic_type:
- apiref
api_name:
- IDeviceIcon.ContentType
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: af48aabb2a64f4c4b8fbd40a3859acc82496a399
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103890489"
---
# <a name="ideviceiconcontenttype-method"></a><span data-ttu-id="21636-106">Метод Идевицеикон:: ContentType</span><span class="sxs-lookup"><span data-stu-id="21636-106">IDeviceIcon::ContentType method</span></span>

<span data-ttu-id="21636-107">Возвращает тип содержимого значка.</span><span class="sxs-lookup"><span data-stu-id="21636-107">Retrieves the content type of the icon.</span></span>

## <a name="syntax"></a><span data-ttu-id="21636-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="21636-108">Syntax</span></span>


```C++
HRESULT ContentType(
  [out] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="21636-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="21636-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21636-110">*значение* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="21636-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="21636-111">Получает указатель на тип содержимого значка.</span><span class="sxs-lookup"><span data-stu-id="21636-111">Receives a pointer to the content type of the icon.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21636-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="21636-112">Return value</span></span>

<span data-ttu-id="21636-113">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="21636-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="21636-114">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="21636-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="21636-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="21636-115">Return code</span></span>                                                                          | <span data-ttu-id="21636-116">Описание</span><span class="sxs-lookup"><span data-stu-id="21636-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="21636-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="21636-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="21636-118">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="21636-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="21636-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="21636-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21636-120">**идевицеикон**</span><span class="sxs-lookup"><span data-stu-id="21636-120">**IDeviceIcon**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon)
</dt> </dl>

 

