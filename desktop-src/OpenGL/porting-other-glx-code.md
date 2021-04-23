---
title: Перенос другого кода ГЛКС
description: Перенос другого кода ГЛКС
ms.assetid: 3a67a206-d249-493c-a774-c3bbaa933611
keywords:
- перенос в OpenGL, код ГЛКС
- Перенос с OpenGL, код ГЛКС
- X Window System, перенос кода ГЛКС
- Функции ГЛКС, перенос
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75c2f9430fbef8bef7c41a2d6c6f86bf6e9f3e7e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105661600"
---
# <a name="porting-other-glx-code"></a><span data-ttu-id="95f46-107">Перенос другого кода ГЛКС</span><span class="sxs-lookup"><span data-stu-id="95f46-107">Porting Other GLX Code</span></span>

<span data-ttu-id="95f46-108">В дополнение к функциям Кслиб и ГЛКС, описанным в предыдущих разделах, возможно, ваша программа содержит некоторые другие функции ГЛКС или Кслиб, перечисленные в разделе [Преобразование библиотеки глкс](translating-the-glx-library.md).</span><span class="sxs-lookup"><span data-stu-id="95f46-108">In addition to the Xlib and GLX functions described in the preceding sections, your program probably contains some of the other GLX or Xlib functions listed in [Translating the GLX Library](translating-the-glx-library.md).</span></span> <span data-ttu-id="95f46-109">Перепишите код системы Window X в Windows, подставив соответствующие функции.</span><span class="sxs-lookup"><span data-stu-id="95f46-109">Rewrite your X Window System code to Windows, substituting the appropriate functions.</span></span>

 

 




