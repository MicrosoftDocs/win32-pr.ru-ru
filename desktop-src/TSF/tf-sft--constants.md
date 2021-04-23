---
title: Константы TF_SFT_ (Ктфутб. h)
description: '\_ \_ Константы TF SFT \ определяют параметры вывода плавающей языковой панели.'
ms.assetid: 628e1d85-9614-4327-b89b-723f6eeb0718
topic_type:
- apiref
api_name:
- TF_SFT_SHOWNORMAL
- TF_SFT_DOCK
- TF_SFT_MINIMIZED
- TF_SFT_HIDDEN
- TF_SFT_NOTRANSPARENCY
- TF_SFT_LOWTRANSPARENCY
- TF_SFT_HIGHTRANSPARENCY
- TF_SFT_LABELS
- TF_SFT_NOLABELS
- TF_SFT_EXTRAICONSONMINIMIZED
- TF_SFT_NOEXTRAICONSONMINIMIZED
- TF_SFT_DESKBAND
api_location:
- Ctfutb.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93a947960bfbe67585dc02a37de2da3dc6737540
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681909"
---
# <a name="tf_sft_-constants"></a><span data-ttu-id="d5eb7-103">TF \_ SFT \_ \* константы</span><span class="sxs-lookup"><span data-stu-id="d5eb7-103">TF\_SFT\_\* Constants</span></span>

<span data-ttu-id="d5eb7-104">Константы \*\* \_ tf \_ \* SFT\* _. указывают параметры экрана плавающей языковой панели.</span><span class="sxs-lookup"><span data-stu-id="d5eb7-104">The \**TF\_SFT\_\** _ constants specify display settings of a floating language bar.</span></span>



