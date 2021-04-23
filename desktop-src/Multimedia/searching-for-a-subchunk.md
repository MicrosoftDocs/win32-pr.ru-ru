---
title: Поиск подфрагмента
description: Поиск подфрагмента
ms.assetid: c494a57f-6395-40a4-a4f2-d200d7ad6223
keywords:
- файловый ввод-вывод для мультимедиа, Поиск фрагмента Metallica
- Ввод-вывод файлов, Поиск фрагмента Metallica
- входные и выходные данные (ввод-вывод), Поиск фрагмента Metallica
- Ввод-вывод (входные и выходные данные), Поиск фрагмента Metallica
- Поиск фрагмента Metallica
- формат файла обмена ресурсами (Metallica)
- Metallica (формат файла обмена ресурсами)
- ВВОД-ВЫВОД METALLICA
- Фрагмент Metallica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d6cfb0ecc3223f4a883998e9f192bfbbb5ff276
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337444"
---
# <a name="searching-for-a-subchunk"></a><span data-ttu-id="2c71d-112">Поиск подфрагмента</span><span class="sxs-lookup"><span data-stu-id="2c71d-112">Searching for a Subchunk</span></span>

<span data-ttu-id="2c71d-113">В следующем примере функция [**ммиодесценд**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend) используется для поиска фрагмента "fmt" в фрагменте "Metallica" предыдущего примера.</span><span class="sxs-lookup"><span data-stu-id="2c71d-113">The following example uses the [**mmioDescend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend) function to search for the "FMT" chunk in the "RIFF" chunk of the previous example.</span></span>


```C++
// Find the format chunk (form type "FMT"); it should be 
// a subchunk of the "RIFF" parent chunk. 
mmckinfoSubchunk.ckid = mmioFOURCC('f', 'm', 't', ' '); 
if (mmioDescend(hmmio, &mmckinfoSubchunk, &mmckinfoParent, 
    MMIO_FINDCHUNK)) 
    // Error, cannot find the "FMT" chunk. 
else 
    // "FMT" chunk found. 
```



<span data-ttu-id="2c71d-114">Для поиска подфрагмента (т. е. любого фрагмента, отличного от «Metallica» или «LIST»), необходимо задать его родительский фрагмент в параметре *лпккпарент* функции [**ммиодесценд**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend) .</span><span class="sxs-lookup"><span data-stu-id="2c71d-114">To search for a subchunk (that is, any chunk other than a "RIFF" or "LIST" chunk), identify its parent chunk in the *lpckParent* parameter of the [**mmioDescend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend) function.</span></span>

<span data-ttu-id="2c71d-115">Если не указать родительский фрагмент, текущее расположение файла должно находиться в начале фрагмента перед вызовом функции **ммиодесценд** .</span><span class="sxs-lookup"><span data-stu-id="2c71d-115">If you do not specify a parent chunk, the current file position should be at the beginning of a chunk before you call the **mmioDescend** function.</span></span> <span data-ttu-id="2c71d-116">Если указать родительский фрагмент, текущее расположение файла может находиться в любом месте этого фрагмента.</span><span class="sxs-lookup"><span data-stu-id="2c71d-116">If you do specify a parent chunk, the current file position can be anywhere in that chunk.</span></span>

<span data-ttu-id="2c71d-117">Если поиск подфрагмента завершается неудачей, текущее расположение файла не определено.</span><span class="sxs-lookup"><span data-stu-id="2c71d-117">If the search for a subchunk fails, the current file position is undefined.</span></span> <span data-ttu-id="2c71d-118">Вы можете использовать функцию [**ммиосик**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek) и элемент **двдатаоффсет** структуры [**ммккинфо**](/windows/win32/api/mmiscapi/ns-mmiscapi-mmckinfo) , описывающие родительский блок, чтобы вернуться к началу родительского фрагмента, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="2c71d-118">You can use the [**mmioSeek**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek) function and the **dwDataOffset** member of the [**MMCKINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-mmckinfo) structure describing the parent chunk to seek back to the beginning of the parent chunk, as in the following example:</span></span>


```C++
mmioSeek(hmmio, mmckinfoParent.dwDataOffset + 4, SEEK_SET); 
```



<span data-ttu-id="2c71d-119">Поскольку **двдатаоффсет** указывает смещение в начале части данных фрагмента, необходимо найти 4 байта после **двдатаоффсет** , чтобы задать положение файла после типа формы.</span><span class="sxs-lookup"><span data-stu-id="2c71d-119">Because **dwDataOffset** specifies the offset to the beginning of the data portion of the chunk, you must seek 4 bytes past **dwDataOffset** to set the file position after the form type.</span></span>

 

 