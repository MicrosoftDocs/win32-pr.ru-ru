---
description: Останавливает текущий проход кодировки или запрашивает, является ли текущий проход кодировки последним.
ms.assetid: 847f638f-9ab9-42ca-8e39-82c113cee92f
title: Свойство Авенккоммонпассенд (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 026b20cf0c13536403e7ccf32b160e8c6fc08141
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495639"
---
# <a name="avenccommonpassend-property"></a><span data-ttu-id="77a51-103">Авенккоммонпассенд, свойство</span><span class="sxs-lookup"><span data-stu-id="77a51-103">AVEncCommonPassEnd property</span></span>

<span data-ttu-id="77a51-104">Останавливает текущий проход кодировки или запрашивает, является ли текущий проход кодировки последним.</span><span class="sxs-lookup"><span data-stu-id="77a51-104">Stops the current encoding pass, or queries whether the current encoding pass is the last one.</span></span>

<span data-ttu-id="77a51-105">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="77a51-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="77a51-106">Тип данных</span><span class="sxs-lookup"><span data-stu-id="77a51-106">Data type</span></span>

<span data-ttu-id="77a51-107">**Вариант \_ BOOL** (**\_ логическое значение VT**)</span><span class="sxs-lookup"><span data-stu-id="77a51-107">**VARIANT\_BOOL** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="77a51-108">GUID свойства</span><span class="sxs-lookup"><span data-stu-id="77a51-108">Property GUID</span></span>

<span data-ttu-id="77a51-109">**КОДЕКАПИ \_ авенккоммонпассенд**</span><span class="sxs-lookup"><span data-stu-id="77a51-109">**CODECAPI\_AVEncCommonPassEnd**</span></span>

## <a name="remarks"></a><span data-ttu-id="77a51-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="77a51-110">Remarks</span></span>

<span data-ttu-id="77a51-111">Установка этого свойства в значение **Variant \_ true** завершает текущий проход кодирования.</span><span class="sxs-lookup"><span data-stu-id="77a51-111">Setting this property to **VARIANT\_TRUE** ends the current encoding pass.</span></span> <span data-ttu-id="77a51-112">Присвоение этому свойству значения **Variant \_ false** завершает многопроходную кодировку.</span><span class="sxs-lookup"><span data-stu-id="77a51-112">Setting this property to **VARIANT\_FALSE** terminates multipass encoding.</span></span>

<span data-ttu-id="77a51-113">Чтение этого свойства запрашивает, является ли текущий проход кодировки последним.</span><span class="sxs-lookup"><span data-stu-id="77a51-113">Reading this property queries whether the current encoding pass is the last one.</span></span>

## <a name="requirements"></a><span data-ttu-id="77a51-114">Требования</span><span class="sxs-lookup"><span data-stu-id="77a51-114">Requirements</span></span>



| <span data-ttu-id="77a51-115">Требование</span><span class="sxs-lookup"><span data-stu-id="77a51-115">Requirement</span></span> | <span data-ttu-id="77a51-116">Значение</span><span class="sxs-lookup"><span data-stu-id="77a51-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="77a51-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="77a51-117">Minimum supported client</span></span><br/> | <span data-ttu-id="77a51-118">Приложения Windows 2000 Professional \[ классические приложения \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="77a51-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="77a51-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="77a51-119">Minimum supported server</span></span><br/> | <span data-ttu-id="77a51-120">\[Приложения UWP для классических приложений Windows 2000 \|\]</span><span class="sxs-lookup"><span data-stu-id="77a51-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="77a51-121">Header</span><span class="sxs-lookup"><span data-stu-id="77a51-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="77a51-122"><dt>Кодекапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="77a51-122"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77a51-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="77a51-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77a51-124">Свойства кодека API</span><span class="sxs-lookup"><span data-stu-id="77a51-124">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="77a51-125">**Интерфейс Икодекапи**</span><span class="sxs-lookup"><span data-stu-id="77a51-125">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




