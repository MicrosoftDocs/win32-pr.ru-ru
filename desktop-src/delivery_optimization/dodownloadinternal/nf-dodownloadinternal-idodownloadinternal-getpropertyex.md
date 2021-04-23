---
title: 'Метод Идодовнлоадинтернал:: Жетпропертекс'
description: Извлекает указатель на **вариант** , содержащий определенное значение расширенного свойства загрузки.
keywords:
- 'Метод Идодовнлоадинтернал:: Жетпропертекс'
topic_type:
- apiref
api_name:
- IDODownloadInternal.GetPropertyEx
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/29/2019
ms.openlocfilehash: 908f9b15df5c0c4a2769149419ff12d545201e5c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413222"
---
# <a name="idodownloadinternalgetpropertyex-method"></a><span data-ttu-id="69c53-104">Метод Идодовнлоадинтернал:: Жетпропертекс</span><span class="sxs-lookup"><span data-stu-id="69c53-104">IDODownloadInternal::GetPropertyEx method</span></span>

> [!IMPORTANT]
> <span data-ttu-id="69c53-105">Интерфейс **идодовнлоадинтернал** является устаревшим.</span><span class="sxs-lookup"><span data-stu-id="69c53-105">The **IDODownloadInternal** interface is deprecated.</span></span> <span data-ttu-id="69c53-106">Вместо этого используйте интерфейс [идодовнлоад](../do/nn-do-idodownload.md) .</span><span class="sxs-lookup"><span data-stu-id="69c53-106">Instead, use the [IDODownload](../do/nn-do-idodownload.md) interface.</span></span>

<span data-ttu-id="69c53-107">Извлекает указатель на **вариант** , содержащий определенное значение расширенного свойства загрузки.</span><span class="sxs-lookup"><span data-stu-id="69c53-107">Retrieves a pointer to a **VARIANT** that contains a specific extended download property value.</span></span>

## <a name="syntax"></a><span data-ttu-id="69c53-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="69c53-108">Syntax</span></span>

```cpp
HRESULT GetPropertyEx(
  DODownloadPropertyEx propId, 
  VARIANT* propVal
);
```

## <a name="parameters"></a><span data-ttu-id="69c53-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="69c53-109">Parameters</span></span>

`propId`

<span data-ttu-id="69c53-110">Обязательный идентификатор свойства для получения (типа **додовнлоадпропертекс**).</span><span class="sxs-lookup"><span data-stu-id="69c53-110">The required property ID to get (of type **DODownloadPropertyEx**).</span></span>

`propVal`

<span data-ttu-id="69c53-111">Результирующее значение свойства, хранящееся в **варианте**.</span><span class="sxs-lookup"><span data-stu-id="69c53-111">The resulting property value, stored in a **VARIANT**.</span></span>

## <a name="return-value"></a><span data-ttu-id="69c53-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="69c53-112">Return Value</span></span>

<span data-ttu-id="69c53-113">Если функция завершается с ошибкой, она возвращает **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="69c53-113">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="69c53-114">В противном случае возвращается [](/windows/desktop/com/structure-of-com-error-codes) [код ошибки](/windows/desktop/com/com-error-codes-10)HRESULT.</span><span class="sxs-lookup"><span data-stu-id="69c53-114">Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).</span></span>

|<span data-ttu-id="69c53-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="69c53-115">Return value</span></span>|<span data-ttu-id="69c53-116">Описание</span><span class="sxs-lookup"><span data-stu-id="69c53-116">Description</span></span>|
|-|-|
|<span data-ttu-id="69c53-117">DO_E_UNKNOWN_PROPERTY_ID</span><span class="sxs-lookup"><span data-stu-id="69c53-117">DO_E_UNKNOWN_PROPERTY_ID</span></span>|<span data-ttu-id="69c53-118">*propId* неизвестен.</span><span class="sxs-lookup"><span data-stu-id="69c53-118">*propId* is unknown.</span></span>|
|<span data-ttu-id="69c53-119">DO_E_WRITE_ONLY_PROPERTY</span><span class="sxs-lookup"><span data-stu-id="69c53-119">DO_E_WRITE_ONLY_PROPERTY</span></span>|<span data-ttu-id="69c53-120">Свойство доступно только для записи и не может быть прочитано.</span><span class="sxs-lookup"><span data-stu-id="69c53-120">The property is write-only, and cannot be read.</span></span>|
|<span data-ttu-id="69c53-121">E_NOT_SET</span><span class="sxs-lookup"><span data-stu-id="69c53-121">E_NOT_SET</span></span>|<span data-ttu-id="69c53-122">Такое свойство не было задано через **сетпропертекс**.</span><span class="sxs-lookup"><span data-stu-id="69c53-122">No such property was set via **SetPropertyEx**.</span></span>|

## <a name="requirements"></a><span data-ttu-id="69c53-123">Требования</span><span class="sxs-lookup"><span data-stu-id="69c53-123">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="69c53-124">**Минимальная версия клиента**</span><span class="sxs-lookup"><span data-stu-id="69c53-124">**Minimum supported client**</span></span> | <span data-ttu-id="69c53-125">Windows 10, \[ только приложения Win32 версии 1809\]</span><span class="sxs-lookup"><span data-stu-id="69c53-125">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="69c53-126">**Минимальная версия сервера**</span><span class="sxs-lookup"><span data-stu-id="69c53-126">**Minimum supported server**</span></span> | <span data-ttu-id="69c53-127">Windows Server, \[ только приложения Win32 версии 1809\]</span><span class="sxs-lookup"><span data-stu-id="69c53-127">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="69c53-128">**Header**</span><span class="sxs-lookup"><span data-stu-id="69c53-128">**Header**</span></span> | <span data-ttu-id="69c53-129">Додовнлоадинтернал. h</span><span class="sxs-lookup"><span data-stu-id="69c53-129">DODownloadInternal.h</span></span> |