| <span data-ttu-id="d5eb7-105">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="d5eb7-105">Constant/value</span></span>                                                                                                                                                                                                                                                                    | <span data-ttu-id="d5eb7-106">Описание</span><span class="sxs-lookup"><span data-stu-id="d5eb7-106">Description</span></span>                                                                                                                                                                                                                                                                             |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_SFT_SHOWNORMAL"></span><span id="tf_sft_shownormal"></span><dl> <span data-ttu-id="d5eb7-107"><dt>_ \* TF \_ SFT \_ шовнормал \* \*</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="d5eb7-107"><dt>_\*TF\_SFT\_SHOWNORMAL\*\*</dt> <dt>0x00000001</dt></span></span> </dl>                                        | <span data-ttu-id="d5eb7-108">Отображение языковой панели в виде плавающего окна.</span><span class="sxs-lookup"><span data-stu-id="d5eb7-108">Display the language bar as a floating window.</span></span> <span data-ttu-id="d5eb7-109">Эта константа не может быть объединена с помощью TF \_ SFT \_ Dock, TF \_ SFT \_ сворачивания, TF \_ SFT \_ Hidden или TF \_ SFT \_ дескбанд констант.</span><span class="sxs-lookup"><span data-stu-id="d5eb7-109">This constant cannot be combined with the TF\_SFT\_DOCK, TF\_SFT\_MINIMIZED, TF\_SFT\_HIDDEN, or TF\_SFT\_DESKBAND constants.</span></span><br/>                                                                                                 |
| <span id="TF_SFT_DOCK"></span><span id="tf_sft_dock"></span><dl> <span data-ttu-id="d5eb7-110"><dt>**Tf \_ SFT \_ DOCKER**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="d5eb7-110"><dt>**TF\_SFT\_DOCK**</dt> <dt>0x00000002</dt></span></span> </dl>                                                          | <span data-ttu-id="d5eb7-111">Закрепите языковую панель в отдельной области задач.</span><span class="sxs-lookup"><span data-stu-id="d5eb7-111">Dock the language bar in its own task pane.</span></span> <span data-ttu-id="d5eb7-112">Эта константа не может использоваться в сочетании с TF \_ SFT \_ ШОВНОРМАЛ, TF \_ SFT \_ сворачивания, TF \_ SFT \_ Hidden или TF \_ SFT \_ дескбанд константами.</span><span class="sxs-lookup"><span data-stu-id="d5eb7-112">This constant cannot be combined with the TF\_SFT\_SHOWNORMAL, TF\_SFT\_MINIMIZED, TF\_SFT\_HIDDEN, or TF\_SFT\_DESKBAND constants.</span></span> <span data-ttu-id="d5eb7-113">Доступно только в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d5eb7-113">Available only on Windows XP.</span></span><br/>                                                                |
| <span id="TF_SFT_MINIMIZED"></span><span id="tf_sft_minimized"></span><dl> <span data-ttu-id="d5eb7-114"><dt>**Tf \_ SFT, \_ уменьшено до**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="d5eb7-114"><dt>**TF\_SFT\_MINIMIZED**</dt> <dt>0x00000004</dt></span></span> </dl>                                           | <span data-ttu-id="d5eb7-115">Отображение языковой панели в виде одного значка в области уведомлений.</span><span class="sxs-lookup"><span data-stu-id="d5eb7-115">Display the language bar as a single icon in the system tray.</span></span> <span data-ttu-id="d5eb7-116">Эту константу нельзя сочетать с \_ \_ константами TF SFT ШОВНОРМАЛ, TF \_ SFT \_ DOCKER, TF \_ SFT \_ Hidden или TF \_ SFT \_ дескбанд.</span><span class="sxs-lookup"><span data-stu-id="d5eb7-116">This constant cannot be combined with the TF\_SFT\_SHOWNORMAL, TF\_SFT\_DOCK, TF\_SFT\_HIDDEN, or TF\_SFT\_DESKBAND constants.</span></span> <span data-ttu-id="d5eb7-117">В Windows XP используйте \_ \_ вместо него TF SFT дескбанд.</span><span class="sxs-lookup"><span data-stu-id="d5eb7-117">In Windows XP, use TF\_SFT\_DESKBAND instead.</span></span><br/>                                   |
| <span id="TF_SFT_HIDDEN"></span><span id="tf_sft_hidden"></span><dl> <span data-ttu-id="d5eb7-118"><dt>**Tf \_ \_Скрытые**</dt> <dt>0x00000008</dt></span><span class="sxs-lookup"><span data-stu-id="d5eb7-118"><dt>**TF\_SFT\_HIDDEN**</dt> <dt>0x00000008</dt></span></span> </dl>                                                    | <span data-ttu-id="d5eb7-119">Скрыть языковую панель.</span><span class="sxs-lookup"><span data-stu-id="d5eb7-119">Hide the language bar.</span></span> <span data-ttu-id="d5eb7-120">Эта константа не может быть объединена с TF \_ SFT \_ ШОВНОРМАЛ, TF \_ SFT \_ Dock, TF \_ SFT \_ сворачивания или TF \_ SFT \_ дескбанд константами.</span><span class="sxs-lookup"><span data-stu-id="d5eb7-120">This constant cannot be combined with the TF\_SFT\_SHOWNORMAL, TF\_SFT\_DOCK, TF\_SFT\_MINIMIZED, or TF\_SFT\_DESKBAND constants.</span></span><br/>                                                                                                                     |
| <span id="TF_SFT_NOTRANSPARENCY"></span><span id="tf_sft_notransparency"></span><dl> <span data-ttu-id="d5eb7-121"><dt>**Tf \_ \_НЕпрозрачное для SFT**</dt> <dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="d5eb7-121"><dt>**TF\_SFT\_NOTRANSPARENCY**</dt> <dt>0x00000010</dt></span></span> </dl>                            | <span data-ttu-id="d5eb7-122">Сделать языковую панель непрозрачной.</span><span class="sxs-lookup"><span data-stu-id="d5eb7-122">Make the language bar opaque.</span></span><br/>                                                                                                                                                                                                                                                |
| <span id="TF_SFT_LOWTRANSPARENCY"></span><span id="tf_sft_lowtransparency"></span><dl> <span data-ttu-id="d5eb7-123"><dt>**Tf \_ SFT \_ ловтранспаренци**</dt> <dt>0x00000020</dt></span><span class="sxs-lookup"><span data-stu-id="d5eb7-123"><dt>**TF\_SFT\_LOWTRANSPARENCY**</dt> <dt>0x00000020</dt></span></span> </dl>                         | <span data-ttu-id="d5eb7-124">Сделать языковую панель частично прозрачной.</span><span class="sxs-lookup"><span data-stu-id="d5eb7-124">Make the language bar partially transparent.</span></span> <span data-ttu-id="d5eb7-125">Доступно только в Windows 2000 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="d5eb7-125">Available only on Windows 2000 or later.</span></span><br/>                                                                                                                                                                                        |
| <span id="TF_SFT_HIGHTRANSPARENCY"></span><span id="tf_sft_hightransparency"></span><dl> <span data-ttu-id="d5eb7-126"><dt>**Tf \_ SFT \_ хигхтранспаренци**</dt> <dt>0x00000040</dt></span><span class="sxs-lookup"><span data-stu-id="d5eb7-126"><dt>**TF\_SFT\_HIGHTRANSPARENCY**</dt> <dt>0x00000040</dt></span></span> </dl>                      | <span data-ttu-id="d5eb7-127">Сделать языковую панель сильно прозрачной.</span><span class="sxs-lookup"><span data-stu-id="d5eb7-127">Make the language bar highly transparent.</span></span> <span data-ttu-id="d5eb7-128">Доступно только в Windows 2000 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="d5eb7-128">Available only on Windows 2000 or later.</span></span><br/>                                                                                                                                                                                           |
| <span id="TF_SFT_LABELS"></span><span id="tf_sft_labels"></span><dl> <span data-ttu-id="d5eb7-129"><dt>**Tf \_ \_Метки SFT**</dt> <dt>0x00000080</dt></span><span class="sxs-lookup"><span data-stu-id="d5eb7-129"><dt>**TF\_SFT\_LABELS**</dt> <dt>0x00000080</dt></span></span> </dl>                                                    | <span data-ttu-id="d5eb7-130">Отображать текстовые метки рядом со значками языковой панели.</span><span class="sxs-lookup"><span data-stu-id="d5eb7-130">Display text labels next to language bar icons.</span></span><br/>                                                                                                                                                                                                                              |
| <span id="TF_SFT_NOLABELS"></span><span id="tf_sft_nolabels"></span><dl> <span data-ttu-id="d5eb7-131"><dt>**Tf \_ \_**</dt> <dt>0x00000100ы</dt> SFT</span><span class="sxs-lookup"><span data-stu-id="d5eb7-131"><dt>**TF\_SFT\_NOLABELS**</dt> <dt>0x00000100</dt></span></span> </dl>                                              | <span data-ttu-id="d5eb7-132">Скрыть текстовые метки значков языковой панели.</span><span class="sxs-lookup"><span data-stu-id="d5eb7-132">Hide language bar icon text labels.</span></span><br/>                                                                                                                                                                                                                                          |
| <span id="TF_SFT_EXTRAICONSONMINIMIZED"></span><span id="tf_sft_extraiconsonminimized"></span><dl> <span data-ttu-id="d5eb7-133"><dt>**Tf \_ SFT \_ екстраиконсонминимизед**</dt> <dt>0x00000200</dt></span><span class="sxs-lookup"><span data-stu-id="d5eb7-133"><dt>**TF\_SFT\_EXTRAICONSONMINIMIZED**</dt> <dt>0x00000200</dt></span></span> </dl>       | <span data-ttu-id="d5eb7-134">Отображение значков службы текста на панели задач, когда панель языка свернута.</span><span class="sxs-lookup"><span data-stu-id="d5eb7-134">Display text service icons on the taskbar when the language bar is minimized.</span></span><br/>                                                                                                                                                                                                |
| <span id="TF_SFT_NOEXTRAICONSONMINIMIZED"></span><span id="tf_sft_noextraiconsonminimized"></span><dl> <span data-ttu-id="d5eb7-135"><dt>**Tf \_ SFT \_ ноекстраиконсонминимизед**</dt> <dt>0x00000400</dt></span><span class="sxs-lookup"><span data-stu-id="d5eb7-135"><dt>**TF\_SFT\_NOEXTRAICONSONMINIMIZED**</dt> <dt>0x00000400</dt></span></span> </dl> | <span data-ttu-id="d5eb7-136">Скрытие значков службы текста на панели задач при сворачивании языковой панели.</span><span class="sxs-lookup"><span data-stu-id="d5eb7-136">Hide text service icons on the taskbar when the language bar is minimized.</span></span><br/>                                                                                                                                                                                                   |
| <span id="TF_SFT_DESKBAND"></span><span id="tf_sft_deskband"></span><dl> <span data-ttu-id="d5eb7-137"><dt>**Tf \_ SFT \_ дескбанд**</dt> <dt>0x00000800</dt></span><span class="sxs-lookup"><span data-stu-id="d5eb7-137"><dt>**TF\_SFT\_DESKBAND**</dt> <dt>0x00000800</dt></span></span> </dl>                                              | <span data-ttu-id="d5eb7-138">Закрепите языковую панель на ригхсанд конец панели задач системы (непосредственно слева от области уведомлений или часов).</span><span class="sxs-lookup"><span data-stu-id="d5eb7-138">Dock the language bar in the righthand end of the system task bar (immediately left of the system tray/clock).</span></span> <span data-ttu-id="d5eb7-139">Эту константу невозможно объединить с TF \_ SFT \_ ШОВНОРМАЛ, TF \_ SFT \_ Dock, TF \_ SFT \_ сворачивания или TF \_ SFT \_ Hidden константы.</span><span class="sxs-lookup"><span data-stu-id="d5eb7-139">This constant cannot be combined with the TF\_SFT\_SHOWNORMAL, TF\_SFT\_DOCK, TF\_SFT\_MINIMIZED, or TF\_SFT\_HIDDEN constants.</span></span> <span data-ttu-id="d5eb7-140">Доступно только в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d5eb7-140">Available only on Windows XP.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="d5eb7-141">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d5eb7-141">Remarks</span></span>

