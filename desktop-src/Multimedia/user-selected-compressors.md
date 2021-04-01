---
title: User-Selected программы сжатия
description: User-Selected программы сжатия
ms.assetid: 38569f9c-2df3-4959-990b-5c33203ff916
keywords:
- Диспетчер сжатия видео (ВКМ), выбранные пользователем компрессоры
- ВКМ (диспетчер сжатия видео), выбранные пользователем компрессоры
- Функция Иккомпрессорчусе
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbbba48b919265ea6e0bab2c3d891f628c4e660a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986639"
---
# <a name="user-selected-compressors"></a><span data-ttu-id="625c7-106">User-Selected программы сжатия</span><span class="sxs-lookup"><span data-stu-id="625c7-106">User-Selected Compressors</span></span>

<span data-ttu-id="625c7-107">При сжатии данных приложение может использовать функцию [**иккомпрессорчусе**](/windows/desktop/api/Vfw/nf-vfw-iccompressorchoose) для создания диалогового окна, в котором пользователь может выбрать программу сжатия.</span><span class="sxs-lookup"><span data-stu-id="625c7-107">When compressing data, your application can use the [**ICCompressorChoose**](/windows/desktop/api/Vfw/nf-vfw-iccompressorchoose) function to create a dialog box in which the user can select the compressor.</span></span> <span data-ttu-id="625c7-108">Можно задать флаги для этой функции, чтобы разрешить пользователю указывать частоту ключевых кадров и скорость передачи данных с помощью фильмов, а также отображать окно предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="625c7-108">You can specify flags for this function to allow the user to specify the key-frame frequency and the movie-data rate, or to display a preview window.</span></span>

<span data-ttu-id="625c7-109">Автоматически открывается компрессор, выбранный пользователем, и его маркер возвращается в элемент ХИК структуры [**компварс**](/windows/desktop/api/Vfw/ns-vfw-compvars) , указанной в **иккомпрессорчусе**.</span><span class="sxs-lookup"><span data-stu-id="625c7-109">The compressor selected by the user is automatically opened and its handle is returned in the hic member of the [**COMPVARS**](/windows/desktop/api/Vfw/ns-vfw-compvars) structure specified in **ICCompressorChoose**.</span></span>

<span data-ttu-id="625c7-110">При использовании **иккомпрессорчусе** используйте функцию [**иккомпрессорфри**](/windows/desktop/api/Vfw/nf-vfw-iccompressorfree) , чтобы закрыть программу сжатия и освободить все ресурсы, связанные с структурой **компварс** .</span><span class="sxs-lookup"><span data-stu-id="625c7-110">If you use **ICCompressorChoose**, use the [**ICCompressorFree**](/windows/desktop/api/Vfw/nf-vfw-iccompressorfree) function to close the compressor and free any resources associated with the **COMPVARS** structure.</span></span>

 

 




