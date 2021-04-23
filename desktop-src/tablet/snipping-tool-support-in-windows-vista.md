---
description: В этом разделе описывается, как в приложении можно указать URL-адрес, который должен получить средство выделения для планшетного ПК при записи приложения.
ms.assetid: e31e63e8-8f6b-41f7-8bd6-afc5ca32456b
title: Поддержка ножниц в Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 046dd6c8a97d1dacc20065dc1f741610fec13865
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911712"
---
# <a name="snipping-tool-support-in-windows-vista"></a><span data-ttu-id="70300-103">Поддержка ножниц в Windows Vista</span><span class="sxs-lookup"><span data-stu-id="70300-103">Snipping Tool Support in Windows Vista</span></span>

<span data-ttu-id="70300-104">В этом разделе описывается, как в приложении можно указать URL-адрес, который должен получить средство выделения для планшетного ПК при записи приложения.</span><span class="sxs-lookup"><span data-stu-id="70300-104">This topic describes how your application can specify what URL the Tablet PC Snipping Tool should obtain when capturing your application.</span></span>

## <a name="specifying-the-url-via-registry-key"></a><span data-ttu-id="70300-105">Указание URL-адреса через раздел реестра</span><span class="sxs-lookup"><span data-stu-id="70300-105">Specifying the URL via Registry Key</span></span>

<span data-ttu-id="70300-106">Ножницы позволяют пользователям захватить фрагмент (снимок экрана) любого объекта на экране, а затем добавить к нему заметки, сохранить или поделиться этим изображением.</span><span class="sxs-lookup"><span data-stu-id="70300-106">Snipping Tool allows users to capture a snip (screen shot) of any object on the screen and then annotate, save, or share the image.</span></span> <span data-ttu-id="70300-107">Если данные сохраняются в формате HTML или отправляются в почтовый клиент, поддерживающий встроенный HTML, средство выделения фрагментов кода может добавить URL-адрес к фрагменту, если приложение предоставляет сведения о том, как получить URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="70300-107">When the data is saved in HTML format, or when it is sent to an email client that supports inline HTML, Snipping Tool can add a URL to the snip if the application provides information on how to obtain the URL.</span></span>

<span data-ttu-id="70300-108">Средство выделения фрагментов получает URL-адрес через объекты специальных возможностей.</span><span class="sxs-lookup"><span data-stu-id="70300-108">Snipping Tool obtains the URL via accessibility objects.</span></span> <span data-ttu-id="70300-109">Приложения должны указать необходимые сведения в следующих разделах реестра:</span><span class="sxs-lookup"><span data-stu-id="70300-109">Applications should specify the necessary information under the following registry keys:</span></span>

<span data-ttu-id="70300-110">HKLM \\ Software \\ Microsoft \\ Windows \\ TabletPC \\ ножниц Tool \\ линкфинжерпринтс,</span><span class="sxs-lookup"><span data-stu-id="70300-110">HKLM\\Software\\Microsoft\\Windows\\TabletPC\\Snipping Tool\\LinkFingerprints,</span></span>

<span data-ttu-id="70300-111">И должны создать подраздел, имя которого совпадает с именем класса окна, из которого должна быть получена ссылка.</span><span class="sxs-lookup"><span data-stu-id="70300-111">And should create a subkey whose name is the same as the window class from which the link should be obtained.</span></span> <span data-ttu-id="70300-112">Имя класса Window должно быть самым верхним окном приложения.</span><span class="sxs-lookup"><span data-stu-id="70300-112">The window class name should be the topmost window of the application.</span></span>

<span data-ttu-id="70300-113">HKLM \\ Software \\ Microsoft \\ Windows \\ TabletPC \\ ножниц Tool \\ линкфинжерпринтс\\<Window Class Name></span><span class="sxs-lookup"><span data-stu-id="70300-113">HKLM\\Software\\Microsoft\\Windows\\TabletPC\\Snipping Tool\\LinkFingerprints\\<Window Class Name></span></span>

