---
title: EC_WMT_EVENT (пакет SDK для формата Windows Media 11)
description: '\_событие EC ВМТ \_'
ms.assetid: 51d51659-8e7d-49b7-83f2-a80e99d39d78
keywords:
- Пакет SDK Windows Media Format, EC_WMT_EVENT
- DirectShow, EC_WMT_EVENT
- EC_WMT_EVENT
- Управление цифровыми правами (DRM), EC_WMT_EVENT
- DRM (Управление цифровыми правами), EC_WMT_EVENT
- Расширенный формат систем (ASF), EC_WMT_EVENT
- ASF (Расширенный системный формат), EC_WMT_EVENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebe74baaba676a97e609b4c03cd4db9010bd8f6a
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104488748"
---
# <a name="ec_wmt_event-windows-media-format-11-sdk"></a><span data-ttu-id="e2a43-110">EC_WMT_EVENT (пакет SDK для формата Windows Media 11)</span><span class="sxs-lookup"><span data-stu-id="e2a43-110">EC_WMT_EVENT (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="e2a43-111">Отправляется пакетом SDK для формата Windows Media, когда приложение использует фильтр чтения ASF для воспроизведения файлов ASF, защищенных с помощью управления цифровыми правами (DRM).</span><span class="sxs-lookup"><span data-stu-id="e2a43-111">Sent by the Windows Media Format SDK when an application uses the ASF Reader filter to play ASF files protected by digital rights management (DRM).</span></span>

<span data-ttu-id="e2a43-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="e2a43-112">Parameters</span></span>

<span data-ttu-id="e2a43-113">*lParam1*</span><span class="sxs-lookup"><span data-stu-id="e2a43-113">*lParam1*</span></span>

<span data-ttu-id="e2a43-114">Может быть одним из следующих \_ значений состояния ВМТ.</span><span class="sxs-lookup"><span data-stu-id="e2a43-114">Can be one of the following WMT\_STATUS values.</span></span>



| <span data-ttu-id="e2a43-115">\_Сообщение о состоянии ВМТ</span><span class="sxs-lookup"><span data-stu-id="e2a43-115">WMT\_STATUS Message</span></span>           | <span data-ttu-id="e2a43-116">Описание</span><span class="sxs-lookup"><span data-stu-id="e2a43-116">Description</span></span>                                                                                                                    |
|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2a43-117">ВМТ \_ без \_ прав</span><span class="sxs-lookup"><span data-stu-id="e2a43-117">WMT\_NO\_RIGHTS</span></span>               | <span data-ttu-id="e2a43-118">Файл защищен с помощью DRM версии 1, и приложение не имеет прав на выполнение запрошенного действия.</span><span class="sxs-lookup"><span data-stu-id="e2a43-118">The file is protected with DRM version 1 and the application has no rights to perform the requested action.</span></span>                    |
| <span data-ttu-id="e2a43-119">ВМТ \_ получить \_ лицензию</span><span class="sxs-lookup"><span data-stu-id="e2a43-119">WMT\_ACQUIRE\_LICENSE</span></span>         | <span data-ttu-id="e2a43-120">Процесс получения лицензии завершен.</span><span class="sxs-lookup"><span data-stu-id="e2a43-120">The license acquisition process has been completed.</span></span> <span data-ttu-id="e2a43-121">(Это не обязательно означает, что лицензия была успешно получена.)</span><span class="sxs-lookup"><span data-stu-id="e2a43-121">(This does not necessarily mean that a license was successfully acquired.)</span></span> |
| <span data-ttu-id="e2a43-122">ВМТ \_ без \_ прав \_</span><span class="sxs-lookup"><span data-stu-id="e2a43-122">WMT\_NO\_RIGHTS\_EX</span></span>           | <span data-ttu-id="e2a43-123">Файл защищен с помощью DRM версии 7, и приложение не имеет прав на выполнение запрошенного действия.</span><span class="sxs-lookup"><span data-stu-id="e2a43-123">The file is protected with DRM version 7 and the application has no rights to perform the requested action.</span></span>                    |
| <span data-ttu-id="e2a43-124">ВМТ \_ нуждается в \_ индивидуализации</span><span class="sxs-lookup"><span data-stu-id="e2a43-124">WMT\_NEEDS\_INDIVIDUALIZATION</span></span> | <span data-ttu-id="e2a43-125">Лицензия позволяет выполнять запрошенное действие только для отдельных приложений.</span><span class="sxs-lookup"><span data-stu-id="e2a43-125">The license allows only individualized applications to perform the requested action.</span></span>                                           |
| <span data-ttu-id="e2a43-126">ВМТ \_ индивидуализируйте</span><span class="sxs-lookup"><span data-stu-id="e2a43-126">WMT\_INDIVIDUALIZE</span></span>            | <span data-ttu-id="e2a43-127">Процесс индивидуализации теперь выполняется или завершен.</span><span class="sxs-lookup"><span data-stu-id="e2a43-127">The individualization process is now being performed or has been completed.</span></span>                                                    |



 

