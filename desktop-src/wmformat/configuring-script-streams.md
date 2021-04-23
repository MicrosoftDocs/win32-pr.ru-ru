---
title: Настройка потоков скриптов
description: Настройка потоков скриптов
ms.assetid: f8f1656e-69c6-47f7-a8eb-c1039a84ebf3
keywords:
- потоки, Настройка потоков скриптов
- кодеки, Настройка потоков сценариев
- Создание скриптов для потоков, Настройка
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e063865b301c8c7c2a4171aa530a89464306c0ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067847"
---
# <a name="configuring-script-streams"></a><span data-ttu-id="f1593-106">Настройка потоков скриптов</span><span class="sxs-lookup"><span data-stu-id="f1593-106">Configuring Script Streams</span></span>

<span data-ttu-id="f1593-107">Как и для всех произвольных типов потоков, потоки сценариев должны иметь определенную скорость потока и окно буфера.</span><span class="sxs-lookup"><span data-stu-id="f1593-107">Like all arbitrary stream types, script streams need to have a bit rate and buffer window defined for them.</span></span> <span data-ttu-id="f1593-108">Основной тип носителя в структуре [**\_ \_ типа мультимедиа WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) должен быть установлен в вммедиатипе \_ script.</span><span class="sxs-lookup"><span data-stu-id="f1593-108">The major media type in the [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure must be set to WMMEDIATYPE\_Script.</span></span>

<span data-ttu-id="f1593-109">Для потоков сценариев необходимо, чтобы член **форматтипе** **\_ \_ типа мультимедиа WM** был установлен в вмформат \_ скрипт, который указывает, что элемент **пбформат** указывает на структуру [**вмскриптформат**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmscriptformat) .</span><span class="sxs-lookup"><span data-stu-id="f1593-109">Script streams need to have the **formattype** member of **WM\_MEDIA\_TYPE** set to WMFORMAT\_Script, which indicates that the **pbFormat** member points to a [**WMSCRIPTFORMAT**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmscriptformat) structure.</span></span>

<span data-ttu-id="f1593-110">Существует только один поддерживаемый тип скрипта, ВМСКРИПТТИПЕ \_ твострингс.</span><span class="sxs-lookup"><span data-stu-id="f1593-110">There is only one supported script type, WMSCRIPTTYPE\_TwoStrings.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f1593-111">См. также</span><span class="sxs-lookup"><span data-stu-id="f1593-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1593-112">**Общая конфигурация для всех потоков**</span><span class="sxs-lookup"><span data-stu-id="f1593-112">**Configuration Common to All Streams**</span></span>](configuration-common-to-all-streams.md)
</dt> <dt>

[<span data-ttu-id="f1593-113">**Настройка произвольных типов потоков**</span><span class="sxs-lookup"><span data-stu-id="f1593-113">**Configuring Arbitrary Stream Types**</span></span>](configuring-arbitrary-stream-types.md)
</dt> <dt>

[<span data-ttu-id="f1593-114">**Команды скриптов**</span><span class="sxs-lookup"><span data-stu-id="f1593-114">**Script Commands**</span></span>](script-commands.md)
</dt> </dl>

 

 