<span data-ttu-id="d5eb7-142">Метод [итфлангбармгр:: шовфлоатинг](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbarmgr-showfloating) задает результат логической операции **or** над одной или несколькими константами для указания атрибутов элемента языковой панели.</span><span class="sxs-lookup"><span data-stu-id="d5eb7-142">The [ITfLangBarMgr::ShowFloating](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbarmgr-showfloating) method sets the result of a logical **OR** operation on one or more of these constants to specify the attributes of the language bar item.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5eb7-143">Требования</span><span class="sxs-lookup"><span data-stu-id="d5eb7-143">Requirements</span></span>



| <span data-ttu-id="d5eb7-144">Требование</span><span class="sxs-lookup"><span data-stu-id="d5eb7-144">Requirement</span></span> | <span data-ttu-id="d5eb7-145">Значение</span><span class="sxs-lookup"><span data-stu-id="d5eb7-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d5eb7-146">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d5eb7-146">Minimum supported client</span></span><br/> | <span data-ttu-id="d5eb7-147">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d5eb7-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="d5eb7-148">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d5eb7-148">Minimum supported server</span></span><br/> | <span data-ttu-id="d5eb7-149">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d5eb7-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d5eb7-150">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="d5eb7-150">Redistributable</span></span><br/>          | <span data-ttu-id="d5eb7-151">TSF 1,0 в Windows 2000 профессиональная</span><span class="sxs-lookup"><span data-stu-id="d5eb7-151">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                       |
| <span data-ttu-id="d5eb7-152">Header</span><span class="sxs-lookup"><span data-stu-id="d5eb7-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5eb7-153"><dt>Ктфутб. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5eb7-153"><dt>Ctfutb.h</dt></span></span> </dl>   |
| <span data-ttu-id="d5eb7-154">IDL</span><span class="sxs-lookup"><span data-stu-id="d5eb7-154">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d5eb7-155"><dt>Ктфутб. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d5eb7-155"><dt>Ctfutb.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5eb7-156">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d5eb7-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5eb7-157">Итфлангбармгр:: Шовфлоатинг</span><span class="sxs-lookup"><span data-stu-id="d5eb7-157">ITfLangBarMgr::ShowFloating</span></span>](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbarmgr-showfloating)
</dt> </dl>

 

 





