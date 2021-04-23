---
title: Функции обратного вызова Прожфс
description: Следующие функции обратного вызова объявляются в прожектедфслиб. h.
ms.assetid: <GUID-GOES-HERE>
ms.date: 01/17/2020
ms.topic: article
ms.openlocfilehash: 1412fc4b406b668ad6651d69835f8cdea56857c5
ms.sourcegitcommit: 62e758931c610782807c7c9fad284921a6c56232
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/22/2020
ms.locfileid: "103890175"
---
# <a name="callback-functions"></a><span data-ttu-id="a0401-103">Функции обратного вызова</span><span class="sxs-lookup"><span data-stu-id="a0401-103">Callback functions</span></span>

<span data-ttu-id="a0401-104">Следующие функции обратного вызова объявляются в прожектедфслиб. h.</span><span class="sxs-lookup"><span data-stu-id="a0401-104">The following callback functions are declared in projectedfslib.h.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="a0401-105">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="a0401-105">In this section</span></span>

| <span data-ttu-id="a0401-106">Раздел</span><span class="sxs-lookup"><span data-stu-id="a0401-106">Topic</span></span> | <span data-ttu-id="a0401-107">Описание</span><span class="sxs-lookup"><span data-stu-id="a0401-107">Description</span></span> |
|-|-|
| [<span data-ttu-id="a0401-108">**PRJ_CANCEL_COMMAND_CB**</span><span class="sxs-lookup"><span data-stu-id="a0401-108">**PRJ_CANCEL_COMMAND_CB**</span></span>](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_cancel_command_cb) | <span data-ttu-id="a0401-109">Уведомляет поставщик о том, что операция с предыдущим вызовом обратного вызова должна быть отменена.</span><span class="sxs-lookup"><span data-stu-id="a0401-109">Notifies the provider that an operation by an earlier invocation of a callback should be canceled.</span></span> |
| [<span data-ttu-id="a0401-110">**PRJ_END_DIRECTORY_ENUMERATION_CB**</span><span class="sxs-lookup"><span data-stu-id="a0401-110">**PRJ_END_DIRECTORY_ENUMERATION_CB**</span></span>](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_end_directory_enumeration_cb) | <span data-ttu-id="a0401-111">Информирует поставщика о перечислении каталогов.</span><span class="sxs-lookup"><span data-stu-id="a0401-111">Informs the provider that a directory enumeration is over.</span></span> |
| [<span data-ttu-id="a0401-112">**PRJ_GET_DIRECTORY_ENUMERATION_CB**</span><span class="sxs-lookup"><span data-stu-id="a0401-112">**PRJ_GET_DIRECTORY_ENUMERATION_CB**</span></span>](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_directory_enumeration_cb) | <span data-ttu-id="a0401-113">Запрашивает сведения о перечислении каталога от поставщика.</span><span class="sxs-lookup"><span data-stu-id="a0401-113">Requests directory enumeration information from the provider.</span></span>
| [<span data-ttu-id="a0401-114">**PRJ_GET_FILE_DATA_CB**</span><span class="sxs-lookup"><span data-stu-id="a0401-114">**PRJ_GET_FILE_DATA_CB**</span></span>](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_file_data_cb) | <span data-ttu-id="a0401-115">Запрашивает содержимое первичного потока данных файла.</span><span class="sxs-lookup"><span data-stu-id="a0401-115">Requests the contents of a file's primary data stream.</span></span>
| [<span data-ttu-id="a0401-116">**PRJ_GET_PLACEHOLDER_INFO_CB**</span><span class="sxs-lookup"><span data-stu-id="a0401-116">**PRJ_GET_PLACEHOLDER_INFO_CB**</span></span>](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_placeholder_info_cb) | <span data-ttu-id="a0401-117">Запрашивает сведения о файле или каталоге от поставщика.</span><span class="sxs-lookup"><span data-stu-id="a0401-117">Requests information for a file or directory from the provider.</span></span>
| [<span data-ttu-id="a0401-118">**PRJ_NOTIFICATION_CB**</span><span class="sxs-lookup"><span data-stu-id="a0401-118">**PRJ_NOTIFICATION_CB**</span></span>](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_notification_cb) | <span data-ttu-id="a0401-119">Доставляет уведомления поставщику об операциях файловой системы.</span><span class="sxs-lookup"><span data-stu-id="a0401-119">Delivers notifications to the provider about file system operations.</span></span>
| [<span data-ttu-id="a0401-120">**PRJ_QUERY_FILE_NAME_CB**</span><span class="sxs-lookup"><span data-stu-id="a0401-120">**PRJ_QUERY_FILE_NAME_CB**</span></span>](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_query_file_name_cb) | <span data-ttu-id="a0401-121">Определяет, существует ли указанный путь к файлу в резервном хранилище поставщика.</span><span class="sxs-lookup"><span data-stu-id="a0401-121">Determines whether a given file path exists in the provider's backing store.</span></span>
| [<span data-ttu-id="a0401-122">**PRJ_START_DIRECTORY_ENUMERATION_CB**</span><span class="sxs-lookup"><span data-stu-id="a0401-122">**PRJ_START_DIRECTORY_ENUMERATION_CB**</span></span>](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_start_directory_enumeration_cb) | <span data-ttu-id="a0401-123">Информирует поставщика о запуске перечисления каталогов.</span><span class="sxs-lookup"><span data-stu-id="a0401-123">Informs the provider that a directory enumeration is starting.</span></span>