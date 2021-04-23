---
title: Создание временных потоков
description: Создание временных потоков
ms.assetid: 8fe75ae1-0111-4b02-a00d-1ef2ca462452
keywords:
- Функция Авистреамкреате
- Функция Авистреамрелеасе
- Функция Авимакекомпресседстреам
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 209259f46e25275094dcd1eb5eeddd4f336ee906
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486760"
---
# <a name="creating-temporary-streams"></a><span data-ttu-id="6be75-106">Создание временных потоков</span><span class="sxs-lookup"><span data-stu-id="6be75-106">Creating Temporary Streams</span></span>

<span data-ttu-id="6be75-107">Временные потоки могут быть полезными несколькими способами.</span><span class="sxs-lookup"><span data-stu-id="6be75-107">Temporary streams can be beneficial in several ways.</span></span> <span data-ttu-id="6be75-108">Можно использовать временный поток в качестве рабочего потока, например, при изменении формата потока.</span><span class="sxs-lookup"><span data-stu-id="6be75-108">You can use a temporary stream as a work stream, for example, when changing the stream format.</span></span> <span data-ttu-id="6be75-109">Или можно создать временный поток для хранения скопированных частей других потоков.</span><span class="sxs-lookup"><span data-stu-id="6be75-109">Or you can create a temporary stream to hold portions of other streams that have been copied.</span></span>

<span data-ttu-id="6be75-110">В памяти можно создать поток, не связанный с каким-либо файлом, с помощью функции [**авистреамкреате**](/windows/desktop/api/Vfw/nf-vfw-avistreamcreate) .</span><span class="sxs-lookup"><span data-stu-id="6be75-110">You can create a stream in memory that is not associated with any file by using the [**AVIStreamCreate**](/windows/desktop/api/Vfw/nf-vfw-avistreamcreate) function.</span></span> <span data-ttu-id="6be75-111">Эта функция возвращает адрес интерфейса в новом потоке в указанном расположении и используется внутри другими функциями, которые создают временные потоки.</span><span class="sxs-lookup"><span data-stu-id="6be75-111">This function returns the address of the interface to the new stream in a specified location and is used internally by other functions that create temporary streams.</span></span>

<span data-ttu-id="6be75-112">Вы можете создать сжатый поток из несжатого потока с помощью функции [**авимакекомпресседстреам**](/windows/desktop/api/Vfw/nf-vfw-avimakecompressedstream) .</span><span class="sxs-lookup"><span data-stu-id="6be75-112">You can create a compressed stream from an uncompressed stream by using the [**AVIMakeCompressedStream**](/windows/desktop/api/Vfw/nf-vfw-avimakecompressedstream) function.</span></span> <span data-ttu-id="6be75-113">Вы определяете поток для сжатия, метод сжатия и параметры сжатия, а также обработчик для нового потока.</span><span class="sxs-lookup"><span data-stu-id="6be75-113">You identify the stream to compress, the compression method and compression options, and the handler for the new stream.</span></span>

<span data-ttu-id="6be75-114">Когда вы завершите использование потока, созданного с помощью **авистреамкреате** или **авимакекомпресседстреам**, закройте поток, используя функцию [**авистреамрелеасе**](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease) .</span><span class="sxs-lookup"><span data-stu-id="6be75-114">When you finish using a stream created with **AVIStreamCreate** or **AVIMakeCompressedStream**, close the stream by using the [**AVIStreamRelease**](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease) function.</span></span> <span data-ttu-id="6be75-115">**Авистреамрелеасе** освобождает ресурсы, используемые временным потоком.</span><span class="sxs-lookup"><span data-stu-id="6be75-115">**AVIStreamRelease** frees the resources the temporary stream used.</span></span>

 

 




