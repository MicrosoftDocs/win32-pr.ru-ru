---
title: Метод Игасернотифи Ондатамове (не рекомендуется)
description: Этот раздел интерфейса поиска на рабочем столе Windows устарел и заменен API-интерфейсом Windows Search Исеарчперсистентитемсчанжедсинк в Windows SDK. | Метод Игасернотифи Ондатамове (не рекомендуется)
ms.assetid: cc223d0f-6508-4e38-b365-c60660db5324
keywords:
- Ондатамове (устаревший) метод устаревших функций среды Windows
- Ондатамове (устаревший) метод устаревших функций среды Windows, интерфейс Игасернотифи
- Устаревшие функции среды Windows интерфейса Игасернотифи, Ондатамове (устаревший метод)
topic_type:
- apiref
api_name:
- IGatherNotify.OnDataMove (Deprecated)
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9fe38cd11e9072981334e5b724445ea3393d4361
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353005"
---
# <a name="igathernotifyondatamove-deprecated-method"></a><span data-ttu-id="d2931-107">Метод Игасернотифи:: Ондатамове (не рекомендуется)</span><span class="sxs-lookup"><span data-stu-id="d2931-107">IGatherNotify::OnDataMove (Deprecated) method</span></span>

<span data-ttu-id="d2931-108">\[**Ондатамове** может быть изменен или недоступен в последующих версиях операционной системы или продукта.\]</span><span class="sxs-lookup"><span data-stu-id="d2931-108">\[**OnDataMove** may be altered or unavailable in subsequent versions of the operating system or product.\]</span></span>

<span data-ttu-id="d2931-109">Этот раздел интерфейса поиска на рабочем столе Windows устарел и заменен API-интерфейсом Windows Search [**исеарчперсистентитемсчанжедсинк**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) в Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="d2931-109">This Windows Desktop Search interface topic is deprecated and is superseded by the Windows Search [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) API in the Windows SDK.</span></span>

<span data-ttu-id="d2931-110">Этот метод уведомляет индексатор о перемещенных данных.</span><span class="sxs-lookup"><span data-stu-id="d2931-110">This method notifies the indexer of data that has been moved.</span></span> <span data-ttu-id="d2931-111">При отправке уведомления индексатору он включает старый адрес, новый адрес и логический адрес.</span><span class="sxs-lookup"><span data-stu-id="d2931-111">When it sends the notification to the indexer, it includes the old address, new address, and logical address.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2931-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d2931-112">Syntax</span></span>


```C++
void OnDataMove (Deprecated)(
  [in] long eChangeAdviseSemantics,
  [in] BSTR bstrOldAddress,
  [in] BSTR bstrNewAddress,
  [in] BSTR bstrLogicalAddress
);
```



## <a name="parameters"></a><span data-ttu-id="d2931-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="d2931-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2931-114">*ечанжеадвисесемантикс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d2931-114">*eChangeAdviseSemantics* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2931-115">Тип: **Long**</span><span class="sxs-lookup"><span data-stu-id="d2931-115">Type: **long**</span></span>

<span data-ttu-id="d2931-116">Перечислимый параметр, описывающий тип произошедшего перемещения.</span><span class="sxs-lookup"><span data-stu-id="d2931-116">An enumerated parameter that describes the type of move that occurred.</span></span>

</dd> <dt>

<span data-ttu-id="d2931-117">*бстролдаддресс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d2931-117">*bstrOldAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2931-118">Тип: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="d2931-118">Type: **BSTR**</span></span>

<span data-ttu-id="d2931-119">Старый адрес элемента, который был перемещен.</span><span class="sxs-lookup"><span data-stu-id="d2931-119">The old address of the item that moved.</span></span> <span data-ttu-id="d2931-120">Для обычных файлов *ечанжеадвисесематикс* имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="d2931-120">For normal files,*eChangeAdviseSematics* is **NULL**.</span></span> <span data-ttu-id="d2931-121">Для папки или каталога задайте для *ечанжеадвисесематикс* \_ \_ Каталог семантики ЦС ГСР \_ .</span><span class="sxs-lookup"><span data-stu-id="d2931-121">For a folder or directory, set *eChangeAdviseSematics* to GTHR\_CA\_SEMANTICS\_DIRECTORY.</span></span>

</dd> <dt>

<span data-ttu-id="d2931-122">*бстрневаддресс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d2931-122">*bstrNewAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2931-123">Тип: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="d2931-123">Type: **BSTR**</span></span>

<span data-ttu-id="d2931-124">Новый адрес элемента, который был перемещен.</span><span class="sxs-lookup"><span data-stu-id="d2931-124">The new address of the item that moved.</span></span>

</dd> <dt>

<span data-ttu-id="d2931-125">*бстрлогикаладдресс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d2931-125">*bstrLogicalAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2931-126">Тип: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="d2931-126">Type: **BSTR**</span></span>

<span data-ttu-id="d2931-127">Логический адрес перемещенного элемента.</span><span class="sxs-lookup"><span data-stu-id="d2931-127">The logical address of the item that moved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2931-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d2931-128">Return value</span></span>

<span data-ttu-id="d2931-129">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="d2931-129">This method does not return a value.</span></span>

 

 
