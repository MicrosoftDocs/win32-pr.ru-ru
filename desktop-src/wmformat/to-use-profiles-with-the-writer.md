---
title: Использование профилей с модулем записи
description: Использование профилей с модулем записи
ms.assetid: 8805bc57-5f19-4544-bcb8-5af880ba8ea0
keywords:
- Windows Media Format SDK, написание файлов ASF
- Windows Media Format SDK, создание файлов ASF
- Windows Media Format SDK, расширенный формат систем (ASF)
- Расширенный системный формат (ASF), запись файлов
- ASF (Расширенный системный формат), запись файлов
- Расширенный системный формат (ASF), создание файлов
- ASF (Расширенный системный формат), создание файлов
- профили, создание файлов ASF
- профили, запись файлов ASF
- профили, создание файлов ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d027e6ea0e669d2a5206901faefab1f5a9583153
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2020
ms.locfileid: "104069689"
---
# <a name="to-use-profiles-with-the-writer"></a><span data-ttu-id="e7388-113">Использование профилей с модулем записи</span><span class="sxs-lookup"><span data-stu-id="e7388-113">To Use Profiles with the Writer</span></span>

<span data-ttu-id="e7388-114">Модуль записи использует данные профиля для создания файлов ASF.</span><span class="sxs-lookup"><span data-stu-id="e7388-114">The writer uses profile data to create ASF files.</span></span> <span data-ttu-id="e7388-115">Необходимо указать профиль для использования перед выполнением каких-либо других действий с модулем записи.</span><span class="sxs-lookup"><span data-stu-id="e7388-115">You must specify a profile for use before doing anything else with the writer.</span></span>

<span data-ttu-id="e7388-116">Вы можете задать системный профиль для модуля записи, передав идентификатор профиля в метод [**ивмвритер:: сетпрофилебид**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofilebyid) .</span><span class="sxs-lookup"><span data-stu-id="e7388-116">You can set a system profile for use with the writer by passing the profile ID to the [**IWMWriter::SetProfileByID**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofilebyid) method.</span></span>

<span data-ttu-id="e7388-117">Чтобы указать настраиваемый профиль для использования с модулем записи, необходимо получить интерфейс [**ивмпрофиле**](iwmprofile.md) для объекта, содержащего данные требуемого профиля.</span><span class="sxs-lookup"><span data-stu-id="e7388-117">To specify a custom profile for use with the writer, you must obtain an [**IWMProfile**](iwmprofile.md) interface to an object containing the desired profile data.</span></span> <span data-ttu-id="e7388-118">Для этого можно использовать один из методов загрузки интерфейса [**ивмпрофилеманажер**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) .</span><span class="sxs-lookup"><span data-stu-id="e7388-118">You can use one of the loading methods of the [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) interface to accomplish this.</span></span> <span data-ttu-id="e7388-119">После создания допустимого интерфейса **ивмпрофиле** можно передать указатель на него в метод [**Ивмвритер:: сетпрофиле**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) .</span><span class="sxs-lookup"><span data-stu-id="e7388-119">After you have a valid **IWMProfile** interface, you can pass a pointer to it to the [**IWMWriter::SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) method.</span></span> <span data-ttu-id="e7388-120">Дополнительные сведения о параметрах профиля см. [в разделе Работа с профилями](working-with-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="e7388-120">For more information about profile settings, see [Working with Profiles](working-with-profiles.md).</span></span>

<span data-ttu-id="e7388-121">При внесении изменений в объект Profile с помощью интерфейса **ивмпрофиле** после задания профиля в средстве записи необходимо вызвать **сетпрофиле** повторно, иначе изменения не будут отражены в модуле записи.</span><span class="sxs-lookup"><span data-stu-id="e7388-121">If you make changes to the profile object by using the **IWMProfile** interface after setting the profile in the writer, you must call **SetProfile** again, or else the changes will not be reflected in the writer.</span></span> <span data-ttu-id="e7388-122">Однако вызов **сетпрофиле** приведет к сбросу всех атрибутов заголовка, поэтому обязательно задайте необходимые атрибуты заголовка после вызова этого метода.</span><span class="sxs-lookup"><span data-stu-id="e7388-122">However, calling **SetProfile** will reset all header attributes, so be sure to set any required header attributes after calling this method.</span></span>

<span data-ttu-id="e7388-123">Следующий пример функции задает для профиля значение "Windows Media Video 8 для коммутируемых модемов (56 кбит/с)":</span><span class="sxs-lookup"><span data-stu-id="e7388-123">The following example function sets the profile to "Windows Media Video 8 for Dial-up Modems (56 Kbps)":</span></span>


```C++
#include <wmsysprf.h>

HRESULT SetProfileExample()
{
  HRESULT hr;
  IWMWriter *pWriter = NULL;
  hr = WMCreateWriter(NULL, &pWriter);
  if (FAILED(hr)) return hr;
  hr = pWriter->SetProfileByID(WMProfile_V80_56Video);
  return hr;
}

```



> [!Note]  
> <span data-ttu-id="e7388-124">Нет стандартных системных профилей, использующих кодеки Windows Media Audio и Video 9.</span><span class="sxs-lookup"><span data-stu-id="e7388-124">There are no predefined system profiles that use the Windows Media Audio and Video 9 Series codecs.</span></span> <span data-ttu-id="e7388-125">Дополнительные сведения см. в разделе [повторное использование конфигураций потоков](reusing-stream-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="e7388-125">For more information, see [Reusing Stream Configurations](reusing-stream-configurations.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="e7388-126">См. также</span><span class="sxs-lookup"><span data-stu-id="e7388-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e7388-127">**Ивмвритер:: Сетпрофилебид**</span><span class="sxs-lookup"><span data-stu-id="e7388-127">**IWMWriter::SetProfileByID**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofilebyid)
</dt> <dt>

[<span data-ttu-id="e7388-128">**Работа с профилями**</span><span class="sxs-lookup"><span data-stu-id="e7388-128">**Working with Profiles**</span></span>](working-with-profiles.md)
</dt> <dt>

[<span data-ttu-id="e7388-129">**Запись файлов ASF**</span><span class="sxs-lookup"><span data-stu-id="e7388-129">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




