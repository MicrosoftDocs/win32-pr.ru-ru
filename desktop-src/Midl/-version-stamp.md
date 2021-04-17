---
title: version_stamp Switch
description: '\_Параметр метки/Version подавляет создание макросов, указывающих минимальный необходимый номер версии файла заголовка RPC, рпкндр. h.'
ms.assetid: ec03f68b-60f7-431e-9fba-4434ef082058
keywords:
- /version_stamp параметр MIDL
topic_type:
- apiref
api_name:
- /version_stamp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 704393dce869df4e5f715a1157cdb57967135e42
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "105681543"
---
# <a name="version_stamp-switch"></a><span data-ttu-id="ae4e7-104">\_параметр метки/Version</span><span class="sxs-lookup"><span data-stu-id="ae4e7-104">/version\_stamp switch</span></span>

<span data-ttu-id="ae4e7-105">Параметр **\_ метки/Version** подавляет создание макросов, указывающих минимальный необходимый номер версии файла заголовка RPC, рпкндр. h.</span><span class="sxs-lookup"><span data-stu-id="ae4e7-105">The **/version\_stamp** switch suppresses the generation of macros that specify the minimum required version number of the RPC header file, Rpcndr.h.</span></span>

<span data-ttu-id="ae4e7-106">Новые возможности MIDL могут потребовать, чтобы дополнительные определения правильно компилируют заглушку, поэтому заглушка содержит макросы, которые проверяют совместимость двоичных файлов MIDL и среды сборки.</span><span class="sxs-lookup"><span data-stu-id="ae4e7-106">New MIDL features might require additional definitions to compile the stub correctly, so the stub has macros that check compatibility between MIDL binary files and the build environment.</span></span> <span data-ttu-id="ae4e7-107">Этот параметр может потребоваться использовать при перемещении MIDL в среду построения, отличную от среды, в которой сначала были установлены двоичные файлы MIDL.</span><span class="sxs-lookup"><span data-stu-id="ae4e7-107">You might need to use this switch if you move MIDL to a different build environment than the one in which you first installed the MIDL binary files.</span></span>

<span data-ttu-id="ae4e7-108">Обратите внимание, что смешивание сред сборки не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ae4e7-108">Note that mixing build environments is not supported.</span></span>

``` syntax
midl /version_stamp
```

## <a name="switch-options"></a><span data-ttu-id="ae4e7-109">Параметры коммутатора</span><span class="sxs-lookup"><span data-stu-id="ae4e7-109">Switch Options</span></span>

<span data-ttu-id="ae4e7-110">Этот параметр не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="ae4e7-110">This switch has no parameters.</span></span>

 

 




