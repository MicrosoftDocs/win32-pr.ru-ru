---
title: Установка визуализаций
description: Установка визуализаций
ms.assetid: ca391e38-def5-47da-81f7-94aa96530387
keywords:
- Подключаемые модули проигрывателя Windows Media, визуализации
- подключаемые модули, визуализации
- визуализации, установка
- Пользовательские визуализации, установка
- Установка визуализаций
- визуализации, регистрация
- Пользовательские визуализации, регистрация
- реестр, визуализации
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f1dc8f33d7b5f5b938bee6c89d946955509ab34
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105681466"
---
# <a name="installing-visualizations"></a><span data-ttu-id="8b688-111">Установка визуализаций</span><span class="sxs-lookup"><span data-stu-id="8b688-111">Installing Visualizations</span></span>

<span data-ttu-id="8b688-112">Необходимо указать процесс установки для пользователя визуализации.</span><span class="sxs-lookup"><span data-stu-id="8b688-112">You must provide an installation process for the user of your visualization.</span></span> <span data-ttu-id="8b688-113">Необходимо также предоставить процесс удаления для пользователя.</span><span class="sxs-lookup"><span data-stu-id="8b688-113">You must also provide an uninstall process for the user.</span></span> <span data-ttu-id="8b688-114">Текущая версия проигрывателя Windows Media не устанавливает визуализации из пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="8b688-114">The current version of Windows Media Player does not install visualizations from the user interface.</span></span>

## <a name="installing-to-the-visualization-folder"></a><span data-ttu-id="8b688-115">Установка в папку визуализации</span><span class="sxs-lookup"><span data-stu-id="8b688-115">Installing to the Visualization Folder</span></span>

<span data-ttu-id="8b688-116">Рекомендуется установить все визуализации в подпапке визуализации папки, в которой установлен проигрыватель Windows Media.</span><span class="sxs-lookup"><span data-stu-id="8b688-116">It is recommended that you install all visualizations in the Visualizations subfolder of the folder where Windows Media Player is installed.</span></span>

## <a name="registering-your-visualization"></a><span data-ttu-id="8b688-117">Регистрация визуализации</span><span class="sxs-lookup"><span data-stu-id="8b688-117">Registering Your Visualization</span></span>

<span data-ttu-id="8b688-118">Визуализации представляют собой DLL-библиотеки COM и следуют всем обычным правилам установки и удаления.</span><span class="sxs-lookup"><span data-stu-id="8b688-118">Visualizations are COM DLLs and follow all the normal rules of installation and removal.</span></span> <span data-ttu-id="8b688-119">Для регистрации визуализации можно использовать regsvr32.exe или другие средства установки.</span><span class="sxs-lookup"><span data-stu-id="8b688-119">You can use regsvr32.exe or other installation tools to register your visualization.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8b688-120">См. также</span><span class="sxs-lookup"><span data-stu-id="8b688-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8b688-121">**О пользовательских визуализациях**</span><span class="sxs-lookup"><span data-stu-id="8b688-121">**About Custom Visualizations**</span></span>](about-custom-visualizations.md)
</dt> </dl>

 

 




