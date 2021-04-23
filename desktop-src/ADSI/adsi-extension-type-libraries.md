---
title: Библиотеки типов расширений ADSI
description: Библиотеки типов для расширений не объединяются.
ms.assetid: 33cde2fe-9b90-4f63-a215-cf0c8f8defb1
ms.tgt_platform: multiple
keywords:
- Библиотеки типов расширений ADSI ADSI
- расширения ADSI, библиотеки типов расширений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7efc89bd491d5ee244c5a2a64dd7df4c84b61ff
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104531862"
---
# <a name="adsi-extension-type-libraries"></a><span data-ttu-id="b10b3-105">Библиотеки типов расширений ADSI</span><span class="sxs-lookup"><span data-stu-id="b10b3-105">ADSI Extension Type Libraries</span></span>

<span data-ttu-id="b10b3-106">Библиотеки типов для расширений не объединяются.</span><span class="sxs-lookup"><span data-stu-id="b10b3-106">The type libraries for extensions are not merged.</span></span> <span data-ttu-id="b10b3-107">Клиенты ADSI должны явно включать библиотеку типов для каждого расширения.</span><span class="sxs-lookup"><span data-stu-id="b10b3-107">ADSI clients must specifically include the type library for each extension.</span></span> <span data-ttu-id="b10b3-108">Библиотека типов необходима для Visual Basic для включения ранних привязок.</span><span class="sxs-lookup"><span data-stu-id="b10b3-108">The type library is required for Visual Basic to enable early bindings.</span></span> <span data-ttu-id="b10b3-109">Клиентские приложения, написанные на C/C++, могут вызывать метод **QueryInterface** для интерфейсов расширения, определенных в файлах заголовков расширений.</span><span class="sxs-lookup"><span data-stu-id="b10b3-109">Client applications written in C/C++ can call the **QueryInterface** method on the extension interfaces defined in the extension header files.</span></span>

 

 




