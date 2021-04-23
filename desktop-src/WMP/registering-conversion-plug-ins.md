---
title: Регистрация подключаемых модулей преобразования
description: Регистрация подключаемых модулей преобразования
ms.assetid: d7d6e733-7288-4707-a54a-dcaa71601646
keywords:
- Проигрыватель Windows Media, подключаемые модули преобразования
- Подключаемые модули проигрывателя Windows Media, преобразование
- подключаемые модули, преобразование
- подключаемые модули преобразования, регистрация
- реестр, подключаемые модули преобразования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 301d24e38cb4672936923cea9edd7fe6b3d2dc5c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105681418"
---
# <a name="registering-conversion-plug-ins"></a><span data-ttu-id="93f35-108">Регистрация подключаемых модулей преобразования</span><span class="sxs-lookup"><span data-stu-id="93f35-108">Registering Conversion Plug-ins</span></span>

<span data-ttu-id="93f35-109">Форматы сторонних производителей должны быть зарегистрированы до того, как проигрыватель Windows Media сможет создать экземпляр и использовать подключаемый модуль преобразования.</span><span class="sxs-lookup"><span data-stu-id="93f35-109">Third-party formats must be registered before Windows Media Player can instantiate and use the conversion plug-in.</span></span> <span data-ttu-id="93f35-110">Чтобы зарегистрировать файл для преобразования, необходимо зарегистрировать расширение имени файла, связанное с вашим форматом.</span><span class="sxs-lookup"><span data-stu-id="93f35-110">To register your file for conversion, you must register the file name extension associated with your format.</span></span>

<span data-ttu-id="93f35-111">Список зарегистрированных расширений имен файлов сохраняется в виде набора разделов реестра.</span><span class="sxs-lookup"><span data-stu-id="93f35-111">The list of registered file name extensions is maintained as a set of registry keys.</span></span> <span data-ttu-id="93f35-112">Дополнительные сведения о регистрации форматов сторонних производителей см. в разделе [параметры реестра для расширения имени файла](file-name-extension-registry-settings.md).</span><span class="sxs-lookup"><span data-stu-id="93f35-112">For details about registering third-party formats, see [File Name Extension Registry Settings](file-name-extension-registry-settings.md).</span></span> <span data-ttu-id="93f35-113">В следующей таблице перечислены параметры реестра для регистрации формата стороннего производителя для преобразования с помощью подключаемого модуля преобразования.</span><span class="sxs-lookup"><span data-stu-id="93f35-113">The following table lists the registry value settings to register a third-party format for conversion by using a conversion plug-in.</span></span>



| <span data-ttu-id="93f35-114">Значение</span><span class="sxs-lookup"><span data-stu-id="93f35-114">Value</span></span>                  | <span data-ttu-id="93f35-115">Параметр</span><span class="sxs-lookup"><span data-stu-id="93f35-115">Setting</span></span>                                                     |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="93f35-116">**Параметры выполнения**</span><span class="sxs-lookup"><span data-stu-id="93f35-116">**Runtime**</span></span>            | <span data-ttu-id="93f35-117">13</span><span class="sxs-lookup"><span data-stu-id="93f35-117">13</span></span>                                                          |
| <span data-ttu-id="93f35-118">**Разрешения**</span><span class="sxs-lookup"><span data-stu-id="93f35-118">**Permissions**</span></span>        | <span data-ttu-id="93f35-119">8 (разрешение для библиотеки).</span><span class="sxs-lookup"><span data-stu-id="93f35-119">8 (Permission for the library).</span></span>                             |
| <span data-ttu-id="93f35-120">**конвертплугинклсид**</span><span class="sxs-lookup"><span data-stu-id="93f35-120">**ConvertPluginCLSID**</span></span> | <span data-ttu-id="93f35-121">Идентификатор класса подключаемого модуля преобразования в формате реестра.</span><span class="sxs-lookup"><span data-stu-id="93f35-121">The class ID of the conversion plug-in, in registry format.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="93f35-122">См. также</span><span class="sxs-lookup"><span data-stu-id="93f35-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="93f35-123">**Справочник по программированию подключаемых модулей преобразования**</span><span class="sxs-lookup"><span data-stu-id="93f35-123">**Conversion Plug-ins Programming Reference**</span></span>](conversion-plug-ins-programming-reference.md)
</dt> </dl>

 

 




