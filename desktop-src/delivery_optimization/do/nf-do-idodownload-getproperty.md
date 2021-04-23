---
title: 'Идодовнлоад:: метод Property'
description: Извлекает указатель на **вариант** , содержащий определенное свойство загрузки.
keywords:
- 'Идодовнлоад:: метод Property'
topic_type:
- apiref
api_name:
- IDODownload.GetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: e734f109e596663ee699c764ca85f1ee45ad7947
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2019
ms.locfileid: "103890080"
---
# <a name="idodownloadgetproperty-method"></a><span data-ttu-id="9c23e-104">Идодовнлоад:: метод Property</span><span class="sxs-lookup"><span data-stu-id="9c23e-104">IDODownload::GetProperty method</span></span>

<span data-ttu-id="9c23e-105">Извлекает указатель на **вариант** , содержащий определенное свойство загрузки.</span><span class="sxs-lookup"><span data-stu-id="9c23e-105">Retrieves a pointer to a **VARIANT** that contains a specific download property.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c23e-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9c23e-106">Syntax</span></span>

```cpp
HRESULT GetProperty(
  DODownloadProperty propId, 
  VARIANT* propVal
);
```

## <a name="parameters"></a><span data-ttu-id="9c23e-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="9c23e-107">Parameters</span></span>

`propId`

<span data-ttu-id="9c23e-108">Обязательный идентификатор свойства для получения (типа **додовнлоадпроперти**).</span><span class="sxs-lookup"><span data-stu-id="9c23e-108">The required property ID to get (of type **DODownloadProperty**).</span></span>

`propVal`

<span data-ttu-id="9c23e-109">Результирующее значение свойства, хранящееся в **варианте**.</span><span class="sxs-lookup"><span data-stu-id="9c23e-109">The resulting property value, stored in a **VARIANT**.</span></span>

## <a name="return-value"></a><span data-ttu-id="9c23e-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9c23e-110">Return Value</span></span>

<span data-ttu-id="9c23e-111">Если функция завершается с ошибкой, она возвращает **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="9c23e-111">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="9c23e-112">В противном случае возвращается [](/windows/desktop/com/structure-of-com-error-codes) [код ошибки](/windows/desktop/com/com-error-codes-10)HRESULT.</span><span class="sxs-lookup"><span data-stu-id="9c23e-112">Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).</span></span>

|<span data-ttu-id="9c23e-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9c23e-113">Return value</span></span>|<span data-ttu-id="9c23e-114">Описание</span><span class="sxs-lookup"><span data-stu-id="9c23e-114">Description</span></span>|
|-|-|
|<span data-ttu-id="9c23e-115">DO_E_UNKNOWN_PROPERTY_ID</span><span class="sxs-lookup"><span data-stu-id="9c23e-115">DO_E_UNKNOWN_PROPERTY_ID</span></span>|<span data-ttu-id="9c23e-116">*propId* неизвестен.</span><span class="sxs-lookup"><span data-stu-id="9c23e-116">*propId* is unknown.</span></span>|
|<span data-ttu-id="9c23e-117">DO_E_WRITE_ONLY_PROPERTY</span><span class="sxs-lookup"><span data-stu-id="9c23e-117">DO_E_WRITE_ONLY_PROPERTY</span></span>|<span data-ttu-id="9c23e-118">Свойство доступно только для записи и не может быть прочитано.</span><span class="sxs-lookup"><span data-stu-id="9c23e-118">The property is write-only, and cannot be read.</span></span>|
|<span data-ttu-id="9c23e-119">E_NOT_SET</span><span class="sxs-lookup"><span data-stu-id="9c23e-119">E_NOT_SET</span></span>|<span data-ttu-id="9c23e-120">Такое свойство не было задано с помощью **SetProperty**.</span><span class="sxs-lookup"><span data-stu-id="9c23e-120">No such property was set via **SetProperty**.</span></span>|

## <a name="requirements"></a><span data-ttu-id="9c23e-121">Требования</span><span class="sxs-lookup"><span data-stu-id="9c23e-121">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="9c23e-122">**Минимальная версия клиента**</span><span class="sxs-lookup"><span data-stu-id="9c23e-122">**Minimum supported client**</span></span> | <span data-ttu-id="9c23e-123">Windows 10, \[ только приложения Win32 версии 1809\]</span><span class="sxs-lookup"><span data-stu-id="9c23e-123">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="9c23e-124">**Минимальная версия сервера**</span><span class="sxs-lookup"><span data-stu-id="9c23e-124">**Minimum supported server**</span></span> | <span data-ttu-id="9c23e-125">Windows Server, \[ только приложения Win32 версии 1809\]</span><span class="sxs-lookup"><span data-stu-id="9c23e-125">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="9c23e-126">**Header**</span><span class="sxs-lookup"><span data-stu-id="9c23e-126">**Header**</span></span> | <span data-ttu-id="9c23e-127">Do. h</span><span class="sxs-lookup"><span data-stu-id="9c23e-127">Do.h</span></span> |
