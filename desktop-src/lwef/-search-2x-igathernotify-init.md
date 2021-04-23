---
title: Метод init Игасернотифи (не рекомендуется)
description: Этот раздел интерфейса поиска на рабочем столе Windows устарел и заменен API-интерфейсом Windows Search Исеарчперсистентитемсчанжедсинк в Windows SDK. | Метод init Игасернотифи (не рекомендуется)
ms.assetid: 6a5f89eb-10f4-4262-89bf-b47e345f12eb
keywords:
- Метод init (не рекомендуется). устаревшие функции среды Windows
- Метод init (не рекомендуется). устаревшие функции среды Windows, интерфейс Игасернотифи
- Интерфейс Игасернотифи устаревшие функции среды Windows, метод init (устарел)
topic_type:
- apiref
api_name:
- IGatherNotify.Init (Deprecated)
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 81379bb4a9a7c6099912bfc9ebca170141d76cd2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105694021"
---
# <a name="igathernotifyinit-deprecated-method"></a><span data-ttu-id="05438-107">Метод Игасернотифи:: init (устарел)</span><span class="sxs-lookup"><span data-stu-id="05438-107">IGatherNotify::Init (Deprecated) method</span></span>

<span data-ttu-id="05438-108">\[**Инициализация** может быть изменена или недоступна в последующих версиях операционной системы или продукта.\]</span><span class="sxs-lookup"><span data-stu-id="05438-108">\[**Init** may be altered or unavailable in subsequent versions of the operating system or product.\]</span></span>

<span data-ttu-id="05438-109">Этот раздел интерфейса поиска на рабочем столе Windows устарел и заменен API-интерфейсом Windows Search [**исеарчперсистентитемсчанжедсинк**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) в Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="05438-109">This Windows Desktop Search interface topic is deprecated and is superseded by the Windows Search [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) API in the Windows SDK.</span></span>

<span data-ttu-id="05438-110">Инициализирует интерфейс средства сбора данных.</span><span class="sxs-lookup"><span data-stu-id="05438-110">Initializes the Gatherer interface.</span></span> <span data-ttu-id="05438-111">Также указывает индекс для уведомления и хранилище приложений для отслеживания.</span><span class="sxs-lookup"><span data-stu-id="05438-111">Also specifies the index to notify and the application store to monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="05438-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="05438-112">Syntax</span></span>


```C++
void Init (Deprecated)(
  [in] BSTR    bstrApplication,
  [in] BSTR    bstrProject,
  [in] variant varScopesBstrArray
);
```



## <a name="parameters"></a><span data-ttu-id="05438-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="05438-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05438-114">*бстраппликатион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="05438-114">*bstrApplication* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05438-115">Тип: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="05438-115">Type: **BSTR**</span></span>

<span data-ttu-id="05438-116">Строка, указывающая целевое приложение.</span><span class="sxs-lookup"><span data-stu-id="05438-116">A string that specifies the target application.</span></span>

</dd> <dt>

<span data-ttu-id="05438-117">*бстрпрожект* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="05438-117">*bstrProject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05438-118">Тип: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="05438-118">Type: **BSTR**</span></span>

<span data-ttu-id="05438-119">Строка, указывающая имя индексатора, в который передаются сведения о сборщике.</span><span class="sxs-lookup"><span data-stu-id="05438-119">A string that specifies the name of the indexer to pass gatherer information to.</span></span>

</dd> <dt>

<span data-ttu-id="05438-120">*варскопесбстраррай* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="05438-120">*varScopesBstrArray* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05438-121">Тип: **Variant**</span><span class="sxs-lookup"><span data-stu-id="05438-121">Type: **variant**</span></span>

<span data-ttu-id="05438-122">Необязательный параметр, который позволяет передать массив областей для инициализации.</span><span class="sxs-lookup"><span data-stu-id="05438-122">Optional parameter, that enables you to pass an array of scopes to be initialized.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05438-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="05438-123">Return value</span></span>

<span data-ttu-id="05438-124">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="05438-124">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="05438-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="05438-125">Remarks</span></span>

<span data-ttu-id="05438-126">Инициализация с помощью приложения = "Рсапп", Project = "Миндекс".</span><span class="sxs-lookup"><span data-stu-id="05438-126">Initialize with application="RSApp", Project="MyIndex".</span></span>

 

 
