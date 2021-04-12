---
description: Следующие идентификаторы GUID определяют типы для объектов взаимного исключения для потоков ASF.
ms.assetid: 3db8eebd-2e26-4c77-8f66-7d08436c9e42
title: Идентификаторы GUID типов взаимного исключения ASF (Вмконтаинер. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a6fedc766e26c35bb967054a704b732ca03e8a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262824"
---
# <a name="asf-mutual-exclusion-type-guids"></a><span data-ttu-id="8602f-103">Идентификаторы GUID типов взаимного исключения ASF</span><span class="sxs-lookup"><span data-stu-id="8602f-103">ASF Mutual Exclusion Type GUIDs</span></span>

<span data-ttu-id="8602f-104">Следующие идентификаторы GUID определяют типы для объектов взаимного исключения для потоков ASF.</span><span class="sxs-lookup"><span data-stu-id="8602f-104">The following GUIDs define the types for the mutual exclusion object for Advanced Systems Format (ASF) streams.</span></span>



| <span data-ttu-id="8602f-105">Константа</span><span class="sxs-lookup"><span data-stu-id="8602f-105">Constant</span></span>                                                                                                                                                                                                                                              | <span data-ttu-id="8602f-106">Описание</span><span class="sxs-lookup"><span data-stu-id="8602f-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MFASFMutexType_Language"></span><span id="mfasfmutextype_language"></span><span id="MFASFMUTEXTYPE_LANGUAGE"></span><dl> <span data-ttu-id="8602f-107"><dt>**\_Язык мфасфмутекстипе**</dt></span><span class="sxs-lookup"><span data-stu-id="8602f-107"><dt>**MFASFMutexType\_Language**</dt></span></span> </dl>                 | <span data-ttu-id="8602f-108">Потоки являются взаимоисключающими по отношению к языку.</span><span class="sxs-lookup"><span data-stu-id="8602f-108">The streams are mutually exclusive by language.</span></span> <span data-ttu-id="8602f-109">Этот тип взаимного исключения похож на звуковые дорожки на DVD-диске.</span><span class="sxs-lookup"><span data-stu-id="8602f-109">This type of mutual exclusion is similar to the audio tracks on a DVD.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="MFASFMutexType_Bitrate"></span><span id="mfasfmutextype_bitrate"></span><span id="MFASFMUTEXTYPE_BITRATE"></span><dl> <span data-ttu-id="8602f-110"><dt>**\_Скорость мфасфмутекстипе**</dt></span><span class="sxs-lookup"><span data-stu-id="8602f-110"><dt>**MFASFMutexType\_Bitrate**</dt></span></span> </dl>                     | <span data-ttu-id="8602f-111">Потоки являются взаимоисключающими по скорости.</span><span class="sxs-lookup"><span data-stu-id="8602f-111">The streams are mutually exclusive by bit rate.</span></span> <span data-ttu-id="8602f-112">Этот тип взаимного исключения также называется исключением с несколькими битовыми частотами (MBR).</span><span class="sxs-lookup"><span data-stu-id="8602f-112">This type of mutual exclusion is also called multiple bit rate (MBR) exclusion.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                        |
| <span id="MFASFMutexType_Presentation"></span><span id="mfasfmutextype_presentation"></span><span id="MFASFMUTEXTYPE_PRESENTATION"></span><dl> <span data-ttu-id="8602f-113"><dt>**Мфасфмутекстипе \_ презентацию**</dt></span><span class="sxs-lookup"><span data-stu-id="8602f-113"><dt>**MFASFMutexType\_Presentation**</dt></span></span> </dl> | <span data-ttu-id="8602f-114">Потоки являются взаимоисключающими по представлениям.</span><span class="sxs-lookup"><span data-stu-id="8602f-114">The streams are mutually exclusive by presentation.</span></span> <span data-ttu-id="8602f-115">Этот тип можно использовать во многих сценариях, но его следует использовать только в том случае, если содержимое совпадает, но принимает другую форму.</span><span class="sxs-lookup"><span data-stu-id="8602f-115">This type can be used for many scenarios, but it should only be used when the content is the same but takes a different form.</span></span> <span data-ttu-id="8602f-116">Например, два потока, содержащие одно и то же видео, один из которых отформатировано для заполнения экрана, а другой, обслуживающий исходные Широкоэкранные пропорции, должны быть взаимоисключающими с помощью этого типа.</span><span class="sxs-lookup"><span data-stu-id="8602f-116">For example, two streams containing the same video, one formatted to fill the screen and the other maintaining the original widescreen aspect ratio, should be made mutually exclusive by using this type.</span></span> <span data-ttu-id="8602f-117">Еще один пример — потоки, содержащие видео одного снимка сцены из разных углов.</span><span class="sxs-lookup"><span data-stu-id="8602f-117">Another example is streams containing video of the same scene shot from different angles.</span></span><br/> |
| <span id="MFASFMutexType_Unknown"></span><span id="mfasfmutextype_unknown"></span><span id="MFASFMUTEXTYPE_UNKNOWN"></span><dl> <span data-ttu-id="8602f-118"><dt>**Мфасфмутекстипе \_ неизвестный**</dt></span><span class="sxs-lookup"><span data-stu-id="8602f-118"><dt>**MFASFMutexType\_Unknown**</dt></span></span> </dl>                     | <span data-ttu-id="8602f-119">Потоки являются взаимоисключающими на основе настраиваемых критериев.</span><span class="sxs-lookup"><span data-stu-id="8602f-119">The streams are mutually exclusive based on custom criteria.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                           |



## <a name="requirements"></a><span data-ttu-id="8602f-120">Требования</span><span class="sxs-lookup"><span data-stu-id="8602f-120">Requirements</span></span>



| <span data-ttu-id="8602f-121">Требование</span><span class="sxs-lookup"><span data-stu-id="8602f-121">Requirement</span></span> | <span data-ttu-id="8602f-122">Значение</span><span class="sxs-lookup"><span data-stu-id="8602f-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8602f-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8602f-123">Minimum supported client</span></span><br/> | <span data-ttu-id="8602f-124">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8602f-124">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="8602f-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8602f-125">Minimum supported server</span></span><br/> | <span data-ttu-id="8602f-126">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8602f-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="8602f-127">Header</span><span class="sxs-lookup"><span data-stu-id="8602f-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="8602f-128"><dt>Вмконтаинер. h</dt></span><span class="sxs-lookup"><span data-stu-id="8602f-128"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8602f-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8602f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8602f-130">**Имфасфмутуалексклусион:: GetType**</span><span class="sxs-lookup"><span data-stu-id="8602f-130">**IMFASFMutualExclusion::GetType**</span></span>](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-gettype)
</dt> <dt>

[<span data-ttu-id="8602f-131">**Имфасфмутуалексклусион:: Сеттипе**</span><span class="sxs-lookup"><span data-stu-id="8602f-131">**IMFASFMutualExclusion::SetType**</span></span>](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-settype)
</dt> <dt>

[<span data-ttu-id="8602f-132">Константы Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8602f-132">Media Foundation Constants</span></span>](media-foundation-constants.md)
</dt> </dl>

 

 