### <a name="window-class-key-details"></a><span data-ttu-id="70300-114">Сведения о ключе класса Window</span><span class="sxs-lookup"><span data-stu-id="70300-114">Window Class Key Details</span></span>

<span data-ttu-id="70300-115">В разделе "ключ класса окон" должны быть заданы соответствующие значения, чтобы указать, что средство выделения должно обнаруживать правильный объект специальных возможностей.</span><span class="sxs-lookup"><span data-stu-id="70300-115">Under the window class key, the appropriate values should be set in order to indicate Snipping Tool should detect the correct accessibility object.</span></span>



| <span data-ttu-id="70300-116">Значение</span><span class="sxs-lookup"><span data-stu-id="70300-116">VALUE</span></span>                        | <span data-ttu-id="70300-117">TYPE</span><span class="sxs-lookup"><span data-stu-id="70300-117">TYPE</span></span>                  | <span data-ttu-id="70300-118">ВИДЕ</span><span class="sxs-lookup"><span data-stu-id="70300-118">MASK</span></span>            | <span data-ttu-id="70300-119">ХРАНЯЩИЕСЯ СВЕДЕНИЯ</span><span class="sxs-lookup"><span data-stu-id="70300-119">INFORMATION STORED</span></span>                                          |
|------------------------------|-----------------------|-----------------|-------------------------------------------------------------|
| <span data-ttu-id="70300-120">Mask</span><span class="sxs-lookup"><span data-stu-id="70300-120">Mask</span></span><br/>              | <span data-ttu-id="70300-121">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="70300-121">REG\_DWORD</span></span><br/> |                 | <span data-ttu-id="70300-122">Указывает, какие из следующих полей следует проверить</span><span class="sxs-lookup"><span data-stu-id="70300-122">Indicates which of the following fields to check</span></span><br/> |
| <span data-ttu-id="70300-123">Имя</span><span class="sxs-lookup"><span data-stu-id="70300-123">Name</span></span><br/>              | <span data-ttu-id="70300-124">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="70300-124">REG\_SZ</span></span><br/>    | <span data-ttu-id="70300-125">0x02</span><span class="sxs-lookup"><span data-stu-id="70300-125">0x02</span></span><br/> | <span data-ttu-id="70300-126">Имя специальных возможностей</span><span class="sxs-lookup"><span data-stu-id="70300-126">Accessibility name</span></span><br/>                               |
| <span data-ttu-id="70300-127">Описание</span><span class="sxs-lookup"><span data-stu-id="70300-127">Description</span></span><br/>       | <span data-ttu-id="70300-128">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="70300-128">REG\_SZ</span></span><br/>    | <span data-ttu-id="70300-129">0x04</span><span class="sxs-lookup"><span data-stu-id="70300-129">0x04</span></span><br/> | <span data-ttu-id="70300-130">Описание специальных возможностей</span><span class="sxs-lookup"><span data-stu-id="70300-130">Accessibility description</span></span><br/>                        |
| <span data-ttu-id="70300-131">Роль</span><span class="sxs-lookup"><span data-stu-id="70300-131">Role</span></span><br/>              | <span data-ttu-id="70300-132">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="70300-132">REG\_DWORD</span></span><br/> | <span data-ttu-id="70300-133">0x08</span><span class="sxs-lookup"><span data-stu-id="70300-133">0x08</span></span><br/> | <span data-ttu-id="70300-134">Роль специальных возможностей</span><span class="sxs-lookup"><span data-stu-id="70300-134">Accessibility role</span></span><br/>                               |
| <span data-ttu-id="70300-135">ParentName</span><span class="sxs-lookup"><span data-stu-id="70300-135">ParentName</span></span><br/>        | <span data-ttu-id="70300-136">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="70300-136">REG\_SZ</span></span><br/>    | <span data-ttu-id="70300-137">0x10</span><span class="sxs-lookup"><span data-stu-id="70300-137">0x10</span></span><br/> | <span data-ttu-id="70300-138">Имя родительского элемента</span><span class="sxs-lookup"><span data-stu-id="70300-138">Accessibility name of parent</span></span><br/>                     |
| <span data-ttu-id="70300-139">парентвалуе</span><span class="sxs-lookup"><span data-stu-id="70300-139">ParentValue</span></span><br/>       | <span data-ttu-id="70300-140">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="70300-140">REG\_SZ</span></span><br/>    | <span data-ttu-id="70300-141">0x20</span><span class="sxs-lookup"><span data-stu-id="70300-141">0x20</span></span><br/> | <span data-ttu-id="70300-142">Значение доступности родителя</span><span class="sxs-lookup"><span data-stu-id="70300-142">Accessibility value of parent</span></span><br/>                    |
| <span data-ttu-id="70300-143">парентроле</span><span class="sxs-lookup"><span data-stu-id="70300-143">ParentRole</span></span><br/>        | <span data-ttu-id="70300-144">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="70300-144">REG\_DWORD</span></span><br/> | <span data-ttu-id="70300-145">0x40</span><span class="sxs-lookup"><span data-stu-id="70300-145">0x40</span></span><br/> | <span data-ttu-id="70300-146">Роль доступности родителя</span><span class="sxs-lookup"><span data-stu-id="70300-146">Accessibility role of parent</span></span><br/>                     |
| <span data-ttu-id="70300-147">парентдескриптион</span><span class="sxs-lookup"><span data-stu-id="70300-147">ParentDescription</span></span><br/> | <span data-ttu-id="70300-148">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="70300-148">REG\_SZ</span></span><br/>    | <span data-ttu-id="70300-149">0x80</span><span class="sxs-lookup"><span data-stu-id="70300-149">0x80</span></span><br/> | <span data-ttu-id="70300-150">Описание специальных возможностей родителя</span><span class="sxs-lookup"><span data-stu-id="70300-150">Accessibility description of parent</span></span><br/>              |



 

