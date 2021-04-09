---
title: Основы сжатия и декомпрессора
description: Основы сжатия и декомпрессора
ms.assetid: 49a958c1-1798-4c6c-913c-5bf5869f926b
keywords:
- Диспетчер сжатия видео (ВКМ), открытие компрессоров
- ВКМ (диспетчер сжатия видео), открытие компрессоров
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08b51e0221c495d5e2d0782f4e56e0778c0d2462
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888288"
---
# <a name="compressor-and-decompressor-basics"></a><span data-ttu-id="77eda-105">Основы сжатия и декомпрессора</span><span class="sxs-lookup"><span data-stu-id="77eda-105">Compressor and Decompressor Basics</span></span>

<span data-ttu-id="77eda-106">Чтобы открыть и указать программу сжатия, можно использовать функции [**иклокате**](/windows/desktop/api/Vfw/nf-vfw-iclocate) и [**икопен**](/windows/desktop/api/Vfw/nf-vfw-icopen) .</span><span class="sxs-lookup"><span data-stu-id="77eda-106">To open and locate a compressor, you can use the [**ICLocate**](/windows/desktop/api/Vfw/nf-vfw-iclocate) and [**ICOpen**](/windows/desktop/api/Vfw/nf-vfw-icopen) functions.</span></span> <span data-ttu-id="77eda-107">**Иклокате** можно использовать для поиска программы сжатия определенного типа и получения ее маркера для использования в других функциях ВКМ.</span><span class="sxs-lookup"><span data-stu-id="77eda-107">You can use **ICLocate** to find a compressor of a specific type and to obtain a handle of it for use in other VCM functions.</span></span> <span data-ttu-id="77eda-108">Чтобы открыть программу сжатия, можно использовать **икопен**.</span><span class="sxs-lookup"><span data-stu-id="77eda-108">To open a compressor, you can use **ICOpen**.</span></span> <span data-ttu-id="77eda-109">Приложение использует маркер, возвращенный этой функцией, для обнаружения открытого компрессора при использовании других функций ВКМ.</span><span class="sxs-lookup"><span data-stu-id="77eda-109">Your application uses the handle returned by this function to identify the opened compressor when it uses other VCM functions.</span></span>

<span data-ttu-id="77eda-110">Для открытия и нахождение декомпрессора приложения могут использовать макросы [**икдекомпрессопен**](/windows/desktop/api/Vfw/nf-vfw-icdecompressopen) и [**икдравопен**](/windows/desktop/api/Vfw/nf-vfw-icdrawopen) .</span><span class="sxs-lookup"><span data-stu-id="77eda-110">To open and locate a decompressor, applications can use the [**ICDecompressOpen**](/windows/desktop/api/Vfw/nf-vfw-icdecompressopen) and [**ICDrawOpen**](/windows/desktop/api/Vfw/nf-vfw-icdrawopen) macros.</span></span> <span data-ttu-id="77eda-111">Эти макросы используют **иклокате** для операции.</span><span class="sxs-lookup"><span data-stu-id="77eda-111">These macros use **ICLocate** for operation.</span></span>

<span data-ttu-id="77eda-112">Когда приложение завершит использование программы сжатия или распаковки, оно должно закрыть его, чтобы освободить все ресурсы, используемые для сжатия или распаковки.</span><span class="sxs-lookup"><span data-stu-id="77eda-112">When your application has finished using a compressor or decompressor, it must close it to free any resources used for compression or decompression.</span></span> <span data-ttu-id="77eda-113">Приложение может использовать функцию [**икклосе**](/windows/desktop/api/Vfw/nf-vfw-icclose) для закрытия программы сжатия или распаковки.</span><span class="sxs-lookup"><span data-stu-id="77eda-113">Your application can use the [**ICClose**](/windows/desktop/api/Vfw/nf-vfw-icclose) function to close the compressor or decompressor.</span></span>

<span data-ttu-id="77eda-114">Кроме того, приложение может перечислить программы сжатия или Декомпрессоры в системе с помощью функции [**иЦинфо**](/windows/desktop/api/Vfw/nf-vfw-icinfo) .</span><span class="sxs-lookup"><span data-stu-id="77eda-114">Also, your application can enumerate the compressors or decompressors on a system by using the [**ICInfo**](/windows/desktop/api/Vfw/nf-vfw-icinfo) function.</span></span>

> [!Note]  
> <span data-ttu-id="77eda-115">Заголовок потока в файле AVI содержит сведения о типе потока и конкретном обработчике для этого потока.</span><span class="sxs-lookup"><span data-stu-id="77eda-115">The stream header in an AVI file contains information about the stream type and the specific handler for that stream.</span></span> <span data-ttu-id="77eda-116">В заголовке потока члены **фкктипе** и **фкчандлер** определяют тип потока и обработчик потока, указанный для потока.</span><span class="sxs-lookup"><span data-stu-id="77eda-116">Within the stream header, the **fccType** and **fccHandler** members identify the stream type and the stream handler specified for the stream.</span></span>

 

 

 




