---
description: Сценарии и приложения, написанные для 32-разрядных операционных систем, должны продолжать работать должным образом.
ms.assetid: b437b9ed-b9e4-4fc5-9b86-0eb77bb41b8e
ms.tgt_platform: multiple
title: Предоставление данных WMI на 64-разрядной платформе
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec1d6b348c16765014c4eb6988b64976ba3f11a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543687"
---
# <a name="providing-wmi-data-on-a-64-bit-platform"></a><span data-ttu-id="b8d1c-103">Предоставление данных WMI на 64-разрядной платформе</span><span class="sxs-lookup"><span data-stu-id="b8d1c-103">Providing WMI Data on a 64-bit Platform</span></span>

<span data-ttu-id="b8d1c-104">Сценарии и приложения, написанные для 32-разрядных операционных систем, должны продолжать работать должным образом.</span><span class="sxs-lookup"><span data-stu-id="b8d1c-104">Scripts and applications written for 32-bit operating systems should continue to run properly.</span></span> <span data-ttu-id="b8d1c-105">Если у вас есть имеющийся 32-разрядный поставщик, вы можете оценить, нужно ли писать 64-разрядную версию для параллельной работы.</span><span class="sxs-lookup"><span data-stu-id="b8d1c-105">If you have an existing 32-bit provider, you can evaluate whether you need to write a 64-bit version for side-by-side operation.</span></span> <span data-ttu-id="b8d1c-106">Как правило, обе версии не требуются, и 64-разрядная версия может обслуживать как 32-разрядные, так и 64-разрядные локальные или удаленные клиенты.</span><span class="sxs-lookup"><span data-stu-id="b8d1c-106">Generally, both versions are not necessary and the 64-bit version can service both 32-bit and 64-bit local or remote clients.</span></span> <span data-ttu-id="b8d1c-107">Однако для режима совместимости с 32-разрядным приложением Используйте имеющийся 32-разрядный поставщик WMI в 64-разрядной системе, работающей в режиме 32-bit WOW64.</span><span class="sxs-lookup"><span data-stu-id="b8d1c-107">However, for 32-bit application compatibility mode, use your existing 32-bit WMI provider on a 64-bit system that runs in the 32-bit WOW64 mode.</span></span>

<span data-ttu-id="b8d1c-108">В редких ситуациях как 32-разрядный, так и 64-разрядный поставщики должны работать параллельно с 64-разрядными системами.</span><span class="sxs-lookup"><span data-stu-id="b8d1c-108">In rare situations, both the 32-bit and 64-bit providers must run side-by-side on 64-bit systems.</span></span> <span data-ttu-id="b8d1c-109">В этом случае соответствующая версия поставщика загружается в зависимости от того, является ли вызывающий объект 32-разрядным или 64-битным, а также локальным или удаленным.</span><span class="sxs-lookup"><span data-stu-id="b8d1c-109">In this case, the appropriate version of provider that is loaded depends on whether the caller is 32-bit or 64-bit and local or remote.</span></span> <span data-ttu-id="b8d1c-110">Вызывающий объект, использующий флаги контекста объекта соединения, **\_ \_ провидерарчитектуре** и **\_ \_ рекуиредарчитектуре**, может запрашивать у WMI загрузку поставщика, не используемого по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b8d1c-110">A caller using the connection object context flags, **\_\_ProviderArchitecture** and **\_\_RequiredArchitecture**, can request that WMI load a nondefault provider.</span></span> <span data-ttu-id="b8d1c-111">Дополнительные сведения см. в разделе [Получение и предоставление данных на 64-разрядном компьютере](getting-and-providing-data-on-a-64-bit-computer.md).</span><span class="sxs-lookup"><span data-stu-id="b8d1c-111">For more information, see [Getting and Providing Data on a 64-bit Computer](getting-and-providing-data-on-a-64-bit-computer.md).</span></span>

<span data-ttu-id="b8d1c-112">В необычных случаях, когда необходимо одновременно запускать и 32-разрядный, и 64-разрядный поставщики, необходимо убедиться, что сценарии установки и удаления обрабатываются аккуратно.</span><span class="sxs-lookup"><span data-stu-id="b8d1c-112">In the unusual case that you must run both the 32-bit and 64-bit providers side-by-side, then you must ensure that install and uninstall scenarios are handled carefully.</span></span> <span data-ttu-id="b8d1c-113">Это связано с тем, что в WMI есть только один [*репозиторий*](gloss-w.md) , а также 32-разрядная и 64-разрядная версии [**mofcomp.exe**](mofcomp.md) помещают данные в один и тот же репозиторий. между 32-битным или 64-битным файлом. mof нет различий.</span><span class="sxs-lookup"><span data-stu-id="b8d1c-113">This is because WMI has only one [*repository*](gloss-w.md) and both the 32-bit and 64-bit versions of [**mofcomp.exe**](mofcomp.md) put the data in the same repository; there is no distinction between a 32-bit or a 64-bit .mof file.</span></span> <span data-ttu-id="b8d1c-114">Переустановка одной версии поставщика не приведет к повреду: файлы. mof будут скомпилированы и классы, хранящиеся в репозитории.</span><span class="sxs-lookup"><span data-stu-id="b8d1c-114">Reinstalling one version of the provider will not hurt: the .mof files will be compiled and the classes stored in the repository.</span></span> <span data-ttu-id="b8d1c-115">Однако вторая операция удаления, удаляющая пространство имен, может помешать работе другого поставщика.</span><span class="sxs-lookup"><span data-stu-id="b8d1c-115">However, a second uninstall that deletes a namespace can interfere with the operation of the other provider.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b8d1c-116">См. также</span><span class="sxs-lookup"><span data-stu-id="b8d1c-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8d1c-117">Получение и предоставление данных на 64-разрядном компьютере</span><span class="sxs-lookup"><span data-stu-id="b8d1c-117">Getting and Providing Data on a 64-bit Computer</span></span>](getting-and-providing-data-on-a-64-bit-computer.md)
</dt> <dt>

[<span data-ttu-id="b8d1c-118">Запрос данных WMI на 64-разрядной платформе</span><span class="sxs-lookup"><span data-stu-id="b8d1c-118">Requesting WMI Data on a 64-bit Platform</span></span>](requesting-wmi-data-on-a-64-bit-platform.md)
</dt> <dt>

[<span data-ttu-id="b8d1c-119">Предоставление данных инструментарию WMI</span><span class="sxs-lookup"><span data-stu-id="b8d1c-119">Providing Data to WMI</span></span>](providing-data-to-wmi.md)
</dt> </dl>

 

 



