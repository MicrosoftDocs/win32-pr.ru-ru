---
title: 'Метод Идодовнлоад:: SetProperty'
description: Задает свойство загрузки.
keywords:
- 'Метод Идодовнлоад:: SetProperty'
topic_type:
- apiref
api_name:
- IDODownload.SetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 0d496f49851aab665e49f3aaeb51e4b941d6c183
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2019
ms.locfileid: "103785100"
---
# <a name="idodownloadsetproperty-method"></a><span data-ttu-id="a4ead-104">Метод Идодовнлоад:: SetProperty</span><span class="sxs-lookup"><span data-stu-id="a4ead-104">IDODownload::SetProperty method</span></span>

<span data-ttu-id="a4ead-105">Задает свойство загрузки.</span><span class="sxs-lookup"><span data-stu-id="a4ead-105">Sets a download property.</span></span> <span data-ttu-id="a4ead-106">Метод принимает указатель на **вариант** , который содержит определенное свойство, применяемое к скачиванию.</span><span class="sxs-lookup"><span data-stu-id="a4ead-106">The method accepts a pointer to a **VARIANT** that contains a specific property to apply to the download.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4ead-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a4ead-107">Syntax</span></span>

```cpp
HRESULT SetProperty(
  DODownloadProperty propId,
  VARIANT* propVal
);
```

## <a name="parameters"></a><span data-ttu-id="a4ead-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a4ead-108">Parameters</span></span>

`propId`

<span data-ttu-id="a4ead-109">Обязательный идентификатор свойства для задания (типа **додовнлоадпроперти**).</span><span class="sxs-lookup"><span data-stu-id="a4ead-109">The required property ID to set (of type **DODownloadProperty**).</span></span>

`propVal`

<span data-ttu-id="a4ead-110">Заданное значение свойства, хранящееся в **варианте**.</span><span class="sxs-lookup"><span data-stu-id="a4ead-110">The property value to set, stored in a **VARIANT**.</span></span>

## <a name="return-value"></a><span data-ttu-id="a4ead-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a4ead-111">Return Value</span></span>

<span data-ttu-id="a4ead-112">Если функция завершается с ошибкой, она возвращает **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="a4ead-112">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="a4ead-113">В противном случае возвращается [](/windows/desktop/com/structure-of-com-error-codes) [код ошибки](/windows/desktop/com/com-error-codes-10)HRESULT.</span><span class="sxs-lookup"><span data-stu-id="a4ead-113">Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).</span></span>

|<span data-ttu-id="a4ead-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a4ead-114">Return value</span></span>|<span data-ttu-id="a4ead-115">Описание</span><span class="sxs-lookup"><span data-stu-id="a4ead-115">Description</span></span>|
|-|-|
|<span data-ttu-id="a4ead-116">DO_E_UNKNOWN_PROPERTY_ID</span><span class="sxs-lookup"><span data-stu-id="a4ead-116">DO_E_UNKNOWN_PROPERTY_ID</span></span>|<span data-ttu-id="a4ead-117">*propId* неизвестен.</span><span class="sxs-lookup"><span data-stu-id="a4ead-117">*propId* is unknown.</span></span>|
|<span data-ttu-id="a4ead-118">DO_E_INVALID_STATE</span><span class="sxs-lookup"><span data-stu-id="a4ead-118">DO_E_INVALID_STATE</span></span>|<span data-ttu-id="a4ead-119">Скачивание сейчас не находится в состоянии, допускающем установку свойств.</span><span class="sxs-lookup"><span data-stu-id="a4ead-119">The download is not currently in a state that allows setting properties.</span></span>|

## <a name="requirements"></a><span data-ttu-id="a4ead-120">Требования</span><span class="sxs-lookup"><span data-stu-id="a4ead-120">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="a4ead-121">**Минимальная версия клиента**</span><span class="sxs-lookup"><span data-stu-id="a4ead-121">**Minimum supported client**</span></span> | <span data-ttu-id="a4ead-122">Windows 10, \[ только приложения Win32 версии 1809\]</span><span class="sxs-lookup"><span data-stu-id="a4ead-122">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="a4ead-123">**Минимальная версия сервера**</span><span class="sxs-lookup"><span data-stu-id="a4ead-123">**Minimum supported server**</span></span> | <span data-ttu-id="a4ead-124">Windows Server, \[ только приложения Win32 версии 1809\]</span><span class="sxs-lookup"><span data-stu-id="a4ead-124">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="a4ead-125">**Header**</span><span class="sxs-lookup"><span data-stu-id="a4ead-125">**Header**</span></span> | <span data-ttu-id="a4ead-126">Do. h</span><span class="sxs-lookup"><span data-stu-id="a4ead-126">Do.h</span></span> |
