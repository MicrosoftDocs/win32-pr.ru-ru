---
description: Устанавливает драйверы устройств из программ с настройками сценариев и INF-файлов. Написание программы установки для настройки устройств и установки драйверов. Этот API больше не рекомендуется использовать в целях установки программных приложений.
ms.assetid: 96a9e472-9b92-4976-9379-dc0c96524963
title: API установки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6101c2673e72095d0cf4ebe59c1cece83449d647
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663510"
---
# <a name="setup-api"></a><span data-ttu-id="37dfb-105">API установки</span><span class="sxs-lookup"><span data-stu-id="37dfb-105">Setup API</span></span>

## <a name="purpose"></a><span data-ttu-id="37dfb-106">Назначение</span><span class="sxs-lookup"><span data-stu-id="37dfb-106">Purpose</span></span>

<span data-ttu-id="37dfb-107">API установки предоставляет набор функций, которые приложение установки вызывает для выполнения операций установки.</span><span class="sxs-lookup"><span data-stu-id="37dfb-107">The Setup API provides a set of functions that a setup application calls to perform installation operations.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="37dfb-108">Где применимо</span><span class="sxs-lookup"><span data-stu-id="37dfb-108">Where applicable</span></span>

<span data-ttu-id="37dfb-109">Эти функции установки доступны для разработки приложения установки.</span><span class="sxs-lookup"><span data-stu-id="37dfb-109">These setup functions are available to develop a setup application.</span></span> <span data-ttu-id="37dfb-110">API установки больше не следует использовать для установки приложений.</span><span class="sxs-lookup"><span data-stu-id="37dfb-110">Setup API should no longer be used for installing applications.</span></span> <span data-ttu-id="37dfb-111">Вместо этого используйте [установщик Windows](/windows/desktop/Msi/windows-installer-portal)для разработки установщиков приложений.</span><span class="sxs-lookup"><span data-stu-id="37dfb-111">Instead, use the [Windows Installer](/windows/desktop/Msi/windows-installer-portal)for developing application installers.</span></span> <span data-ttu-id="37dfb-112">API установки будет использоваться для установки драйверов устройств.</span><span class="sxs-lookup"><span data-stu-id="37dfb-112">Setup API continues to be used for installing device drivers.</span></span>

<span data-ttu-id="37dfb-113">API установки предназначен для разработки приложений в стиле рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="37dfb-113">The Setup API is intended for the development of desktop style applications.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="37dfb-114">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="37dfb-114">Developer audience</span></span>

<span data-ttu-id="37dfb-115">Разработчик может использовать API установки, если для приложения установки требуются следующие функциональные возможности.</span><span class="sxs-lookup"><span data-stu-id="37dfb-115">A developer can use the Setup API if their setup application requires the following functionality:</span></span>

-   <span data-ttu-id="37dfb-116">Очередь файлов.</span><span class="sxs-lookup"><span data-stu-id="37dfb-116">Queuing of files.</span></span>
-   <span data-ttu-id="37dfb-117">Установка файлов.</span><span class="sxs-lookup"><span data-stu-id="37dfb-117">Installation of files.</span></span>
-   <span data-ttu-id="37dfb-118">Обработка ошибок установки и запрос носителя.</span><span class="sxs-lookup"><span data-stu-id="37dfb-118">Handling of installation errors and prompting for media.</span></span>
-   <span data-ttu-id="37dfb-119">Обновление записей реестра.</span><span class="sxs-lookup"><span data-stu-id="37dfb-119">Updating registry entries.</span></span>
-   <span data-ttu-id="37dfb-120">Ведение журнала файлов по мере их установки.</span><span class="sxs-lookup"><span data-stu-id="37dfb-120">Logging of files as they are installed.</span></span>
-   <span data-ttu-id="37dfb-121">Хранение последних использованных путей к источникам.</span><span class="sxs-lookup"><span data-stu-id="37dfb-121">Storage of the most recently used source paths.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="37dfb-122">Требования к среде выполнения</span><span class="sxs-lookup"><span data-stu-id="37dfb-122">Run-time requirements</span></span>

<span data-ttu-id="37dfb-123">Сведения о том, какие операционные системы требуются для использования определенной функции, см. в разделе "требования" документации по функции.</span><span class="sxs-lookup"><span data-stu-id="37dfb-123">For information about which operating systems are required to use a particular function, see the Requirements section of the documentation for the function.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="37dfb-124">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="37dfb-124">In this section</span></span>



| <span data-ttu-id="37dfb-125">Раздел</span><span class="sxs-lookup"><span data-stu-id="37dfb-125">Topic</span></span>                                 | <span data-ttu-id="37dfb-126">Описание</span><span class="sxs-lookup"><span data-stu-id="37dfb-126">Description</span></span>                                                                                 |
|---------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="37dfb-127">Обзор</span><span class="sxs-lookup"><span data-stu-id="37dfb-127">Overview</span></span>](overview.md)<br/>   | <span data-ttu-id="37dfb-128">Общие сведения об API установки.</span><span class="sxs-lookup"><span data-stu-id="37dfb-128">General information about Setup API.</span></span><br/>                                             |
| [<span data-ttu-id="37dfb-129">Ссылки</span><span class="sxs-lookup"><span data-stu-id="37dfb-129">Reference</span></span>](reference.md)<br/> | <span data-ttu-id="37dfb-130">Документация по типам данных, структурам, функциям и уведомлениям API установки.</span><span class="sxs-lookup"><span data-stu-id="37dfb-130">Documentation of Setup API data types, structures, functions, and notifications.</span></span><br/> |



 

 

