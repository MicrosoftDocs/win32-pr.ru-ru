---
title: Перечисление Додовнлоадстате
description: Указывает идентификатор текущего состояния загрузки, который является частью структуры **DO_DOWNLOAD_STATUS** .
keywords:
- Перечисление Додовнлоадстате, Додовнлоадстате
topic_type:
- apiref
api_name:
- DODownloadState
api_location:
- deliveryoptimizationdownloadtypes.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/02/2019
ms.openlocfilehash: 4fb882a26d20de3094aa46763d6e1538ccf0c643
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534931"
---
# <a name="dodownloadstate-enumeration"></a><span data-ttu-id="51634-104">Перечисление Додовнлоадстате</span><span class="sxs-lookup"><span data-stu-id="51634-104">DODownloadState enumeration</span></span>

<span data-ttu-id="51634-105">Перечисление **додовнлоадстате** указывает идентификатор текущего состояния загрузки, который является частью структуры **DO_DOWNLOAD_STATUS** .</span><span class="sxs-lookup"><span data-stu-id="51634-105">The **DODownloadState** enumeration specifies the ID of the current download state, which is part of the **DO_DOWNLOAD_STATUS** structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="51634-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="51634-106">Syntax</span></span>

```cpp
typedef enum _DODownloadState
{
  DODownloadState_Created = 0, 
  DODownloadState_Transferring,
  DODownloadState_Transferred, 
  DODownloadState_Finalized,   
  DODownloadState_Aborted,     
  DODownloadState_Paused
} DODownloadState;
```

## <a name="constants"></a><span data-ttu-id="51634-107">Константы</span><span class="sxs-lookup"><span data-stu-id="51634-107">Constants</span></span>

| <span data-ttu-id="51634-108">Требование</span><span class="sxs-lookup"><span data-stu-id="51634-108">Requirement</span></span> | <span data-ttu-id="51634-109">Значение</span><span class="sxs-lookup"><span data-stu-id="51634-109">Value</span></span> |
|-|-|
| <span data-ttu-id="51634-110">DODownloadState_Created</span><span class="sxs-lookup"><span data-stu-id="51634-110">DODownloadState_Created</span></span> | <span data-ttu-id="51634-111">Объект скачивания создан, но еще не запущен.</span><span class="sxs-lookup"><span data-stu-id="51634-111">Download object is created but hasn't been started yet.</span></span> |
| <span data-ttu-id="51634-112">DODownloadState_Transferring</span><span class="sxs-lookup"><span data-stu-id="51634-112">DODownloadState_Transferring</span></span> | <span data-ttu-id="51634-113">Идет скачивание.</span><span class="sxs-lookup"><span data-stu-id="51634-113">Download is in progress.</span></span> |
| <span data-ttu-id="51634-114">DODownloadState_Transferred</span><span class="sxs-lookup"><span data-stu-id="51634-114">DODownloadState_Transferred</span></span> | <span data-ttu-id="51634-115">Загрузка передается, и ее можно запустить снова, загрузив другую часть файла.</span><span class="sxs-lookup"><span data-stu-id="51634-115">Download is transferred and can start again by downloading another portion of the file.</span></span> |
| <span data-ttu-id="51634-116">DODownloadState_Finalized</span><span class="sxs-lookup"><span data-stu-id="51634-116">DODownloadState_Finalized</span></span> | <span data-ttu-id="51634-117">Скачивание завершено, и его невозможно запустить снова.</span><span class="sxs-lookup"><span data-stu-id="51634-117">Download is finalized and cannot be started again.</span></span> |
| <span data-ttu-id="51634-118">DODownloadState_Aborted</span><span class="sxs-lookup"><span data-stu-id="51634-118">DODownloadState_Aborted</span></span> | <span data-ttu-id="51634-119">Скачивание прервано.</span><span class="sxs-lookup"><span data-stu-id="51634-119">Download was aborted.</span></span> |
| <span data-ttu-id="51634-120">DODownloadState_Paused</span><span class="sxs-lookup"><span data-stu-id="51634-120">DODownloadState_Paused</span></span> | <span data-ttu-id="51634-121">Скачивание приостановлено по требованию или из-за временной ошибки.</span><span class="sxs-lookup"><span data-stu-id="51634-121">Download has been paused on demand or due to transient error.</span></span> |

## <a name="requirements"></a><span data-ttu-id="51634-122">Требования</span><span class="sxs-lookup"><span data-stu-id="51634-122">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="51634-123">**Минимальная версия клиента**</span><span class="sxs-lookup"><span data-stu-id="51634-123">**Minimum supported client**</span></span> | <span data-ttu-id="51634-124">Windows 10, \[ только приложения Win32 версии 1809\]</span><span class="sxs-lookup"><span data-stu-id="51634-124">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="51634-125">**Минимальная версия сервера**</span><span class="sxs-lookup"><span data-stu-id="51634-125">**Minimum supported server**</span></span> | <span data-ttu-id="51634-126">Windows Server, \[ только приложения Win32 версии 1809\]</span><span class="sxs-lookup"><span data-stu-id="51634-126">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="51634-127">**Header**</span><span class="sxs-lookup"><span data-stu-id="51634-127">**Header**</span></span> | <span data-ttu-id="51634-128">Деливерйоптимизатиондовнлоадтипес. h</span><span class="sxs-lookup"><span data-stu-id="51634-128">DeliveryOptimizationDownloadTypes.h</span></span> |
