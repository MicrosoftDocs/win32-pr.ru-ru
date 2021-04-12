---
title: Метод Игасернотифи AddScope (не рекомендуется)
description: Этот раздел интерфейса поиска на рабочем столе Windows устарел и заменен API-интерфейсом Windows Search Исеарчперсистентитемсчанжедсинк в Windows SDK. | Метод Игасернотифи AddScope (не рекомендуется)
ms.assetid: 3b250818-1876-40b2-9a85-91f2bf6f52ec
keywords:
- AddScope (устаревший) метод устаревших функций среды Windows
- AddScope (устаревший) метод устаревших функций среды Windows, интерфейс Игасернотифи
- Устаревшие функции среды Windows интерфейса Игасернотифи, AddScope (устаревший метод)
topic_type:
- apiref
api_name:
- IGatherNotify.AddScope (Deprecated)
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 967dc4f30acee2f8d8adbcfec04f0508e53bba15
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353012"
---
# <a name="igathernotifyaddscope-deprecated-method"></a><span data-ttu-id="48b91-107">Метод Игасернотифи:: AddScope (не рекомендуется)</span><span class="sxs-lookup"><span data-stu-id="48b91-107">IGatherNotify::AddScope (Deprecated) method</span></span>

<span data-ttu-id="48b91-108">\[**AddScope** может быть изменен или недоступен в последующих версиях операционной системы или продукта.\]</span><span class="sxs-lookup"><span data-stu-id="48b91-108">\[**AddScope** may be altered or unavailable in subsequent versions of the operating system or product.\]</span></span>

<span data-ttu-id="48b91-109">Этот раздел интерфейса поиска на рабочем столе Windows устарел и заменен API-интерфейсом Windows Search [**исеарчперсистентитемсчанжедсинк**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) в Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="48b91-109">This Windows Desktop Search interface topic is deprecated and is superseded by the Windows Search [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) API in the Windows SDK.</span></span>

<span data-ttu-id="48b91-110">Добавляет начальную страницу или URL-адрес, который вы отслеживаете.</span><span class="sxs-lookup"><span data-stu-id="48b91-110">Adds the start page or URL you are monitoring.</span></span> <span data-ttu-id="48b91-111">Это инициирует добавочное сканирование при подключении, а затем предполагает, что все дальнейшие изменения URL-адреса обрабатываются уведомлением.</span><span class="sxs-lookup"><span data-stu-id="48b91-111">This initiates an incremental crawl when you connect, and then assumes all further URL changes are by notification.</span></span>

## <a name="syntax"></a><span data-ttu-id="48b91-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="48b91-112">Syntax</span></span>


```C++
void AddScope (Deprecated)(
  [in] BSTR bstrScope
);
```



## <a name="parameters"></a><span data-ttu-id="48b91-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="48b91-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48b91-114">*бстрскопе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="48b91-114">*bstrScope* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48b91-115">Тип: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="48b91-115">Type: **BSTR**</span></span>

<span data-ttu-id="48b91-116">Строка, указывающая начальную страницу или Урлсат, которые вы отслеживаете.</span><span class="sxs-lookup"><span data-stu-id="48b91-116">A string that specifies the start page or URLthat you are monitoring.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48b91-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="48b91-117">Return value</span></span>

<span data-ttu-id="48b91-118">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="48b91-118">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="48b91-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="48b91-119">Remarks</span></span>

<span data-ttu-id="48b91-120">Вызов этого метода запускает добавочное сканирование при подключении к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="48b91-120">Calling this method starts an incremental crawl when connected to the store.</span></span> <span data-ttu-id="48b91-121">После этого предполагается, что все изменения URL-адресов задаются уведомлением после первоначального обновления.</span><span class="sxs-lookup"><span data-stu-id="48b91-121">Thereafter, it is assumed that all URL changes are by notification after the initial update.</span></span>

 

 
