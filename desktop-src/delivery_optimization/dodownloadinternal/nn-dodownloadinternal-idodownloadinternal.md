---
title: Интерфейс Идодовнлоадинтернал
description: Используется для получения или задания расширенных свойств загрузки.
keywords:
- Интерфейс Идодовнлоадинтернал
topic_type:
- apiref
api_name:
- IDODownloadInternal
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/29/2019
ms.openlocfilehash: 89dcf0e397e9761c1b156a4ad4b245209cf50020
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104134250"
---
# <a name="idodownloadinternal-interface"></a><span data-ttu-id="cf4f8-104">Интерфейс Идодовнлоадинтернал</span><span class="sxs-lookup"><span data-stu-id="cf4f8-104">IDODownloadInternal interface</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cf4f8-105">Интерфейс **идодовнлоадинтернал** является устаревшим.</span><span class="sxs-lookup"><span data-stu-id="cf4f8-105">The **IDODownloadInternal** interface is deprecated.</span></span> <span data-ttu-id="cf4f8-106">Вместо этого используйте интерфейс [идодовнлоад](../do/nn-do-idodownload.md) .</span><span class="sxs-lookup"><span data-stu-id="cf4f8-106">Instead, use the [IDODownload](../do/nn-do-idodownload.md) interface.</span></span>

<span data-ttu-id="cf4f8-107">Интерфейс **идодовнлоадинтернал** используется для получения или задания расширенных свойств загрузки.</span><span class="sxs-lookup"><span data-stu-id="cf4f8-107">The **IDODownloadInternal** interface is used to get or set extended download properties.</span></span>

## <a name="methods"></a><span data-ttu-id="cf4f8-108">Методы</span><span class="sxs-lookup"><span data-stu-id="cf4f8-108">Methods</span></span>

<span data-ttu-id="cf4f8-109">Интерфейс **идодовнлоадинтернал** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="cf4f8-109">The **IDODownloadInternal** interface has these methods.</span></span>

| <span data-ttu-id="cf4f8-110">Метод</span><span class="sxs-lookup"><span data-stu-id="cf4f8-110">Method</span></span> | <span data-ttu-id="cf4f8-111">Описание</span><span class="sxs-lookup"><span data-stu-id="cf4f8-111">Description</span></span> |
| ---- |:---- |
| [<span data-ttu-id="cf4f8-112">Идодовнлоадинтернал:: Жетпропертекс</span><span class="sxs-lookup"><span data-stu-id="cf4f8-112">IDODownloadInternal::GetPropertyEx</span></span>](./nf-dodownloadinternal-idodownloadinternal-getpropertyex.md) | <span data-ttu-id="cf4f8-113">Извлекает указатель на **вариант** , содержащий определенное значение расширенного свойства загрузки.</span><span class="sxs-lookup"><span data-stu-id="cf4f8-113">Retrieves a pointer to a **VARIANT** that contains a specific extended download property value.</span></span> |
| [<span data-ttu-id="cf4f8-114">Идодовнлоадинтернал:: Сетпропертекс</span><span class="sxs-lookup"><span data-stu-id="cf4f8-114">IDODownloadInternal::SetPropertyEx</span></span>](./nf-dodownloadinternal-idodownloadinternal-setpropertyex.md) | <span data-ttu-id="cf4f8-115">Задает свойство расширенной загрузки.</span><span class="sxs-lookup"><span data-stu-id="cf4f8-115">Sets an extended download property.</span></span> <span data-ttu-id="cf4f8-116">Метод принимает указатель на **вариант** , который содержит определенное значение свойства, применяемое к скачиванию.</span><span class="sxs-lookup"><span data-stu-id="cf4f8-116">The method accepts a pointer to a **VARIANT** that contains a specific property value to apply to the download.</span></span> |

## <a name="requirements"></a><span data-ttu-id="cf4f8-117">Требования</span><span class="sxs-lookup"><span data-stu-id="cf4f8-117">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="cf4f8-118">**Минимальная версия клиента**</span><span class="sxs-lookup"><span data-stu-id="cf4f8-118">**Minimum supported client**</span></span> | <span data-ttu-id="cf4f8-119">Windows 10, \[ только приложения Win32 версии 1809\]</span><span class="sxs-lookup"><span data-stu-id="cf4f8-119">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="cf4f8-120">**Минимальная версия сервера**</span><span class="sxs-lookup"><span data-stu-id="cf4f8-120">**Minimum supported server**</span></span> | <span data-ttu-id="cf4f8-121">Windows Server, \[ только приложения Win32 версии 1809\]</span><span class="sxs-lookup"><span data-stu-id="cf4f8-121">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="cf4f8-122">**Header**</span><span class="sxs-lookup"><span data-stu-id="cf4f8-122">**Header**</span></span> | <span data-ttu-id="cf4f8-123">Додовнлоадинтернал. h</span><span class="sxs-lookup"><span data-stu-id="cf4f8-123">DODownloadInternal.h</span></span> |