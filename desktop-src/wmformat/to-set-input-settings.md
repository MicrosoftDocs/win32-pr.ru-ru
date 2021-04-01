---
title: Установка параметров ввода
description: Установка параметров ввода
ms.assetid: 288801a7-793f-43bd-9c5a-f9e1bd86ecc3
keywords:
- Расширенный формат систем (ASF), параметры ввода
- ASF (Расширенный системный формат), параметры ввода
- профили, параметры ввода
- кодеки, параметры ввода
- потоки, параметры ввода
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e7b2db64a7346cc8b9d46c48f0add79dafcac95
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "103987205"
---
# <a name="to-set-input-settings"></a><span data-ttu-id="7d077-108">Установка параметров ввода</span><span class="sxs-lookup"><span data-stu-id="7d077-108">To Set Input Settings</span></span>

<span data-ttu-id="7d077-109">Основные свойства входного носителя и потока мультимедиа определяются структурой [**типа WM \_ Media \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) .</span><span class="sxs-lookup"><span data-stu-id="7d077-109">The basic properties of input media and stream media are defined by the [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure.</span></span> <span data-ttu-id="7d077-110">Для входных форматов данные типа мультимедиа задаются приложением.</span><span class="sxs-lookup"><span data-stu-id="7d077-110">For input formats, the media type information is set by your application.</span></span> <span data-ttu-id="7d077-111">Для форматов потока сведения о типе мультимедиа задаются в профиле, который назначается модулю записи.</span><span class="sxs-lookup"><span data-stu-id="7d077-111">For stream formats, the media type information is set in the profile you assign to the writer.</span></span> <span data-ttu-id="7d077-112">Некоторые свойства не зависят от типа мультимедиа и должны быть заданы для входных данных перед началом записи.</span><span class="sxs-lookup"><span data-stu-id="7d077-112">Some properties are independent of media type and must be set for an input before writing begins.</span></span> <span data-ttu-id="7d077-113">Эти свойства являются компонентами кодека и модуля записи, которые не зависят от типа потока, и должны быть заданы после назначения профиля в модуле записи, но перед началом записи.</span><span class="sxs-lookup"><span data-stu-id="7d077-113">These properties are codec and writer features that are independent of stream type, and must be set after the profile is assigned in the writer but before writing begins.</span></span>

<span data-ttu-id="7d077-114">Для установки входного параметра требуется вызов [**IWMWriterAdvanced2:: сетинпутсеттинг**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting).</span><span class="sxs-lookup"><span data-stu-id="7d077-114">Setting an input setting requires a call to [**IWMWriterAdvanced2::SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting).</span></span> <span data-ttu-id="7d077-115">Можно также проверить текущее значение параметра с помощью вызова [**IWMWriterAdvanced2:: жетинпутсеттинг**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-getinputsetting).</span><span class="sxs-lookup"><span data-stu-id="7d077-115">You can also check the current value of a setting with a call to [**IWMWriterAdvanced2::GetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-getinputsetting).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7d077-116">См. также</span><span class="sxs-lookup"><span data-stu-id="7d077-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7d077-117">**Использование профилей с модулем записи**</span><span class="sxs-lookup"><span data-stu-id="7d077-117">**To Use Profiles with the Writer**</span></span>](to-use-profiles-with-the-writer.md)
</dt> <dt>

[<span data-ttu-id="7d077-118">**Запись файлов ASF**</span><span class="sxs-lookup"><span data-stu-id="7d077-118">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> <dt>

[<span data-ttu-id="7d077-119">**Запись потоков изображений**</span><span class="sxs-lookup"><span data-stu-id="7d077-119">**Writing Image Streams**</span></span>](writing-image-streams.md)
</dt> </dl>

 

 




