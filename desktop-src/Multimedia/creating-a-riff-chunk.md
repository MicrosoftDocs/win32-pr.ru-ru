---
title: Создание фрагмента Metallica
description: Создание фрагмента Metallica
ms.assetid: d17f6215-f04f-4776-826e-eedb245f549b
keywords:
- файловый ввод-вывод с мультимедийными файлами, создание фрагмента Metallica
- Ввод-вывод файлов, создание фрагмента Metallica
- Ввод и вывод (I/O), создание фрагмента Metallica
- Ввод-вывод (входные и выходные данные), создание фрагмента Metallica
- Создание фрагмента Metallica
- Функция Ммиокреатечунк
- формат файла обмена ресурсами (Metallica)
- Metallica (формат файла обмена ресурсами)
- ВВОД-ВЫВОД METALLICA
- Фрагмент Metallica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adca2cca96b45ecf0313f811b5df4e966be8fc0f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103890545"
---
# <a name="creating-a-riff-chunk"></a><span data-ttu-id="9fa22-113">Создание фрагмента Metallica</span><span class="sxs-lookup"><span data-stu-id="9fa22-113">Creating a RIFF Chunk</span></span>

<span data-ttu-id="9fa22-114">В следующем примере функция [**ммиокреатечунк**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiocreatechunk) используется для создания фрагмента с идентификатором фрагмента "Metallica" и типом формы "рдиб".</span><span class="sxs-lookup"><span data-stu-id="9fa22-114">The following example uses the [**mmioCreateChunk**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiocreatechunk) function to create a chunk with a chunk identifier of "RIFF" and a form type of "RDIB".</span></span>


```C++
HMMIO    hmmio; 
MMCKINFO mmckinfo; 
. 
. 
. 
mmckinfo.fccType = mmioFOURCC('R', 'D', 'I', 'B'); 
mmioCreateChunk(hmmio, &mmckinfo, MMIO_CREATERIFF); 
```



<span data-ttu-id="9fa22-115">При создании фрагмента "Metallica" или "LIST" необходимо указать тип формы или списка в элементе **фкктипе** структуры [**ммккинфо**](/windows/win32/api/mmiscapi/ns-mmiscapi-mmckinfo) .</span><span class="sxs-lookup"><span data-stu-id="9fa22-115">If you are creating a "RIFF" or "LIST" chunk, you must specify the form type or list type in the **fccType** member of the [**MMCKINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-mmckinfo) structure.</span></span> <span data-ttu-id="9fa22-116">В предыдущем примере «РДИБ» — это тип формы.</span><span class="sxs-lookup"><span data-stu-id="9fa22-116">In the previous example, "RDIB" is the form type.</span></span>

<span data-ttu-id="9fa22-117">Если вы знакомы с размером поля данных в новом фрагменте, можно задать элемент **кксизе** структуры **ммккинфо** при создании фрагмента.</span><span class="sxs-lookup"><span data-stu-id="9fa22-117">If you know the size of the data field in a new chunk, you can set the **cksize** member of the **MMCKINFO** structure when you create the chunk.</span></span> <span data-ttu-id="9fa22-118">Это значение будет записано в поле Размер данных в новом фрагменте.</span><span class="sxs-lookup"><span data-stu-id="9fa22-118">This value will be written to the data size field in the new chunk.</span></span> <span data-ttu-id="9fa22-119">Если это значение неверно при вызове [**ммиоасценд**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioascend) для пометки конца фрагмента, он будет автоматически переписан для отражения правильного размера поля данных.</span><span class="sxs-lookup"><span data-stu-id="9fa22-119">If this value is not correct when you call [**mmioAscend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioascend) to mark the end of the chunk, it will be automatically rewritten to reflect the correct size of the data field.</span></span>

<span data-ttu-id="9fa22-120">После создания фрагмента с помощью функции [**ммиокреатечунк**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiocreatechunk) в качестве расположения файла устанавливается значение поля данных фрагмента (8 байт с начала фрагмента).</span><span class="sxs-lookup"><span data-stu-id="9fa22-120">After you create a chunk by using the [**mmioCreateChunk**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiocreatechunk) function, the file position is set to the data field of the chunk (8 bytes from the beginning of the chunk).</span></span> <span data-ttu-id="9fa22-121">Если фрагмент является блоком "Metallica" или "LIST", позиция файла устанавливается в расположение, следующее за типом или типом списка (12 байт с начала фрагмента).</span><span class="sxs-lookup"><span data-stu-id="9fa22-121">If the chunk is a "RIFF" or "LIST" chunk, the file position is set to the location following the form type or list type (12 bytes from the beginning of the chunk).</span></span>

 

 