---
description: Эти флаги определяют поведение указателя мультимедиа.
ms.assetid: 60afb2e8-cdd1-493e-8fc8-6fa581720b8d
title: Флаги проверки имени файла (Кедит. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SFN_VALIDATEF_CHECK
- SFN_VALIDATEF_POPUP
- SFN_VALIDATEF_TELLME
- SFN_VALIDATEF_REPLACE
- SFN_VALIDATEF_USELOCAL
- SFN_VALIDATEF_NOFIND
- SFN_VALIDATEF_IGNOREMUTED
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: d8930241be0306c637bcab36207fec1de2e489c9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675465"
---
# <a name="file-name-validation-flags"></a><span data-ttu-id="d6936-103">Флаги проверки имени файла</span><span class="sxs-lookup"><span data-stu-id="d6936-103">File Name Validation Flags</span></span>

<span data-ttu-id="d6936-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="d6936-104">\[Deprecated.</span></span> <span data-ttu-id="d6936-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d6936-105">This API may be removed from future releases of Windows.\]</span></span>

<span data-ttu-id="d6936-106">Эти флаги определяют поведение указателя мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="d6936-106">These flags specify the behavior of the media locator.</span></span>



| <span data-ttu-id="d6936-107">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="d6936-107">Constant/value</span></span>                                                                                                                                                                                                                                               | <span data-ttu-id="d6936-108">Описание</span><span class="sxs-lookup"><span data-stu-id="d6936-108">Description</span></span>                                                                                                                                                                                                                    |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SFN_VALIDATEF_CHECK"></span><span id="sfn_validatef_check"></span><dl> <span data-ttu-id="d6936-109"><dt>**СФН \_ ВАЛИДАТЕФ \_ Проверка**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="d6936-109"><dt>**SFN\_VALIDATEF\_CHECK**</dt> <dt>0x01</dt></span></span> </dl>                   | <span data-ttu-id="d6936-110">Проверьте правильность имен файлов.</span><span class="sxs-lookup"><span data-stu-id="d6936-110">Check the validity of file names.</span></span> <span data-ttu-id="d6936-111">Этот флаг необходимо установить для проверки имен файлов.</span><span class="sxs-lookup"><span data-stu-id="d6936-111">You must set this flag to validate file names.</span></span> <span data-ttu-id="d6936-112">В противном случае другие флаги не оказывают никакого влияния.</span><span class="sxs-lookup"><span data-stu-id="d6936-112">If not, the other flags have no effect.</span></span><br/>                                                                                            |
| <span id="SFN_VALIDATEF_POPUP"></span><span id="sfn_validatef_popup"></span><dl> <span data-ttu-id="d6936-113"><dt>**СФН \_ \_Всплывающее меню валидатеф**</dt> <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="d6936-113"><dt>**SFN\_VALIDATEF\_POPUP**</dt> <dt>0x02</dt></span></span> </dl>                   | <span data-ttu-id="d6936-114">Если файл не найден, отобразите диалоговое окно Открытие файла для конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="d6936-114">If a file is not located, display an Open File dialog box for the end user.</span></span><br/>                                                                                                                                         |
| <span id="SFN_VALIDATEF_TELLME"></span><span id="sfn_validatef_tellme"></span><dl> <span data-ttu-id="d6936-115"><dt>**СФН \_ ВАЛИДАТЕФ \_ теллме**</dt> <dt>0x04</dt></span><span class="sxs-lookup"><span data-stu-id="d6936-115"><dt>**SFN\_VALIDATEF\_TELLME**</dt> <dt>0x04</dt></span></span> </dl>                | <span data-ttu-id="d6936-116">Если отсутствующий файл найден, ненадолго отобразите окно сообщения с именем и расположением файла.</span><span class="sxs-lookup"><span data-stu-id="d6936-116">If a missing file is located, briefly display a message box with the name and location of the file.</span></span> <span data-ttu-id="d6936-117">Этот флаг в основном полезен в целях тестирования. возможно, окно сообщения не подходит для розничного продукта.</span><span class="sxs-lookup"><span data-stu-id="d6936-117">This flag is mostly useful for testing purposes; the message box is probably not suitable for a retail product.</span></span><br/> |
| <span id="SFN_VALIDATEF_REPLACE"></span><span id="sfn_validatef_replace"></span><dl> <span data-ttu-id="d6936-118"><dt>**СФН \_ ВАЛИДАТЕФ \_ заменить**</dt> <dt>0x08</dt></span><span class="sxs-lookup"><span data-stu-id="d6936-118"><dt>**SFN\_VALIDATEF\_REPLACE**</dt> <dt>0x08</dt></span></span> </dl>             | <span data-ttu-id="d6936-119">Если отсутствующий файл найден, обновите имя исходного объекта.</span><span class="sxs-lookup"><span data-stu-id="d6936-119">If a missing file is located, update the name of the source object.</span></span> <span data-ttu-id="d6936-120">(Допускается только в методе [**иамтимелине:: валидатесаурценамес**](iamtimeline-validatesourcenames.md) .)</span><span class="sxs-lookup"><span data-stu-id="d6936-120">(Only valid in the [**IAMTimeline::ValidateSourceNames**](iamtimeline-validatesourcenames.md) method.)</span></span><br/>                                         |
| <span id="SFN_VALIDATEF_USELOCAL"></span><span id="sfn_validatef_uselocal"></span><dl> <span data-ttu-id="d6936-121"><dt>**СФН \_ ВАЛИДАТЕФ \_ уселокал**</dt> <dt>0x10</dt></span><span class="sxs-lookup"><span data-stu-id="d6936-121"><dt>**SFN\_VALIDATEF\_USELOCAL**</dt> <dt>0x10</dt></span></span> </dl>          | <span data-ttu-id="d6936-122">Всегда используйте локальный файл, даже если версия файла существует в сети.</span><span class="sxs-lookup"><span data-stu-id="d6936-122">Always use a local file, even if a version of the file exists on the network.</span></span><br/>                                                                                                                                       |
| <span id="SFN_VALIDATEF_NOFIND"></span><span id="sfn_validatef_nofind"></span><dl> <span data-ttu-id="d6936-123"><dt>**СФН \_ ВАЛИДАТЕФ \_**</dt> , отличный от Find <dt>0x20</dt></span><span class="sxs-lookup"><span data-stu-id="d6936-123"><dt>**SFN\_VALIDATEF\_NOFIND**</dt> <dt>0x20</dt></span></span> </dl>                | <span data-ttu-id="d6936-124">Не искать отсутствующие файлы.</span><span class="sxs-lookup"><span data-stu-id="d6936-124">Do not search for missing files.</span></span> <span data-ttu-id="d6936-125">Имена файлов по-прежнему проверяются, если \_ установлен \_ флаг проверки СФН валидатеф.</span><span class="sxs-lookup"><span data-stu-id="d6936-125">File names are still validated if you set the SFN\_VALIDATEF\_CHECK flag.</span></span><br/>                                                                                                          |
| <span id="SFN_VALIDATEF_IGNOREMUTED"></span><span id="sfn_validatef_ignoremuted"></span><dl> <span data-ttu-id="d6936-126"><dt>**СФН \_ ВАЛИДАТЕФ \_ игноремутед**</dt> <dt>0x40</dt></span><span class="sxs-lookup"><span data-stu-id="d6936-126"><dt>**SFN\_VALIDATEF\_IGNOREMUTED**</dt> <dt>0x40</dt></span></span> </dl> | <span data-ttu-id="d6936-127">Не учитывать отключенные исходные объекты.</span><span class="sxs-lookup"><span data-stu-id="d6936-127">Ignore muted source objects.</span></span> <span data-ttu-id="d6936-128">(Допускается только в методе [**иамтимелине:: валидатесаурценамес**](iamtimeline-validatesourcenames.md) .)</span><span class="sxs-lookup"><span data-stu-id="d6936-128">(Only valid in the [**IAMTimeline::ValidateSourceNames**](iamtimeline-validatesourcenames.md) method.)</span></span><br/>                                                                                |



## <a name="requirements"></a><span data-ttu-id="d6936-129">Требования</span><span class="sxs-lookup"><span data-stu-id="d6936-129">Requirements</span></span>



| <span data-ttu-id="d6936-130">Требование</span><span class="sxs-lookup"><span data-stu-id="d6936-130">Requirement</span></span> | <span data-ttu-id="d6936-131">Значение</span><span class="sxs-lookup"><span data-stu-id="d6936-131">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d6936-132">Header</span><span class="sxs-lookup"><span data-stu-id="d6936-132">Header</span></span><br/> | <dl> <span data-ttu-id="d6936-133"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6936-133"><dt>Qedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6936-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d6936-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6936-135">**Имедиалокатор:: Финдмедиафиле**</span><span class="sxs-lookup"><span data-stu-id="d6936-135">**IMediaLocator::FindMediaFile**</span></span>](imedialocator-findmediafile.md)
</dt> <dt>

[<span data-ttu-id="d6936-136">**Ирендеренгине:: Сетсаурценамевалидатион**</span><span class="sxs-lookup"><span data-stu-id="d6936-136">**IRenderEngine::SetSourceNameValidation**</span></span>](irenderengine-setsourcenamevalidation.md)
</dt> </dl>

 

 