<span data-ttu-id="70300-151">Кроме того, если задано значение битовой маски 0x1, то URL-адрес должен быть взят из имени специальных возможностей. в противном случае URL-адрес должен быть получен из значения специальных возможностей.</span><span class="sxs-lookup"><span data-stu-id="70300-151">Additionally, if the mask bit value 0x1 is set, then the URL should be taken from the accessibility name; otherwise, the URL should be taken from the accessibility value.</span></span>

<span data-ttu-id="70300-152">Если приложение использует локализованные строки для значений REG \_ SZ, приведенных выше, строка должна быть указана в качестве косвенной строки в следующем формате:</span><span class="sxs-lookup"><span data-stu-id="70300-152">If the application uses localized strings for the REG\_SZ values above, the string should be provided as an indirect string by using the following format:</span></span>

<span data-ttu-id="70300-153">@filename, ресурс</span><span class="sxs-lookup"><span data-stu-id="70300-153">@filename,resource</span></span>

<span data-ttu-id="70300-154">Строка извлекается из файла с именем и используется значение ресурса в качестве указателя.</span><span class="sxs-lookup"><span data-stu-id="70300-154">The string is extracted from the file named, using the resource value as a locator.</span></span> <span data-ttu-id="70300-155">Если значение ресурса равно нулю или больше, то число становится индексом строки в двоичном файле.</span><span class="sxs-lookup"><span data-stu-id="70300-155">If the resource value is zero or greater, the number becomes the index of the string in the binary file.</span></span> <span data-ttu-id="70300-156">Если число отрицательное, оно становится идентификатором ресурса (ИДЕНТИФИКАТОРом).</span><span class="sxs-lookup"><span data-stu-id="70300-156">If the number is negative, it becomes a resource identifier (ID).</span></span>

> [!Note]  
> <span data-ttu-id="70300-157">Константы ролей можно найти в олеакк. h в Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="70300-157">Role constants can be found in oleacc.h in the Windows SDK.</span></span> <span data-ttu-id="70300-158">Описанные в реестре параметры относятся только к Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="70300-158">The registry values described are specific to Windows Vista.</span></span>

 

 

 




