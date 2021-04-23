---
title: Просмотр атрибутов защищенных файлов
description: Просмотр атрибутов защищенных файлов
ms.assetid: fbfa1a1b-afd0-4f61-86ae-488716e16355
keywords:
- Windows Media Format SDK, просмотр атрибутов защищенных файлов
- Windows Media Format SDK, атрибуты защищенных файлов
- Windows Media Format SDK, защищенные файлы
- Расширенный системный формат (ASF), просмотр атрибутов защищенных файлов
- ASF (Расширенный системный формат), просмотр атрибутов защищенных файлов
- Расширенный формат систем (ASF), атрибуты защищенных файлов
- ASF (Расширенный системный формат), атрибуты защищенных файлов
- Расширенный формат систем (ASF), защищенные файлы
- ASF (Расширенный системный формат), защищенные файлы
- Управление цифровыми правами (DRM), просмотр атрибутов защищенных файлов
- DRM (Управление цифровыми правами), просмотр атрибутов защищенных файлов
- Управление цифровыми правами (DRM), атрибуты защищенных файлов
- DRM (Управление цифровыми правами), атрибуты защищенных файлов
- Управление цифровыми правами (DRM), защищенные файлы
- DRM (Управление цифровыми правами), защищенные файлы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 642e9f580c3dffa1d3785985d548a5f971cfc218
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "103788688"
---
# <a name="viewing-attributes-of-protected-files"></a><span data-ttu-id="7b29f-118">Просмотр атрибутов защищенных файлов</span><span class="sxs-lookup"><span data-stu-id="7b29f-118">Viewing Attributes of Protected Files</span></span>

<span data-ttu-id="7b29f-119">В некоторых сценариях может потребоваться извлечение определенных атрибутов DRM в файле без фактического доступа к содержимому файла.</span><span class="sxs-lookup"><span data-stu-id="7b29f-119">In some scenarios, you may need to retrieve certain DRM attributes in a file without actually accessing the contents of the file.</span></span> <span data-ttu-id="7b29f-120">Эта возможность полезна, например, в приложениях, обрабатывающих пакеты файлов различными способами на основе информации в заголовке файла.</span><span class="sxs-lookup"><span data-stu-id="7b29f-120">This capability is useful, for example, in applications that process batches of files in different ways based on information in the file header.</span></span> <span data-ttu-id="7b29f-121">В предыдущих версиях пакета Windows Media Format SDK для открытия любого защищенного файла приложениям требовалось установить связь с статической библиотекой DRM.</span><span class="sxs-lookup"><span data-stu-id="7b29f-121">In previous versions of the Windows Media Format SDK, applications were required to link to the DRM static library in order to open any protected file.</span></span> <span data-ttu-id="7b29f-122">Приложения, не имеющие библиотеки DRM, могут использовать интерфейс [**ивмдрмедитор:: жетдрмпроперти**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmeditor-getdrmproperty) в объекте редактора метаданных для проверки определенных атрибутов DRM.</span><span class="sxs-lookup"><span data-stu-id="7b29f-122">Applications that do not have the DRM library can use the [**IWMDRMEditor::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmeditor-getdrmproperty) interface on the metadata editor object to examine certain DRM attributes.</span></span>

> [!Note]  
> <span data-ttu-id="7b29f-123">DRM не поддерживает версию этого пакета SDK на базе x64.</span><span class="sxs-lookup"><span data-stu-id="7b29f-123">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="7b29f-124">См. также</span><span class="sxs-lookup"><span data-stu-id="7b29f-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b29f-125">**Список атрибутов DRM**</span><span class="sxs-lookup"><span data-stu-id="7b29f-125">**DRM Attribute List**</span></span>](drm-attribute-list.md)
</dt> <dt>

[<span data-ttu-id="7b29f-126">**Включение поддержки DRM**</span><span class="sxs-lookup"><span data-stu-id="7b29f-126">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> <dt>

[<span data-ttu-id="7b29f-127">**Интерфейс Ивмдрмедитор**</span><span class="sxs-lookup"><span data-stu-id="7b29f-127">**IWMDRMEditor Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor)
</dt> </dl>

 

 




