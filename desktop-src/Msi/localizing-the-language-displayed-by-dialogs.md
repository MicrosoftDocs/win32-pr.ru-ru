---
description: Служба установщик Windows использует язык текущего пользователя во всех диалоговых окнах до тех пор, пока не будет открыт пакет установщик Windows.
ms.assetid: c9902990-7a26-48fd-96ac-4d5a749e34be
title: Локализация языка, отображаемого диалоговыми окнами
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 042b2b7f9ac256ebad265b75a8756fc422403e37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683729"
---
# <a name="localizing-the-language-displayed-by-dialogs"></a><span data-ttu-id="8de79-103">Локализация языка, отображаемого диалоговыми окнами</span><span class="sxs-lookup"><span data-stu-id="8de79-103">Localizing the Language Displayed by Dialogs</span></span>

<span data-ttu-id="8de79-104">Служба установщик Windows использует язык текущего пользователя во всех диалоговых окнах до тех пор, пока не будет открыт пакет установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="8de79-104">The Windows Installer service uses the current user's language in all dialogs until a Windows Installer package is opened.</span></span> <span data-ttu-id="8de79-105">Установщик Windows определяет это с помощью **жетусердефаултуилангуаже**.</span><span class="sxs-lookup"><span data-stu-id="8de79-105">The Windows Installer determines this by using **GetUserDefaultUILanguage**.</span></span> <span data-ttu-id="8de79-106">При открытии пакета установщик Windows программа установки отображает диалоговые окна с помощью языка пакета, как указано в свойстве " [**Сводка" шаблона**](template-summary.md) .</span><span class="sxs-lookup"><span data-stu-id="8de79-106">When a Windows Installer package is opened, the installer displays dialogs using the package's language as specified by the [**Template Summary**](template-summary.md) Property.</span></span>

<span data-ttu-id="8de79-107">Дополнительные сведения о локализации языка пакета установщик Windows см. [в разделе Пример локализации](a-localization-example.md).</span><span class="sxs-lookup"><span data-stu-id="8de79-107">For more information about localizing the language of a Windows Installer package, see also [A Localization Example](a-localization-example.md).</span></span>

 

 