<span data-ttu-id="e2a43-128">*lParam2*</span><span class="sxs-lookup"><span data-stu-id="e2a43-128">*lParam2*</span></span>

<span data-ttu-id="e2a43-129">Указатель на структуру **\_ \_ \_ данных события ВМТ** , которая содержит сведения о событии в указателе на член **PData** , а также код состояния **HRESULT** , отправленный пакетом SDK Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="e2a43-129">Pointer to an **AM\_WMT\_EVENT\_DATA** structure that contains information about the event in the **pData** member pointer, as well as an **HRESULT** status code sent by the Windows Media Format SDK.</span></span> <span data-ttu-id="e2a43-130">Значение *lParam2* зависит от значения *lParam1*, как описано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="e2a43-130">The value of *lParam2* depends on the value of *lParam1*, as described in the following table.</span></span> <span data-ttu-id="e2a43-131">( \_ Структуры WM определены в пакете SDK формата Windows Media.)</span><span class="sxs-lookup"><span data-stu-id="e2a43-131">(The "WM\_" structures are defined in the Windows Media Format SDK.)</span></span>



| <span data-ttu-id="e2a43-132">Если lParam1 имеет значение...</span><span class="sxs-lookup"><span data-stu-id="e2a43-132">If lParam1 is...</span></span>              | <span data-ttu-id="e2a43-133">\_Данные о \_ событии ВМТ \_ . pData —...</span><span class="sxs-lookup"><span data-stu-id="e2a43-133">AM\_WMT\_EVENT\_DATA.pData is...</span></span>                            |
|-------------------------------|-------------------------------------------------------------|
| <span data-ttu-id="e2a43-134">ВМТ \_ без \_ прав</span><span class="sxs-lookup"><span data-stu-id="e2a43-134">WMT\_NO\_RIGHTS</span></span>               | <span data-ttu-id="e2a43-135">Указатель на строку типа **WCHAR** , содержащую URL-адрес запроса.</span><span class="sxs-lookup"><span data-stu-id="e2a43-135">A pointer to a **WCHAR** string containing a challenge URL.</span></span> |
| <span data-ttu-id="e2a43-136">ВМТ \_ получить \_ лицензию</span><span class="sxs-lookup"><span data-stu-id="e2a43-136">WMT\_ACQUIRE\_LICENSE</span></span>         | <span data-ttu-id="e2a43-137">Указатель на структуру **\_ \_ \_ данных лицензии WM Get** .</span><span class="sxs-lookup"><span data-stu-id="e2a43-137">A pointer to a **WM\_GET\_LICENSE\_DATA** structure.</span></span>        |
| <span data-ttu-id="e2a43-138">ВМТ \_ без \_ прав \_</span><span class="sxs-lookup"><span data-stu-id="e2a43-138">WMT\_NO\_RIGHTS\_EX</span></span>           | <span data-ttu-id="e2a43-139">Указатель на структуру **\_ \_ \_ данных лицензии WM Get** .</span><span class="sxs-lookup"><span data-stu-id="e2a43-139">A pointer to a **WM\_GET\_LICENSE\_DATA** structure.</span></span>        |
| <span data-ttu-id="e2a43-140">ВМТ \_ нуждается в \_ индивидуализации</span><span class="sxs-lookup"><span data-stu-id="e2a43-140">WMT\_NEEDS\_INDIVIDUALIZATION</span></span> | <span data-ttu-id="e2a43-141">NULL.</span><span class="sxs-lookup"><span data-stu-id="e2a43-141">NULL.</span></span>                                                       |
| <span data-ttu-id="e2a43-142">ВМТ \_ индивидуализируйте</span><span class="sxs-lookup"><span data-stu-id="e2a43-142">WMT\_INDIVIDUALIZE</span></span>            | <span data-ttu-id="e2a43-143">Указатель на структуру **состояния WM \_ индивидуализируйте \_** .</span><span class="sxs-lookup"><span data-stu-id="e2a43-143">A pointer to a **WM\_INDIVIDUALIZE\_STATUS** structure.</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="e2a43-144">См. также</span><span class="sxs-lookup"><span data-stu-id="e2a43-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2a43-145">**Функции цифровых Rights Management**</span><span class="sxs-lookup"><span data-stu-id="e2a43-145">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> <dt>

[<span data-ttu-id="e2a43-146">**Справочник по КАСФ DirectShow**</span><span class="sxs-lookup"><span data-stu-id="e2a43-146">**DirectShow QASF Reference**</span></span>](directshow-qasf-reference.md)
</dt> <dt>

[<span data-ttu-id="e2a43-147">**Включение поддержки DRM**</span><span class="sxs-lookup"><span data-stu-id="e2a43-147">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> </dl>

 

 




