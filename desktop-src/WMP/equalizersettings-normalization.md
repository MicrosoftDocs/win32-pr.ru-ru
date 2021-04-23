---
title: ЕКУАЛИЗЕРСЕТТИНГС. Нормализация
description: Атрибут нормализации указывает или получает значение, указывающее, включена ли нормализация.
ms.assetid: d0819624-7bc5-447a-b890-c8af94faa7b0
keywords:
- ЕКУАЛИЗЕРСЕТТИНГС. Нормализация проигрывателя Windows Media
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.normalization
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9714359e5d5e2af0c82a0d687555f7cfcbf1cf70
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694781"
---
# <a name="equalizersettingsnormalization"></a><span data-ttu-id="8894f-104">ЕКУАЛИЗЕРСЕТТИНГС. Нормализация</span><span class="sxs-lookup"><span data-stu-id="8894f-104">EQUALIZERSETTINGS.normalization</span></span>

<span data-ttu-id="8894f-105">Атрибут **нормализации** указывает или получает значение, указывающее, включена ли нормализация.</span><span class="sxs-lookup"><span data-stu-id="8894f-105">The **normalization** attribute specifies or retrieves a value indicating whether normalization is enabled.</span></span>

``` syntax
        elementID.normalization
```

## <a name="possible-values"></a><span data-ttu-id="8894f-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="8894f-106">Possible Values</span></span>

<span data-ttu-id="8894f-107">Этот атрибут является **логическим значением** для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="8894f-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="8894f-108">Значение</span><span class="sxs-lookup"><span data-stu-id="8894f-108">Value</span></span> | <span data-ttu-id="8894f-109">Описание</span><span class="sxs-lookup"><span data-stu-id="8894f-109">Description</span></span>                         |
|-------|-------------------------------------|
| <span data-ttu-id="8894f-110">true</span><span class="sxs-lookup"><span data-stu-id="8894f-110">true</span></span>  | <span data-ttu-id="8894f-111">Нормализация включена.</span><span class="sxs-lookup"><span data-stu-id="8894f-111">Normalization is enabled.</span></span>           |
| <span data-ttu-id="8894f-112">false</span><span class="sxs-lookup"><span data-stu-id="8894f-112">false</span></span> | <span data-ttu-id="8894f-113">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8894f-113">Default.</span></span> <span data-ttu-id="8894f-114">Нормализация отключена.</span><span class="sxs-lookup"><span data-stu-id="8894f-114">Normalization is disabled.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="8894f-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8894f-115">Remarks</span></span>

<span data-ttu-id="8894f-116">Если нормализация включена, то звуковой сигнал для всего файла цифрового носителя масштабируется до максимального значения.</span><span class="sxs-lookup"><span data-stu-id="8894f-116">When normalization is enabled, the audio signal for an entire digital media file is scaled up to the maximum value.</span></span> <span data-ttu-id="8894f-117">Это позволяет воспроизводить несколько файлов приблизительно на одном томе, не требуя настройки томов.</span><span class="sxs-lookup"><span data-stu-id="8894f-117">This allows multiple files to be played at approximately the same volume without requiring volume adjustments.</span></span>

## <a name="requirements"></a><span data-ttu-id="8894f-118">Требования</span><span class="sxs-lookup"><span data-stu-id="8894f-118">Requirements</span></span>



| <span data-ttu-id="8894f-119">Требование</span><span class="sxs-lookup"><span data-stu-id="8894f-119">Requirement</span></span> | <span data-ttu-id="8894f-120">Значение</span><span class="sxs-lookup"><span data-stu-id="8894f-120">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="8894f-121">Версия</span><span class="sxs-lookup"><span data-stu-id="8894f-121">Version</span></span><br/> | <span data-ttu-id="8894f-122">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="8894f-122">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8894f-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8894f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8894f-124">**ЕКУАЛИЗЕРСЕТТИНГС, элемент**</span><span class="sxs-lookup"><span data-stu-id="8894f-124">**EQUALIZERSETTINGS Element**</span></span>](equalizersettings-element.md)
</dt> <dt>

[<span data-ttu-id="8894f-125">**ЕКУАЛИЗЕРСЕТТИНГС. Нормализатионавераже**</span><span class="sxs-lookup"><span data-stu-id="8894f-125">**EQUALIZERSETTINGS.normalizationAverage**</span></span>](equalizersettings-normalizationaverage.md)
</dt> <dt>

[<span data-ttu-id="8894f-126">**ЕКУАЛИЗЕРСЕТТИНГС. Нормализатионпеак**</span><span class="sxs-lookup"><span data-stu-id="8894f-126">**EQUALIZERSETTINGS.normalizationPeak**</span></span>](equalizersettings-normalizationpeak.md)
</dt> </dl>

 

 





