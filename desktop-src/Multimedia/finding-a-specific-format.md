---
title: Поиск определенного формата
description: Поиск определенного формата
ms.assetid: 0c892758-d409-4ed7-8f38-a24eee646b65
keywords:
- Диспетчер аудиосжатия (ACM), поиск форматов
- ACM (диспетчер аудиосжатия), поиск форматов
- Примеры ACM, поиск форматов
- Поиск форматов
- Функция Акмформатенум
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c148c075df09cb702caf6b1d192fe8ce41b48ad0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986743"
---
# <a name="finding-a-specific-format"></a><span data-ttu-id="34c9a-108">Поиск определенного формата</span><span class="sxs-lookup"><span data-stu-id="34c9a-108">Finding a Specific Format</span></span>

<span data-ttu-id="34c9a-109">Приложение может иметь только частичную спецификацию для формата, когда требуется полная спецификация.</span><span class="sxs-lookup"><span data-stu-id="34c9a-109">An application might have only a partial specification for a format when it needs the full specification.</span></span> <span data-ttu-id="34c9a-110">Например, спецификация может указывать на формат моно, 4-разрядного формата ADPCM в 11 кГц, но не в среднем байт в секунду.</span><span class="sxs-lookup"><span data-stu-id="34c9a-110">For example, the specification might stipulate an 11-kHz mono, 4-bit ADPCM format, but not the average bytes per second.</span></span> <span data-ttu-id="34c9a-111">Приложение может получить полный формат без вмешательства пользователя с помощью функции [**акмформатенум**](/windows/desktop/api/Msacm/nf-msacm-acmformatenum) и указания флагов в параметре *фдвенум* .</span><span class="sxs-lookup"><span data-stu-id="34c9a-111">The application can get the full format without user intervention by using the [**acmFormatEnum**](/windows/desktop/api/Msacm/nf-msacm-acmformatenum) function and specifying flags in the *fdwEnum* parameter.</span></span>

 

 




