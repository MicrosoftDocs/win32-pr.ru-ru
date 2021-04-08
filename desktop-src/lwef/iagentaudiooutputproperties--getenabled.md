---
title: Иажентаудиуутпутпропертиес
description: Иажентаудиуутпутпропертиес
ms.assetid: a1e555e1-98f1-4a3d-b6ba-4cd35348db2b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e86b82c720971ae1e14ee294e6d097fd35ca80a5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067932"
---
# <a name="iagentaudiooutputpropertiesgetenabled"></a><span data-ttu-id="58d2f-103">Иажентаудиуутпутпропертиес:: enable</span><span class="sxs-lookup"><span data-stu-id="58d2f-103">IAgentAudioOutputProperties::GetEnabled</span></span>

<span data-ttu-id="58d2f-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="58d2f-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetEnabled(
long * pbEnabled  // address of variable for audio output Enabled setting 
);                      
```

<span data-ttu-id="58d2f-105">Получает значение, указывающее, включен ли речевой вывод символов.</span><span class="sxs-lookup"><span data-stu-id="58d2f-105">Retrieves a value indicating whether character speech output is enabled.</span></span>

-   <span data-ttu-id="58d2f-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="58d2f-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="58d2f-107"><span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*пбенаблед*</span><span class="sxs-lookup"><span data-stu-id="58d2f-107"><span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbEnabled*</span></span>
</dt> <dd>

<span data-ttu-id="58d2f-108">Адрес переменной, принимающей **значение true** , если речевой вывод включен и **значение false** в случае отключения.</span><span class="sxs-lookup"><span data-stu-id="58d2f-108">Address of a variable that receives **True** if the speech output is currently enabled and **False** if disabled.</span></span>

</dd> </dl>

<span data-ttu-id="58d2f-109">Поскольку этот параметр влияет на речевой вывод (TTS и звуковой файл) для всех символов, только пользователь может изменить это свойство на странице свойств Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="58d2f-109">Because this setting affects spoken output (TTS and sound file) for all characters, only the user can change this property in the Microsoft Agent property sheet.</span></span>

 

 




