---
title: Интерфейс Идодовнлоад
description: Используется для запуска загрузки и управления им.
keywords:
- Интерфейс Идодовнлоад
topic_type:
- apiref
api_name:
- IDODownload
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: ec2f74ce7daae6f612297d21e15e6993fcd78382
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337644"
---
# <a name="idodownload-interface"></a><span data-ttu-id="ed669-104">Интерфейс Идодовнлоад</span><span class="sxs-lookup"><span data-stu-id="ed669-104">IDODownload interface</span></span>

<span data-ttu-id="ed669-105">Интерфейс **идодовнлоад** используется для запуска загрузки и управления им.</span><span class="sxs-lookup"><span data-stu-id="ed669-105">The **IDODownload** interface is used to start and manage a download.</span></span>

## <a name="methods"></a><span data-ttu-id="ed669-106">Методы</span><span class="sxs-lookup"><span data-stu-id="ed669-106">Methods</span></span>

<span data-ttu-id="ed669-107">Интерфейс **идодовнлоад** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="ed669-107">The **IDODownload** interface has these methods.</span></span>

| <span data-ttu-id="ed669-108">Метод</span><span class="sxs-lookup"><span data-stu-id="ed669-108">Method</span></span> | <span data-ttu-id="ed669-109">Описание</span><span class="sxs-lookup"><span data-stu-id="ed669-109">Description</span></span> |
| ---- |:---- |
| [<span data-ttu-id="ed669-110">Идодовнлоад:: Abort</span><span class="sxs-lookup"><span data-stu-id="ed669-110">IDODownload::Abort</span></span>](./nf-do-idomanager-createdownload.md) | <span data-ttu-id="ed669-111">Прерывает скачивание.</span><span class="sxs-lookup"><span data-stu-id="ed669-111">Aborts the download.</span></span> |
| [<span data-ttu-id="ed669-112">Идодовнлоад:: Finalize</span><span class="sxs-lookup"><span data-stu-id="ed669-112">IDODownload::Finalize</span></span>](./nf-do-idodownload-finalize.md) | <span data-ttu-id="ed669-113">Завершает скачивание.</span><span class="sxs-lookup"><span data-stu-id="ed669-113">Finalizes the download.</span></span> |
| [<span data-ttu-id="ed669-114">Идодовнлоад:: Property</span><span class="sxs-lookup"><span data-stu-id="ed669-114">IDODownload::GetProperty</span></span>](./nf-do-idodownload-getproperty.md) | <span data-ttu-id="ed669-115">Извлекает указатель на **вариант** , содержащий определенное свойство загрузки.</span><span class="sxs-lookup"><span data-stu-id="ed669-115">Retrieves a pointer to a **VARIANT** that contains a specific download property.</span></span> |
| [<span data-ttu-id="ed669-116">Идодовнлоад::/Status</span><span class="sxs-lookup"><span data-stu-id="ed669-116">IDODownload::GetStatus</span></span>](./nf-do-idodownload-getstatus.md) | <span data-ttu-id="ed669-117">Получает указатель на структуру **DO_DOWNLOAD_STATUS** , отражающую текущее состояние загрузки.</span><span class="sxs-lookup"><span data-stu-id="ed669-117">Retrieves a pointer to a **DO_DOWNLOAD_STATUS** structure that reflects the current status of the download.</span></span> |
| [<span data-ttu-id="ed669-118">Идодовнлоад::P Аусе</span><span class="sxs-lookup"><span data-stu-id="ed669-118">IDODownload::Pause</span></span>](./nf-do-idodownload-pause.md) | <span data-ttu-id="ed669-119">Приостанавливает скачивание.</span><span class="sxs-lookup"><span data-stu-id="ed669-119">Pauses the download.</span></span> |
| [<span data-ttu-id="ed669-120">Идодовнлоад:: SetProperty</span><span class="sxs-lookup"><span data-stu-id="ed669-120">IDODownload::SetProperty</span></span>](./nf-do-idodownload-setproperty.md) | <span data-ttu-id="ed669-121">Задает свойство загрузки.</span><span class="sxs-lookup"><span data-stu-id="ed669-121">Sets a download property.</span></span> |
| [<span data-ttu-id="ed669-122">Идодовнлоад:: Start</span><span class="sxs-lookup"><span data-stu-id="ed669-122">IDODownload::Start</span></span>](./nf-do-idodownload-start.md) | <span data-ttu-id="ed669-123">Запускает или возобновляет загрузку.</span><span class="sxs-lookup"><span data-stu-id="ed669-123">Starts or resumes a download.</span></span> |

## <a name="requirements"></a><span data-ttu-id="ed669-124">Требования</span><span class="sxs-lookup"><span data-stu-id="ed669-124">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="ed669-125">**Минимальная версия клиента**</span><span class="sxs-lookup"><span data-stu-id="ed669-125">**Minimum supported client**</span></span> | <span data-ttu-id="ed669-126">Windows 10, \[ только приложения Win32 версии 1809\]</span><span class="sxs-lookup"><span data-stu-id="ed669-126">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="ed669-127">**Минимальная версия сервера**</span><span class="sxs-lookup"><span data-stu-id="ed669-127">**Minimum supported server**</span></span> | <span data-ttu-id="ed669-128">Windows Server, \[ только приложения Win32 версии 1809\]</span><span class="sxs-lookup"><span data-stu-id="ed669-128">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="ed669-129">**Header**</span><span class="sxs-lookup"><span data-stu-id="ed669-129">**Header**</span></span> | <span data-ttu-id="ed669-130">Do. h</span><span class="sxs-lookup"><span data-stu-id="ed669-130">Do.h</span></span> |