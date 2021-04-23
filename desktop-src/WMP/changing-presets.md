---
title: Изменение предустановок
description: Изменение предустановок
ms.assetid: f8a5565d-676b-4679-a4cb-4bd7551cf41c
keywords:
- визуализации, пример с свечением
- Пользовательские визуализации, пример свечения
- инструкции по программированию, визуализации
- Примеры, Визуализация свечения
- Пример визуализации с свечением
- визуализации, предустановки
- Пользовательские визуализации, предустановки
- предустановки в визуализациях, пример с свечением
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95d24841c95c3fc1029aa0c405e90b329799fdbe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105691214"
---
# <a name="changing-presets"></a><span data-ttu-id="106ca-111">Изменение предустановок</span><span class="sxs-lookup"><span data-stu-id="106ca-111">Changing Presets</span></span>

<span data-ttu-id="106ca-112">Следующие предварительно заданные разделы кода были изменены, чтобы разрешить три предустановки:</span><span class="sxs-lookup"><span data-stu-id="106ca-112">The following preset code sections were changed to allow three presets:</span></span>

## <a name="getpresettitle"></a><span data-ttu-id="106ca-113">жетпресеттитле</span><span class="sxs-lookup"><span data-stu-id="106ca-113">GetPresetTitle</span></span>

<span data-ttu-id="106ca-114">Этот код был вставлен вместо созданного предустановленного кода:</span><span class="sxs-lookup"><span data-stu-id="106ca-114">This code was inserted in place of the generated preset code:</span></span>


```C++
    switch (nPreset)
    {
    case PRESET_RED:
        bstrTemp.LoadString(IDS_REDPRESETNAME); 
        break;

    case PRESET_GREEN:
        bstrTemp.LoadString(IDS_GREENPRESETNAME); 
        break;

    case PRESET_BLUE:
        bstrTemp.LoadString(IDS_BLUEPRESETNAME); 
        break;
    }

```



## <a name="enumerations"></a><span data-ttu-id="106ca-115">Перечисления</span><span class="sxs-lookup"><span data-stu-id="106ca-115">Enumerations</span></span>

<span data-ttu-id="106ca-116">Следующее перечисление в свечении. h было изменено для разрешения трех предустановок:</span><span class="sxs-lookup"><span data-stu-id="106ca-116">The following enumeration in Glow.h was changed to allow three presets:</span></span>


```C++
enum {
    PRESET_RED = 0,
    PRESET_GREEN,
    PRESET_BLUE,
    PRESET_COUNT
};

```



## <a name="resource-header"></a><span data-ttu-id="106ca-117">Заголовок ресурса</span><span class="sxs-lookup"><span data-stu-id="106ca-117">Resource Header</span></span>

<span data-ttu-id="106ca-118">Следующие ресурсы были определены в Resource. h для разрешения трех предустановок:</span><span class="sxs-lookup"><span data-stu-id="106ca-118">The following resources were defined in Resource.h to allow three presets:</span></span>


```C++
#define IDS_REDPRESETNAME               102
#define IDS_GREENPRESETNAME             103
#define IDS_BLUEPRESETNAME              104

```



<span data-ttu-id="106ca-119">Обратите внимание, что необходимо также изменить номер ресурса **\_ ТД \_ Next \_ Симед в \_ значение** 106.</span><span class="sxs-lookup"><span data-stu-id="106ca-119">Note that you must also change the resource number of **\_APS\_NEXT\_SYMED\_VALUE** to 106.</span></span>

## <a name="resource-file"></a><span data-ttu-id="106ca-120">Файл ресурсов</span><span class="sxs-lookup"><span data-stu-id="106ca-120">Resource File</span></span>

<span data-ttu-id="106ca-121">Следующие строки необходимо изменить в файле Гловдлл. RC, чтобы разрешить три предустановки и присвоить им имена:</span><span class="sxs-lookup"><span data-stu-id="106ca-121">The following strings must be changed in the Glowdll.rc file to allow three presets and give them names:</span></span>


```C++
    IDS_REDPRESETNAME       "Glow Red"
    IDS_GREENPRESETNAME     "Glow Green"
    IDS_BLUEPRESETNAME      "Glow Blue"

```



## <a name="related-topics"></a><span data-ttu-id="106ca-122">См. также</span><span class="sxs-lookup"><span data-stu-id="106ca-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="106ca-123">**Пример свечения**</span><span class="sxs-lookup"><span data-stu-id="106ca-123">**The Glow Sample**</span></span>](the-glow-sample.md)
</dt> </dl>

 

 




