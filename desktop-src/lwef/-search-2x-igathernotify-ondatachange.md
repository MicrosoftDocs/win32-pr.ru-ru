---
title: Метод Игасернотифи Ондатачанже (не рекомендуется)
description: Этот раздел интерфейса поиска на рабочем столе Windows устарел и заменен API-интерфейсом Windows Search Исеарчперсистентитемсчанжедсинк в Windows SDK. | Метод Игасернотифи Ондатачанже (не рекомендуется)
ms.assetid: 0cbfa6b7-44f0-41f0-93a3-d5941b5822de
keywords:
- Ондатачанже (устаревший) метод устаревших функций среды Windows
- Ондатачанже (устаревший) метод устаревших функций среды Windows, интерфейс Игасернотифи
- Устаревшие функции среды Windows интерфейса Игасернотифи, Ондатачанже (устаревший метод)
topic_type:
- apiref
api_name:
- IGatherNotify.OnDataChange (Deprecated)
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d41edeaa591a7f3cbc9494064906af1815597737
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105694020"
---
# <a name="igathernotifyondatachange-deprecated-method"></a><span data-ttu-id="320ee-107">Метод Игасернотифи:: Ондатачанже (не рекомендуется)</span><span class="sxs-lookup"><span data-stu-id="320ee-107">IGatherNotify::OnDataChange (Deprecated) method</span></span>

<span data-ttu-id="320ee-108">\[**Ондатачанже** может быть изменен или недоступен в последующих версиях операционной системы или продукта.\]</span><span class="sxs-lookup"><span data-stu-id="320ee-108">\[**OnDataChange** may be altered or unavailable in subsequent versions of the operating system or product.\]</span></span>

<span data-ttu-id="320ee-109">Этот раздел интерфейса поиска на рабочем столе Windows устарел и заменен API-интерфейсом Windows Search [**исеарчперсистентитемсчанжедсинк**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) в Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="320ee-109">This Windows Desktop Search interface topic is deprecated and is superseded by the Windows Search [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) API in the Windows SDK.</span></span>

<span data-ttu-id="320ee-110">Этот метод уведомляет индексатор измененных данных.</span><span class="sxs-lookup"><span data-stu-id="320ee-110">This method notifies the indexer of data that has changed.</span></span> <span data-ttu-id="320ee-111">При отправке уведомления индексатору он включает тип изменения, физический адрес и логический адрес.</span><span class="sxs-lookup"><span data-stu-id="320ee-111">When it sends the notification to the indexer, it includes the type of change, physical address, and logical address.</span></span>

## <a name="syntax"></a><span data-ttu-id="320ee-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="320ee-112">Syntax</span></span>


```C++
void OnDataChange (Deprecated)(
  [in] long eChangeAdvise,
  [in] BSTR bstrPhysicalAddress,
  [in] BSTR bstrLogicalAddress
);
```



## <a name="parameters"></a><span data-ttu-id="320ee-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="320ee-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="320ee-114">*ечанжеадвисе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="320ee-114">*eChangeAdvise* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="320ee-115">Тип: **Long**</span><span class="sxs-lookup"><span data-stu-id="320ee-115">Type: **long**</span></span>

<span data-ttu-id="320ee-116">Перечислимое значение, указывающее тип изменения.</span><span class="sxs-lookup"><span data-stu-id="320ee-116">An enumerated value that specifies the type of change.</span></span>

</dd> <dt>

<span data-ttu-id="320ee-117">*бстрфисикаладдресс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="320ee-117">*bstrPhysicalAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="320ee-118">Тип: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="320ee-118">Type: **BSTR**</span></span>

<span data-ttu-id="320ee-119">Физический адрес изменяемого элемента.</span><span class="sxs-lookup"><span data-stu-id="320ee-119">The physical address of the item that changed.</span></span>

</dd> <dt>

<span data-ttu-id="320ee-120">*бстрлогикаладдресс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="320ee-120">*bstrLogicalAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="320ee-121">Тип: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="320ee-121">Type: **BSTR**</span></span>

<span data-ttu-id="320ee-122">Логический адрес элемента, который изменился.</span><span class="sxs-lookup"><span data-stu-id="320ee-122">The logical address of the item that changed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="320ee-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="320ee-123">Return value</span></span>

<span data-ttu-id="320ee-124">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="320ee-124">This method does not return a value.</span></span>

 

 
