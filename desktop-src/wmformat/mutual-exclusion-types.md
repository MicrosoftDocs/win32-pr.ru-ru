---
title: Типы взаимного исключения
description: Типы взаимного исключения
ms.assetid: bfe6cfe6-3df4-49c4-8015-fe4479b693c1
keywords:
- Пакет SDK для Windows Media Format, взаимное исключение
- Расширенный формат систем (ASF), взаимное исключение
- ASF (Расширенный системный формат), взаимное исключение
- взаимное исключение, типы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c425e69c2aa3eac012874837a6970dbc26d1a51
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104069528"
---
# <a name="mutual-exclusion-types"></a><span data-ttu-id="6a0ff-107">Типы взаимного исключения</span><span class="sxs-lookup"><span data-stu-id="6a0ff-107">Mutual Exclusion Types</span></span>

<span data-ttu-id="6a0ff-108">Типы взаимного исключения можно использовать для обнаружения природы взаимоисключающих объектов в профиле.</span><span class="sxs-lookup"><span data-stu-id="6a0ff-108">You can use mutual exclusion types to identify the nature of a mutual exclusion object in a profile.</span></span> <span data-ttu-id="6a0ff-109">Типы взаимного исключения используются в качестве параметров для [**ивммутуалексклусион:: GetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-gettype) и [**Ивммутуалексклусион:: сеттипе**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype).</span><span class="sxs-lookup"><span data-stu-id="6a0ff-109">Mutual exclusion types are used as parameters for [**IWMMutualExclusion::GetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-gettype) and [**IWMMutualExclusion::SetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype).</span></span>

<span data-ttu-id="6a0ff-110">В следующей таблице перечислены идентификаторы для взаимоисключающих типов.</span><span class="sxs-lookup"><span data-stu-id="6a0ff-110">The following table lists the identifiers for mutual exclusion types.</span></span>



| <span data-ttu-id="6a0ff-111">Константа типа взаимного исключения</span><span class="sxs-lookup"><span data-stu-id="6a0ff-111">Mutual exclusion type constant</span></span> | <span data-ttu-id="6a0ff-112">Код GUID</span><span class="sxs-lookup"><span data-stu-id="6a0ff-112">GUID</span></span>                                 |
|--------------------------------|--------------------------------------|
| <span data-ttu-id="6a0ff-113">\_Язык CLSID вммутекс \_</span><span class="sxs-lookup"><span data-stu-id="6a0ff-113">CLSID\_WMMUTEX\_Language</span></span>       | <span data-ttu-id="6a0ff-114">D6E22A00-35DA-11D1-9034-00A0C90349BE</span><span class="sxs-lookup"><span data-stu-id="6a0ff-114">D6E22A00-35DA-11D1-9034-00A0C90349BE</span></span> |
| <span data-ttu-id="6a0ff-115">CLSID \_ вммутекс \_ скорость</span><span class="sxs-lookup"><span data-stu-id="6a0ff-115">CLSID\_WMMUTEX\_Bitrate</span></span>        | <span data-ttu-id="6a0ff-116">D6E22A01-35DA-11D1-9034-00A0C90349BE</span><span class="sxs-lookup"><span data-stu-id="6a0ff-116">D6E22A01-35DA-11D1-9034-00A0C90349BE</span></span> |
| <span data-ttu-id="6a0ff-117">\_Вммутекс \_ представление CLSID</span><span class="sxs-lookup"><span data-stu-id="6a0ff-117">CLSID\_WMMUTEX\_Presentation</span></span>   | <span data-ttu-id="6a0ff-118">D6E22A02-35DA-11D1-9034-00A0C90349BE</span><span class="sxs-lookup"><span data-stu-id="6a0ff-118">D6E22A02-35DA-11D1-9034-00A0C90349BE</span></span> |
| <span data-ttu-id="6a0ff-119">\_Неизвестный ВММУТЕКС CLSID \_</span><span class="sxs-lookup"><span data-stu-id="6a0ff-119">CLSID\_WMMUTEX\_Unknown</span></span>        | <span data-ttu-id="6a0ff-120">D6E22A03-35DA-11D1-9034-00A0C90349BE</span><span class="sxs-lookup"><span data-stu-id="6a0ff-120">D6E22A03-35DA-11D1-9034-00A0C90349BE</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="6a0ff-121">См. также</span><span class="sxs-lookup"><span data-stu-id="6a0ff-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a0ff-122">**Значения GUID**</span><span class="sxs-lookup"><span data-stu-id="6a0ff-122">**GUID Values**</span></span>](guid-values.md)
</dt> </dl>

 

 




