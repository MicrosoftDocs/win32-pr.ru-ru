---
title: 'Метод Идодовнлоадинтернал:: Сетпропертекс'
description: Задает свойство расширенной загрузки. Метод принимает указатель на **вариант** , который содержит определенное значение свойства, применяемое к скачиванию.
keywords:
- 'Метод Идодовнлоадинтернал:: Сетпропертекс'
topic_type:
- apiref
api_name:
- IDODownloadInternal.SetPropertyEx
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/29/2019
ms.openlocfilehash: e6630cc3e767531dd94da39fe73d88284c9ca0d0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987559"
---
# <a name="idodownloadinternalsetpropertyex-method"></a><span data-ttu-id="a0651-105">Метод Идодовнлоадинтернал:: Сетпропертекс</span><span class="sxs-lookup"><span data-stu-id="a0651-105">IDODownloadInternal::SetPropertyEx method</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a0651-106">Интерфейс **идодовнлоадинтернал** является устаревшим.</span><span class="sxs-lookup"><span data-stu-id="a0651-106">The **IDODownloadInternal** interface is deprecated.</span></span> <span data-ttu-id="a0651-107">Вместо этого используйте интерфейс [идодовнлоад](../do/nn-do-idodownload.md) .</span><span class="sxs-lookup"><span data-stu-id="a0651-107">Instead, use the [IDODownload](../do/nn-do-idodownload.md) interface.</span></span>

<span data-ttu-id="a0651-108">Задает свойство расширенной загрузки.</span><span class="sxs-lookup"><span data-stu-id="a0651-108">Sets an extended download property.</span></span> <span data-ttu-id="a0651-109">Метод принимает указатель на **вариант** , который содержит определенное значение свойства, применяемое к скачиванию.</span><span class="sxs-lookup"><span data-stu-id="a0651-109">The method accepts a pointer to a **VARIANT** that contains a specific property value to apply to the download.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0651-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a0651-110">Syntax</span></span>

```cpp
HRESULT SetPropertyEx(
  DODownloadPropertyEx propId, 
  VARIANT* propVal
);
```

## <a name="parameters"></a><span data-ttu-id="a0651-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="a0651-111">Parameters</span></span>

`propId`

<span data-ttu-id="a0651-112">Обязательный идентификатор свойства для задания (типа **додовнлоадпропертекс**).</span><span class="sxs-lookup"><span data-stu-id="a0651-112">The required property ID to set (of type **DODownloadPropertyEx**).</span></span>

`propVal`

<span data-ttu-id="a0651-113">Заданное значение свойства, хранящееся в **варианте**.</span><span class="sxs-lookup"><span data-stu-id="a0651-113">The property value to set, stored in a **VARIANT**.</span></span>

## <a name="return-value"></a><span data-ttu-id="a0651-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a0651-114">Return Value</span></span>

<span data-ttu-id="a0651-115">Если функция завершается с ошибкой, она возвращает **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="a0651-115">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="a0651-116">В противном случае возвращается [](/windows/desktop/com/structure-of-com-error-codes) [код ошибки](/windows/desktop/com/com-error-codes-10)HRESULT.</span><span class="sxs-lookup"><span data-stu-id="a0651-116">Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).</span></span>

|<span data-ttu-id="a0651-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a0651-117">Return value</span></span>|<span data-ttu-id="a0651-118">Описание</span><span class="sxs-lookup"><span data-stu-id="a0651-118">Description</span></span>|
|-|-|
|<span data-ttu-id="a0651-119">DO_E_UNKNOWN_PROPERTY_ID</span><span class="sxs-lookup"><span data-stu-id="a0651-119">DO_E_UNKNOWN_PROPERTY_ID</span></span>|<span data-ttu-id="a0651-120">*propId* неизвестен.</span><span class="sxs-lookup"><span data-stu-id="a0651-120">*propId* is unknown.</span></span>|
|<span data-ttu-id="a0651-121">DO_E_INVALID_STATE</span><span class="sxs-lookup"><span data-stu-id="a0651-121">DO_E_INVALID_STATE</span></span>|<span data-ttu-id="a0651-122">Скачивание сейчас не находится в состоянии, допускающем установку свойств.</span><span class="sxs-lookup"><span data-stu-id="a0651-122">The download is not currently in a state that allows setting properties.</span></span>|

## <a name="requirements"></a><span data-ttu-id="a0651-123">Требования</span><span class="sxs-lookup"><span data-stu-id="a0651-123">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="a0651-124">**Минимальная версия клиента**</span><span class="sxs-lookup"><span data-stu-id="a0651-124">**Minimum supported client**</span></span> | <span data-ttu-id="a0651-125">Windows 10, \[ только приложения Win32 версии 1809\]</span><span class="sxs-lookup"><span data-stu-id="a0651-125">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="a0651-126">**Минимальная версия сервера**</span><span class="sxs-lookup"><span data-stu-id="a0651-126">**Minimum supported server**</span></span> | <span data-ttu-id="a0651-127">Windows Server, \[ только приложения Win32 версии 1809\]</span><span class="sxs-lookup"><span data-stu-id="a0651-127">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="a0651-128">**Header**</span><span class="sxs-lookup"><span data-stu-id="a0651-128">**Header**</span></span> | <span data-ttu-id="a0651-129">Додовнлоадинтернал. h</span><span class="sxs-lookup"><span data-stu-id="a0651-129">DODownloadInternal.h</span></span> |