---
title: 'Метод Идоманажер:: Енумдовнлоадс'
description: Извлекает указатель интерфейса на объект перечислителя, используемый для перечисления существующих Скачиваний.
keywords:
- 'Метод Идоманажер:: Енумдовнлоадс'
topic_type:
- apiref
api_name:
- IDOManager.EnumDownloads
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: a1e7fed2955fdc1b5ac0c11cfebc34aa95517603
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2019
ms.locfileid: "105719083"
---
# <a name="idomanagerenumdownloads-method"></a><span data-ttu-id="b9f24-104">Метод Идоманажер:: Енумдовнлоадс</span><span class="sxs-lookup"><span data-stu-id="b9f24-104">IDOManager::EnumDownloads method</span></span>

<span data-ttu-id="b9f24-105">Извлекает указатель интерфейса на объект перечислителя, используемый для перечисления существующих Скачиваний.</span><span class="sxs-lookup"><span data-stu-id="b9f24-105">Retrieves an interface pointer to an enumerator object that is used to enumerate existing downloads.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9f24-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b9f24-106">Syntax</span></span>

```cpp
HRESULT EnumDownloads(
  DO_DOWNLOAD_ENUM_CATEGORY *category, 
  IEnumUnknown **ppEnum
);
```

## <a name="parameters"></a><span data-ttu-id="b9f24-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="b9f24-107">Parameters</span></span>

`category`

<span data-ttu-id="b9f24-108">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="b9f24-108">Optional.</span></span> <span data-ttu-id="b9f24-109">Имя свойства, используемое в качестве категории для перечисления.</span><span class="sxs-lookup"><span data-stu-id="b9f24-109">The property name to be used as a category to enumerate.</span></span> <span data-ttu-id="b9f24-110">При передаче `nullptr` будут получены все существующие файлы для загрузки.</span><span class="sxs-lookup"><span data-stu-id="b9f24-110">Passing `nullptr` will retrieve all existing downloads.</span></span> <span data-ttu-id="b9f24-111">В качестве категории поддерживаются следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="b9f24-111">The following properties are supported as a category.</span></span>

- <span data-ttu-id="b9f24-112">**DODownloadProperty_Id**</span><span class="sxs-lookup"><span data-stu-id="b9f24-112">**DODownloadProperty_Id**</span></span>
- <span data-ttu-id="b9f24-113">**DODownloadProperty_Uri**</span><span class="sxs-lookup"><span data-stu-id="b9f24-113">**DODownloadProperty_Uri**</span></span>
- <span data-ttu-id="b9f24-114">**DODownloadProperty_ContentId**</span><span class="sxs-lookup"><span data-stu-id="b9f24-114">**DODownloadProperty_ContentId**</span></span>
- <span data-ttu-id="b9f24-115">**DODownloadProperty_DisplayName**</span><span class="sxs-lookup"><span data-stu-id="b9f24-115">**DODownloadProperty_DisplayName**</span></span>
- <span data-ttu-id="b9f24-116">**DODownloadProperty_LocalPath**</span><span class="sxs-lookup"><span data-stu-id="b9f24-116">**DODownloadProperty_LocalPath**</span></span>

`ppEnum`

<span data-ttu-id="b9f24-117">Адрес указателя интерфейса на **иенумункновн**, который используется для перечисления существующих Скачиваний.</span><span class="sxs-lookup"><span data-stu-id="b9f24-117">The address of an interface pointer to **IEnumUnknown**, which is used to enumerate existing downloads.</span></span> <span data-ttu-id="b9f24-118">Содержимое перечислителя зависит от значения *Category*.</span><span class="sxs-lookup"><span data-stu-id="b9f24-118">The contents of the enumerator depend on the value of *category*.</span></span> <span data-ttu-id="b9f24-119">Загружаемые файлы, включенные в интерфейс перечисления, — это те, которые ранее были созданы тем же вызывающим объектом для этой функции.</span><span class="sxs-lookup"><span data-stu-id="b9f24-119">The downloads included in the enumeration interface are the ones that were previously created by the same caller to this function.</span></span> 

## <a name="return-value"></a><span data-ttu-id="b9f24-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b9f24-120">Return Value</span></span>

<span data-ttu-id="b9f24-121">Если функция завершается с ошибкой, она возвращает **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="b9f24-121">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="b9f24-122">В противном случае возвращается [](/windows/desktop/com/structure-of-com-error-codes) [код ошибки](/windows/desktop/com/com-error-codes-10)HRESULT.</span><span class="sxs-lookup"><span data-stu-id="b9f24-122">Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).</span></span>

## <a name="requirements"></a><span data-ttu-id="b9f24-123">Требования</span><span class="sxs-lookup"><span data-stu-id="b9f24-123">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="b9f24-124">**Минимальная версия клиента**</span><span class="sxs-lookup"><span data-stu-id="b9f24-124">**Minimum supported client**</span></span> | <span data-ttu-id="b9f24-125">Windows 10, \[ только приложения Win32 версии 1809\]</span><span class="sxs-lookup"><span data-stu-id="b9f24-125">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="b9f24-126">**Минимальная версия сервера**</span><span class="sxs-lookup"><span data-stu-id="b9f24-126">**Minimum supported server**</span></span> | <span data-ttu-id="b9f24-127">Windows Server, \[ только приложения Win32 версии 1809\]</span><span class="sxs-lookup"><span data-stu-id="b9f24-127">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="b9f24-128">**Header**</span><span class="sxs-lookup"><span data-stu-id="b9f24-128">**Header**</span></span> | <span data-ttu-id="b9f24-129">Do. h</span><span class="sxs-lookup"><span data-stu-id="b9f24-129">Do.h</span></span> |
