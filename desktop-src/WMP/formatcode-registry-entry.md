---
title: Запись реестра Форматкоде
description: Запись реестра Форматкоде
ms.assetid: cc444eaa-6898-48ab-9573-9e7d5e25d6db
keywords:
- Проигрыватель Windows Media, записи реестра Форматкоде
- Проигрыватель Windows Media, расширения имен файлов
- Проигрыватель Windows Media, реестр
- реестр, расширения имен файлов
- реестр, записи Форматкоде
- реестр, параметры для проигрывателя Windows Media
- параметры реестра для расширения имени файла
- Записи реестра Форматкоде
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2318d32e9d7a08a2ae23b24e7acd2674b9eecb2
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/20/2020
ms.locfileid: "104260391"
---
# <a name="formatcode-registry-entry"></a><span data-ttu-id="9e257-111">Запись реестра Форматкоде</span><span class="sxs-lookup"><span data-stu-id="9e257-111">FormatCode Registry Entry</span></span>

<span data-ttu-id="9e257-112">Когда проигрыватель Windows Media обнаруживает пользовательское расширение имени файла, он ищет подраздел реестра, соответствующий этому расширению.</span><span class="sxs-lookup"><span data-stu-id="9e257-112">When Windows Media Player encounters a custom file name extension, it looks for a registry subkey that matches the extension.</span></span> <span data-ttu-id="9e257-113">Подраздел описывается в [разделе Параметры реестра расширения имени файла](file-name-extension-registry-settings.md).</span><span class="sxs-lookup"><span data-stu-id="9e257-113">The subkey is described in [File Name Extension Registry Settings](file-name-extension-registry-settings.md).</span></span> <span data-ttu-id="9e257-114">Одна из записей реестра, которые могут отображаться в подразделе расширения, — это запись **форматкоде** .</span><span class="sxs-lookup"><span data-stu-id="9e257-114">One of the registry entries that can appear under the extension's subkey is the **FormatCode** entry.</span></span>

<span data-ttu-id="9e257-115">Запись реестра **форматкоде** указывает код формата протокола MTP для файлов с пользовательским расширением.</span><span class="sxs-lookup"><span data-stu-id="9e257-115">The **FormatCode** registry entry specifies the Media Transport Protocol (MTP) format code for files that have the custom extension.</span></span> <span data-ttu-id="9e257-116">Запись реестра **форматкоде** имеет следующую форму.</span><span class="sxs-lookup"><span data-stu-id="9e257-116">The **FormatCode** registry entry has the following form.</span></span>



| <span data-ttu-id="9e257-117">Имя</span><span class="sxs-lookup"><span data-stu-id="9e257-117">Name</span></span>       | <span data-ttu-id="9e257-118">Тип</span><span class="sxs-lookup"><span data-stu-id="9e257-118">Type</span></span>           | <span data-ttu-id="9e257-119">Значение</span><span class="sxs-lookup"><span data-stu-id="9e257-119">Value</span></span>                                                             |
|------------|----------------|-------------------------------------------------------------------|
| <span data-ttu-id="9e257-120">форматкоде</span><span class="sxs-lookup"><span data-stu-id="9e257-120">FormatCode</span></span> | <span data-ttu-id="9e257-121">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="9e257-121">**REG\_DWORD**</span></span> | <span data-ttu-id="9e257-122">16-разрядное положительное целое число, определяющее формат файла.</span><span class="sxs-lookup"><span data-stu-id="9e257-122">A 16-bit positive integer that identifies the format of the file.</span></span> |



 

<span data-ttu-id="9e257-123">Когда пользователь пытается скопировать файл цифрового мультимедиа с пользовательским расширением имени файла на портативное устройство, проигрыватель Windows Media выполняет поиск в реестре кода формата, связанного с расширением пользовательского имени файла.</span><span class="sxs-lookup"><span data-stu-id="9e257-123">When the user attempts to copy a digital media file that has a custom file name extension to a portable device, Windows Media Player looks in the registry to find a format code associated with the custom file name extension.</span></span> <span data-ttu-id="9e257-124">Если проигрыватель Windows Media находит код формата, он использует MTP, чтобы определить, поддерживает ли устройство пользовательский формат файла.</span><span class="sxs-lookup"><span data-stu-id="9e257-124">If Windows Media Player finds a format code, it uses MTP to determine whether the device supports the custom file format.</span></span> <span data-ttu-id="9e257-125">Если устройство поддерживает формат, файл мультимедиа копируется на устройство без его перекодирования.</span><span class="sxs-lookup"><span data-stu-id="9e257-125">If the device supports the format, the media file is copied to the device without being transcoded.</span></span>

<span data-ttu-id="9e257-126">Устройство, которое поддерживает MTP, может предоставить проигрыватель Windows Media с набором данных DeviceInfo, который, помимо прочего, содержит список кодов форматов, поддерживаемых устройством.</span><span class="sxs-lookup"><span data-stu-id="9e257-126">A device that supports MTP can supply Windows Media Player with a DeviceInfo dataset, which contains, among other things, a list of format codes supported by the device.</span></span>

<span data-ttu-id="9e257-127">В процессе разработки пользовательского формата файла можно запросить код формата от Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="9e257-127">If you are in the process of developing a custom file format, you can request a format code from Microsoft.</span></span> <span data-ttu-id="9e257-128">Дополнительные сведения о том, как запросить код формата, см. в разделе пакет по переносу протокола транспорта Microsoft Media, который доступен в [центре разработчиков Microsoft Windows Media](https://msdn.microsoft.com/windowsmedia/default.aspx).</span><span class="sxs-lookup"><span data-stu-id="9e257-128">For information about how to request a format code, see the Microsoft Media Transport Protocol Porting Kit, which is available at the [Microsoft Windows Media Developer Center](https://msdn.microsoft.com/windowsmedia/default.aspx).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9e257-129">См. также</span><span class="sxs-lookup"><span data-stu-id="9e257-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9e257-130">**Параметры реестра для расширения имени файла**</span><span class="sxs-lookup"><span data-stu-id="9e257-130">**File Name Extension Registry Settings**</span></span>](file-name-extension-registry-settings.md)
</dt> </dl>

 

 




