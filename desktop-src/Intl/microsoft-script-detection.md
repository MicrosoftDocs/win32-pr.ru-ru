---
description: Служба обнаружения скриптов ELS называется обнаружением сценариев Майкрософт.
ms.assetid: daf9f549-1eff-4666-b777-227ec31fba30
title: Обнаружение сценариев Майкрософт
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fd38b36cb409c1f03d84b9fc21f2fe4439b8152
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155158"
---
# <a name="microsoft-script-detection"></a><span data-ttu-id="1e18d-103">Обнаружение сценариев Майкрософт</span><span class="sxs-lookup"><span data-stu-id="1e18d-103">Microsoft Script Detection</span></span>

<span data-ttu-id="1e18d-104">Служба обнаружения скриптов ELS называется обнаружением сценариев Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="1e18d-104">The ELS script detection service is called Microsoft Script Detection.</span></span> <span data-ttu-id="1e18d-105">Эта служба позволяет приложениям обнаруживать скрипты, в которых записывается текст.</span><span class="sxs-lookup"><span data-stu-id="1e18d-105">This service allows applications to detect the scripts in which text is written.</span></span> <span data-ttu-id="1e18d-106">Поддержка национальных языков (NLS) службы обнаружения скриптов является функцией [жетстрингскриптс](/windows/desktop/api/Winnls/nf-winnls-getstringscripts) .</span><span class="sxs-lookup"><span data-stu-id="1e18d-106">The National Language Support (NLS) counterpart of a script detection service is the [GetStringScripts](/windows/desktop/api/Winnls/nf-winnls-getstringscripts) function.</span></span> <span data-ttu-id="1e18d-107">Однако служба ELS дополнительно извлекает текстовые диапазоны, принадлежащие каждой системе записи.</span><span class="sxs-lookup"><span data-stu-id="1e18d-107">However, the ELS service additionally retrieves the text ranges that belong to each writing system.</span></span>

## <a name="input-to-microsoft-script-detection"></a><span data-ttu-id="1e18d-108">Входные данные для обнаружения сценариев Майкрософт</span><span class="sxs-lookup"><span data-stu-id="1e18d-108">Input to Microsoft Script Detection</span></span>

<span data-ttu-id="1e18d-109">Входными данными для службы обнаружения скриптов Майкрософт является текст UTF-16, для которого служба определяет диапазоны скриптов.</span><span class="sxs-lookup"><span data-stu-id="1e18d-109">The input to the Microsoft Script Detection service is UTF-16 text for which the service determines script ranges.</span></span>

## <a name="output-of-microsoft-script-detection"></a><span data-ttu-id="1e18d-110">Выходные данные обнаружения сценариев (Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="1e18d-110">Output of Microsoft Script Detection</span></span>

<span data-ttu-id="1e18d-111">Выходные данные службы обнаружения скриптов Майкрософт — это массив диапазонов, каждый из которых содержит строку UTF-16, заканчивающуюся нулем, с именем связанной системы записи, заданным в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="1e18d-111">The output of the Microsoft Script Detection service is an array of ranges, each containing a null-terminated UTF-16 string with the Unicode-specified name of the associated writing system.</span></span> <span data-ttu-id="1e18d-112">Служба выводит обычные общие (Зиии) и унаследованные (Кааи) символы как принадлежащие предыдущему диапазону скриптов.</span><span class="sxs-lookup"><span data-stu-id="1e18d-112">The service reports regular common (Zyyy) and inherited (Qaai) characters as belonging to the previous script range.</span></span> <span data-ttu-id="1e18d-113">Начало общих и наследуемых символов указывается как принадлежащий следующему диапазону скриптов.</span><span class="sxs-lookup"><span data-stu-id="1e18d-113">Beginning common and inherited characters are reported as belonging to the next script range.</span></span> <span data-ttu-id="1e18d-114">Если все символы во входном тексте являются общими или наследуются, выходные данные службы представляют собой один диапазон с пустой строкой в качестве данных.</span><span class="sxs-lookup"><span data-stu-id="1e18d-114">If all the characters in the input text are common or inherited, the output of the service is a single range with the empty string as its data.</span></span>

## <a name="microsoft-script-detection-operation"></a><span data-ttu-id="1e18d-115">Операция обнаружения скрипта (Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="1e18d-115">Microsoft Script Detection Operation</span></span>

<span data-ttu-id="1e18d-116">Служба обнаружения сценариев (Майкрософт) сопоставляет кодовые точки, относящиеся к общему диапазону, с предыдущей системой записи.</span><span class="sxs-lookup"><span data-stu-id="1e18d-116">The Microsoft Script Detection service maps the code points belonging to the common range to the preceding writing system.</span></span> <span data-ttu-id="1e18d-117">Кроме того, служба может сопоставлять кодовые точки со следующей системой записи, если кодовые точки находятся в начале входной строки.</span><span class="sxs-lookup"><span data-stu-id="1e18d-117">Alternatively, the service can map the code points to the next writing system if the code points are at the beginning of the input string.</span></span> <span data-ttu-id="1e18d-118">Приложению не придется работать с общим диапазоном.</span><span class="sxs-lookup"><span data-stu-id="1e18d-118">The application does not have to deal with the common range at all.</span></span>

## <a name="microsoft-script-detection-guid"></a><span data-ttu-id="1e18d-119">Идентификатор GUID обнаружения сценариев (Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="1e18d-119">Microsoft Script Detection GUID</span></span>

<span data-ttu-id="1e18d-120">Идентификатор GUID для службы Microsoft распознавание языка объявляется в Елссрвк. h, как показано в следующем коде.</span><span class="sxs-lookup"><span data-stu-id="1e18d-120">The GUID for the Microsoft Language Detection service is declared in Elssrvc.h, as shown in the following code.</span></span>


```C++
// {2D64B439-6CAF-4f6b-B688-E5D0F4FAA7D7}
static const GUID ELS_GUID_SCRIPT_DETECTION =
    { 0x2D64B439, 0x6CAF, 0x4F6B, { 0xB6, 0x88, 0xE5, 0xD0, 0xF4, 0xFA, 0xA7, 0xD7 } };
```



## <a name="related-topics"></a><span data-ttu-id="1e18d-121">См. также</span><span class="sxs-lookup"><span data-stu-id="1e18d-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e18d-122">О расширенных лингвистических службах</span><span class="sxs-lookup"><span data-stu-id="1e18d-122">About Extended Linguistic Services</span></span>](about-extended-linguistic-services.md)
</dt> </dl>

 

 



