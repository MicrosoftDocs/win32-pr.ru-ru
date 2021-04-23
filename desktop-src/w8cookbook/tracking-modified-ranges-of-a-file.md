---
title: Отслеживание измененных диапазонов файла
description: Отслеживание измененных диапазонов файла
ms.assetid: 756881E9-EFD0-42FE-9B1C-4A2EF1998D71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 664e7a5c0a9148471d2a1a28f2881e1c375089c1
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "105700957"
---
# <a name="tracking-modified-ranges-of-a-file"></a><span data-ttu-id="21d9d-103">Отслеживание измененных диапазонов файла</span><span class="sxs-lookup"><span data-stu-id="21d9d-103">Tracking modified ranges of a file</span></span>

## <a name="platforms"></a><span data-ttu-id="21d9d-104">Платформы</span><span class="sxs-lookup"><span data-stu-id="21d9d-104">Platforms</span></span>

<span data-ttu-id="21d9d-105">**Клиенты —** Windows 8.1 (все номера SKU)</span><span class="sxs-lookup"><span data-stu-id="21d9d-105">**Clients -** Windows 8.1 (all SKUs)</span></span>  
<span data-ttu-id="21d9d-106">**Серверы —** Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="21d9d-106">**Servers -** Windows Server 2012 R2</span></span>  

## <a name="description"></a><span data-ttu-id="21d9d-107">Описание</span><span class="sxs-lookup"><span data-stu-id="21d9d-107">Description</span></span>

<span data-ttu-id="21d9d-108">Команда NT File System (NTFS) добавила в Windows новую функцию.</span><span class="sxs-lookup"><span data-stu-id="21d9d-108">The NT File System (NTFS) team has added a new feature to Windows.</span></span> <span data-ttu-id="21d9d-109">В журнале USN будет выведена запись с порядковым номером обновления (USN), содержащая измененные диапазоны для файла после закрытия.</span><span class="sxs-lookup"><span data-stu-id="21d9d-109">USN Journal will output an update sequence number (USN) record containing modified ranges for a file upon close.</span></span> <span data-ttu-id="21d9d-110">\_ \_ Для записи этих измененных диапазонов файла введен новый тип записи USN запись v4.</span><span class="sxs-lookup"><span data-stu-id="21d9d-110">A new record type, USN\_RECORD\_V4 has been introduced to record these changed ranges of a file.</span></span>

<span data-ttu-id="21d9d-111">Эта функция не включена по умолчанию. Пользователи должны вызвать команду управления файловой системой (ФСКТЛ), чтобы включить ее.</span><span class="sxs-lookup"><span data-stu-id="21d9d-111">The feature is not enabled by default; users must invoke a file system control (FSCTL) command to enable it.</span></span> <span data-ttu-id="21d9d-112">Однако, так как другие компоненты Windows могут включать отслеживание диапазонов, пользователи и разработчики могут принять во внимание, что эта функция всегда включена.</span><span class="sxs-lookup"><span data-stu-id="21d9d-112">However, because other Windows components may turn on range tracking, users and developers may perceive that the feature is always enabled.</span></span> <span data-ttu-id="21d9d-113">Windows позволяет разработчикам запрашивать журнал USN, чтобы определить, включено ли отслеживание диапазона.</span><span class="sxs-lookup"><span data-stu-id="21d9d-113">Windows will allow developers to query USN journal to find out if range tracking is enabled.</span></span>

<span data-ttu-id="21d9d-114">Документация MSDN будет предоставлена позже, чтобы сообщить разработчикам о том, как получить доступ \_ к \_ записям USN записи версии 4.</span><span class="sxs-lookup"><span data-stu-id="21d9d-114">MSDN documentation will be provided at a later date to instruct developers in how to access USN\_RECORD\_V4 records.</span></span>

## <a name="manifestation"></a><span data-ttu-id="21d9d-115">Проявление</span><span class="sxs-lookup"><span data-stu-id="21d9d-115">Manifestation</span></span>

<span data-ttu-id="21d9d-116">Все существующие приложения, использующие журнал USN, продолжают работать без проблем совместимости.</span><span class="sxs-lookup"><span data-stu-id="21d9d-116">All existing applications that use USN Journal will continue to work well without any compatibility issues.</span></span>

 

 




