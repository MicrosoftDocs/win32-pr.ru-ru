---
title: Обнаружение проигрывателя Windows Media из приложения
description: Обнаружение проигрывателя Windows Media из приложения
ms.assetid: 3cf8a619-3b7e-45af-af6b-4711a45c7e07
keywords:
- Проигрыватель Windows Media, обнаружение из приложений
- обнаружение проигрывателя Windows Media из приложений
- реестр, обнаружение проигрывателя Windows Media из приложений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03ae0c7d30b71749a22ecef10806817cd4182224
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105691356"
---
# <a name="detecting-windows-media-player-from-an-application"></a><span data-ttu-id="2a0ec-106">Обнаружение проигрывателя Windows Media из приложения</span><span class="sxs-lookup"><span data-stu-id="2a0ec-106">Detecting Windows Media Player from an Application</span></span>

<span data-ttu-id="2a0ec-107">Чтобы определить, какая версия проигрывателя Windows Media установлена, проверьте следующий раздел реестра:</span><span class="sxs-lookup"><span data-stu-id="2a0ec-107">You can determine what version of Windows Media Player is installed by checking the following registry key:</span></span>

<span data-ttu-id="2a0ec-108">**HKEY \_ по для локального \_ компьютера \\ программное обеспечение \\ Microsoft \\ Active Setup \\ установленные компоненты**</span><span class="sxs-lookup"><span data-stu-id="2a0ec-108">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Active Setup\\Installed Components**</span></span>

<span data-ttu-id="2a0ec-109">Для проигрывателя Windows Media 6,4 просмотрите раздел **{22d6f312-b0f6-11D0-94ab-0080c74c7e95}**.</span><span class="sxs-lookup"><span data-stu-id="2a0ec-109">For Windows Media Player 6.4, look at key **{22d6f312-b0f6-11d0-94ab-0080c74c7e95}**.</span></span>

<span data-ttu-id="2a0ec-110">Для проигрывателя Windows Media 7 или более поздней версии ознакомьтесь с разделом **{6BF52A52-394A-11D3-B153-00C04F79FAA6}**.</span><span class="sxs-lookup"><span data-stu-id="2a0ec-110">For Windows Media Player 7 or later, look at key **{6BF52A52-394A-11d3-B153-00C04F79FAA6}**.</span></span>

<span data-ttu-id="2a0ec-111">В любом из этих ключей, если **установлен**</span><span class="sxs-lookup"><span data-stu-id="2a0ec-111">Under either of these keys, if the **IsInstalled**</span></span><dl> <dt>

<span data-ttu-id="2a0ec-112">Тип данных</span><span class="sxs-lookup"><span data-stu-id="2a0ec-112">Data type</span></span>
</dt> <dd><span data-ttu-id="2a0ec-113">DWORD</span><span class="sxs-lookup"><span data-stu-id="2a0ec-113">DWORD</span></span></dd> </dl> DWORD value is set to 0x1, you can safely use the **Version**<dl> <dt>

<span data-ttu-id="2a0ec-114">Тип данных</span><span class="sxs-lookup"><span data-stu-id="2a0ec-114">Data type</span></span>
</dt> <dd><span data-ttu-id="2a0ec-115">строка</span><span class="sxs-lookup"><span data-stu-id="2a0ec-115">string</span></span></dd> </dl> string value as the version of Windows Media Player that is installed.

## <a name="related-topics"></a><span data-ttu-id="2a0ec-116">См. также</span><span class="sxs-lookup"><span data-stu-id="2a0ec-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a0ec-117">**Распространение программного обеспечения проигрывателя Windows Media**</span><span class="sxs-lookup"><span data-stu-id="2a0ec-117">**Redistributing Windows Media Player Software**</span></span>](redistributing-windows-media-player-software.md)
</dt> </dl>

 

 




