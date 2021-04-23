---
description: Включает или отключает обравенство громкости в аудио-декодере или в поставщике цифровых сигналов (DSP).
ms.assetid: f02b187f-1bcb-47b3-8ac2-018ed30491c6
title: Свойство Авдсплауднессекуализатион (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38a2fc09077c114ab18f2626b333cfe4c87c97d9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103990256"
---
# <a name="avdsploudnessequalization-property"></a><span data-ttu-id="a4b93-103">Авдсплауднессекуализатион, свойство</span><span class="sxs-lookup"><span data-stu-id="a4b93-103">AVDSPLoudnessEqualization property</span></span>

<span data-ttu-id="a4b93-104">Включает или отключает обравенство громкости в аудио-декодере или в поставщике цифровых сигналов (DSP).</span><span class="sxs-lookup"><span data-stu-id="a4b93-104">Enables or disables loudness equalization in an audio decoder or digital signal processor (DSP).</span></span>

<span data-ttu-id="a4b93-105">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="a4b93-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="a4b93-106">Тип данных</span><span class="sxs-lookup"><span data-stu-id="a4b93-106">Data type</span></span>

<span data-ttu-id="a4b93-107">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="a4b93-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="a4b93-108">GUID свойства</span><span class="sxs-lookup"><span data-stu-id="a4b93-108">Property GUID</span></span>

<span data-ttu-id="a4b93-109">**КОДЕКАПИ \_ авдсплауднессекуализатион**</span><span class="sxs-lookup"><span data-stu-id="a4b93-109">**CODECAPI\_AVDSPLoudnessEqualization**</span></span>

## <a name="property-value"></a><span data-ttu-id="a4b93-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="a4b93-110">Property value</span></span>

<span data-ttu-id="a4b93-111">Значение этого свойства является членом перечисления [**еавдсплауднессекуализатион**](/windows/desktop/api/codecapi/ne-codecapi-eavdsploudnessequalization) .</span><span class="sxs-lookup"><span data-stu-id="a4b93-111">The value of this property is a member of the [**eAVDSPLoudnessEqualization**](/windows/desktop/api/codecapi/ne-codecapi-eavdsploudnessequalization) enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4b93-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a4b93-112">Remarks</span></span>

<span data-ttu-id="a4b93-113">Обравенство громкости — это процесс DSP, который поддерживает последовательный уровень громкости при изменении аудиопотока.</span><span class="sxs-lookup"><span data-stu-id="a4b93-113">Loudness equalization is a DSP process that maintains a consistent volume level when the audio stream changes.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4b93-114">Требования</span><span class="sxs-lookup"><span data-stu-id="a4b93-114">Requirements</span></span>



| <span data-ttu-id="a4b93-115">Требование</span><span class="sxs-lookup"><span data-stu-id="a4b93-115">Requirement</span></span> | <span data-ttu-id="a4b93-116">Значение</span><span class="sxs-lookup"><span data-stu-id="a4b93-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a4b93-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a4b93-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a4b93-118">Приложения Windows 2000 Professional \[ классические приложения \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="a4b93-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="a4b93-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a4b93-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a4b93-120">\[Приложения UWP для классических приложений Windows 2000 \|\]</span><span class="sxs-lookup"><span data-stu-id="a4b93-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="a4b93-121">Header</span><span class="sxs-lookup"><span data-stu-id="a4b93-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a4b93-122"><dt>Кодекапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4b93-122"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4b93-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a4b93-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4b93-124">Свойства кодека API</span><span class="sxs-lookup"><span data-stu-id="a4b93-124">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="a4b93-125">**Интерфейс Икодекапи**</span><span class="sxs-lookup"><span data-stu-id="a4b93-125">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




