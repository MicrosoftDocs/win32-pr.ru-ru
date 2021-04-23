---
title: Интерфейс Идодовнлоадстатускаллбакк
description: Используется для получения уведомлений о скачивании.
keywords:
- Интерфейс Идодовнлоадстатускаллбакк
topic_type:
- apiref
api_name:
- IDODownloadStatusCallback
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 0917b73939535854469a1fe02ea89acc904cf055
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413015"
---
# <a name="idodownloadstatuscallback-interface"></a><span data-ttu-id="36d1f-104">Интерфейс Идодовнлоадстатускаллбакк</span><span class="sxs-lookup"><span data-stu-id="36d1f-104">IDODownloadStatusCallback interface</span></span>

<span data-ttu-id="36d1f-105">Интерфейс **идодовнлоадстатускаллбакк** используется для получения уведомлений о скачивании.</span><span class="sxs-lookup"><span data-stu-id="36d1f-105">The **IDODownloadStatusCallback** interface is used to receive notifications about a download.</span></span>

## <a name="methods"></a><span data-ttu-id="36d1f-106">Методы</span><span class="sxs-lookup"><span data-stu-id="36d1f-106">Methods</span></span>

<span data-ttu-id="36d1f-107">Интерфейс **идодовнлоадстатускаллбакк** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="36d1f-107">The **IDODownloadStatusCallback** interface has these methods.</span></span>

| <span data-ttu-id="36d1f-108">Метод</span><span class="sxs-lookup"><span data-stu-id="36d1f-108">Method</span></span> | <span data-ttu-id="36d1f-109">Описание</span><span class="sxs-lookup"><span data-stu-id="36d1f-109">Description</span></span> |
| ---- |:---- |
| [<span data-ttu-id="36d1f-110">Идодовнлоадстатускаллбакк:: Онстатусчанжед</span><span class="sxs-lookup"><span data-stu-id="36d1f-110">IDODownloadStatusCallback::OnStatusChanged</span></span>](./nf-do-idodownloadstatuscallback-onstatuschanged.md) | <span data-ttu-id="36d1f-111">Вызывает реализацию этого метода при каждом изменении состояния загрузки.</span><span class="sxs-lookup"><span data-stu-id="36d1f-111">DO calls your implementation of this method any time a download status has changed.</span></span> |

## <a name="requirements"></a><span data-ttu-id="36d1f-112">Требования</span><span class="sxs-lookup"><span data-stu-id="36d1f-112">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="36d1f-113">**Минимальная версия клиента**</span><span class="sxs-lookup"><span data-stu-id="36d1f-113">**Minimum supported client**</span></span> | <span data-ttu-id="36d1f-114">Windows 10, \[ только приложения Win32 версии 1809\]</span><span class="sxs-lookup"><span data-stu-id="36d1f-114">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="36d1f-115">**Минимальная версия сервера**</span><span class="sxs-lookup"><span data-stu-id="36d1f-115">**Minimum supported server**</span></span> | <span data-ttu-id="36d1f-116">Windows Server, \[ только приложения Win32 версии 1809\]</span><span class="sxs-lookup"><span data-stu-id="36d1f-116">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="36d1f-117">**Header**</span><span class="sxs-lookup"><span data-stu-id="36d1f-117">**Header**</span></span> | <span data-ttu-id="36d1f-118">Do. h</span><span class="sxs-lookup"><span data-stu-id="36d1f-118">Do.h</span></span> |